---
title: "Kuruluş hiyerarşinizi planlama"
description: "Kuruluşlar ve kuruluş hiyerarşilerini ayarlamadan önce işinizin nasıl en iyi nasıl modellendirileceğini anladığınızdan emin olun."
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d669defa13e8f32cd29463324e580a6d738c3e2a
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-organizational-hierarchy"></a>Kuruluş hiyerarşinizi planlama

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations'da kuruluşlar ve kuruluş hiyerarşilerini ayarlamadan önce işinizin nasıl modellendirileceğini planladığınızdan emin olun. Kuruluş modelinin Finance and Operations'ın uygulanması ve iş süreçleri üzerinde önemli bir etkisi vardır. 

Kuruluş hiyerarşileri, işi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder. Bu nedenle, kuruluşları modellerken dikkate almanız gereken en önemli husus işletmenizin yapısıdır. Kuruluş yapılarını, yöneticilerin ve finans ve muhasebe, insan kaynakları, operasyonlar, satınalma, satış ve pazarlama gibi işlevsel alanlardaki üst düzey yöneticilerin görüşlerini temel belirlemenizi öneririz. 

Hiyerarşileri planlarken, aynı zamanda kuruluş hiyerarşisi ile mali boyutlar arasındaki ilişkiyi dikkate almanız önemlidir. İşinizin farklı görünümlerini göstermek için birden çok kuruluş hiyerarşisi ayarlayabilirsiniz. Mali boyutları kullanarak, bu görünümlere dayalı raporlar oluşturabilirsiniz. Hem kuruluş hem de yasal raporlama gereksinimlerine yönelik hiyerarşileri oluşturmak için Microsoft Dynamics 365 for Finance and Operations iş ortağınızla birlikte çalışın. 

> [!Note]
> Finance and Operations'da tüzel kişilikler oluşturmadan mali boyutları tüzel kişilikleri temsil etmek amacıyla kullanabilmenize karşın, mali boyutlar tüzel kişiliklerin operasyonel veya iş gereksinimlerini karşılamak üzere tasarlanmamıştır. Finance and Operations'daki birimlerarası muhasebe işlevi, yalnızca her hareket tarafından oluşturulan muhasebe girişlerini karşılamak üzere tasarlanmıştır. 

> [!Caution]
> Kuruluş modellerini nasıl yapacağınıza yalnızca bu makaledeki bilgilere dayanarak karar vermemelisiniz. Bu belge bir kılavuzdur. Ek yönergeler için Finance and Operations İş Ortağınızla çalışabilirsiniz. Finance and Operations İi Ortağınız çeşitli endüstrilerde ve müşteri tabanları üzerinde deneyim kazanmıştır.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Dahili kuruluşları tüzel kişilikler olarak mı işletme birimleri olarak mı modelleyeceğinize karar verin.

Finance and Operations'da işinizi temsil etmek için en az bir tüzel kişilik olması gerekir. Tüzel kişilik yasal sözleşmelere girebilir ve performanslarını raporlayacak mali tablolar hazırlaması gerekir. 

Finance and Operations'da tüzel kişilikler hareketsel işler veya konsolidasyon için kullanılabilir. Bu, Finance and Operations'daki bir tüzel kişinin mutlaka işletmenizdeki gerçek bir varlığı temsil etmesi gerekmediği anlamına gelir. Örneğin, hareketlerde yer alan bir şirket bağlı tüzel kişiliklere sahip olabilir. Bu senaryoda, hareketler için bir tüzel kişilik gereklidir ve bağlı tüzel kişiliklerin sonuçlarını ve bakiyelerini konsolide etmek için sanal bir tüzel kişilik gereklidir. 

İşletmenizdeki bölge ofisleri gibi dahili organizasyonlar ek tüzel kişilikler veya ana tüzel kişiliğin işletme birimleri olarak temsil edilebilir. Yasal olarak tanımlanmış bir organizasyon olmak için bir işletme birimi gerekli değildir. İşletme birimleri işletmedeki ekonomik kaynakları ve operasyonel işlemleri denetlemek için kullanılır. Örneğin, departmanlar ve maliyet merkezleri işletme birimleridir. 

Finance and Operations'daki bazı işlevler organizasyonun bir tüzel kişilik veya işletme birimi olmasına bağlı olarak farklı şekilde çalışır. Kararınızı vermeden önce aşağıda açıklanan işlevi dikkatle düşünün. 


### <a name="master-data"></a>Ana veriler
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse      
Müşteriler, ödeme şartları, vergi dairesi ve tesise özel stok siparişi gibi bazı ana veriler, her bir tüzel kişilik için ayarlanmalıdır. Kullanıcılar, ürünler ve çoğu insan kaynakları verileri gibi bazı ana veriler tüm tüzel kişilikler arasında paylaşılır. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Ana veri işletme birimleri arasında paylaşılır. 

### <a name="module-parameters"></a>Modül parametreleri
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse    
Alacak hesapları parametreleri, Borç hesapları parametreleri ve Nakit ve banka yönetimi parametreleri gibi modül parametreleri her tüzel kişilik için ayarlanmalıdır. Tüzel kişilikler için modül kurulumu ayrı olduğundan, her bağlı kuruluşun yerel yasal gerekliliklere ve iş uygulamalarına uyumlu olabilmelidir. Örneğin, profesyonel hizmet tüzel kişiliği ile üretim tüzel kişiliğinin aynı ana şirkete rapor veriyor olmalarına karşın farklı modül parametreleri olabilir. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Modül parametreleri işletim birimleri arasında paylaşılır. 

### <a name="data-security"></a>Veri güvenliği
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse    
Çoğu veri otomatik olarak şirket kimliği ile korunur. Şirket kimliği bir tüzel kişilikle ilişkilendirilen veriler için benzersiz bir tanımlayıcıdır. Bir şirket yalnızca bir tüzel kişilikle ve bir tüzel kişilik yalnızca bir şirketle ilişkilendirilebilir. Kullanıcılar yalnızca erişime sahip oldukları şirketlerin verilerine erişebilir. Verileri şirket kimliğine göre koruma altına almak için Finance and Operations'ı özelleştirmeniz gerekmez. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Veriler her işletme birimi için özelleştirilmiş veri güvenlik ilkeleri oluşturularak güvenlik altına alınabilir. Veri güvenlik ilkeleri, veri erişimini sınırlamak için kullanılır. Örneğin, bir kullanıcıya yalnızca belirli bir işletme biriminde satınalma siparişleri oluşturma izin verildiğini varsayın. Veri güvenlik ilkeleri, kullanıcının diğer işletme birimi satınalma siparişi verilerine erişimini engellemek üzere oluşturulabilir. Hareketlerin hacmi ve güvenlik ilkelerinin sayısı performansını etkileyebilir. Güvenlik ilkeleri tasarlarken performansı göz önünde bulundurun. 

### <a name="ledgers"></a>Genel muhasebe defterleri
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse    
Her bir tüzel kişilik için bir hesap planı, muhasebe para birimi, raporlama para birimi ve mali takvim sağlayan bir defter gereklidir. Bilanço yalnızca bir tüzel kişilik için oluşturulabilir. Ana hesaplar, boyutlar, hesap yapıları, hesap planları ve hesap kuralları birden fazla tüzel kişilik tarafından kullanılabilir.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Bir işletme birimi kendi muhasebe bilgilerine sahip olamaz. Dahili organizasyonlar için benzersiz muhasebe defterleri gerekli değilse, onları işletme birimleri olarak modelleyebilirsiniz. Genel muhasebe bilgileri hiyerarşideki üst tüzel kişilik için ayarlanır. İşletme birimleri için gelir tabloları tüzel kişilik veya üst tüzel kişilik içinde oluşturulabilir. 

### <a name="fiscal-calendars"></a>Mali takvimler 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse    
Her tüzel kişiliğin kendi mali takvimi vardır. Dahili organizasyonlarınız farklı mali yıllar ve mali takvimler kullanıyorsa, organizasyonları tüzel kişilikler olarak modellemeniz gerekir. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
İşletme birimleri mali takvimi paylaşmalıdır. Dahili organizasyonlarınız aynı mali yılları ve mali takvimlerı kullanabiliyorsa, organizasyonları işletme birimleri olarak modelleyebilirsiniz. 

### <a name="consolidation"></a>Konsolidasyon
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse    
Mali tabloları hazırlayabilmek için bölge ofislerinin mali sonuçlarını birleştirilmiş tek bir şirket altında birleştirmeniz gerekir. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Veri zaten işletme birimleri arasında paylaşıldığından konsolidasyon gerekli değildir. 

### <a name="centralized-payments"></a>Merkezi ödemeler
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse 
Merkezi ödemeler ayarlanmalıdır, böylece tüm alt tüzel kişiliklerle ilgili faturalar tek bir üst tüzel kişiliğe veya kişilikten ödenebilir. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Merkezi ödemeler gerekli değildir, çünkü tüm faturalar tek bir tüzel kişilikte kaydedilir.

### <a name="intercompany-transactions"></a>Şirketlerarası hareketler
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse 
Şirketlerarası satış siparişleri, satınalma siparişleri, ödemeler veya girişleri bir başkasına uygulanabilir. Günlük fişleri kullanmanız gerekli değildir. Alt defter düzeyinde (Alacak hesapları, Borç hesapları) şirketlerarası hareketleri görüntüleyebilirsiniz. Aşağıdaki örneklerde şirketlerarası hareketlerin nasıl ele alındığı gösterilmektedir. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Örnek 1: Genel merkez bölgesel ofislere hizmet sağlar ve bu hizmetlerin maliyetini bölgesel ofislerden tahsil etmelidir
Bölgesel ofisi bir tüzel kişilik olarak modellerseniz aşağıdaki seçenekler mevcuttur: 
- Genel merkez gider için bölge ofisini çapraz borçlandırmak üzere bir günlük girişi oluşturur. Hareketler yaşlandırılamaz.
- Genel merkez hizmetler için bölgesel ofise bir satınalma siparişi gönderir. Tüzel kişilikte, şirketlerarası alt muhasebe hareketi ile bölge ofisi için otomatik olarak bir satış siparişi oluşturulur. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Örnek 2: Genel merkez bölge ofisine teslim edilen hizmeti temin eder ve bunun için ödeme yapar
Bölgesel ofisi bir tüzel kişilik olarak modellerseniz aşağıdaki seçenekler mevcuttur: 
- Fatura ve ödeme genel merkezin mevzuat gereksinimlerini izler. Genel merkez gider için bölge ofisini çapraz borçlandırmak üzere bir günlük girişi oluşturur. Hareketler yaşlandırılamaz. 
- Fatura ve ödeme genel merkezin mevzuat gereksinimlerini izler. Genel merkez şirketlerarası alt muhasebe hareketi oluşturabilir.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
İşletme birimleri arasındaki şirketlerarası hareketler yalnızca günlük fişleri aracılığıyla desteklenir. Bir işletme birimi bir satış siparişi, satınalma siparişi veya fatura düzenleyemez veya bunları aynı tüzel kişilikteki diğer işletme biriminden alamaz. Alt defter düzeyinde (Alacak hesapları, Borç hesapları) şirketlerarası hareketleri görüntüleyemezsiniz. Aşağıdaki örneklerde şirketlerarası hareketlerin nasıl ele alındığı gösterilmektedir. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Örnek 1: Genel merkez bölgesel ofislere hizmet sağlar ve bu hizmetlerin maliyetini bölgesel ofislerden tahsil etmelidir
Bölge ofisini bir işletme birimi olarak modellerseniz, genel merkez bir masraf hareketi girer ve bunu bölgesel ofis için kodlar. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Örnek 2: Genel merkez bölge ofisine teslim edilen hizmeti temin eder ve bunun için ödeme yapar.
Bölge ofisini bir işletme birimi olarak modellerseniz, fatura ve ödeme genel merkez mevzuat gereksinimlerini izler. Fatura bölge ofisi için kodlanabilir. Gelir tablosunda, bölge ofisi için maliyetleri raporlamak üzere bir dengeleme mali boyutu kullanın.

### <a name="local-tax-requirements"></a>Yerel vergi gereksinimleri
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Tüzel kişilik, tüzel kişiliğin kayıtlı olduğu ülkenin/bölgenin vergi dairesinin vergi kanunlarına tabidir. Örneğin, Danimarka'da kayıtlı bir tüzel kişilik Danimarka vergi yasalarına ve yönetmeliklerine tabi olur. Finance and Operations'da bir tüzel kişilik yalnızca tek bir ülkeye/bölgeye ait olabilir. Tüzel kişiliğin birincil adresi için seçtiğiniz ülke/bölge, tüzel kişilik tarafından kullanılabilecek ülke/bölgeye özgü özellikleri kontrol etmektedir. Örneğin, tüzel kişiliğin birincil adresi Danimarka'da ise, Danimarka vergi yasaları ve yönetmelikleriyle ilgili özellikler kullanılabilir hale gelir. Bu nedenle, organizasyonlarınız farklı ülkelerde/bölgelerdeyse ve farklı yerel vergi seçenekleri gerekiyorsa, kuruluşları ayrı tüzel kişilikler olarak ayarlamanız gerekir.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
İşletme birimleri üst tüzel kişiliğin ülke bağlamını kullanır. Aynı tüzel kişilikteki işletme birimlerinin farklı ülkeye/bölgeye özgü gereksinimleri olamaz. Organizasyonlarınız aynı ülke/bölge içindeyse ve aynı vergi seçeneklerini kullanıyorsa, bunları işletme birimleri olarak ayarlayabilirsiniz.


### <a name="statutory-reporting-for-a-countryregion"></a>Ülke/bölge için yasal raporlama 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Finance and Operations tarafından desteklenen ülkeler/bölgeler için yasal raporların çoğu oluşturulabilir. Her ülke/bölge için hangi raporların kullanılabilir olduğu hakkında daha fazla bilgi için bkz. Finance and Operations için [Microsoft Dynamics Yerelleştirme Portalı](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC). (Bir CustomerSource oturumu gereklidir.) 

> [!Note]
> Finance and Operations'da genel muhasebedeki deftere nakil katmanı alt şirketten farklı bir muhasebe satndardı kullanan bir ana şirket için ayarlama girişleri yapmanıza olanak sağlar. Örneğin, genel olarak İngiltere'deki kabul görmüş muhasebe uygulamalarını kullanan (UK GAAP) bir şirket için deftere nakil katmanında ayarlama girişleri yapabilirsiniz. Bu girişler, ABD'deki genel kabul görmüş muhasebe ilkelerini (GAAP) kullanan bir ana şirkette birleştirilebilir. Ayarlama girişleri UK GAAP raporunu etkilemez.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Yasal raporlar başka bir uygulama kullanılarak oluşturulmalıdır. Genel merkez gereksinimlerinden farklılık gösteren her işletme biriminin gereksinimlerini destelemek amacıyla bu verilerin Finance and Operations tarafından alındığından emin olmanız gerekir. 

### <a name="currency"></a>Para Birimi
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Organizasyonlarınızın farklı geçerli para birimleri kullanıması gerekiyorsa, organizasyonları tüzel kişilikler olarak modellemeniz gerekir. Geçerli para birimleri her tüzel kişilik için ayarlanır. Ancak, birden fazla para biriminde hareketler girebilirsiniz. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Organizasyonlarınız tek bir geçerli para birimi kullanabiliyorsa, organizasyonları işletim birimleri olarak modelleyebilirsiniz. İşletme birimleri bir geçerli para birimini paylaşmalıdır. Ancak, birden fazla para biriminde hareketler girebilir ve raporlar oluşturabilirsiniz. 


### <a name="year-end-closing"></a> Yıl sonu kapanışı
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Yasalar ve muhasebe uygulamaları, organizasyonlarınızın bulunduğu ülkeler/bölgeler arasında farklılık gösteriyorsa, her organizasyon için farklı yıl sonu yordamları gerekli olabilir. Bu, organizasyonları tüzel kişilikler olarak modellemeniz gerektiği anlamına gelir. Her bir tüzel kişiliğin kendi yıl sonu yordamları vardır. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Yasalar ve muhasebe uygulamaları, organizasyonlarınızın bulunduğu ülkeler/bölgelerde aynıysa, tek bir yıl sonu yordamları kümesi kullanabilirsiniz. Bu, organizasyonları işletme birimleri olarak modelleyebileceğiniz anlamına gelir. Tüm işletme birimlerinin aynı yıl sonu kapatma yordamını kullanması gerekir. 

### <a name="number-sequences"></a>Numara serileri
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Bazı referanslar için numara serileri tüzel kişilik başına ayarlanabilir. Bazı numara serileri paylaşılabilir. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Bazı referanslar için numara serileri işletme birimi başına ayarlanabilir. Bazı numara serileri paylaşılabilir.

### <a name="products"></a>Ürünler 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Ürün tanımları paylaşılır ve hareketlere dahil edilmeden önce ayrı tüzel kişilikler için serbest bırakılması gerekir. Her bir tüzel kişiliğin hareket belgelerine dahil edilebilecek kendi serbest bırakılan ürün kümesi bulunur. Dahili organizasyonlarınızın farklı ürün kümeleri kullanıması gerekiyorsa, organizasyonları tüzel kişilikler olarak modellemeniz gerekir. 

> [!Note]
> Ürün tanımları paylaşılıyor olmasına karşın, bir ürünün serbest bırakıldığı her tüzel kişilikte, her stok tesisindeki madde için farklı satış, satın alma ve stok parametreleri belirtebilirsiniz. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Tüm işletme birimleri ürünleri aynı kümesini paylaşır. Dahili organizasyonlarınız aynı ürün kümelerini paylaşabiliyorsa, organizasyonları işletme birimleri olarak modelleyebilirsiniz. 

### <a name="inquiry-and-reporting"></a>Sorgulama ve raporlama  
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Organizasyon tüzel kişilik olarak modellenmişse
Hareketleri girmek ve birden fazla tüzel kişilikte sorgular gerçekleştirmek için şirketleri el ile değiştirmelisiniz. Veri güvenlik sınırları nedeniyle konsolide sorgulama ve raporlama yoğun kaynak kullanıma neden olabilir ve zaman alıcı olabilir. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Organizasyon bir işletme birimi olarak modellenmişse 
Birden çok işletim birimden verilere erişmek için şirketleri değiştirmeniz gerekmez. Konsolide sorgulama ve raporlama ve ayrı bölgesel sorgulama daha kolay ve hızlıdır.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Organizasyonları ve hiyerarşileri modellemek için en iyi yöntemler
Bir organizasyon hiyerarşisi uygularken aşağıdaki en iyi uygulamaları dikkate alın:
-   Bir tüzel kişilik ile bir işletme birimi arasındaki kesişimi modellemek için bir departman oluşturun. Ardından, yasal raporlama işlemi için verileri bir departmandan tüzel kişiliğe ve dahili raporlama için bir departmandan bir ticari birime aktarabilirsiniz. Departmanlar, kar merkezleri olarak hizmet verebilir. Departmanlar kullanırsanız, hesap yapısında boyutları tüzel kişilikler ve işletme birimleri olarak kullanmanız gerekmez. Boyut olarak yalnızca departmanları kullanabilirsiniz. Ancak,maliyet merkezlerinin yalnızca maliyet toplayıcıları ve departmanların gelir kabulü için kullanılması durumunda hesap yapısında boyut olarak hem maliyet merkezlerini hem de departmanları kullanmanız gerekir.
-   Kar ve zarar raporlama için karmaşık gereksinimleriniz varsa işletme birimleri için birden fazla hiyerarşi modelleyin.
-   Tek bir tüzel kişilik içinde, aynı hiyerarşi amacı için birden fazla hiyerarşi modellemeyin.
-   Her amaç için bir hiyerarşi oluşturmayın. Genellikle, bir hiyerarşiyi birden faza amaç için kullanabilirsiniz. Örneğin, bir işletme birimleri hiyerarşisi, politikayla bağlantılı tüm amaçlara atanabilir.
-   Dengeli hiyerarşiler oluşturun. Bir hiyerarşide kök düğümü ile aynı uzaklıkta bulunan tüm düğümler bir düzey olarak tanımlanır. Dengeli bir hiyerarşi içinde, her düzeyde yalnızca bir işletme birimi türü oluşabilir ve kök düğümün her bir düzeye olan uzaklığı aynıdır. Bir departman ile bir tüzel kişilik veya bir ticari birim arasında ara düzeyler varsa, dengeli bir hiyerarşinin oluşturulması için yer tutucu organizasyonlar gerekebilir.
-   Tüzel kişilikler için yapı aynı zamanda işletim yapınız ise ayrı bir işletme birimleri hiyerarşisi modellemeyin. Tüzel kişilikler ve işletme birimleri içeren karışık bir hiyerarşi her iki amaca da hizmet eder.
-   Temel yeniden yapılandırma senaryoları modellemeden önce bir etki analiz ve bir doğrulama testi gerçekleştirmek için hiyerarşinin geçerlilik tarihlerini kullanın.
-   Bir üretim ortamında yeni bir sürümü yayımlamadan önce hiyerarşi değiştirmek için taslak modunu kullanın.
-   Bir üretim ortamındaki bir hiyerarşiye organizasyon etkilemeye veya bu hiyerarşiden organizasyon çıkarmaya yetkili kişi sayısını sınırlandırın. Bu sayının sınırlandırılması, maliyetli hataların yapılması ihtimalini ve düzeltme ihtiyacını azaltacaktır.

