---
title: Yazdırılabilir FTI formları oluşturma
description: Bu konuda, yazdırılabilir serbest metin faturası (FTI) formlarını Microsoft Office belgeleri olarak oluşturmak için Elektronik raporlama (ER) altyapısının nasıl kullanılacağı açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 168cef1b5f5d48cb739b08fa395c1bcd62089494
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686749"
---
# <a name="generate-printable-fti-forms"></a>Yazdırılabilir FTI formları oluşturma

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) altyapısı, yazdırılabilir serbest metin faturası (FTI) formlarını Microsoft Office belgeleri olarak oluşturmanızı sağlar. Bu konuda, kendi yapılandırmalarınızı oluşturma ve kullanılabilir yapılandırma şablonlarının ayrıntıları hakkında bilgiler sağlanmaktadır.

## <a name="overview"></a>Genel bakış

Microsoft SQL Server Reporting Services (SSRS) kullanılarak yazdırılabilir FTI formları oluşturma özelliğinin yanı sıra artık ER altyapısını da kullanabilirsiniz. Microsoft Office Excel ve Word'de yazdırılabilir FTI formlarını yönetebilirsiniz. Ayrıca özel gereksinimleri karşılamak için kod değişikliği yapmadan düzeni, veri akışını ve biçimlendirmeyi de değiştirebilirsiniz.

> [!NOTE]
> Yazdırılabilir FTI formları çözümünün bu örneği için mevcut ER yapılandırmalarına genel bakış ile başlamak isterseniz doğrudan bu konunun ilerleyen bölümlerinde açıklanan **Yazdırılabilir FTI formları oluşturmak için örnek ER yapılandırmalarını indirme** bölümüne gidebilirsiniz.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Yazdırılabilir FTI formları için özelleştirilmiş yapılandırmalar oluşturma
Yazdırılabilir FTI formları için özelleştirilmiş çözümünüzün bir parçası olarak bir dizi ER yapılandırması oluşturmanız gerekir.

### <a name="configure-the-er-data-model"></a>ER veri modelini yapılandırma
Uygulamanız, müşteri faturalandırması iş etki alanını tanımlayan bir veri modeline sahip ER veri modeli yapılandırmasını içermelidir. Veri modelinin adının **CustomersInvoicing** olması zorunludur. ER veri modellerini tasarlama hakkında bilgi için bkz. [ER Etki alanına özel veri modeli tasarlama](tasks/er-design-domain-specific-data-model-2016-11.md).

### <a name="configure-the-er-model-mapping"></a>ER model eşlemesini yapılandırma
Uygulamanız, CustomersInvoicing veri modeli için ER model eşlemesini içermelidir. Model eşleme, ER veri modeli yapılandırmasında veya ER model eşleme yapılandırmasında olabilir. Ancak model eşleme kök tanımlayıcısının adı **FreeTextInvoice** olmalıdır.

Eşleme aşağıdaki veri kaynaklarını içermelidir:

- Veri kaynağı türü: **Tablo kayıtları**

    - Bu veri kaynağı **CustInvoiceJour** olarak adlandırılmalıdır.
    - CustInvoiceJour uygulama tablosuna başvurmalıdır.
    - Uygulamadan yazdırmak üzere seçilen faturaların listesini eşleyen ER modeline geçmek için çalışma zamanında kullanılır.

- Veri kaynağı türü: **Nesne**

    - Bu veri kaynağı **PrintMgmtPrintSettingDetail** olarak adlandırılmalıdır.
    - **PrintMgmtPrintSettingDetail** uygulama sınıfına başvurmalıdır.
    - Uygulamadan çalışmakta olan ER biçiminin yazdırma yönetimi ayarlarının ER model eşleme ayrıntılarına geçmek için çalışma zamanında kullanılır.

ER altyapısına sahip uygulama tümleştirmesinin ayrıntıları uygulamanın kaynak kodunda **ERPrintMgmtReportFormatSubscriber** sınıfında (ER Uygulama Paketi tümleştirme modeli) bulunabilir.

ER model eşlemelerinin tasarlanması hakkında daha fazla bilgi için bkz. [ER model eşlemelerini tanımlama ve bunlar için veri kaynaklarını seçme](tasks/er-define-model-mapping-select-data-sources-2016-11.md).

### <a name="configure-the-er-format"></a>ER biçimini yapılandırma
Uygulama kurulumunuzda FTI formları oluşturmak için kullanılacak ER biçimi yapılandırmasına sahip olmanız gerekir. 

> [!NOTE]
> Bu biçim yapılandırması CustomersInvoicing veri modeli için oluşturulmalıdır ve **FreeTextInvoice** kök tanımlayıcısına sahip model eşlemesini kullanmalıdır.

ER biçimlerini yapılandırma hakkında daha fazla bilgi için bkz. [ER Biçim yapılandırması oluşturma (Kasım 2016)](tasks/er-format-configuration-2016-11.md). OpenXML biçiminde raporlar oluşturmak üzere ER biçimlerini tasarlama hakkında daha fazla bilgi için bkz. [ER OpenXML biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama (Kasım 2016)](tasks/er-design-reports-openxml-2016-11.md).

## <a name="configure-print-management"></a>Yazdırma yönetimini yapılandırma
ER altyapısını kullanarak FTI formları oluşturmak için ER biçimlerini SSRS raporlarıyla aynı şekilde atayabilirsiniz. ER biçimini tüm Alacak hesapları FTI'larıyla ilişkilendirmek için **Alacak hesapları** \> **Kurulum** \> **Formlar** \> **Form kurulumu** \> **Genel** \> **Yazdırma yönetimi** \> **Serbest metin faturası** \> **Orijinal**'e gidin. ER biçimini belirli bir müşteri veya fatura ile ilişkilendirmek için aşağıdaki adımları izleyin.

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. ER biçimi ile ilişkilendirilecek FTI'yı seçin ve **Yazdırma yönetimi kurulumu** sayfasını açın.
3. İşlenecek faturaların kapsamını belirtmek için belge düzeyini seçin.
4. Belirtilen belge düzeyi için ER biçimini seçin.

![Yazdırma yönetimi kurulumu](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Yalnızca **CustomersInvoicing** veri modelinin **FreeTextInvoice** kök tanımlayıcısını kullanan ER biçimleri seçili biçim için **Rapor biçimi arama** alanında görünür.

## <a name="generate-fti-forms"></a>FTI formları oluşturma
FTI formları ER altyapısında SSRS raporlarıyla aynı şekilde oluşturulur.

FTI formları oluşturmak için faturaları aralığa göre veya seçime göre seçebilirsiniz. 

![Fatura seçimi](media/FTIbyGER-InvoiceSelection.png)

![Fatura önizlemesi](media/FTIbyGER-InvoiceExcelPreview.png)

FTI formlarını bu şekilde yazdırmak için ER biçimlerini kullandığınızda varsayılan ER dosya hedefleri kullanılır. Hedefi değiştiremezsiniz. ER biçimleri için ER hedeflerini yapılandırma hakkında daha fazla bilgi için bkz. [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md).

**Faturayı yazdır** seçeneğini açarak ve **Yazdırma yönetimi hedefini kullan** seçeneğini kapatarak bir FTI'yı deftere naklederken de FTI formları oluşturabilirsiniz.

> [!NOTE]
> FTI formlarını bu şekilde yazdırmak için ER biçimlerini kullandığınızda varsayılan ER dosya hedefleri kullanılır. Hedef zaten yapılandırılmışsa varsayılan hedefi çalışma zamanında değiştirebilirsiniz. Hedefi değiştirmek için aşağıdaki güvenlik ayrıcalığına sahip olmanız gerekir:
>
> - **Ad:** ERFormatDestinationRuntimeMaintain
> - **Etiket:** Çalışma zamanında kullanılacak elektronik raporlama biçimi hedefini koru

![Elektronik raporlama hedefi](media/FTIbyGER-ERFileDestinationSetting.png)

![Elektronik raporlama biçimi hedefi](media/FTIbyGER-ERFileDestinationUsage.png)

ER altyapısı şu anda oluşturulan belgeler için aşağıdaki hedefleri destekler:

- **İndirilen dosya**: Oluşturulan formlar, tarayıcıyı kullanarak kaydedebileceğiniz indirmeler şeklinde sunulur.
- **Ekran**: Microsoft 365 Excel, Excel biçiminde oluşturulan FTI formlarını önizlemek için kullanılır.
- **SharePoint klasörü** - Oluşturulan formlar, Belge yönetimi altyapısının ayarlarına göre depolanır.
- **Uygulama arşivi** - Oluşturulan formlar Microsoft Azure Depolama'da yürütme günlüğü kayıtlarının ekleri olarak depolanır.
- **E-posta**: Oluşturulan formlar e-posta ekleri şeklinde gönderilir.

> [!NOTE]
> Dynamics Yazıcı Yönlendirme Aracısı kullanan doğrudan yazdırma şu anda desteklenmediğinden doğrudan yazıcıda oluşturulan FTI formları gönderemezsiniz.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Yazdırılabilir FTI formları oluşturmak için örnek ER yapılandırmalarını indirme
FTI çözümünüz için şablon olarak kullanmak üzere örnek ER yapılandırmalarını indirebilirsiniz. Yapılandırmalar Microsoft Dynamics Lifecycle Services'de (LCS) Paylaşılan varlık kitaplığında depolanır. Yapılandırmalar şunları içerir:

- **Müşteri faturalandırması modeli** yapılandırması gerekli veri modelini ve model eşlemeyi içerir.
- **Müşteri FTI raporu (GER)** yapılandırması örnek biçimi içerir.

> [!NOTE]
> Bu yapılandırmalar olası senaryoların netleştirilmesine yardımcı olmak için örnek olarak oluşturulmuştur. Bu yapılandırmaların geleceği, bu değerlendirmenin sonuçlarına ve alınan geribildirimlere bağlıdır.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Örnek ER biçimine uygulanan özellikler
Örnek ER biçimi yapılandırmasında, FTI formları oluşturmak için şablon olarak bir Excel dosyası kullanılır.

![Biçim tasarımcısı](media/FTIbyGER-ERFormat.png)

Şu anda bu örnek ER biçimi, FTI formları oluşturmak için aşağıdaki özellikleri desteklemektedir:

- Hem deftere nakledilen orijinal faturalar için hem de henüz deftere nakledilmeyen orijinal faturalar için FTI formları oluşturulur. Düzeltilmiş faturalar ve alacak dekontları desteklenmez.
- FTI formları fatura dilinde oluşturulur. Oluşturulan formlardaki değerlerin ve tarihlerin biçimi, kullanıcının istemci yerel ayarlarını esas alır.
- İşlenen faturalarda satır yoksa oluşturulan faturalar veri kullanılamıyor bildirimlerini gösterir.
- Oluşturulan fatura başlıkları **Alacak hesapları parametreleri** sayfasında FTI formu için seçilen kağıt biçimini esas alır. Şirket bilgileri, oluşturulan fatura formunun başlığında yalnızca kağıt biçimi boşsa görüntülenir.
- Oluşturulan fatura formları **Alacak hesapları parametreleri** sayfasında FTI formu için uygun seçenek seçildiğinde şirket ve müşteri vergi muafiyet numaralarını gösterir.
- Oluşturulan fatura satırları ve fatura toplamları bölümleri, varsayılan faturanın parasal ayrıntılarını fatura kaydı para birimi cinsinden gösterir.
- Oluşturulan fatura toplamları bölümü **Alacak hesapları parametreleri** sayfasında **Euro'yu temsil eden para birimi cinsinden tutarı yazdır** seçeneği etkinleştirildiğinde para birimi ayrıntılarını Euro para birimi ve fatura kaydı para birimi cinsinden gösterebilir.
- Oluşturulan fatura formları **Alacak hesapları parametreleri** sayfasındaki ayarlara göre kullanılabilir tüm işlenmiş fatura notlarını gösterir. Notlar hem tüm faturaya hem de her bir fatura satırına dahil edilir.
- Oluşturulan fatura formları, AR form notları listesinde yapılandırıldıklarında müşteri FTI formuna ve işlenen fatura diline ilişkin notları içerir.
- Oluşturulan faturalar, Yazdırma yönetimi ayarlarına bağlı olarak fatura dili, ER biçimi ve FTI belge kapsamı için yapılandırıldığında özel altbilgi metni içerir.
- Oluşturulan fatura formlarının toplamlar bölümü kullanılabilir nakit iskontosu bilgilerini içerir.
- Oluşturulan fatura formlarının ödeme planı bölümü, kullanılabilir tüm ödeme planı ayrıntılarını içerir.
- Oluşturulan fatura formlarının kar marjı bölümü, kullanılabilir tüm masraf hareketlerini içerir.
- Oluşturulan fatura formları, **Alacak hesapları parametreleri** sayfasında **Satış vergisi belirtimi** ayarına bağlı olarak satış vergisi ayrıntılarını içerir. Bu bölüm, vergi bilgilerini yalnızca fatura kaydı para birimi cinsinden veya aynı anda fatura kaydı para birimi ve şirket muhasebe para birimi cinsinden gösterebilir.
- Oluşturulan fatura formları hesaptan ödeme bildirimi ayrıntılarını gösterir. Örneğin, fatura için zorunlu hesaptan ödeme talimatı koduna sahip ödeme yöntemi seçildiğinde, işlenen fatura Euro para birimi cinsinden kaydedildiğinde ve fatura için hesaptan ödeme talimatı kodu tanımlandığında ayrıntılar gösterilir.
- Oluşturulan faturalar, deftere nakledilmesi uygun olan faturalar için ön ödeme ayrıntılarını gösterir.
- Oluşturulan fatura formları bir fatura müşterisine e-posta eki olarak gönderilebilir. Kullanılan ER biçimi için uygun ER dosya hedefi yapılandırılmalıdır.

### <a name="countryregion-specific-features"></a>Ülkeye/bölgeye özgü özellikler 
ER yapılandırmalarında belirli gereksinimlerin nasıl ele alınabileceğini göstermek için aşağıdaki ülkeye/bölgeye özgü özellikler örnek ER biçimine dahil edilmiştir.

#### <a name="norway"></a>Norveç
Fatura, aşağıdaki şekilde yapılandırılan bir tüzel kişilik için işlendiğinde Kuruluş kaydı koşulu, oluşturulan fatura formunun başlığına yerleştirilir:

- Norveç için ülke/bölge bağlamı kullanılmıştır.
- **Print Foretaksregisteret** parametresi satış belgelerinde etkindir.

#### <a name="spain"></a>İspanya
Fatura aşağıdaki şekilde yapılandırılan bir tüzel kişilik için işlendiğinde **Kasa muhasebesi yöntemi için özel rejim** koşulu, oluşturulan fatura formunun başlığına yerleştirilir:

- İspanya için ülke/bölge bağlamı kullanılmıştır.
- Kasa muhasebesi yöntemi için özel rejim, fatura işleme tarihinde etkinleştirilir.

Nakit iskontosu tutarı ve fatura satırı net tutarı gibi nakit iskontosu ayrıntıları kullanılabilir olduğunda bunlar, aşağıdaki şekilde yapılandırılmış bir tüzel kişilik için işlenerek oluşturulan fatura formunun fatura toplamları bölümünde gösterilir:

- İspanya için ülke/bölge bağlamı kullanılmıştır.
- Fatura seçeneğinde **Faturada nakit iskontosu uygula** seçeneği açılır (**Genel muhasebe parametreleri** \> **Satış vergisi bölümü**).

#### <a name="italy"></a>İtalya
İtalya için ülke/bölge bağlamı kullanılarak yapılandırılan tüzel kişilik için işlendiğinde oluşturulan faturanın fatura satırlarında mal iskontosu işareti yer alır.

#### <a name="finland"></a>Finlandiya
Oluşturulan fatura formuna ek olarak havale parası transfer makbuzları aşağıdaki şekilde oluşturulabilir:

- Finlandiya için ülke/bölge bağlamını kullanan ve **Havale hesabı** ve **Banka barkodu** olarak işaretli en az bir banka hesabı olan tüzel kişilik için. 
- **Fince** ile ilişkilendirilmiş ödeme ekinin gerektirdiği şekilde işaretlenen bir fatura için.

![Havale makbuzu](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> Örnek ER biçimi, ayrı çalışma sayfasında isteğe bağlı olarak havale parası transfer makbuzu oluşturacak şekilde yapılandırılmıştır.

> [!NOTE]
> Öncelikle Excel formatında oluşturulan fatura formunun önizleme yapılacağı yerel makinede barkod oluşturmak için kullanılan yazı tipini yüklemeniz gerekir.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>E-posta hedeflerini yapılandırmak için örnek ER biçimini kullanma
E-posta hedeflerini yapılandırmak için örnek ER biçimine ilişkin aşağıdaki öğeleri kullanın:

- Müşteri ilgili kişisinin e-posta adresine şu ER ifadesi aracılığıyla erişilebilir: **model.InvoiceBase.Contact.ElectronicMail**.
- E-posta konu metnine şu ER ifadesi aracılığıyla erişilebilir: **Emailing.TxtToUse.Subject**.
- E-posta gövde metnine şu ER ifadesi aracılığıyla erişilebilir: **Emailing.TxtToUse.Body**.

![Hedef ayarları](media/FTIbyGER-ERFileDestinationSettingEmail.png)

Varsayılan e-posta konusu ve gövde metni, örnek ER biçiminde tanımlanır. Dil, biçim etiketlerine bağlıdır. Önceden tanımlanmış **ERFTITMP** koduna sahip özel bir kuruluşun e-posta şablonu eklenmemişse e-postalar için bu varsayılan metin kullanılır.

> [!NOTE]
> **ERFTITMP** e-posta şablonu kodu örnek ER biçiminde tanımlanmıştır. Gerektiğinde, bu örnek biçimden oluşturulan yeni bir ER biçimi olarak değiştirilebilir.

Faturasını işlediğiniz tüzel kişilik için önceden tanımlanmış **ERFTITMP** koduna sahip kuruluşun e-posta şablonu eklenirse, e-posta konusunun ve gövde metninin şablonunu, e-postayı oluşturmak için kullanılır. 

![Kuruluş e-posta şablonları](media/FTIbyGER-EmailTemplate.png)

![E-posta şablonu yükleme](media/FTIbyGER-EmailTemplateBody.png)

Örnek ER biçiminin **Emailing.TxtToUse.Subject** ER ifadesi, %1 yer tutucunun herhangi bir oluşumunu işlenen fatura numarasıyla değiştirecek şekilde yapılandırılmıştır.

Örnek biçimin **Emailing.TxtToUse.Body** ifadesi, yer tutucular için aşağıdaki alternatifler için yapılandırılır:

- "%1", müşteri ilgili kişisinin adıyla değiştirilir.
- "%2" şirket adıyla değiştirilir.
- "%3" müşteri adıyla değiştirilir.
- "%4", şirketin ilgili kişisinin adıyla değiştirilir.
- "%5", şirketin ilgili kişisinin unvanıyla değiştirilir.
- "%6", şirketin ilgili kişisinin e-posta adresiyle değiştirilir.

![E-posta](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Ek kaynaklar
[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)
