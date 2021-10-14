---
title: İndirim yönetimi anlaşmaları
description: Bu konuda indirim yönetimi anlaşmaları oluşturma işlemi açıklanmaktadır. Anlaşmalar, indirimleri ve Kâr paylarını hesaplamak için farklı yöntem ve esasları denetlemek amacıyla kullanılır. Bunlar eklemeler ve hariç tutmalar için kurallar içerir.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 18d03ad89942997d8b5e794bb8d79a67821ef2c4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580564"
---
# <a name="rebate-management-deals"></a>İndirim yönetimi anlaşmaları

[!include [banner](../includes/banner.md)]

İndirim yönetimi anlaşmaları, indirimleri ve kâr paylarını hesaplamak için farklı yöntem ve esasları denetlemek amacıyla kullanılır. Bunlar eklemeler ve hariç tutmalar için kurallar içerir. Üç tip İndirim Yönetimi anlaşması vardır: Müşteri indirimleri, müşteri kâr payları ve satıcı indirimleri. Üç tür de benzer ayarlar kullanır. Bu konu, farklılıkların olduğu yerleri gösterir.

## <a name="create-a-deal"></a>Anlaşma oluşturma

1. **İndirim yönetimi \> indirim Yönetimi anlaşmaları \> tüm indirim yönetimi anlaşmaları** kısmına gidin. **Tüm indirim yönetimi anlaşmaları** listesi sayfasında, üç türden tüm anlaşmalar oluşturabilir ve bunlarla çalışabilirsiniz.

    Alternatif olarak, aşağıdaki adımlardan birini uygulayın. Her bir durumda, Görüntülenen liste sayfası, **tüm indirim yönetimi anlaşmaları** liste sayfasındaki aynı ayarları sağlar, ancak yalnızca tek bir türde olan anlaşmaları göstermek üzere filtrelenmiştir.

    - Yalnızca müşteri indirim anlaşmaları oluşturmak için **İndirim yönetimi \> indirim Yönetimi anlaşmaları \> müşteri indirim anlaşmaları** kısmına gidin.
    - Yalnızca müşteri kâr payı anlaşmaları oluşturmak için **İndirim yönetimi \> indirim Yönetimi anlaşmaları \> müşteri kâr payı anlaşmaları** kısmına gidin.
    - Yalnızca satıcı indirim anlaşmaları oluşturmak için **İndirim yönetimi \> indirim Yönetimi anlaşmaları \> satıcı indirim anlaşmaları** kısmına gidin.

1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Yeni anlaşma oluştur** iletişim kutusunda, aşağıdaki alanları ayarlayın:

    - **İndirim Yönetimi anlaşması**: İndirim anlaşmaları için [bir numara serisi ayarladıysanız](rebate-management-parameters.md), bu alan otomatik olarak benzersiz, sistem tarafından oluşturulan bir kimliğe ayarlanır. Aksi durumda, benzersiz bir kimlik girin.
    - **Açıklama**: Anlaşma açıklamasını girin.
    - **Modül**: Anlaşma için geçerli olan ortak türünü seçin (*müşteri* veya *satıcı*). Başladığınız sayfaya bağlı olarak, bu alan seçilen anlaşma türüne göre otomatik olarak ayarlanabilir. Bu durumda alan salt okunurdur.
    - **Tür**: Anlaşma türünü seçin (*indirim* veya *Bağlılık*). Başladığınız sayfaya bağlı olarak, bu alan seçilen anlaşma türüne göre otomatik olarak ayarlanabilir. Bu durumda alan salt okunurdur.
    - **Mutabakat ölçütü**: Anlaşmanın nasıl hesaplanacağı ve mutabık kılacağını seçin:

        - *Anlaşma*: Tek bir indirimin, anlaşma içindeki tüm indirimler ve kesintiler için işlenmesi gerekir.
        - *Satır*: Anlaşmadaki her bir satır için indirimler işlenmelidir.

    - **Nakil profili**: Anlaşmanın geçerli olduğu işlemler için kullanılacak [nakil profilini](rebate-management-posting.md) seçin. Bu alan, yalnızca **Mutabakat ölçütü** alanı *Anlaşma* olarak ayarlandığında kullanılabilir. *Satır* olarak ayarlanmışsa, bu profili daha sonra, anlaşmaya eklediğiniz her satır için atarsınız.
    - **Garanti için Nakil profili**: Garanti işlemleri için kullanılacak [nakil profilini](rebate-management-posting.md) seçin. Yalnızca garanti bir kâr payı için geçerliyse garanti işlemleri için nakil profilleri gerekir. Tersi durumda, nakil profili zorunlu olmasa da, bir nakil profili belirtilmemişse, garanti deftere nakledildiğinde hata görüntülenir. Bu alan, yalnızca **Tür** alanı *Kâr payı* olarak ayarlandığında kullanılabilir. 
    - **İndirim çıkışı**: İndirim ya da kâr payının nasıl ödeneceğini seçin:

        - *Finansal*: Ödemelerin daha sonra yapılabilmesi veya alınabilmesi için ücretsiz bir metin borç dekontu veya borç hesapları dekontu oluşturun. Bu seçeneğin seçildiği indirimlerle provizyonların **kullanılabileceğini** unutmayın. Bu seçenek, **Tür** alanı *kâr payı* olarak ayarlandığında kullanılabilecek tek seçenektir.
        - *Madde*: Anlaşmanın ayarlanışına göre maddeler için bir satış siparişi oluşturun. Bu satış siparişinde, her maddeye 0 (sıfır) fiyatı atanır. Bu seçeneğin seçildiği indirimlerle provizyonların **kullanılamayacağını** unutmayın.

    - **İndirim para birimi**: İndirim, kesinti veya kâr payı ödemesi yapılırken kullanılacak para birimini seçin.
    - **Belge notları**: Gerektiğinde anlaşma hakkında notlar girin.
    - **Toplam garanti**: Bu seçeneği yalnızca **tür** alanı *kâr payı* olarak ayarlandığında *Evet* olarak ayarlayabilirsiniz. Bu seçenek, garantili kesinti ödemeleri hesaplamasını etkiler. Aşağıda bir örnek verilmiştir:

        - Anlaşma garantisi, üç aylık dönem başına 10.000 $ ödemeye sağlayacak bir değer satmaya yöneliktir.
        - Malları satan kuruluş üç aylık 1. dönemde 12.000 $ kesinti ödemesine neden olan bir değer satıyor. Sonuç, ödenen 12.000 $ kâr payı eksi 10.000 $ garantidir.
        - **Toplam garanti** seçeneği *Evet* olarak ayarlanmışsa, 1. üç aylık dönemde ödenen ek 2.000 $ kâr payı 2. üç aylık döneme de uygulanır. Bu nedenle, müşteriye 8.000 $ garanti ödemesi yapılır (10.000 $ garanti eksi 2.000 $ ek ödeme).
        - 2. üç aylık dönemde, 5.000 $ değerinde kâr payı tetikleyen satışlar kaydedersiniz.
        - Sistem 3.000 $ değerinde ödeme tanımlar (8.000 $ garanti, eksi ödenen 5.000 $ kâr payı).
        - **Toplam garanti** seçeneği *Hayır* olarak ayarlanmışsa , her üç ayda bir tam 10.000 $ garanti edilir. Bu garanti 2. üç aylık dönemde 5.000 $ değerinde önerilen ödemeye karşılık gelir (10.000 $ garanti eksi Ödenen 5.000 $ kâr payı).

1. Anlaşma oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.

Bu yordam yeni anlaşmanın başlık düzeyini oluşturur. Daha sonra, anlaşmaya satır ekleyeceksiniz.

## <a name="add-lines-to-a-deal"></a>Anlaşmaya satır ekleme

Önceki bölümde anlatıldığı gibi bir anlaşma oluşturduktan sonra, bunu liste sayfasından açabilirsiniz. Daha sonra, müşteri veya satıcıları, maddeleri, zaman çerçevesini, bir esası ve anlaşma için hesaplama yöntemlerini tanımlayacak satırları ekleyebilirsiniz. Bir anlaşma bir veya daha fazla satır içerebilir. Bir anlaşma birden çok satıra sahip ise, bunlar genellikle aynı tipte olurlar veya aynı parametreler bunlarla ilişkilendirilir. Bir anlaşmaya satır ekleyene kadar, anlaşma hiçbir şey yapmaz.

1. Önceki bölümde açıklandığı gibi, uygun indirim anlaşmaları liste sayfasını açın.
1. Çalışmak istediğiniz anlaşmayı bulun ve açın.
1. **İndirim Yönetimi** hızlı sekmesinde, kılavuza bir anlaşma satırı eklemek için aşağıdaki düğmelerden birini seçin:

    - **Satır Ekle**: Yeni, boş bir anlaşma satırı ekleyin.
    - **Satır Kopyala**: Varolan bir anlaşma satırı, eklemek istediğiniz anlaşma satırına benziyorsa, bu düğmeyi kopyalamak üzere seçerek bir kopyasını ekleyebilirsiniz. Yeni anlaşma satırı, ilgili İndirim yönetimi ayrıntılarının tüm ayarlarını içerir. Daha sonra ayarları düzenleyebilirsiniz. Örneğin, genellikle Madde ilişkisini ve indirim yüzdesini güncellersiniz.

1. Yeni anlaşma satırında aşağıdaki alanları ayarlayın:

    - **İndirim Yönetimi numarası**: İndirim anlaşmaları numaraları için [bir numara serisi ayarladıysanız](rebate-management-parameters.md), bu alan otomatik olarak benzersiz, sistem tarafından oluşturulan bir kimliğe ayarlanır. Aksi durumda, benzersiz bir kimlik girin.
    - **Tür**: Satırın uygulandığı anlaşma türü (*indirim* veya *kâr payı*). Değer başlıktan kopyalanır ve değiştirilemez.
    - **Açıklama**: Anlaşma satırının açıklamasını girin.
    - **Şirket**: Anlaşma satırının geçerli olduğu şirketi (yasal varlık) seçin. İşlem sırasında, kullanıcılar yalnızca kullanmakta oldukları şirkete atanan anlaşma satırlarını işleyebilir. **Müşteri indirimleri anlaşmaları** liste sayfası, kullanıcının güvenlik erişimine dayalı olarak çoklu şirket görünümünde bir görünüm sağlar. Ancak, yalnızca şu anda kullanmakta olduğunuz şirketle ilgili indirimleri düzenleyebilir ve işleyebilirsiniz.
    - **Hesap kodu**: Anlaşma satırının uygulanacağı müşteri veya satıcıların kapsamını seçin:

        - *Tablo*: Anlaşma satırı belirli bir müşteri veya satıcı için geçerlidir.
        - *Grup*: Anlaşma satırı bir grup müşteri veya satıcı için geçerlidir. Grupların nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [İndirim yönetimi grupları](rebate-management-groups.md).
        - *Tümü*: Anlaşma satırı tüm müşteri veya satıcılar için geçerlidir.

    - **Hesap ilişkisi**: **Hesap kodu** alanında *Tablo*'yu seçtiyseniz, anlaşmanın uygulandığı müşteriyi veya satıcıyı seçin. *Grup* seçeneğini belirlediyseniz müşteri veya satıcı grubunu seçin. *Tümü*’nü seçtiyseniz bu alan kullanılamaz.
    - **Madde kodu**: Anlaşma satırının uygulanacağı madde kapsamını seçin:

        - *Tablo*: Anlaşma satırı belirli bir madde için geçerlidir.
        - *Grup*: Anlaşma satırı bir grup madde için geçerlidir. Grupların nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [İndirim yönetimi grupları](rebate-management-groups.md).
        - *Tümü*: Anlaşma satırı tüm maddeler için geçerlidir.

    - **Madde ilişkisi**: **Madde kodu** alanında *Tablo*'yu seçtiyseniz, anlaşma satırının uygulandığı maddeyi seçin. *Grup* seçeneğini belirlediyseniz madde grubunu seçin. *Tümü*’nü seçtiyseniz bu alan kullanılamaz.
    - **Birim türü**: Anlaşma satırı için geçerli olan birim türünü seçin (*Stok birimi* veya *Fiili ağırlık birimi*). Bu alanın daha eski kayıtlar için boş olabileceğini unutmayın. Bu durumda *Stok birimi* değeri varsayılan olarak alınır.
    - **(Stok yönetimi parametreleri)**: Anlaşma satırındaki geri kalan alanlarda, anlaşmaya dahil olan maddeleri (madde boyutu, renk, stil, tesis ve ambar gibi) tanımlamak için kullanılacak stok yönetimi parametrelerinin değerlerini belirtin. Boyutları eklemek veya kaldırmak için, Eylem bölmesinde **boyutları görüntüle**'yi seçin.

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Bir anlaşma satırının geçerli olduğu madde kümesini daha fazla sınırlandırmak istiyorsanız, satırı seçin ve ardından **indirim Yönetimi** hızlı sekmesinde, Standart **sorgu** iletişim kutusu açmak için **filtre**'yi seçin.
1. Eklediğiniz her bir anlaşma satırı için, sonraki bölümde açıklandığı gibi, indirim **yönetimi detayları** hızlı sekmesinde, hesaplama ayrıntılarını ve diğer ayrıntıları ayarlayın.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Bir anlaşma satırına indirim yönetimi ayrıntıları Ekleme

Anlaşmanızdaki her bir satır için, **indirim yönetimi detayları** hızlı sekmesinde ayrıntıları ayarlamalısınız. Önce, **indirim yönetimi** hızlı sekmesinde, anlaşma satırını seçin. Daha sonra, **indirim yönetimi ayrıntıları** hızlı sekmesindeki çeşitli sekmeleri kullanarak o anlaşma satırı için değerleri ayarlayın. Aşağıdaki alt kısımlar, her sekmenin nasıl kullanılacağını açıklar.

### <a name="settings-on-the-general-tab"></a>Genel sekmesindeki ayarlar

**İndirim yönetimi ayrıntıları** hızlı sekmesindeki **Genel** sekmesi, Seçili anlaşma satırına ilişkin hesaplama yöntemini ve temeli ayarlamanıza olanak tanır. Bu kurulum minimum bir satın almanın gerekli olup olmadığını, anlaşma satırıyla ilişkilendirilmiş nakil profillerini ve hesaplamanın ayrıntılarını kontrol eder. Aşağıdaki tabloda, kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Hesaplama yöntemi | Seçilen anlaşma satırı diğer anlaşma satırlarıyla (*Adımlı*, *Kümülatif*, *Hareketli* veya *Toplam*) birleştirildiğinde kullanılacak yöntemi seçin. Bu alanın değeri, indirim hesaplamalarınızın sonucunu önemli ölçüde etkileyebilir. İndirim hesaplamasını nasıl etkilediğini gösteren örnekler ve her yöntemin tam açıklaması için Bu konunun ilerleyen kısımlarında yer alan [anlaşma satırları için hesaplama yöntemleri](#calc-methods) konusuna bakın. |
| Temel | İndirimin miktara dayalı (satın alınan veya satılan birimlerin toplam sayısı) veya değere dayalı (diğer bir deyişle, satın alınan veya satılan malların toplam fiyatı) olarak uygulandığını seçin. |
| Hareket türü | <p>Süreçte Hesaplamanın gerçekleşmesi gereken noktayı seçin:</p><ul><li>*Sipariş*: Hesaplama için temel olarak sipariş edilen miktar veya değeri kullanın.</li><li>*Teslim edilen*: Hesaplama için temel olarak teslim edilen miktar veya değeri kullanın.</li><li>*Fatura*: Hesaplama için temel olarak fatura edilen miktar veya değeri kullanın.</li></ul> |
| Birim | **Temel** alanında *miktar*'ı seçtiyseniz, miktarın belirtilmesi gereken birimi seçin. |
| Minimum tutar | Dönem başına ödenmesi gereken minimum tutarı girin. Alacak dekontları döneme ait satışları aşarsa, negatif indirim tutarlarına izin vermek için negatif bir değer girebilirsiniz. |
| İndirim azaltma ilkesi | Anlaşma satırı için geçerli olan [indirim azaltma ilkesini](rebate-reduction-principle.md) seçin. |
| Varyant numarası | Anlaşma satırı, varyantları olan bir madde için geçerliyse, anlaşma satırının geçerli olduğu varyantı seçin. |
| Satıcı indirimi temeli | <p>Bu alan yalnızca satıcı indirimleri (diğer bir deyişle, **modül** alanı *satıcı* olarak ayarlanmış olan anlaşmalar) için gösterilir. Satıcı indirimi için temel seçin:</p><ul><li>*Satın alma siparişi*: Satıcının aldığı indirim, satın alma siparişindeki miktar veya değere dayanır.</li><li>*Satış siparişi*: Satıcı, yalnızca mallar satıldıktan sonra bir indirim alır. İndirim, satış siparişindeki miktar veya değere dayanır.</li></ul> |
| Fiyat tabanı | <p>Bu alan yalnızca satıcı indirimleri (**modül** alanı *satıcı* olarak ayarlanmış olan anlaşmalar) için gösterilir. **Satıcı indirim temeli** alanında *satış siparişi*'ni seçtiyseniz, uygun fiyat temelini seçin:</p><ul><li><p>*FIFO*: İndirimi hesaplamak için **FIFO satın alma fiyatını hesapla** periyodik görevinin çalıştırılması gerekir. (Görevi çalıştırmak için şuraya gidin **İndirimler Yönetimi \> Periyodik Görevler \> FIFO satın alma fiyatını hesapla**.) Satılan stokun değerini hesaplamak için ilk giren ilk çıkar (FIFO) kuralı kullanılacaktır. Bu değer daha sonra satıcı indirimlerinin hesaplanması için kullanılacaktır. Aşağıda bir örnek verilmiştir:</p><ul><li>**Satılan hisse senedi:** Her biri 3,00 $ değerinde 1.000 birim = 3.000 $</li><li>**FIFO temelinde geçerli olan satın alma fiyatı:** 2,00 $</li><li>**Çalışma hesaplaması:** *Satılan birimler* × *geçerli satın alma fiyatı* = 1.000 × 2,00 $= 2.000 $</li></ul></li><li><p>*En son Satın alma Fiyatı*: Satıcı indirimlerinin hesaplanmasında son satın alma hareketindeki değer kullanılır. Aşağıda bir örnek verilmiştir:</p><ul><li>**Satılan hisse senedi:** Her biri 3,00 $ değerinde 1.000 birim = 3.000 $</li><li>**En son satın alma fiyatı**: 2,00 $</li><li>**Çalışma hesaplaması:** *Satılan birimler* × *En son satın alma fiyatı* = 1.000 × 2,00 $= 2.000 $</li></ul></li><li><p>*Ortalama Satın alma Fiyatı*: Satıcı indirimlerin hesaplanmasında son *X* ayın ağırlıklı ortalama değeri kullanılır. Bu seçeneği belirlerseniz **ay sayısı** alanına ay sayısını girmeniz gerekir (Bu yalnızca **Fiyat tabanı** alanı *ortalama satın alma fiyatı* olarak ayarlandığında kullanılabilir). Aşağıda bir örnek verilmiştir:</p><ul><li>**Satılan hisse senedi:** Her biri 3,00 $ değerinde 1.000 birim = 3.000 $</li><li>**Ortalama satın alma fiyatı:** 2,00 $</li><li>**Çalışma hesaplaması:** *Satılan birimler* × *Ortalama satın alma fiyatı* = 1.000 × 2,00 $= 2.000 $</li></ul></li><li><p>*Satış Fiyatı*: Satış fiyatı satıcı indirimlerinin hesaplanmasında kullanılır. Aşağıda bir örnek verilmiştir:</p><ul><li>**Satılan hisse senedi:** Her biri 3,00 $ değerinde 1.000 birim = 3.000 $</li><li>**Ortalama satın alma fiyatı:** 2,00 $</li><li>**Çalışma hesaplaması:** *Satılan birimler* × *Satış fiyatı* = 1.000 × 3,00 $= 3.000 $</li></ul></li></ul> |
| Ayların sayısı | Bu alan yalnızca satıcı indirimleri (**modül** alanı *satıcı* olarak ayarlanmış olan anlaşmalar) için gösterilir. **Fiyat tabanı** alanında *ortalama satın alma fiyatını* seçtiyseniz, kullanılması gereken ay sayısını girin. |
| Deftere nakil profili | Seçili Anlaşma satırı için geçerli olan [nakil profilini](rebate-management-posting.md) seçin. Bu profil yalnızca, anlaşma başlığındaki **mutabakat ölçütü** alanı *satır* olarak ayarlandığında kullanılır. **Mutabakat ölçütü** alanı *Anlaşma* olarak ayarlanmışsa, anlaşma başlığında ayarlanan nakil profili her zaman kullanılır. Anlaşma satırında nakil profili ayarlanmamışsa anlaşma başlığında ayarlanan nakil profili kullanılır. |
| Garanti için nakil profili | Bu alan **nakil profili** alanı gibi çalışır, ancak yalnızca kâr paylarına uygulanır. |
| Ödeme türü | Anlaşma için seçilen nakil profili için ödeme türü. |
| Satış vergisi dahil | İşleme verginin dahil olup olmayacağını seçin. Verginin dahil olması, yalnızca **Taban** alanı *değere* ayarlandığında ilgilidir. Fatura tutarı vergi dahil tutar olarak kullanılacaktır. İndirim hesaplaması bir yüzdeye dayanıyorsa, sistem indirim yüzdesini vergi dahil tutarla çarpar. Hesaplamanın, anlaşma satırındaki Satış vergisi değerini kullandığına dikkat edin. |
| Alacak dekontlarını dahil et | <p>Alacak dekontlarını indirim hesaplamasına dahil etmek için bu seçeneği *Evet* olarak ayarlayın.</p><p>Bu seçeneği *Evet* olarak ayarlarsanız, efekt, **İşlem türü** alanının değerine bağlı olarak değişir:</p><ul><li>**İşlem türü** alanı *fatura* olarak ayarlanmışsa hesaplama alacak dekontlarında dikkate alınacaktır. Bu yapılandırma her zamanki yapılandırmadır.</li><li>**İşlem türü** alanı *sipariş* olarak ayarlanmışsa, hesaplama, hem negatif değerler içeren satış siparişlerinde hem de iade edilen açık siparişlerde dikkate alınır.</li></ul> |
| İskonto uygulanan tutar | Anlaşma satır iskontolarının verildiği durumlarda maddenin veya maddelerin indirimli tutarına göre hesaplamayı temel almak için bu seçeneği *Evet* olarak ayarlayın. |
| Yalnızca ödenmiş faturalar | Hesaplamanın yalnızca tam olarak ödenen faturaları dikkate alması gerekiyorsa bu seçeneği *Evet* olarak ayarlayın. (Başka bir deyişle, indirimler kısmen ödenen faturalar için hesaplanmaz.) Bu seçenek yalnızca **İşlem türü** alanı *fatura* olarak ayarlandığında kullanılabilir. |
| Serbest metinleri dahil et | Serbest metin faturalarını indirim hesaplamasına dahil etmek için bu seçeneği *Evet* olarak ayarlayın. Serbest metin faturaları yalnızca **Madde kodu** alanı *tümü* olarak ayarlanmış olan anlaşma satırları için dahil edilebilir. |
| Kapatma iskontosunu dahil etme | İlk kapatma iskontosuna göre indirimi azaltmak için bu seçeneği *Evet* olarak ayarlayın. Kuruluşun ilk kapatma iskontosunu alacağı varsayılır. Kapanış iskontosunun daha sonra kullanılmasını etkinleştirmek için bu seçeneği *Hayır* olarak ayarlayın. |
| Belge notları | İndirim işlemi yevmiye defteri satırlarında işlem metni olarak kullanılması gereken notları girin. |

### <a name="settings-on-the-dates-tab"></a>Tarihler sekmesindeki ayarlar

**İndirim yönetimi ayrıntıları** hızlı sekmesindeki **tarihler** sekmesinde bulunan ayarlar, **Genel** sekmesinde belirtilen hesaplamaların sıklığını ve zamanlamasını tanımlar. Bunlar, işlem sırasında hesaplamaların nasıl gerçekleşeceğini belirler.

Bu sekme, seçili anlaşma satırının geçerli olduğu tarih aralığını ve hesaplama sıklığını belirtmenizi sağlar. Ayrıca, garantinin deftere nakledilip edilmeyeceğini ve zamanını da belirtebilirsiniz.

Kılavuza tarih satırı eklemek veya bunları kaldırmak için araç çubuğundaki düğmeleri kullanabilirsiniz. Çoklu Tarih satırı varsa, geçerli tarih aralıkları çakışmamalıdır. Aksi durumda, anlaşmayı kaydetmeyi denediğinizde bir hata iletisi alırsınız.

Aşağıdaki tabloda, her tarih satırında kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Başlangıç tarihi | Tarih satırının geçerli olduğu ilk tarihi girin. Anlaşma başlığında "başlangıç" ve "bitiş" tarihleri belirtilirse, bunlar her yeni Tarih satırı için varsayılan değerler olarak kullanılırlar. |
| Bitiş tarihi | Tarih satırının geçerli olduğu son tarihi girin. Anlaşma başlığında "başlangıç" ve "bitiş" tarihleri belirtilirse, bunlar her yeni Tarih satırı için varsayılan değerler olarak kullanılırlar. |
| Birim miktar | Anlaşma satırının ne kadar sıklıkla hesaplanacağını belirtin. Buraya bir tamsayı girin ve sonra **birikme ölçütü** alanında bir birim seçin. Örneğin, her iki haftada bir hesaplamak için, **Her** alanını *2* ve **birikme ölçütü** alanını *hafta* olarak ayarlayın. |
| Birikme ölçütü | **Her** ayarı için geçerli olan birimi seçin. Anlaşma satırının tam kullanım süresini hesaplamak üzere *Kullanım süresini* seçin. Genel kayıt defterinde tanımlanan bir dönem seçmek için *özelleştirilmiş dönem*'i seçin. Bu durumda, **dönem türü** alanını da ayarlamanız gerekir. |
| Dönem türü | Bu alan, yalnızca **Birikme ölçütü** alanı *Özelleştirilmiş dönem* olarak ayarlandığında kullanılabilir. Seçim için kullanılabilen değerler, genel kayıt defterinde tanımlanan dönem türlerinden gelmektedir. |
| Haftanın ilk günü | Dönem için haftaların nasıl tanımlandığını belirtin. Bu alan, yalnızca **Birikme ölçütü** alanı *Hafta* olarak ayarlandığında kullanılabilir. |
| Talep sıklığı | İndirim tutarlarının anlaşma satırı için ne sıklıkta talep edilebileceğini belirtin. Buraya bir tamsayı girin ve sonra **Talep ölçütü** alanında bir birim seçin. |
| Talep ölçütü | **Talep sıklığı** ayarı için geçerli olan birimi seçin. Anlaşma satırının tam ömrü boyunca taleplere yalnızca bir kez izin vermek için *ömür*'ü seçin. Genel kayıt defterinde tanımlanan bir dönem seçmek için *özelleştirilmiş dönem*'i seçin. Bu durumda, **Talep dönemi türü** alanını da ayarlamanız gerekir. |
| Talep dönemi türü | Bu alan, yalnızca **Talep ölçütü** alanı *Özelleştirilmiş dönem* olarak ayarlandığında kullanılabilir. Seçim için kullanılabilen değerler, genel kayıt defterinde tanımlanan dönem türlerinden gelmektedir. |
| Deftere naklederken işle | Talep satırının deftere nakil sırasında işlenmesi gerekiyorsa bu onay kutusunu işaretleyin. Bu seçenek yalnızca, **Genel** sekmesindeki **işlem türü** alanının *teslim edildi* veya *Fatura* olarak ayarlandığı anlaşma satırları için kullanılabilir. Provizyonlar için, teslimat notu veya fatura oluşturulduğunda, bu provizyon deftere nakledilir. |
| Garanti sıklığı | Bu alan yalnızca kâr payı anlaşmaları için geçerlidir. **Birikme ölçütü** ayarında tanımlanan dönem içinde, kâr payı garantisinin ne sıklıkta hesaplanacağını belirtin. Buraya bir tamsayı girin ve sonra **Ödenen garanti** alanında bir ödeme zamanı seçin. |
| Ödenen garanti | <p>Bu alan yalnızca kâr payı anlaşmaları için geçerlidir. Garanti hesaplama sıklığını tanımlamak için **garanti sıklığı** alanı ile birlikte çalışır. Aşağıdaki değerlerden birini seçin:</p><ul><li><p>*Dönem başlangıcı*: Garanti, Tarih satırı için tanımlanan anlaşma döneminin başlangıcında ödenir. Tam garanti önce işlenir. Yalnızca garantili tutarı aşan kâr payları değeri kâr payı olarak deftere nakledilir. Aşağıda bir örnek verilmiştir:</p><ul><li>**Minimum Garanti:** İki ayda 10.000 $.</li><li>**1. Ay:** 10.000 $ garanti olarak deftere nakledildi ve kâr payında 0 $ deftere nakledildi.</li><li>**2. Ay:** 2.000 $ kâr payı olarak deftere nakledildi ve garantide 0 $ deftere nakledildi.</li><li>**Çalışma hesaplaması:** *Kalan garanti* – *Deftere nakledilen kâr payı* = 0 $ – 2.000 $ = -2.000 $.</li></ul><p>2.000 $ kâr payı ödemesi gerekli olduğundan, 2.000 $ için bir günlük oluşturulur.</p><p>**Not:** Garanti, ilk dönem için kesintiler ile birlikte hesaplanmalıdır ve nakledilmelidir.</p></li><li><p>*Dönem sonu*: Garanti, kesinti anlaşmasının sonuna kadar tarih satırında tanımlandığı şekilde ödenmez. Aşağıda bir örnek verilmiştir:</p><ul><li>**Minimum Garanti:** İki ayda 10.000 $.</li><li>**1. Ay:** 5.000 $ kâr payı olarak nakledildi ve bir günlük oluşturuldu.</li><li>**2. Ay:** 7.000 $ kâr payı olarak nakledildi ve bir günlük oluşturuldu.</li><li>**Çalışma hesaplaması:** Kâr payı garanti tutarını aştığından 0 $ garantiye nakledilir.</li></ul><p>**Not:** Garanti, son dönem için sadece kesintiler ve indirim işlemleri ile birlikte hesaplanmalıdır ve nakledilmelidir.</p></li></ul> |
| Minimum garanti | Bu alan yalnızca kâr payı anlaşmaları için geçerlidir. Kâr payı için minimum garanti tutarını, anlaşma başlığında tanımlanan para biriminde girin. |

### <a name="settings-on-the-lines-tab"></a>Satırlar sekmesindeki ayarlar

**İndirim yönetimi ayrıntıları** hızlı sekmesindeki **Satırlar** sekmesi, Seçili anlaşma satırına ilişkin hesaplama satırlarını tanımlamanıza olanak tanır. Her hesaplama satırı, bir miktar veya değer eşiği ile ilgili ücret tutarını veya maddelerini oluşturur. **Genel** alanındaki **Taban** alanı, her hesaplama satırının bir miktara veya bir değere dayalı olup olmayacağını belirtir.

Kılavuza hesaplama satırı eklemek veya bunları kaldırmak için araç çubuğundaki düğmeleri kullanabilirsiniz. Herhangi bir sayıda hesaplama satırı olabilir. Ancak, birden fazla hesaplama satırı varsa, "bitiş" ve "başlangıç" miktar veya değer aralıkları çakışmamalıdır.

Aşağıdaki tabloda, her hesaplama satırında kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Başlangıç miktarı/değeri | Hesaplama satırının uygulanacağı minimum miktar veya değeri girin. |
| Bitiş miktarı/değeri | Hesaplama satırının uygulanacağı maksimum miktar veya değeri girin. |
| İndirim yönetimi yöntemi | <p>Bu alan yalnızca başlıktaki **indirim çıkışı** alanının *mali* olarak ayarlandığı anlaşmalar için kullanılabilir. İndirimi hesaplamak için kullanılacak yöntemi seçin:</p><ul><li>*Sabit*: Satır için sabit bir fiyat tutarı kullanılır.</li><li>*Yüzde*: Satış tutarının bir yüzdesi kullanılır.</li><li>*Oran*: Her sipariş için sabit bir fiyat tutarı kullanılır.</li></ul><p>**Önemli:** **Satırlar** sekmesindeki her bir hesaplama satırı için aynı yöntemi kullanmanızı öneririz. Yeni bir yöntem gerekiyorsa, yeni bir anlaşma satırı oluşturun. Varolan bir anlaşma satırından yeni bir anlaşma satırı oluşturmak için, **indirim yönetimi** hızlı sekmesindeki **satır Kopyala** düğmesini kullanabileceğinizi unutmayın.</p><p>**Not:** **İndirim çıkışı** alanı *madde* olarak ayarlanmışsa bu alan her zaman *sabit* olarak ayarlanır. Maddelerin nasıl belirtileceği konusunda daha fazla bilgi için, bu tabloyu izleyen metne bakın. |
| İndirim yönetimi miktarı | Bu alan yalnızca başlıktaki **indirim çıkışı** alanının *mali* olarak ayarlandığı anlaşmalar için kullanılabilir. **İndirim yönetimi yöntemi** alanında seçtiğiniz yönteme göre, indirimi hesaplamak için kullanılması gereken tutarı girin. |

Önceki tabloda belirtildiği gibi, başlıktaki **indirim çıktısı** alanının *madde* olarak ayarlandığı anlaşmalar için, **Satırlar** sekmesindeki her bir hesaplama satırı için sağlanacak maddeleri belirtmeniz gerekir. Maddeleri belirtmek için, aşağıdaki adımları izleyin.

1. **Satırlar** sekmesinde, mevcut değilse, gerekli hesaplama satırını oluşturun ve seçin.
1. Hesaplama satırı oluşturulduktan sonra anlaşma kaydedilmediyse, Eylem bölmesinde **kaydet**'i seçin.
1. **Satırlar** sekmesinde, **maddeler**'i seçin.
1. **Öğeler** sayfasında, kılavuza öğe eklemek Için eylem bölmesindeki düğmeleri kullanın veya gerekirse öğeleri kaldırın. Her satır için aşağıdaki alanları ayarlayın:

    - **Madde numarası**: Sağlanacak maddeyi seçin.
    - **(Diğer boyutlar)**: Maddeyi tanımlamak için daha fazla boyut kullanmanız gerekiyorsa (örneğin, madde konfigürasyonu, boyut, renk, stil, site veya ambar), bunları belirtin. Mevcut Boyutları eklemek veya kaldırmak için, Eylem bölmesinde **boyutları görüntüle**'yi seçin.
    - **Miktar**: Seçilen hesaplama satırı için eşik karşılandığında sağlanacak miktarı girin.
    - **Birim**: **Miktar** değerinin belirtildiği birimi seçin.
    - **Birden çok**: Bu alan, **Miktar** alanıyla birlikte çalışır. Örneğin, bir madde satırında **miktar** alanını *2* ve **Birden çok** alanını *100* olarak ayarlarsınız. Daha sonra toplam satış siparişi miktarı 150 olursa, maddelerin ikisi ücretsiz olur (100 adet başına iki).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Stok boyutları sekmesindeki ayarlar

**İndirim yönetimi ayrıntıları** hızlı sekmesindeki **stok boyutları** sekmesinde, Seçili anlaşma satırı için belirtilen ürünle ilgili tüm kullanılabilir boyut değerleri gösterilir. **İndirim yönetimi** hızlı sekmesinde gösterilmeyen boyutları içerir. Yalnızca seçili ürün için geçerli olan boyutların değerlerini düzenleyebilirsiniz.

**İndirim Yönetimi** hızlı sekmesindeki kılavuza, eylem bölmesindeki **boyutları görüntüle**'yi seçerek daha fazla boyut ekleyebilirsiniz.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Anlaşma satırları için hesaplama yöntemleri

Önceki bölümde açıklandığı gibi, bir işlem satırınızın ayrıntılarını her ayarladığınızda, o satırın hesaplama yöntemini seçmeniz gerekir. Bu bölüm her hesaplama yöntemini açıklar ve her yöntemin siparişler ve anlaşma satırları için toplam indirimi nasıl hesapladığını gösteren örnekler sağlar. Bu örneklerde, siparişler ve anlaşma satırları birbirinin aynısıdır. Yalnızca hesaplama yöntemleri farklılık gösterir.

### <a name="stepped-calculation-method"></a>Adımlı hesaplama yöntemi

Adımlı hesaplama yöntemi, satış miktarına veya değerine ulaşılana kadar her bir anlaşma satırının indirim için artarak katkıda bulunduğu adım adım esasına göre hesaplanır. Bu adımlar, **indirim yönetimi ayrıntıları** hızlı sekmesindeki **Genel** sekmesinde bulunan **Taban** alanın ayarına bağlı olarak, satılan malların miktarını veya değerini temel alabilir.

Örneğin, bir anlaşma satırı, **Hesaplama yöntemi** alanı *Adımlı* ve **Taban** alanı *değer* olacak şekilde ayarlanır. Aşağıdaki indirimleri sağlayan hesaplama satırlarını içerir:

- **Satır A:** 1.000 $ değerine kadar yüzde 10
- **Satır B:** 2.500 $ değerine kadar yüzde 25

Satın alınan veya satılan malların değeri 2.000 $ ise elde edilen 350 $ indirim aşağıdaki şekilde hesaplanır:

- **İndirim (A):** *Eşik (A)* × *yüzde (A)* = 1.000 $ × %10 = 100 $
- **İndirim (B):** (*satılan değer* – *eşik (A)*) × *yüzde (B)* = (2.000 $ – 1.000 $) × %25 = 250 $
- **Toplam indirim:** *İndirim (A)* + *İndirim (B)* = 100 $ + 250 $ = 350 $

**Taban** alanı *değer* yerine *miktar* olarak ayarlanmışsa, adımlı hesaplama yöntemi benzer şekilde çalışır. İkinci adıma ulaşılana kadar, tanımlanan miktar için ilk adım kullanılır. Ardından üçüncü adıma ulaşılana kadar, ilk adımdan fazla olan tüm miktarlar için ikinci adım kullanılır. Bu işlem daha sonra sonraki tüm adımlarla devam eder.

### <a name="cumulative-calculation-method"></a>Kümülatif hesaplama yöntemi

Kümülatif hesaplama yönteminde, indirimi hesaplamak için tek bir hesaplama satırı kullanılır. Anlaşma satırı için çoklu hesaplama satırı varsa, ulaşılmış olan en yüksek değerli veya en yüksek miktar hesaplama satırı tüm miktar veya değer için kullanılır. Diğer hesaplama yöntemleri gibi, kümülatif Yöntem de indirimleri hesaplamak için satış miktarının veya satış değerinin kullanıldığını belirlemek üzere **indirim yönetimi ayrıntıları** hızlı sekmesinin **Genel** sekmesinde **taban** alanı ayarını kullanır.

Örneğin, bir anlaşma satırı, **Hesaplama yöntemi** alanı *Kümülatif* ve **Taban** alanı *değer* olacak şekilde ayarlanır. Aşağıdaki indirimleri sağlayan hesaplama satırlarını içerir:

- **Satır A:** 1.000 $ değerine kadar yüzde 10
- **Satır B:** 2.500 $ değerine kadar yüzde 25

Satın alınan veya satılan malların değeri 2.000 $ ise hesaplama sadece satır B'yi kullanır. Elde edilen 500 $ indirim aşağıdaki şekilde hesaplanır:

- **Toplam indirim:** *Satılan değer* × *indirim (B)* = 2.000 $ × %25 = 500 $

### <a name="rolling-calculation-method"></a>Hareketli hesaplama yöntemi

Hareketli hesaplama yöntemi, tüm olası hesaplama satırlarını anlaşma için hesaplar. Birden fazla hesaplama satırı varsa ve bunlardan birden fazlasına ulaşıldığında, erişilen tüm hesaplama satırları kullanılır, ancak üst eşikler her bir yüzdeye uygulanır. Diğer hesaplama yöntemleri gibi, hareketli yöntem de indirimleri hesaplamak için satış miktarının veya satış değerinin kullanıldığını belirlemek üzere **indirim yönetimi ayrıntıları** hızlı sekmesinin **Genel** sekmesinde **taban** alanı ayarını kullanır.

Örneğin, bir anlaşma satırı, **Hesaplama yöntemi** alanı *Hareketli* ve **Taban** alanı *değer* olacak şekilde ayarlanır. Aşağıdaki indirimleri sağlayan hesaplama satırlarını içerir:

- **Satır A:** 1.000 $ değerine kadar yüzde 10
- **Satır B:** 2.500 $ değerine kadar yüzde 25

Satın alınan veya satılan malların değeri 2.000 $ ise elde edilen 600 $ indirim aşağıdaki şekilde hesaplanır:

- **İndirim (A):** *Eşik (A)* × *yüzde (A)* = 1.000 $ × %10 = 100 $
- **İndirim (B):** *Satılan değer* × *yüzde (B)* = 2.000 $ × %25 = 500 $
- **Toplam indirim:** *İndirim (A)* + *İndirim (B)* = 100 $ + 500 $ = 600 $

### <a name="total-calculation-method"></a>Toplam Hesaplama yöntemi

Toplam hesaplama yönteminde, indirimi hesaplamak için tüm hesaplama satırları kullanılır. Ulaşılan Her bir hesaplama satırı için indirimi hesaplamak üzere toplam miktarı uygular ve her bir hesaplama satırı yüzdesini Tam tutara uygular. Diğer hesaplama yöntemleri gibi, toplam yöntemi de indirimleri hesaplamak için satış miktarının veya satış değerinin kullanıldığını belirlemek üzere **indirim yönetimi ayrıntıları** hızlı sekmesinin **Genel** sekmesinde **taban** alanı ayarını kullanır.

Örneğin, bir anlaşma satırı, **Hesaplama yöntemi** alanı *Toplam* ve **Taban** alanı *değer* olacak şekilde ayarlanır. Aşağıdaki indirimleri sağlayan hesaplama satırlarını içerir:

- **Satır A:** 1.000 $ değerine kadar yüzde 10
- **Satır B:** 2.500 $ değerine kadar yüzde 25

Satın alınan veya satılan malların değeri 2.000 $ ise elde edilen 700 $ indirim aşağıdaki şekilde hesaplanır:

- **İndirim (A):** *Satılan değer* × *yüzde (A)* = 2.000 $ × %10 = 200 $
- **İndirim (B):** *Satılan değer* × *yüzde (B)* = 2.000 $ × %25 = 500 $
- **Toplam indirim:** *İndirim (A)* + *İndirim (B)* = 200 $ + 500 $ = 700 $
