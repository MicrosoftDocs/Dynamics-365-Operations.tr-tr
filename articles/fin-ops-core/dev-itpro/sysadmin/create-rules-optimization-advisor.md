---
title: En iyi duruma getirme danışmanı için kurallar oluşturma
description: Bu konu En iyi duruma getirme danışmanına nasıl yeni kurallar ekleneceğini açıklar.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181002"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="7509c-103">En iyi duruma getirme danışmanı için kurallar oluşturma</span><span class="sxs-lookup"><span data-stu-id="7509c-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7509c-104">Bu konu **En iyi duruma getirme danışmanı** için nasıl yeni kurallar oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7509c-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="7509c-105">Örneğin, hangi Teklif Talebi (RFQ) servis taleplerinin boş bir başlığı olacağını tanımlayan yeni bir kural oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7509c-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="7509c-106">Servis taleplerinde başlıklar kullanmak bunların kolayca tanımlanabilmesini ve aranabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="7509c-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="7509c-107">Bu örnek son derece basit olmakla birlikte en iyi durumu getirme kuralları ile nelerin elde edilebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7509c-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="7509c-108">*Kural* uygulama verilerindeki bir denetimdir.</span><span class="sxs-lookup"><span data-stu-id="7509c-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="7509c-109">Kuralın değerlendirdiği durum karşılanırsa, süreçleri en iyi duruma veya verileri iyileştirme fırsatları oluşur.</span><span class="sxs-lookup"><span data-stu-id="7509c-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="7509c-110">Fırsatlar üzerinde harekete geçilebilir ve isteğe bağlı olarak eylemlerin etkisi ölçülebilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="7509c-111">**En iyi duruma getirme danışmanı** için yeni bir kural oluşturmak üzere **SelfHealingRule** soyut sınıfını genişleten, **IDiagnosticsRule** arabirimini uygulayan ve **DiagnosticRule** özniteliğiyle tasarlanan yeni bir sınıf ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7509c-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="7509c-112">Sınıf ayrıca **DiagnosticsRuleSubscription** özniteliğiyle tasarlanmış bir yönteme de sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7509c-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="7509c-113">Kural olarak bu, daha sonra açıklanacak olan **opportunityTitle** yöntemiyle yapılır.</span><span class="sxs-lookup"><span data-stu-id="7509c-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="7509c-114">Bu yeni sınıf, **SelfHealingRules** modelindeki bir bağımlılıkla özel bir modele eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="7509c-115">Aşağıdaki örnekte, uygulanan kural **RFQTitleSelfHealingRule** olarak adlandırılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7509c-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="7509c-116">**SelfHealingRule** soyut sınıfı, devralınan sınıflarda uygulanması gereken soyut yöntemlere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7509c-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="7509c-117">Temeli **değerlendirme** yöntemidir; bu yöntem kural tarafından tanımlanan fırsatların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7509c-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="7509c-118">Fırsatlar tüzel kişilik başına olabilir veya tüm sisteme uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
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

<span data-ttu-id="7509c-119">Yukarıda gösterilen yöntem şirketler üzerinde döngü yapar ve **findRFQCasesWithEmptyTitle** yönteminde boş başlıkları bulunan RFQ servis taleplerini seçer.</span><span class="sxs-lookup"><span data-stu-id="7509c-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="7509c-120">Bu durumdaki en az bir servis talebi bulunması durumunda, şirkete özel fırsat **getOpportunityForCompany** yöntemiyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7509c-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="7509c-121">**SelfHealingOpportunity** tablosundaki **Veri** alanının **Kapsayıcı** türünde olduğunu ve bu nedenle bu kurala özel mantıkla ilgili tüm verileri içerebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7509c-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="7509c-122">**OpportunityDate** seçeneği geçerli zaman damgasıyla ayarladığınızda, fırsat için en son değerlendirme zamanı kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="7509c-123">Fırsatlar şirketler arası da olabilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="7509c-124">Bu durumda, şirketler üzerindeki döngü gerekli değildir ve fırsat **getOpportunityAcrossCompanies** yöntemiyle oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7509c-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="7509c-125">Aşağıdaki kod **findRFQCasesWithEmptyTitle** yöntemini gösterir; bu yöntem boş başlıkları bulunan RFQ servis taleplerinin kodlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7509c-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
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

<span data-ttu-id="7509c-126">Uygulanması gereken diğer iki yöntem **opportunityTitle** ve **opportunityDetails** yöntemleridir.</span><span class="sxs-lookup"><span data-stu-id="7509c-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="7509c-127">İlk yöntem fırsat için kısa bir başlık döndürür; ikinci yöntem fırsat için veri de içerebilecek olan ayrıntılı bir açıklama döndürür.</span><span class="sxs-lookup"><span data-stu-id="7509c-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="7509c-128">**opportunityTitle** tarafından getirilen başlık **En iyi duruma getirme danışmanı** çalışma alanındaki **En iyi duruma getirme fırsatı** sütununda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7509c-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="7509c-129">Ayrıca, fırsatla ilgili daha fazla bilgi gösteren yan bölmenin başlığı olarak da görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7509c-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="7509c-130">Kural olarak, bu yöntem aşağıdaki bağımsız değişkenleri alan **DiagnosticRuleSubscription** özniteliğiyle donatılır:</span><span class="sxs-lookup"><span data-stu-id="7509c-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="7509c-131">**Tanı alanı** – Kuralık uygulamanın hangi alanına ait olduğunu açıklayan (**DiagnosticArea::SCM** gibi) **DiagnosticArea** türünde bir numaralandırmadır.</span><span class="sxs-lookup"><span data-stu-id="7509c-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="7509c-132">**Kural adı** – Kural adını içeren bir dize.</span><span class="sxs-lookup"><span data-stu-id="7509c-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="7509c-133">**Tanı doğrulama kuralı** formunun **Kural adı** sütununda görüntülenir (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="7509c-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="7509c-134">**Çalışma sıklığı** – Kuralın hangi sıklıkta çalıştırılması gerektiğini açıklayan (**DiagnosticRunFrequency::Daily** gibi) **DiagnosticRunFrequency** türünde bir numaralandırmadır.</span><span class="sxs-lookup"><span data-stu-id="7509c-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="7509c-135">**Kural açıklaması** – Kuralın daha ayrıntılı açıklamasını içeren bir dize.</span><span class="sxs-lookup"><span data-stu-id="7509c-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="7509c-136">**Tanı doğrulama kuralı** formunun **Kural açıklaması** sütununda görüntülenir (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="7509c-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="7509c-137">Kuralın çalışması için **DiagnosticRuleSubscription** özniteliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7509c-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="7509c-138">Genellikle, **opportunityTitle** üzerinde kullanılır ancak sınıftaki herhangi bir yöntemi donatabilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="7509c-139">Aşağıda örnek bir uygulama verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7509c-139">The following is an example implementation.</span></span> <span data-ttu-id="7509c-140">Kolaylık sağlamak için ham dizeler kullanılır ancak doğru bir uygulama etiketler gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7509c-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="7509c-141">**opportunityDetails** tarafından döndürülen açıklama fırsatla ilgili daha fazla bilgi gösteren yan bölmede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7509c-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="7509c-142">Fırsatla ilgili daha fazla ayrıntı sunmak için kullanılabilen **Veri** alanı olan **SelfHealingOpportunity** bağımsız değişkenini alır.</span><span class="sxs-lookup"><span data-stu-id="7509c-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="7509c-143">Örnekte, yöntem boş başlığı bulunan RFQ servis taleplerinin kodlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7509c-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
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

<span data-ttu-id="7509c-144">Uygulanması gereken diğer iki soyut yöntem **provideHealingAction** ve **securityMenuItem** yöntemleridir.</span><span class="sxs-lookup"><span data-stu-id="7509c-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="7509c-145">**provideHealingAction** bir iyileştirme eylemi sağlandığında gerçek değeri döndürür; aksi halde yanlış değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7509c-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="7509c-146">Doğru değeri döndürülürse, **performAction** yönteminin uygulanması gerekir. Aksi halde bir hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="7509c-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="7509c-147">**performAction** yöntemi, verilerin eylem için kullanılabildiği bir **SelfHealingOpportunity** bağımsız değişkeni alır.</span><span class="sxs-lookup"><span data-stu-id="7509c-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="7509c-148">Örnekte, eylem ile düzeltme için **PurchRFQCaseTableListPage** öğesini açar.</span><span class="sxs-lookup"><span data-stu-id="7509c-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="7509c-149">Kuralın ayrıntılarına bağlı olarak, fırsat verisini kullanan bir otomatik eylem gerçekleştirmek de mümkün olabilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="7509c-150">Bu örnekte, sistem RFQ servis talepleri için otomatik olarak başlık oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="7509c-151">**securityMenuItem** bir eylem menüsü öğesinin adını döndürür; böylece kural yalnızca eylem menüsü öğesine erişimi olan kullanıcılar için görünebilir olur.</span><span class="sxs-lookup"><span data-stu-id="7509c-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="7509c-152">Güvenlik özel kurallara veya fırsatlara yalnızca yetkili kullanıcıların erişmesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="7509c-153">Örnekte, yalnızca **PurchRFQCaseTitleAction** için erişim izni olan kullanıcılar fırsatı görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7509c-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="7509c-154">Bu eylem menüsü öğesinin bu örnek için oluşturulduğunu ve **PurchRFQCaseTableMaintain** güvenlik ayrıcalığı için bir giriş noktası olarak eklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7509c-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="7509c-155">Güvenliğin düzgün çalışması için menü öğesinin eylem menü öğesi olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7509c-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="7509c-156">**Görüntüleme menüsü öğeleri** gibi diğer menü öğesi türleri düzgün çalışmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="7509c-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="7509c-157">Kural derlendikten sonra, kullanıcı arabiriminde (UI) görüntülenmesi için aşağıdaki işi yürütün.</span><span class="sxs-lookup"><span data-stu-id="7509c-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
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

<span data-ttu-id="7509c-158">Kural **Sistem yönetimi** > **Periyodik görevler** > **Tanı doğrulama kuralını koru** altında bulunan **Tanılama doğrulama kuralı** formunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7509c-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="7509c-159">Değerlendirilmesini sağlamak için, **Sistem yönetimi** > **Periyodik görevler** > **Tanılama doğrulama kuralı planla**'ya gidin ve kural sıklığını (**Günlük** gibi) seçin.</span><span class="sxs-lookup"><span data-stu-id="7509c-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="7509c-160">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7509c-160">Click **OK**.</span></span> <span data-ttu-id="7509c-161">Yeni fırsatı görüntülemek için **Sistem yönetimi** > **En iyi duruma getirme danışmanı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7509c-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="7509c-162">Aşağıdaki örnek gerekli tüm yöntemleri ve öznitelikleri içeren bir kuralın iskeletine sahip bir kod parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="7509c-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="7509c-163">Yeni kurallar yazmaya başlamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7509c-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="7509c-164"> Örnekte kullanılan etiketler ve eylem menüsü öğeleri yalnızca tanıtım amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7509c-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
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

<span data-ttu-id="7509c-165">Daha fazla bilgi için kısa YouTube videosunu izleyin: [Dynamics 365 for Finance and Operations içinde iyileştirme danışmanı](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="7509c-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
