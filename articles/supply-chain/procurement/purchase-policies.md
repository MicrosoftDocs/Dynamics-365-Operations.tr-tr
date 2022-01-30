---
title: Satınalma ilkelerine genel bakış
description: Bu makale, satınalma ilkeleri hakkında bilgi sağlar. Satınalma ilkesi talep işlemini denetleyen kurallar topluluğudur. Satınalma ilkeleri satınalma yöneticilerinin kuruluşun stratejik satınalma gereksinimlerine uygun bir ilke yapısı oluşturarak satınalma stratejilerini uygulamalarına yardımcı olur.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage, PurchReqControlRule, RequisitionReplenishCatAccessPolicyRule, PurchReApprovalPolicyRule, RequisitionReplenishControlRule, PurchReqControlRFQRule
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11614"
- intro-internal
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cc150ae1a912fbfb4daf505e4240786c2f380a3
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982289"
---
# <a name="purchasing-policies-overview"></a>Satınalma ilkelerine genel bakış

[!include [banner](../includes/banner.md)]

Bu makale, satınalma ilkeleri hakkında bilgi sağlar. Satınalma ilkesi talep işlemini denetleyen kurallar topluluğudur. Satınalma ilkeleri satınalma yöneticilerinin kuruluşun stratejik satınalma gereksinimlerine uygun bir ilke yapısı oluşturarak satınalma stratejilerini uygulamalarına yardımcı olur.

Bir satın alma politikası bir takım politika kurallarından meydana gelir. Bir politika kuralı tanımlarken öncelikle bir kural türü seçersiniz. Ardından, kural için ayarları, başlangıç tarihini ve bitiş tarihini tanımlayarak kural türü için bir kural oluşturursunuz.  

Örneğin, bir yönetici bir kural oluşturur, **Katalog politikası** kural türünü seçer ve ardından politikaya bir katalog politika kuralı ekler. Bu katalog politika kuralı, Macera katalogunun mutlaka dahili satın alma işlemler için kullanılması gerektiğini belirtir. Satın alma politikası belirli bir organizasyon ile ilişkilendirildikten sonra organizasyonun personeli, talep oluşturduklarında Macera katalogunu görür.

## <a name="assigning-policies-to-organizations"></a>Organizasyonlara politika atama
Bir politikanın yürürlüğe girebilmesi için mutlaka bir organizasyonla ilişkilendirilmelidir. Satın alma politikaları, **Satın alma iç kontrol** hiyerarşi amacıyla ilişkilendirilir. Bu nedenle, satın alma politikaları sadece hiyerarşilerde bulunan ve **Satın alma iç kontrolü** hiyerarşi amacına sahip olan organizasyonlar için geçerlidir. Organizasyonları ayrıca CompanyInfo tablosundaki tüzel kuruluşlar düz listesinden de seçebilirsiniz. Bu tüzel kişilikler, politika kapsamında "Şirket" olarak tanımlanır.

## <a name="determining-which-rule-to-apply"></a>Hangi kuralın uygulanacağının belirlenmesi
Satın alma politikalarınızı nasıl yapılandırdığınıza bağlı olarak, bir organizasyondaki kullanıcıları birden çok kural etkileyebilir. Aşağıdaki örneklerde, satın alma politikalarını yapılandırmak ve bir işlem meydana geldiğinde politikaların nasıl uygulanacağını seçmek üzere kullanılabilecek çeşitli yöntemler gösterilmiştir.

### <a name="example-1-simple-purchasing-policy-configuration"></a>Örnek 1: Basit satın alma politikası yapılandırma

Küçük ve daha az karmaşık olan organizasyonlar, satın alma politikalarını tüzel kişiliğe göre kurabilir ve sadece Şirketler organizasyon hiyerarşisini kullanabilir.  

Bir küçük işletme olan Fabrikam için, organizasyon genelinde satın alma gereksinimleri çok düşüktür. Satın alma kuralları sadece organizasyonun tüzel kişilikleri arasında farklı olabilir. Örneğin, Fabrikam Kanada personeli ve Fabrikam ABD personeli farklı kataloglardan ve farklı satıcılardan mal ve hizmet alımı yaparlar. Bu nedenle, Fabrikam, satın alma politikalarını tüzel kişilik düzeyinde kurar.  

Fabrikam, iki satın alma politikası oluşturuyor. ABD tüzel kişiliğine İlke A uygulanır, 1111. Kanada tüzel kişiliğine İlke B uygulanır, 2222. Tüzel kişilik 1111'deki bir personel bir satınalma talebi oluşturduğunda, ilke kuralları A ilkesinden türetilir. Örneğin, personelin gördüğü ürün kataloğu, A ilkesinin katalog ilkesi kuralında belirtilir.  

Tüzel kişilik 2222 personeli bir satınalma talebi oluşturduğunda, ilke kuralları B ilkesinden türetilir.  

**Not:** 1111 tüzel kişiliğinin bir personeli, 2222 tüzel kişiliğinin bir personeli adına bir ürün satın aldığında ise tüzel kişilik 2222 için belirlenen ilke kuralları (yani, ilke B'den alınan ilke kuralları) geçerli olacaktır.

### <a name="example-2-complex-purchasing-policy-configuration"></a>Örnek 2: Kapsamlı satın alma politikası yapılandırma

Önceki örnekte, tüm satın alma kuralları tek bir organizasyon hiyerarşisinde, yani Şirketler organizasyon hiyerarşisine tanımlandı. Ancak, kapsamlı bir organizasyon birden fazla organizasyon hiyerarşisi için politikalar tanımlayabilir.  


Contoso, talep oluşturma sürecini kontrol etmek için kapsamlı satın alma kuralları oluşturması gereken, büyük bir şirkettir. Contoso biri Departman ve diğeri Küresel satın alma kontrolü olmak üzere iki farklı organizasyon hiyerarşisi için kurallar tanımlamıştır.  

Politika 123, Birleşik Krallık Satışları – Satış Departmanı için Departman organizasyon hiyerarşisi için tanımlanmıştır. 123 politikasında satın alma talebi kontrol kuralı, minimum sipariş miktarları için mutlaka uygulanması gereken kısıtlamaları belirler. Bu kuralda **Minimum sipariş miktarı kısıtlamalarını uygula** seçimi yapılmıştır.  

Politika 456, Satış ve Pazarlama departmanı için Küresel satın alma kontrolü organizasyon hiyerarşisi için tanımlanmıştır. 456 politikasında satın alma talebi kontrol kuralı, minimum sipariş miktarları için mutlaka uygulanması gereken kısıtlamaları belirlemez. Bu kuralda **Minimum sipariş miktarı kısıtlamalarını uygula** seçimi kaldırılmıştır.  

Sam, Contoso’nun Birleşik Krallık ofisinde, Birleşik Krallık Satışları – Satış departmanında çalışmaktadır. Hem Departman hem Küresel satın alma kontrolü organizasyon hiyerarşileri için politikalar bu departman için geçerli olacaktır. SAM bir satın alma talebi oluşturduğunda sistemin mutlaka hangi politikayı uygulayacağını belirlemesi gerekir. Sistem yöneticisi, satın alma politikalarının aşağıdaki öncelik sırasına göre uygulanmasını sağlamak için satın alma politikası parametrelerini ayarlar:

1.  Küresel satın alma kontrolü
2.  Departman
3.  Şirketler

Bu nedenle, politika 456, Sam'in oluşturduğu satın alma talebine uygulanır ve satın alma talebi için bir minimum sipariş miktarı gerekli değildir.

## <a name="policy-rules"></a>İlke kuralları
### <a name="catalog-policy-rule"></a>Katalog ilke kuralı

Katalog politika kuralı, hangi satın alma katalogu kullanıcıların satın alma taleplerinin oluşturulduğu zamanı görebileceğini belirler. Bir kullanıcıya başka bir kullanıcı adına ürün sipariş verme izni verilmişse satın alma talebi, hangi katalogun görüntüleneceğini belirlemek için talepte bulunanın tüzel kişiliği ve işletme birimi için tanımlanan katalog politika kuralını kullanır. Bir katalog politika kuralı tanımlamadan önce mutlaka bir satın alma katalogu oluşturmanız ve yayınlamanız gerekir.

### <a name="category-access-policy-rule"></a>Kategori erişimi ilke kuralı

Kategori erişimi politika kuralı, satın alma talepleri oluşturulduğunda hangi kategori kullanıcılarının erişime sahip olacağını belirler. Hiçbir kural yoksa tüm tedarik kategorileri, satın alma talebine eklenebilir.

1.  Ana organizasyonun kategori erişim politikası kuralını kategoriye uygulamak için **Ana kuralı ekle** öğesini seçin.
2.  **Mevcut kategoriler** panosu altından kuralın uygulanacağı kategorileri seçin. Bir kategori seçtiğinizde hiyerarşide bu kategoriden daha yüksek olan tüm kategoriler **Seçilen kategoriler** listesine eklenir.
3.  Kuralı seçilen kategorinin tüm alt kategorilerine uygulamak için **Alt kategorileri dahil et** öğesini seçin.

### <a name="category-policy-rule"></a>Kategori ilke kuralı

Kategori politika kuralı, kullanıcıların her bir kategori için satıcıları nasıl seçeceğini tanımlar. Ayrıca, teslim alma ve faturalandırma süreçleri için gereksinimleri de tanımlar.

### <a name="re-approval-rule-for-purchase-orders"></a>Satın alma emirleri için yeniden onaylama kuralı

Yeniden onaylama, bir satın alma emri değiştirildiğinde yeniden onay gerektiren kriterleri tanımlayan, isteğe bağlı bir kuraldır. İş akışında "Satın alma emri yeniden onayı gerekiyor" koşulu ayarlandığında seçilen alanlar satın alma emri iş akışında değerlendirilir.

> [!NOTE]
> Muhasebe dağıtımı, değişim yönetimi etkinleştirilmiş bir onaylanmış bir satınalma siparişi değiştirildiğinde her zaman sıfırlanacaktır. Yani, belirli alanlar değiştirildiğinde satınalma siparişinin yeniden onaylanmasını önlemek istiyorsanız, alan Muhasebe dağıtımı.değişiklik yeniden onay için seçilmiş bir alan olarak dahil EDİLMEMELİDİR: 

### <a name="purchase-requisition-rfq-rule"></a>Satın alma talebi RFQ kuralı

Satın alma talebi RFQ kuralı bir satın alma talebi satırı için teklif talebi (RFQ) gerektiren kriterleri tanımlar. Bir satır, koşulları karşılıyorsa talep satırında "resmi olmayan RFQ" veya "resmi RFQ" damgası görünür.

### <a name="purchase-requisition-control-rule"></a>Satınalma talebi denetim kuralı

**Tüketim** türündeki taleplerin satınalma talebi kontrol kuralı isteğe bağlı bir kuraldır. Bu türde kurallar oluşturduğunuzda çeşitli sekmelerdeki seçenekleri yapılandırabilirsiniz:

-   **İş akışı gönderme** sekmesinde talebin onaya gönderilebilmesi için talep satırında mutlaka doldurulması gereken alanları yapılandırabilirsiniz.
-   **Sipariş miktarları** sekmesinde, belirli koşullar altında satın alma talebinde mutlaka bulunması gereken alanları yapılandırabilirsiniz. Sipariş miktarlarını da zorlayabilirsiniz.
-   **Tarihler** sekmesinde, hesaplama tarihinin talep edilen tarihle aynı olup olmayacağını yapılandırabilirsiniz.
-   **Adres** sekmesinde, kullanıcının satın alma talebine uygulanmak üzere sistemde yeni adres oluşturmasına izin verilip verilmeyeceğini tanımlayabilirsiniz.

### <a name="requisition-purpose-rule"></a>Talep amacı kuralı

Talep amacı kuralı, belirli bir tüzel kişilik için izin verilen talep amacı türünü tanımlayan, isteğe bağlı bir kuraldır. Bu kural altında başka bir amaç belirtilmediği sürece talepler oluşturulduğunda otomatik olarak **Tüketim** amacını alacaktır.

### <a name="replenishment-category-access-policy-rule"></a>Stok yenileme kategorisi erişim ilkesi kuralı

Stok yenileme kategori erişim politikası kuralı, talep amacı **Stok yenileme** olduğunda belirli bir tüzel kişilik için talep isteğinin yerine getirilmesi için mevcut ürünleri belirleyen, isteğe bağlı bir kuraldır.

### <a name="replenishment-control-rule"></a>Stok yenileme denetim kuralı

Stok yenileme kontrol kuralı, talep amacı **Stok yenileme** olduğunda talebin onaya gönderilebilmesi için talep satırında bulunması gereken alanları tanımlayan, isteğe bağlı bir kuraldır.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Satınalma siparişi oluşturma ve talep konsolidasyon kuralı

Satınalma siparişi oluşturma ve konsolidasyon kuralı isteği, onaylanan bir satınalma talebinden bir satınalma siparişi oluşturulurken kullanılacak ilke kurallarını tanımlar. Bu türde kurallar oluşturduğunuzda çeşitli sekmelerdeki seçenekleri yapılandırabilirsiniz:

-   **Satın alma emrini böl** sekmesinde, satın alma talep satırlarını ayrı satın alma taleplerine bölmeniz için kriterlerini tanımlayabilirsiniz.
-   **Fiyat/iskonto transferi** sekmesinde, bir satın alma emri oluşturulduğunda fiyat anlaşmasının ne zaman yeniden hesaplanacağını tanımlayabilirsiniz:
    -   **Sadece ticaret anlaşması yoksa** – fiyatlar ve iskontolar, satın alma talebinden ancak bir ticaret anlaşması veya taban fiyat bulunmuyorsa transfer edilir. Ürün veya satıcı için bir ticaret anlaşması veya taban fiyatı bulunuyorsa fiyatlar ve iskontolar, ticaret anlaşmasına veya taban fiyatına dayalı olarak yeniden hesaplanır ve satın alma emrine uygulanır. Aksi belirtilmediği sürece varsayılan davranış bu şekildedir.
    -   **Her zaman** – Fiyatlar ve iskontolar her zaman satın alma talebinden transfer edilir.

    Ayrıca, talepte bulunan kişinin tanımlanan fiyat/iskonto transfer kuralı ne olursa olsun her bir satın alma talebi satırı için fiyat ve iskonto transfer yöntemini değiştirmesine izin verebilirsiniz. Bu özelliği etkinleştirmek için **Her bir satın alma talebi satırı için manuel atlatmaya izin ver** öğesini seçin.
-   **Madde açıklaması transferi** sekmesinde, bir RFQ'dan geliyorsa madde açıklamasını talepten transfer edebilirsiniz.
-   **Fiyat Toleransı** sekmesinde, bir tedarik katalogu maddesinin fiyatı arttığında onaylanan satın alma taleplerinin tekrar gözden geçirme sürecine tabi tutulmasını sağlamak için kurallar tanımlayabilirsiniz. Bir satın alma talebinde bir satır maddesindeki net tutarın, satın alma talebinin onaylandığı zaman ile satın alma emrinin oluşturulduğu zaman arasında kalan sürede yükselebileceği maksimum tutarı ayarlayın. Net tutar aşağıdaki formül kullanılarak hesaplanır: (\[Miktar × (Birim fiyat – İskonto) ÷ Fiyat birimi\] + Satın alma muhtelif giderleri) × (100 – İskonto yüzdesi) ÷ 100 Ayarladığınız fiyat toleransını geçen satın alma talebi satırları manuel işleme için tutulur. **Hata işleme** sekmesinde yapılandırılan kurallar, satın alma talebi satırlarının nasıl işleneceğini belirler.
-   **Hata işleme** sekmesinde, bir satıcı hatası veya bir fiyat toleransı hatası nedeniyle satın alma emri oluşturulması sırasında doğrulamanın başarısız olması durumunda satın alma talebine uygulanacak işleme kuralını yapılandırabilirsiniz. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Eylem yok** – Satın alma talebi satırları **Onaylanan satın alma taleplerini serbest bırak** sayfasında kalır. Satın alma talebi satırlarının durumu **Onaylandı** olarak kalır. Ancak, satın alma talebi satırları için bir satın alma emri oluşturulmadan önce hataların mutlaka giderilmesi gerekir.
    -   **Satın alma talebi satırını iptal et** – Satın alma talebi satırları iptal edilir. Talepte bulunan kişi hala satır maddelerini talep etmek istiyorsa iptal edilen satırlar için yeni bir satın alma talebi oluşturabilir.
    -   **Yeni bir satın alma talebi satırı oluştur** – Satın alma talebi satırları iptal edilir. Sadece doğrulamadan geçemeyen satın alma talebi satırlarını içeren, yeni satın alma talepleri oluşturulur. Oluşturulan yeni satın alma taleplerinin durumu **Taslak** olarak ayarlanır. Bu satın alma talepleri, doğrulama hataları giderildikten sonra gözden geçirilmek üzere yeniden gönderilebilir. Satın alma talebi satırlarını hazırlayan kişi, satırların iptal edildiği ve başarısız olan satın alma talebi satırları için yeni satın alma taleplerinin oluşturulduğu konusunda bilgilendirilir.
-   **Manuel satın alma emri oluşturma** sekmesinde bir satın alma talebinin mutlaka manuel olarak işlenmesinin gerekli olup olmadığını veya bunun otomatik olarak bir satın alma emrine dönüştürülüp dönüştürülmeyeceğini tanımlayabilirsiniz. Parametreler dahili katalog maddeleri, harici katalog maddeleri ve katalog dışı maddeler için geçerli olabilir. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Manuel olarak satın alma emirleri oluştur** – Tüm satın alma talepleri için satın alma emirleri manuel olarak oluşturulur.
    -   **Otomatik olarak satın alma emirleri oluştur** – Onaylanmış tüm satın alma talepleri için satın alma emirleri otomatik olarak oluşturulur. Manuel satın alma emir oluşturma işlevi için hiçbir satın alma talebi tutulmaz.
    -   **Bu koşullar altındakiler dışındaki satın alma emirlerini otomatik olarak oluştur** – Tanımladığınız kriterlerle eşleşen satın alma talepleri için satın alma emirleri manuel olarak oluşturulur. Onaylanmamış diğer tüm satın alma talepleri otomatik olarak satın alma emirlerine dönüştürülür. **Bu koşullar altındakiler hariç satın alma emirlerini otomatik olarak oluştur** öğesini seçerseniz, manuel işleme için hangi onaylanmış satın alma talebi satırlarının tutulacağını belirlemek için satın alma kategoriler ve satıcılar ekleyebilirsiniz. Bu seçenek dahili katalog maddeleri, harici katalog maddeleri ve katalog dışı maddeler için geçerli olabilir. Bir tedarik kategorisi seçtiğinizde, bu tedarik kategorisi için mevcut alt kategoriler de seçilir. Belirli bir satın alma talebi türü için tüm satırları manuel işlemek üzere tutmak istiyorsanız, istediğiniz satın alma türü için **Tümü** öğesini seçin.

    Satın alma emri için toplu iş oluşturma işlevi kullanılırken satın alma emirlerinin onaylanmış satın alma taleplerinden otomatik olarak oluşturulmasını istiyorsanız, **Otomatik satın alma emri oluşturma işlevini bir yığın iş olarak yürüt** öğesini seçin. Bu seçenek sadece manuel işleme gerektirmeyen satın alma talepleri için geçerlidir. Otomatik satın alma emri oluşturma işlemini bir toplu iş olarak yürüterek, kaynakların kısıtlayıcı olmadığı durumlarda bu işlemi tek seferde planlayabilirsiniz. Satın alma talep satırlarında **Ön ödeme gerekiyor** öğesi seçilmişse, onaylanan satın alma taleplerini manuel işleme için tutmak üzere **Talep ön ödeme için ayarlandığında** öğesini seçin. Manuel işleme için tutulan satın alma talepleri, sadece ön ödeme gerektiren satın alma talep satırları görüntülenecek şekilde filtrelenebilir.
-   **Talep birleştirme** sekmesinde, manuel olarak işlenen satın alma taleplerinin satın alma talebi birleştirilmesi için dikkate alınıp alınmayacağını belirleyen parametreleri tanımlayabilirsiniz. Parametreler dahili katalog maddeleri, harici katalog maddeleri ve katalog dışı maddeler için geçerli olabilir. Aşağıdaki seçeneklerden birini belirleyin:
    -   **Talep birleştirmeye izin verme** – Talep birleştirme için onaylanan satın alma talebi satırlarının hiçbiri kullanılmaz. Bu seçenek varsayılan olarak seçilidir ve yalnızca satın alma emrinin oluşturulması için manuel işleme gerektiren satın alma talebi satırları için geçerlidir.
    -   **Talep birleştirmeye daima izin ver** – Tüm onaylanan satın alma talebi satırları talep birleştirme için uygundur. **Not:** **Talep birleştirme** sekmesinden **Talep birleştirmeye daima izin ver** öğesini seçerseniz, ancak **Manuel satın alma emri oluşturma** sekmesinin altından **Satın alma emirlerini otomatik olarak oluştur** öğesini seçerseniz, tüm satın alma talepleri manuel işleme için tutulacaktır.
    -   **Bu koşullarda talep birleştirmeye izin ver** – Onaylanan satın alma talebi satırlarının talep birleştirme için uygun olup olmadığını belirleyen kriterleri tanımlayın. Her bir satın alma talebi satırı türü için, tedarik kategorisine ve satıcıya göre kriterler ayarlayabilirsiniz. **Bu koşullarda talep birleştirmeye izin ver** öğesini seçerseniz, her bir satın alma talebi satırı türü için kriterleri tedarik kategorisine ve satıcıya göre ayarlayabilirsiniz. Bir tedarik kategorisi seçtiğinizde, bu tedarik kategorisi için mevcut alt kategoriler de seçilir. Belirli bir satır türü için **Tümü** öğesini seçerseniz, bu satır türündeki tüm satın alma talebi satırları talep birleştirme için uygun olacaktır.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]