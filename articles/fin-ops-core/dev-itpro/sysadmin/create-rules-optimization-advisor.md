---
title: En iyi duruma getirme danışmanı için kurallar oluşturma
description: Bu makalede, İyileştirme danışmanı'na nasıl yeni kurallar ekleneceğini açıklanmaktadır.
author: kamaybac
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: kamaybac
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: SelfHealingWorkspace
ms.openlocfilehash: a4addc98e3d5496bc8d2fafb3918931da876739f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273932"
---
# <a name="create-rules-for-optimization-advisor"></a>En iyi duruma getirme danışmanı için kurallar oluşturma

[!include [banner](../includes/banner.md)]

Bu konu **İyileştirme danışmanı** için nasıl yeni kurallar oluşturulacağı açıklanmaktadır. Örneğin, hangi Teklif Talebi (RFQ) servis taleplerinin boş bir başlığı olacağını tanımlayan yeni bir kural oluşturabilirsiniz. Servis taleplerinde başlıklar kullanmak bunların kolayca tanımlanabilmesini ve aranabilmesini sağlar. Bu örnek son derece basit olmakla birlikte en iyi durumu getirme kuralları ile nelerin elde edilebileceğini gösterir. 

*Kural* uygulama verilerindeki bir denetimdir. Kuralın değerlendirdiği durum karşılanırsa, süreçleri en iyi duruma veya verileri iyileştirme fırsatları oluşur. Fırsatlar üzerinde harekete geçilebilir ve isteğe bağlı olarak eylemlerin etkisi ölçülebilir. 

**En iyi duruma getirme danışmanı** için yeni bir kural oluşturmak üzere **SelfHealingRule** soyut sınıfını genişleten, **IDiagnosticsRule** arabirimini uygulayan ve **DiagnosticRule** özniteliğiyle tasarlanan yeni bir sınıf ekleyin. Sınıf ayrıca **DiagnosticsRuleSubscription** özniteliğiyle tasarlanmış bir yönteme de sahip olmalıdır. Kural olarak bu, daha sonra açıklanacak olan **opportunityTitle** yöntemiyle yapılır. Bu yeni sınıf, **SelfHealingRules** modelindeki bir bağımlılıkla özel bir modele eklenebilir. Aşağıdaki örnekte, uygulanan kural **RFQTitleSelfHealingRule** olarak adlandırılmaktadır.

```xpp
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

**SelfHealingRule** soyut sınıfı, devralınan sınıflarda uygulanması gereken soyut yöntemlere sahiptir. Temeli **değerlendirme** yöntemidir; bu yöntem kural tarafından tanımlanan fırsatların listesini döndürür. Fırsatlar tüzel kişilik başına olabilir veya tüm sisteme uygulanabilir.

```xpp
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

Yukarıda gösterilen yöntem şirketler üzerinde döngü yapar ve **findRFQCasesWithEmptyTitle** yönteminde boş başlıkları bulunan RFQ servis taleplerini seçer. Bu durumdaki en az bir servis talebi bulunması durumunda, şirkete özel fırsat **getOpportunityForCompany** yöntemiyle oluşturulur. **SelfHealingOpportunity** tablosundaki **Veri** alanının **Kapsayıcı** türünde olduğunu ve bu nedenle bu kurala özel mantıkla ilgili tüm verileri içerebileceğini unutmayın. **OpportunityDate** seçeneği geçerli zaman damgasıyla ayarladığınızda, fırsat için en son değerlendirme zamanı kaydedilir.  

Fırsatlar şirketler arası da olabilir. Bu durumda, şirketler üzerindeki döngü gerekli değildir ve fırsat **getOpportunityAcrossCompanies** yöntemiyle oluşturulmalıdır. 

Aşağıdaki kod **findRFQCasesWithEmptyTitle** yöntemini gösterir; bu yöntem boş başlıkları bulunan RFQ servis taleplerinin kodlarını döndürür.

```xpp
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

Uygulanması gereken diğer iki yöntem **opportunityTitle** ve **opportunityDetails** yöntemleridir. İlk yöntem fırsat için kısa bir başlık döndürür; ikinci yöntem fırsat için veri de içerebilecek olan ayrıntılı bir açıklama döndürür.

**opportunityTitle** tarafından getirilen başlık **En iyi duruma getirme danışmanı** çalışma alanındaki **En iyi duruma getirme fırsatı** sütununda görüntülenir. Ayrıca, fırsatla ilgili daha fazla bilgi gösteren yan bölmenin başlığı olarak da görüntülenir. Kural olarak, bu yöntem aşağıdaki bağımsız değişkenleri alan **DiagnosticRuleSubscription** özniteliğiyle donatılır: 

* **Tanı alanı** – Kuralık uygulamanın hangi alanına ait olduğunu açıklayan (**DiagnosticArea::SCM** gibi) **DiagnosticArea** türünde bir numaralandırmadır. 

* **Kural adı** – Kural adını içeren bir dize. **Tanı doğrulama kuralı** formunun **Kural adı** sütununda görüntülenir (**DiagnosticsValidationRuleMaintain**). 

* **Çalışma sıklığı** – Kuralın hangi sıklıkta çalıştırılması gerektiğini açıklayan (**DiagnosticRunFrequency::Daily** gibi) **DiagnosticRunFrequency** türünde bir numaralandırmadır. 

* **Kural açıklaması** – Kuralın daha ayrıntılı açıklamasını içeren bir dize. **Tanı doğrulama kuralı** formunun **Kural açıklaması** sütununda görüntülenir (**DiagnosticsValidationRuleMaintain**). 

> [!NOTE]
> Kuralın çalışması için **DiagnosticRuleSubscription** özniteliği gereklidir. Genellikle, **opportunityTitle** üzerinde kullanılır ancak sınıftaki herhangi bir yöntemi donatabilir.

Aşağıda örnek bir uygulama verilmiştir. Kolaylık sağlamak için ham dizeler kullanılır ancak doğru bir uygulama etiketler gerektirir. 

```xpp
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

**opportunityDetails** tarafından döndürülen açıklama fırsatla ilgili daha fazla bilgi gösteren yan bölmede görüntülenir. Fırsatla ilgili daha fazla ayrıntı sunmak için kullanılabilen **Veri** alanı olan **SelfHealingOpportunity** bağımsız değişkenini alır. Örnekte, yöntem boş başlığı bulunan RFQ servis taleplerinin kodlarını döndürür. 

```xpp
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

Uygulanması gereken diğer iki soyut yöntem **provideHealingAction** ve **securityMenuItem** yöntemleridir. 

**provideHealingAction** bir iyileştirme eylemi sağlandığında gerçek değeri döndürür; aksi halde yanlış değeri döndürür. Doğru değeri döndürülürse, **performAction** yönteminin uygulanması gerekir. Aksi halde bir hata oluşur. **performAction** yöntemi, verilerin eylem için kullanılabildiği bir **SelfHealingOpportunity** bağımsız değişkeni alır. Örnekte, eylem ile düzeltme için **PurchRFQCaseTableListPage** öğesini açar. 

```xpp
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

Kuralın ayrıntılarına bağlı olarak, fırsat verisini kullanan bir otomatik eylem gerçekleştirmek de mümkün olabilir. Bu örnekte, sistem RFQ servis talepleri için otomatik olarak başlık oluşturabilir. 

**securityMenuItem** bir eylem menüsü öğesinin adını döndürür; böylece kural yalnızca eylem menüsü öğesine erişimi olan kullanıcılar için görünebilir olur. Güvenlik özel kurallara veya fırsatlara yalnızca yetkili kullanıcıların erişmesini gerektirebilir. Örnekte, yalnızca **PurchRFQCaseTitleAction** için erişim izni olan kullanıcılar fırsatı görüntüleyebilir. Bu eylem menüsü öğesinin bu örnek için oluşturulduğunu ve **PurchRFQCaseTableMaintain** güvenlik ayrıcalığı için bir giriş noktası olarak eklendiğini unutmayın. 

> [!NOTE]
> Güvenliğin düzgün çalışması için menü öğesinin eylem menü öğesi olması gerekir. **Görüntüleme menüsü öğeleri** gibi diğer menü öğesi türleri düzgün çalışmayacaktır.

```xpp
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

Kural derlendikten sonra, kullanıcı arabiriminde (UI) görüntülenmesi için aşağıdaki işi yürütün.

```xpp
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

Kural **Sistem yönetimi** > **Periyodik görevler** > **Tanı doğrulama kuralını koru** altında bulunan **Tanılama doğrulama kuralı** formunda görüntülenir. Değerlendirilmesini sağlamak için, **Sistem yönetimi** > **Periyodik görevler** > **Tanılama doğrulama kuralı planla**'ya gidin ve kural sıklığını (**Günlük** gibi) seçin. **Tamam** seçeneğini tıklatın. Yeni fırsatı görüntülemek için **Sistem yönetimi** > **En iyi duruma getirme danışmanı**'na gidin. 

Aşağıdaki örnek gerekli tüm yöntemleri ve öznitelikleri içeren bir kuralın iskeletine sahip bir kod parçasıdır. Yeni kurallar yazmaya başlamanıza yardımcı olur. Örnekte kullanılan etiketler ve eylem menüsü öğeleri yalnızca tanıtım amacıyla kullanılmıştır.

```xpp
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

Daha fazla bilgi için YouTube'daki [Dynamics 365 Finance'te İyileştirme danışmanı](https://www.youtube.com/watch?v=MRsAzgFCUSQ) başlıklı kısa videoyu izleyin


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
