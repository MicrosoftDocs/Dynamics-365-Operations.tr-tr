---
title: Fiyatlandırma ayarları
description: Bu makalede, Microsoft Dynamics 365 Commerce headquarters'daki fiyatlandırma ve iskonto yönetimiyle ilgili çeşitli ayarlar açıklanır.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 79130e0ef285d6bd5e544f2d6a6368c0393fa7fa
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474055"
---
# <a name="pricing-settings"></a>Fiyatlandırma ayarları

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce headquarters'daki fiyatlandırma ve iskonto yönetimiyle ilgili çeşitli ayarlar açıklanır. Bu ayarlar, kuruluşların, belirli iş ihtiyaçlarını karşılamak üzere Commerce çözümünde fiyatlandırma davranışı tanımlamasına olanak tanır.

## <a name="company-level-pricing-settings"></a>Şirket düzeyi fiyatlandırma ayarları

Fiyatlandırma ayarlarının çoğu şirket düzeyindedir ve Commerce headquarters'da **Commerce parametreleri \> Fiyatlar ve iskontolar**'da bulunabilir.

### <a name="best-price-and-compound-concurrency-control-model"></a>En iyi fiyat ve bileşik eşzamanlılık denetim modeli

**En iyi fiyat ve bileşik eşzamanlılık denetim modeli** ayarı, fiyatlandırma altyapısının **en iyi fiyat** veya **bileşik** eşzamanlılık modunda çoklu indirimleri nasıl işleyeceğini belirler. 

Parametre **En iyi fiyat ve öncelik içinde bileşim, öncelikler arasında kesinlikle bileşim yok** olarak ayarlanmışsa, aynı fiyatlandırma önceliğine sahip tüm **bileşik** iskontolar bileştirilir. Bileşik sonuç daha sonra, aynı fiyatlandırma önceliğine sahip olan herhangi bir **en iyi fiyat** ile rekabet eder, en iyi fiyat uygulanır ve fiyatlandırma önceliği daha düşük olan hiçbir iskonto dikkate alınmaz.

Parametre **Yalnızca öncelik içinde en iyi fiyat, öncelikler genelinde her zaman bileştir** olarak ayarlanırsa tüm **bileşik** iskontolar **en iyi fiyat** iskontoları olarak ele alınır. Fiyatlandırma önceliğinde yalnızca tek bir iskonto kazanır. Bu tek iskonto **en iyi fiyat** iskontosu veya **bileşik** iskonto ise, daha düşük bir fiyatlandırma önceliği olan tüm ek **en iyi fiyat** iskontoları veya **bileşik** iskontolarla bileştirilir.

### <a name="discount-compound-behavior"></a>Bileşik iskonto davranışı

**İskonto bileşik davranışı** ayarı, fiyatlandırma altyapısının birden çok bileşik iskontoyu nasıl hesaplayacağını belirler.

Parametre **Bileşik** olarak ayarlandığında, bir indirim diğerinin üzerine birikecek şekilde uygulanır. **Orijinal fiyat üzerinden bileşik** olarak ayarlandıysa, tüm iskontolar birbirinden bağımsız olarak değerlendirilir ve aynı orijinal fiyata uygulanır.

Örneğin, 100 $ orijinal fiyatına sahip bir ürün için, yüzde 10 ve yüzde 20 indirimlerini bileştirmek istiyorsunuz. **İskonto bileşik davranışı** parametresini **Bileşik** olarak ayarlarsanız, son fiyat 72 $ (100 $ &times; %90 &times; %80) olur. **Orijinal fiyat üzerinden bileşik** olarak ayarlarsanız son fiyat 70 $ (100 $ – 10 $ – 20 $) olur.

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Özel eşik ile diğer periyodik iskontolar arasında karşılaştırmayı etkinleştirme

**Özel eşik ile diğer periyodik iskontolar arasında karşılaştırmayı etkinleştir** parametresi **Evet** olarak ayarlandığında fiyatlandırma altyapısı, özel eşik iskontolarının özel eşik olmayan iskontolarla rekabet etmelerini sağlar. Fiyatlandırma önceliği yine de geçerlidir. **En iyi fiyat** ve **bileşik** eşik iskontolarının davranışı olduğu gibi kalır. Başka bir deyişle, eşik olmayan iskontolarla rekabet etmezler.

### <a name="manual-line-discount-and-system-discount"></a>El ile satır iskontosu ve sistem iskontosu

**El ile satır iskontosu ve sistem iskontosu** ayarı, fiyatlandırma altyapısının aynı satıra el ile satır iskontosu ve sistem iskontosunu nasıl uygulayacağını belirler. El ile satır iskontosu sistem iskontosunun üzerine bileştirilebilir veya sistem iskontosunu değiştirebilir. El ile satır iskontosu ve sistem iskontosu bileştirildiğinde hesaplama mantığı, **İskonto bileşik davranışı** ayarına uyar. Tüm sipariş için geçerli olan el ile toplam iskonto bu ayara uymaz.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>İskonto fiyatı yuvarlama işlemi için maddeleri aynı satış satırında tut

Bazı durumlarda, miktar iskontosu tutarı uygun miktara eşit olarak bölünemeyebilir (örneğin, iskonto tutarı satın alınan üç birim için 10 $ ise). Bu gibi durumlarda, **İskonto fiyatı yuvarlama işlemi için maddeleri aynı satış satırında tut** ayarı fiyatlandırma altyapısının nasıl uygulanacağını ve bu iskonto tutarının nasıl dağıtılacağını belirler. Parametre **Evet** olarak ayarlanırsa, indirim tutarı bir bütün olarak uygulanır ve bölünmez. **Hayır** olarak ayarlandıysa, indirim tutarı uygun miktara bölünür ve yuvarlanır. Örneğin, üç birime yönelik 10 $ indirim tutarı bir birim için 3,33 $, ikinci birim için 3,33 $ ve üçüncü birim için 3,34 $ olarak bölünür.

### <a name="apply-discounts-to-key-in-price-products"></a>Fiyatı kasada girilen ürünlere iskonto uygulama

**Fiyatı kasada girilen ürünlere iskonto uygula** ayarı iskontoların satış noktasında (POS) girilen "fiyat anahtarları" ile birlikte uygulanıp uygulanmayacağını belirler. Ürün yapılandırmasındaki **Fiyat anahtarı** ayarı, bir ürünün fiyat anahtarını destekleyip desteklemediğini ve nasıl desteklediğini belirler.

### <a name="apply-discounts-to-price-overrides"></a>Fiyat geçersiz kılma işlemlerine iskonto uygulama

**Fiyat geçersiz kılma işlemlerine iskonto uygula** ayarı, iskontoların fiyat geçersiz kılmalarıyla birlikte uygulanıp uygulanmayacağını belirler.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>En ucuz iskontolar için iskontoları dağıtma

"En ucuz" hesaplama türünü kullanan karıştır ve eşle iskontoları için, **En ucuz iskontolar için iskontoları dağıt** ayarı, fiyatlandırma altyapısının iskontoyu satırlar arasında dağıtıp dağıtmayacağını belirler.

Parametre **Hayır** olarak ayarlanırsa, indirim yalnızca en ucuz satırlara uygulanır. Örneğin, "2 alana 1 hediye" karıştır ve eşleştir indirimi için, en ucuz madde ücretsiz, diğer iki madde ise tam fiyat olur. Bu durumda, tam fiyatlı maddeleri iade eden bir müşteri yine de üçüncü öğeyi ücretsiz olarak alacaktır. Bu senaryo satıcı için bir kayba neden olabilir.

Parametre **Evet** olarak ayarlanırsa, fiyatlandırma altyapısı iskontoyu ilgili satırların tümüne dağıtır. Bu ayar, iadelerden ortaya çıkan kaybın azaltılmasına yardımcı olabilir.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Çok satırlı fiyatları ve iskontoları el ile hesapla

**Çok satırlı fiyatları ve iskontoları el ile hesapla** ayarı, fiyatlandırma altyapısının POS uygulaması ve çağrı merkezi kanalı için gecikmeli fiyat ve iskonto hesaplaması kullanıp kullanmadığını kontrol eder. Parametre **Evet** olarak ayarlanırsa, POS uygulamasında veya çağrı merkezi kanalında bir satış siparişi oluşturulduğunda veya düzenlendiğinde, fiyatlandırma altyapısı çok satırlı iskontoları (miktar iskontoları, eşik iskontoları ve karıştır ve eşle iskontoları gibi) hemen hesaplamaz.

> [!NOTE]
> Commerce sürüm 10.0.30 ve önceki sürümlerde, **Çok satırlı fiyatları ve iskontoları el ile hesapla** ayarı yalnızca çağrı merkezi kanalını kontrol eder. İşlev profilindeki ayrı bir **Birden fazla madde iskontosunu el ile hesapla** ayarı, POS uygulamasındaki fiyat hesaplama davranışını denetler. Commerce sürüm 10.0.31'de, iki ayar tek bir şirket düzeyinde ayar olarak birleştirilir.

### <a name="retention-period-in-days"></a>Gün olarak tutma dönemi

**Gün olarak tutma süresi** ayarı, sona erme tarihinden (sona erme tarihi ayarlanmış ise) veya devre dışı bırakma tarihinden (sona erme tarihi ayarlanmamışsa) kaç gün sonra bir indirimin sistematik olarak silinip silinmeyeceğini gösterir. Parametre **0** (sıfır) olarak ayarlandığında, otomatik silme gerçekleşmez.

> [!NOTE]
> Commerce sürüm 10.0.30 ve önceki sürümlerde bu ayar **Süresi dolan iskontoların silinmesi için geçmesi gereken gün sayısı** olarak adlandırılır.

### <a name="coupon-bar-code"></a>Kupon barkodu

**Kupon barkodu** ayarı, kupon barkodları oluşturmak için hangi barkodun kullanıldığını belirler. Kullanıcılar, **Barkod kurulumu** sayfasında yapılandırılan önceden tanımlanmış barkodlar arasından birini seçebilir. Barkodlar ve barkod maskeleri hakkında daha fazla bilgi için bkz. [Barkodları ayarlama](set-up-bar-codes.md) ve [Barkod maskelerini ayarlama](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kupon kodu iade hareketlerine el ile uygulanmalıdır

**Kupon kodu iade hareketlerine el ile uygulanmalıdır** ayarı yalnızca satış makbuzu sağlanmayan iade hareketleri için geçerlidir. Kupon kodlarının harekete otomatik olarak uygulanması gerekiyorsa, parametreyi **Hayır** olarak ayarlayın. Kupon kodlarının harekete el ile eklenmesi gerekiyorsa **Evet** olarak ayarlayın.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Kuruluş için ayarlanan satış sözleşmelerini kullan

İşletmeler arası (B2B) siparişlerde, **Kuruluş için ayarlanan satış sözleşmelerini kullan** parametresi **Evet** olarak ayarlanmışsa fiyatlandırma altyapısı, sözleşmeye dayalı fiyatı belirlemek için kullanıcının müşteri hiyerarşisindeki kuruluş için tanımlanan satış sözleşmelerini kullanır. Parametre **Hayır** olarak ayarlanırsa veya müşteri hiyerarşisi tanımlanmamışsa fiyatlandırma altyapısı, sözleşmeye dayalı fiyatı belirlemek üzere kullanıcı için tanımlanan satış sözleşmelerini arar. B2B e-ticaret için müşteri hiyerarşileri hakkında daha fazla bilgi için bkz. [Müşteri hiyerarşilerini kullanarak B2B iş ortaklarını yönetme](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Kanal düzeyi fiyatlandırma ayarları

Aşağıdaki ayarlar, kuruluşların belirli satış kanallarındaki fiyatlandırma davranışını denetlemesini sağlar.

### <a name="enable-order-price-control"></a>Sipariş fiyatı denetimini etkinleştir

**Sipariş fiyatı denetimini etkinleştir** parametresi, **Çağrı merkezi yapılandırması** sayfasının **Genel** hızlı sekmesinde bulunur. Ayar, fiyatlandırma altyapısının çağrı merkezi kanalındaki fiyat geçersiz kılma işlemi üzerinde bir kısıtlamayı zorunlu kılıp kılmayacağını belirler. Bu işlem, ürün düzeyindeki **Fiyat ayarlamasına izin ver** ayarıyla birlikte çalışır.

Sipariş fiyatı kontrolü kapatılmışsa, tüm çağrı merkezi kullanıcıları, ilgili ürünlerin fiyat ayarlamasına izin verip vermediği dikkate alınmadan, çağrı merkezi kanalındaki satış satırlarında fiyat değişiklikleri yapabilir.

Sipariş fiyatı kontrolü açıksa, yalnızca **Fiyat ayarlamasına izin ver** parametresinin **Evet** olarak ayarlandığı ürünler çağrı merkezi kanalı satış siparişlerinde fiyat geçersiz kılmalara izin verir ve ilgili satış satırlarında bir neden kodu sağlanmalıdır. Bir çağrı merkezi kullanıcısı satış fiyatını yalnızca, **Retail ve Commerce \> Kanal kurulumu \> Çağrı merkezi kurulumu \> Geçersiz kılma izinleri** ile tanımlanan **Kar marjı yüzdesi** değerine kadar değiştirebilir. Bir fiyat geçersiz kılması bu yüzdeyi aşarsa, kullanıcının bir istek göndermesi gerekir. Bu istek daha sonra daha sonra, gözden geçirme ve onay için önceden tanımlanmış bir Commerce iş akışı üzerinden işlenir. Commerce iş akışları oluşturmayla ilgili daha fazla bilgi için bkz. [İş akışı sistemine genel bakış](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system).

## <a name="product-level-pricing-settings"></a>Ürün düzeyi fiyatlandırma ayarları

Aşağıdaki ayarlar, fiyatlandırma kurallarını ürün düzeyinde uygular ve bir kuruluşun **Ürün yapılandırması** sayfasında bulunabilir.

### <a name="allow-price-adjust"></a>Fiyat ayarlamasına izin ver

**Fiyat ayarlamasına izin ver** parametresi **Evet** olarak ayarlanmışsa, çağrı merkezi kanalı satış siparişlerindeki ürüne bir fiyat geçersiz kılma uygulanabilir.

### <a name="key-in-price"></a>Fiyat gir

**Fiyat anahtarı** ayarı, POS'taki bir satış hareketine ürün eklendiğinde bir fiyat anahtarının zorunlu olup olmadığını belirler. Ayrıca karşılık gelen fiyat değeri sınırlamalarını da tanımlar.

### <a name="zero-price-valid"></a>Sıfır fiyat geçerli

**Sıfır fiyat geçerli** ayarı, bir ürün için önceden tanımlanmış, sistem tarafından hesaplanan veya el ile düzeltilmiş satış fiyatlarının 0 (sıfır) olup olamayacağını belirler. Sıfır fiyatına izin veriliyorsa parametreyi **Evet** olarak ayarlayın. Bu ayar ayrıca Commerce ürün hiyerarşisinden kategori düzeyinde de belirtilebilir.

### <a name="prevent-all-discounts"></a>Tüm iskontoları engelle

**Tüm iskontoları engelle** parametresini **Evet** olarak ayarlayarak, her türlü iskonto tipinin (el ile yapılan iskontolar dahil) bir ürüne uygulanmasını engellersiniz. Bu ayar ayrıca Commerce ürün hiyerarşisinden kategori düzeyinde de belirtilebilir.

> [!NOTE]
> Bu ayar, fiyat geçersiz kılma işlemini kısıtlamaz çünkü bu işlem, fiyatı belirler ve bir indirim olarak görülmez.

### <a name="prevent-manual-discounts"></a>İle ile iskontoları engelle

**El ile iskontoları engelle** parametresini **Evet** olarak ayarlayarak, el ile satır veya hareket iskontolarının bir ürüne uygulanmasını engellersiniz. Diğer tüm iskontolar yine de uygulanabilir. Bu ayar ayrıca Commerce ürün hiyerarşisinden kategori düzeyinde de belirtilebilir.

> [!NOTE]
> Bu ayar, fiyat geçersiz kılma işlemini kısıtlamaz çünkü bu işlem, fiyatı belirler ve bir indirim olarak görülmez.

### <a name="prevent-retail-discounts"></a>Perakende iskontolarını engelle

**Perakende iskontolarını engelle** parametresi **Evet** olarak ayarlanırsa, **basit**, **miktar**, **eşik**, **karıştır ve eşleştir** ve **sevkiyat** iskontoları bir ürüne uygulanamaz. Diğer tüm iskontolar (el ile iskontolar dahil) yine de uygulanabilir.

### <a name="prevent-tender-based-discounts"></a>Ödeme tabanlı iskontoları engelle

**Ödeme tabanlı iskontoları engelle** parametresi **Evet** olarak ayarlanırsa, bir ürüne **ödeme tabanlı** bir iskonto uygulanamaz. Diğer tüm iskontolar (el ile iskontolar dahil) yine de uygulanabilir.

Perakendeciler, yeni maddeler veya talep edilen maddeler gibi bazı ürünleri madde tabanlı iskontolar (basit iskontolar ve miktar iskontoları) dışında tutmayı seçer. Ancak bir müşteri tercih edilen ödemeyi kullanarak ödeme yaparsa, ödeme tabanlı iskontolar uygulamak isteyebilirler. Bu sonucu elde etmek için perakendeciler, **Tüm iskontoları önle** ve **Ödeme tabanlı iskontoları önle** parametrelerini **Hayır** olarak ayarlayabilir ve **Perakende iskontolarını önle** ve **El ile iskontoları önle** parametrelerini **Evet** olarak ayarlayabilir.

## <a name="deprecated-or-removed-settings"></a>Kullanım dışı bırakılan veya kaldırılan özellikler

Aşağıdaki fiyatlandırma ayarları Dynamics 365 Commerce'ten kaldırılmış veya bunların kaldırılması planlanmıştır.

| Ayar | Kullanım dışı bırakma veya kaldırma nedeni | Kullanım dışı bırakma veya kaldırma durumu |
|---------|-----------------------------------|-------------------------------|
| Çakışan iskontoları işleme | Fiyatlandırma altyapısının nasıl arama yaptığını ve uygulanacak en iyi iskonto birleşimini nasıl belirlediğini kontrol etmek için Commerce parametrelerinde bu ayarı sağladık. **En iyi iskonto** seçeneği, fiyatlandırma hesaplaması sırasında tüm olası iskonto kombinasyonlarını zorlar. **En iyi performans** seçeneği, en iyi birleşimi zamanında önceliklendirmek, değerlendirmek ve belirlemek için buluşsal algoritma kullanan optimize edilmiş bir seçenektir. Kod tabanındaki **Dengelenmiş hesaplama** seçeneği **En iyi performans** seçeneği ile aynı şekilde çalışır. Bu nedenle, bu seçenek esasen yinelenmiş bir seçenektir. Performansın artırılmasına yardımcı olmak için fiyatlandırma altyapısı, standart seçenek olarak yalnızca **En iyi performans** kullanacak şekilde güncelleştirilmiştir. Bu nedenle, bu ayar artık uygulanabilir değildir. | 10.0.21 sürümünde kullanım dışı bırakıldı ve 2022 Ekim'de kaldırılacaktır. |
| Fiyat ayarlamalarının ürün fiyatını artırmasına izin verme | Fiyat ayarlama işlevinin ürün fiyatlarını artırıp artıramayacağını kontrol etmek için bu ayar kullanılıyordu. Parametre kapalıysa kuruluşlar yalnızca, bir ürünün birim fiyatını taban fiyatından ve ticari sözleşme satış fiyatından daha düşük olacak şekilde ayarlamak için fiyat ayarlama işlevini kullanabilir. Fiyat ayarlaması işlevi, kullanıma hazır iki yönlü ayarlamaları (artış veya azaltma) destekleyecek şekilde güncelleştirildiği için bu ayarı kullanım dışı bıraktık. | 10.0.30 sürümünde kullanım dışı bırakıldı ve 2023 Ekim'de kaldırılacaktır. |
| Perakende mağaza için fiyat raporunu etkinleştir | Bu ayar, **Fiyat raporu** işlevinin mağaza yapılandırma sayfasında kullanıma uygun olup olmayacağını kontrol etmek için kullanılıyordu. Mağaza yapılandırma sayfası her zaman **Fiyat raporu** işlevini standart işlev olarak sağlayacak şekilde güncelleştirildiği için bu ayarı kullanım dışı bıraktık. | 10.0.31 sürümünde kullanım dışı bırakıldı ve 2023 Ekim'de kaldırılacaktır. |
| Fiyatları hesaplamak için bugünün tarihini kullanma | Dynamics 365 Supply Chain Management fiyatlandırma altyapısı, bugünün tarihiyle talep edilen sevk tarihi veya talep edilen giriş tarihi temel alınarak verilen fiyatlandırma hesaplamasını destekler. Commerce fiyatlandırma altyapısı yalnızca bugünün tarihine dayalı fiyatlandırma hesaplamalarını destekler. Hem Supply Chain Management hem de Commerce yeteneklerini kullanan müşteriler için bu ayarı sunmuş ve İki fiyatlandırma altyapısının birlikte çalışabilmesi için müşterilerin bu ayarı her zaman bunları **Evet** olarak ayarlamasını önermiştik. Hesaplama davranışını temelde değiştirmediği ve dolayısıyla gereksiz olduğu için bu ayarı kullanım dışı bıraktık. | 10.0.31 sürümünde kullanım dışı bırakıldı ve 2023 Ekim'de kaldırılacaktır. |
| Maksimum fiyat | Yalnızca belirtilen maksimum fiyat altında bir satış fiyatına sahip ürünlerin belirli mağazalardaki POS ile satılıp satılmayacağını kontrol etmek için bu ayarı işlevsellik profilinde sunuyorduk. Özellik kullanımı düşük olduğundan, bu ayarı kullanımdan kaldırdık. | 10.0.31 sürümünde kullanım dışı bırakıldı ve 2023 Ekim'de kaldırılacaktır. |
| Birim fiyatına iskontoları uygula | Bu ayar, fiyatlandırma hesaplaması sırasında fiyatların ve iskontoların birim fiyat düzeyinde mı yoksa satış satır düzeyinde mi yuvarlanacağını kontrol etmek amacıyla tasarlanmıştır. Geçerli kod tabanındaki herhangi bir yerde kullanılmadığından bunu kullanımdan kaldırdık. | 10.0.31 sürümünde kullanım dışı bırakıldı ve 2023 Ekim'de kaldırılacaktır. |
| Birden fazla madde iskontosunu el ile hesapla | Fiyatlandırma altyapısının perakende mağaza kanalı için gecikmeli fiyat hesaplamasını kullanıp kullanmadığını kontrol etmek için bu ayar sağlanıyordu. Parametre **Evet** olarak ayarlanırsa, POS uygulamasında bir satış siparişi oluşturulduğunda veya düzenlendiğinde, fiyatlandırma altyapısı çok satırlı iskontoları (miktar iskontoları, eşik iskontoları ve karıştır ve eşle iskontoları gibi) hemen hesaplamaz. Çok yönlü kanal denetimi yapmak için, bu ayarı Commerce parametrelerindeki benzer bir ayarla konsolide etmeye karar verdik. | 10.0.31 sürümünde kullanım dışı bırakıldı ve 2023 Ekim'de kaldırılacaktır. |

Dynamics 365 Commerce'teki kaldırılmış veya kullanım dışı bırakılmış özelliklerin tam listesi için bkz. [Dynamics 365 Commerce'teki kaldırılmış veya kullanım dışı bırakılmış özellikler](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
