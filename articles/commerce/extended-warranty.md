---
title: Genişletilmiş garantiler oluşturma ve yapılandırma
description: Bu konu genişletilmiş garantileri kapsar ve bunların Microsoft Dynamics 365 Commerce'te nasıl oluşturacağını ve yapılandırılacağını açıklar.
author: sijoshi
manager: annbe
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a875343d9b93f5ebf2c2992fba8b2f182310461e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416317"
---
# <a name="create-and-configure-extended-warranties"></a>Genişletilmiş garantiler oluşturma ve yapılandırma

[!include [banner](includes/banner.md)]

Bu konu genişletilmiş garantileri kapsar ve bunların Microsoft Dynamics 365 Commerce'te nasıl oluşturacağını ve yapılandırılacağını açıklar.

## <a name="overview"></a>Özet

Müşteriler, ürün satın aldıklarında genişletilmiş destek ve hizmetleri, özellikle de telefon ve bilgisayarlar gibi üstün bir fiyat noktasında satılan tüketici ürünleri için giderek daha fazla tercih ediyor. Perakendeciler satın alma için genişletilmiş garantiler sağlayarak müşteri bağlılığı oluşturmaya yardımcı olabilir. Genişletilmiş garantiler, müşterilerin servis ve destek için gidebilecekleri yerleri bilmelerini sağlar. Bu nedenle, sorunların etkili şekilde ele alınabileceğine güvenilebilirler.

Genişletilmiş garantiler, müşterilere ilk ürün satın alma sırasında bir perakende kanalında satılabilir. Bunlar aynı zamanda ilk satın almadan sonra sınırlı bir süre içinde de satılabilir.

### <a name="warranty-item-setup"></a>Garanti maddesi kurulumu

Dynamics 365 Commerce, garanti maddesi oluşturmanıza ve bunun için öznitelik ayarlamanıza olanak tanıyan işlevler sağlar. Bu öznitelikler arasında, bir ürün ve garanti maddesi arasındaki ilişki, garantinin fiyatı ve garantinin süresi bulunur. Garanti maddesi yapılandırılıp kuruluş birimine serbest bırakıldıktan sonra, perakendeci Modern Point of Sale (MPOS), çevrimiçi mağazalar ve diğer perakende kanalları üzerinden garanti satabilir.

### <a name="warranty-item-sales"></a>Garanti maddesi satışı

Genişletilmiş garantiler, ilk ürün satın alma sırasında bir perakende kanalında satılır. Bunlar aynı zamanda ilk satın almadan sonra sınırlı bir süre içinde de satılabilir.

Satış noktasında (POS), müşterinin alışveriş sepetine ilgili bir ürün eklendiğinde satış temsilcilerinden bir genişletilmiş garanti eklemeleri istenir. Bu nedenle, satış akışının bir parçası olarak satış sorumlularına yukarı satış veya çapraz satış fırsatı sunulur.

Müşteriler daha sonra da dönüş yapabilir ve daha önce satın aldıkları ürünler için genişletilmiş garanti alabilir. Bu gibi durumlarda, satış sorumlusu orijinal hareketi arayabilir ve müşteriye ilgili genişletilmiş garanti maddesini satabilir.

### <a name="warranty-terminology"></a>Garanti terminolojisi

Aşağıdaki tablo, garantiyle ilgili bazı terimleri tanımlar.

| Vade | Tanım |
|------------------------------|--------------|
| Genişletilmiş garanti/Garanti | *Genişletilmiş garanti*, müşterilere uzatılmış garanti sağlayan bir servis anlaşması veya sözleşmeyi belirtir. Genişletilmiş garanti, genişletilmiş garantinin karşılama dönemi boyunca ürünlerin değiştirilmesi veya onarılmasına ilişkin ek hizmet içerir. |
| Üreticinin garantisi | Bir *üreticinin garantisi* (genellikle *sınırlı garanti* olarak bilinir), müşterilerin bir ürün satın aldığı zaman alacağı garantidir. Üreticinin garantisinin birkaç özelliği aşağıda belirtilmiştir:<ul><li>Garanti maliyeti ürünün maliyetine dahildir. Müşterilerin, üreticinin garantisi için herhangi bir ek tutar ödemesine gerek yoktur.</li><li>Ürün kategorisine bağlı olarak, bir üreticinin garantisi genellikle 30 gün, altı ay veya bir yıl sürer. (Çoğu tüketici elektroniği için, garanti süresi bir yıldır).</li><li>Garanti, mekanik veya elektrik arızalarının neden olduğu kusurları kapsamaktadır. Kapsam sınırlıdır ve satın alınan ürünün kazayla hasar görmesini kapsamaz. Satın aldıkları ürünleri günlük zararlardan korumak isteyen müşterilerin genişletilmiş bir garanti alması gerekir. Ürün kategorisine bağlı olarak, genişletilmiş garanti süresi iki ile on yıl arasındadır. Ayrıca, kapsamları daha geniştir ve örneğin düşme, damlama ve lekeler gibi gündelik kazalara karşı garanti sunarlar.</li></ul> |
| Garanti öğesi | *Garanti maddesi*, garanti verilebilir bir madde için satılan genişletilmiş garanti maddesidir. Dizüstü bilgisayarlar için kazalara karşı iki yıllık koruma planı örnek olarak verilebilir. |
| Garanti verilebilir madde | *Garanti verilebilir madde*, garantinin satıldığı serileştirilmiş bir üründür. Örneğin, bir dizüstü bilgisayar, iki yıllık ve üç yıllık genişletilmiş garantilerin satılabildiği garanti verilebilir bir maddedir. |
| Garanti grubu | *Garanti grubu*, garanti maddeleri ile garanti verilebilir maddeler arasındaki ilişkidir. POS, müşteri sepetine garanti verilebilir bir madde eklendiğinde, satış sorumlularına hangi garanti maddelerinin eklenmesi gerektiğini belirtmek üzere garanti gruplarını kullanır. |
| Garanti ilkesi | *Garanti İlkesi*, garanti ilkesi satıldığında Commerce'ta oluşturulan bir varlıktır. Garanti ilkesi, satın alınan garanti maddesinin başlangıç ve bitiş tarihleri, hüküm ve koşulları ve garanti edilen ürünün seri numarası gibi bilgileri içerir. Garanti İlkesi numaraları müşterilerle paylaşılabilir, böylece müşterilerin satın aldıkları genişletilmiş garanti maddesi için bir referansı olur. |

## <a name="create-a-warranty-item"></a>Garanti maddesi oluşturma

Commerce'te garanti maddesi oluşturmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Ürünler ve kategoriler \> Ürünler**'e gidin.
1. Bir garanti maddesi oluşturmak için **Yeni**'yi seçin.
1. **Yeni ürün** iletişim kutusunda, **Ürün türü** alanında **Servis**'i seçin.
1. **Ürün alt türü** alanında, **Ürün**'ü seçin.
1. **Ürün servis türü** alanında, **Servis**'i seçin.
1. **Ürün adı** alanına ürün adını girin.
1. **Perakende kategorisi** alanında, açılan iletişim kutusundan bir değer seçin ve **Tamam**'ı seçin.
1. **Ürün numarası** alanına ürün numarasını girin.
1. **Tamam**'ı seçin.
1. **Ürün ayrıntıları** sayfasında, **Garanti** hızlı sekmesinde, **Zaman birimi** ve **Zaman uzunluğu** alanlarını ayarlayın.

    | Alan adı | Değer | Tanım |
    |------------|-------|-------------|
    | Zaman birimi | **Gün**, **Hafta**, **Ay** veya **Yıl** | Bu alan, garanti için kullanılan zaman birimini belirtir. |
    | Süre uzunluğu | Pozitif tamsayı değeri | Bu alan, garantinin süresini seçilen zaman birimi cinsinden belirtir. |

    Örneğin, iki yıllık bir garanti için, **Zaman birimi** alanını **Yıl** ve **Zaman uzunluğu** alanını **2** olarak ayarlayın. Alternatif olarak, aşağıdaki resimde gösterildiği gibi **Zaman birimi** alanını **Ay** ve **Zaman uzunluğu** alanını **24** olarak da ayarlayabilirsiniz.

    ![Garanti maddesi için ürün ayrıntıları sayfası](./media/ew-time-properties.png)

1. Garanti maddesini kaydetmek için **Kaydet**'i seçin.
1. Satılabilmesi için garanti ürününü şirkete serbest bırakın. Daha fazla bilgi için bkz. [Perakende ürünleri ayarlama](set-up-retail-products.md).
1. **Serbest bırakılan ürün ayrıntıları** sayfasında, **Garanti** hızlı sekmesinde, **Fiyat aralığı tabanı**, **Alt sınır** ve **Üst sınır** alanlarını ayarlayın.

    | Alan adı | Değer | Tanım |
    |------------|-------|-------------|
    | Fiyat aralığı tabanı | **Hiçbiri**, **Temel fiyat** veya **Satış fiyatı** | <ul><li>**Hiçbiri**: Fiyat aralıklarının **Alt sınır** ve **Üst sınır** değerleri uygulanamaz.</li><li>**Temel fiyat**: Garanti verilebilir ürünün temel fiyatı (indirimler olmadan fiyatı) belirtilen **Alt sınır** ile **Üst sınır** değerleri arasındaysa, garanti verilebilir maddenin fiyatına göre belirli bir garanti uygulanır.</li><li>**Satış fiyatı**: Bu değer gelecekte kullanılmak üzere ayrılmıştır.</li></ul> |
    | Alt sınır, Üst sınır | Pozitif tamsayı değeri | Bu alanlar, garanti verilebilir maddesinin üst ve alt fiyat sınırlarını ve geçerli garanti maddesinin garanti verilen ürüne nasıl uygulanacağını tanımlar. Bu sınırlar için garanti verilen maddenin temel fiyatı temel alınabilir (üreticinin önerilen perakende fiyatı \[MSRP\] olarak da bilinir). **Fiyat aralığı tabanı** alanı **Temel fiyat** olarak ayarlanırsa, yalnızca temel fiyatı **Alt sınır** ile **Üst sınır** değerleri arasında olan bir garanti verilebilir madde POS'ta garanti maddesi ekleme istemini tetikler. |

    Örneğin, aşağıdaki şekilde **Fiyat aralığı tabanı** alanı **Temel fiyat** olarak, **Alt sınır** alanı 500 ABD doları ve **Üst sınır** alanının 1000 ABD doları olarak ayarlandığı gösterilir.
    
    ![Garanti maddesi için serbest bırakılan ürün ayrıntıları sayfası](./media/ew-release-product-details.png)

1. Garanti maddesini satılacağı kanala tahsis edin. Daha fazla bilgi için bkz. [Ürün çeşitleri ayarlama](set-up-assortments.md).

### <a name="example"></a>Örnek

Garanti verilebilir madde (ürün) olan bir dizüstü bilgisayarın temel fiyatı 999 ABD dolarıdır ve iki dizüstü bilgisayar garanti öğesi vardır:

- Garanti\_1'in alt sınırı 500 ABD doları ve üst sınırı 1000 ABD dolarıdır ve **Fiyat aralığı tabanı** alanı **Temel fiyat** olarak ayarlanmıştır.
- Garanti\_2'in alt sınırı 1.001 ABD doları ve üst sınırı 2.000 ABD dolarıdır ve **Fiyat aralığı tabanı** alanı **Temel fiyat** olarak ayarlanmıştır.

Bu durumda, dizüstü bilgisayar garanti verilebilir maddesi müşteri sepetine eklendiğinde, dizüstü bilgisayarın fiyatı Garanti\_1'in alt ve üst sınırları arasında olduğundan, POS'ta Garanti\_1'i ekleme istemi görüntülenir.

> [!NOTE]
> Bu örnekte, istemin garanti verilebilir maddenin fiyatından bağımsız olarak, hem Garanti\_1, hem de Garanti\_2 için gösterilmesini istiyorsanız, **Fiyat aralığı tabanı** alanını **Hiçbiri** olarak ayarlayın.

## <a name="configure-channel-specific-settings"></a>Kanala özgü ayarları yapılandırma

Kanala özgü ayarlar, müşterinin sepetine bir garanti verilebilir madde eklendiğinde, POS'ta bir garanti maddesi ekleme istemi gösterilip gösterilmeyeceğini belirtmenize olanak tanır.

Commerce'ta kanala özel ayarları yapılandırmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Ürünler ve kategoriler \> Garanti \> Garanti ayarları**'na gidin.
1. **Kanala özgü** sekmesinde, kanalınızın **Garanti iste** sütununda, aşağıdaki adımlardan birini izleyin:

    - Sepete bir garanti verilebilir madde eklendiğinde POS'ta bir garanti maddesi istemi gösterilmesi gerekiyorsa onay kutusunu seçin.
    - Sepete bir garanti verilebilir madde eklendiğinde POS'ta bir garanti maddesi istemi gösterilmesi gerekmiyorsa onay kutusunun işaretini kaldırın.

1. Verileri kanalla eşitlemek için **1070** işini çalıştırın.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Garanti ilkeleri için numara serisi yapılandırma

Her garanti ilkesi benzersiz olarak bir numara serisi tarafından oluşturulan bir garanti ilkesi numarasıyla tanımlanır. Numara serileri hakkında daha fazla bilgi için bkz. [Numara serilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Commerce'ta garanti ilkeleri için numara serisi yapılandırmak üzere aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Ürünler ve kategoriler \> Garanti \> Garanti ayarları**'na gidin.
1. **Numara serileri** sekmesinde, **Garanti ilkesi** referansına ilişkin satırda, **Numara serisi kodu** alanında bir değer girin veya seçin.

## <a name="set-up-a-warranty-group"></a>Garanti grubu ayarlama

Garanti grubu, garanti maddeleri ile garanti verilebilir maddeler arasındaki ilişkidir. POS, müşteri sepetine garanti verilebilir bir madde eklendiğinde, satış sorumlularına hangi garanti maddelerinin eklenmesi gerektiğini belirtmek üzere garanti gruplarını kullanır.

Commerce'ta garanti grubu ayarlamak için bu adımları izleyin.

1.  **Retail ve Commerce \> Ürünler ve kategoriler \> Garanti \> Garanti grupları**'na gidin.
1. Bir garanti grubu oluşturmak için **Yeni**'yi seçin.
1. **Ad** alanına, yeni grup için bir ad girin.
1. **Genel** hızlı sekmesinde, **Açıklama** alanına grubun açıklamasını girin.
1. **Garanti ürünleri** hızlı sekmesinde, garanti maddesi eklemek için **Satır ekle**'yi seçin.
1. **Görüntüleme sırası** alanına, garanti grubunu POS'ta sıralamak için bir numara girin. POS garanti maddelerini, garanti istemi gerçekleştiğinde artan sırada gösterir.
1. **Garanti verilebilen ürünler** hızlı sekmesinde, garanti verilebilen maddeler eklemek için **Satır ekle**'yi seçin.
1. Garanti maddesi, garanti verilebilir maddelere (ürünler) ilişkin kategorinin tamamına uygulanabilir ise, **Kategori** alanında kategoriyi seçin. Garanti maddesi belirli bir garanti verilebilir madde (ürün) için uygulanabilir ise, **Ürün** alanında ürünü seçin.
1. **Geçerli kanallar** hızlı sekmesinde, garanti maddesini satmak istediğiniz kanalı eklemek için **Satır ekle**'yi seçin.
1. Yapılandırmayı kaydetmek için **Kaydet**'i seçin.
1. Garanti grubunu yayımlamak için **Yayımla**'yı seçin.
1. Verileri kanalla eşitlemek için **1040** işini çalıştırın.

## <a name="sell-warranty-items-at-the-pos"></a>POS'ta garanti maddeleri satma

İki POS işlemi, satış görevlilerine müşter satın almaları için iş akışı sırasında garanti maddeleri satma olanağı sunar:

- **Garanti ekle**: Bu işlem, sepette seçilmiş olan bir garanti verilebilir madde için uygun garantileri gösteren bir istemi tetikler.
- **Mevcut harekete garanti ekle**: Bu işlem, satış görevlilerine daha önce satılmış olan garanti verilebilir maddeleri için garanti satma olanağı sağlar. Satış görevlileri, hareketin makbuz numarasını girerek garanti verilebilir ürünle ilişkili orijinal hareket numarasını bulabilirler.

Aşağıdaki resimde, garanti verilebilir maddeyle ilgili geçerli satın alma için garanti maddesi ekleme isteminin yer aldığı POS terminal sayfası örneği gösterilmektedir.

![Geçerli satınalma için garanti maddesi ekleme istemi örneği](./media/ew-sell-warranty.png)

Aşağıdaki resimde, daha önce satılmış olan bir garanti verilebilir maddeyle ilgili garanti maddesi ekleme özelliğine ilişkin bir örnek gösterilmektedir.

![Daha önce satılmış olan garanti verilebilir madde için garanti maddesi ekleme özelliği örneği](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Garanti hareketlerini işle

Garantiler peşin hareketlerde satıldığında, hareketler Commerce Headquarters'da deftere nakledildikten sonra, Commerce kullanıcıları, garanti hareketlerini işlemek ve garanti ilkeleri oluşturmak için **Garanti hareketleri işle** işini çalıştırabilir.

Commerce Headquarters'da garanti hareketlerini işlemek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Ürünler ve kategoriler \> Garanti \> Garanti hareketlerini işle**'ye gidin.
1. **Kuruluş düğümleri seç** iletişim kutusunda, **Kuruluş hiyerarşisi** alanında bir değer seçin.
1. **Kullanılabilir kuruluş düğümleri** listesinde, tek bir mağaza seçin veya bir mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm seçin.
1. Seçiminizi **Seçili kuruluş düğümleri** listesine eklemek için sağ ok düğmesini seçin.
1. **Arka planda çalıştır** sekmesini seçin.
1. **Toplu işleme** seçeneğini **Evet** olarak ayarlayıp **Yineleme**'yi seçin.
1. **Yinelemeyi tanımla** iletişim kutusunda, **Başlangıç tarihi** alanında, yinelemenin başlangıç tarihini seçin veya girin.
1. **Başlangıç saati** alanında, yinelemenin başlangıç saatini seçin veya girin.
1. Şu adımlardan birini izleyin:

    - Yinelemenin asla bitmemesi gerekiyorsa, **Bitiş tarihi yok** seçeneğini belirleyin.
    - Yinelemenin belirli bir çalıştırma sayısı sonunda bitmesi gerekiyorsa **Bu tarihten sonra bitir** seçeneğini seçin. Bu seçeneği seçerseniz, çalışma sayısını girin.
    - Yinelemenin belirli bir tarihte bitmesi gerekiyorsa, **Şu tarihte sonlandır:** seçeneğini belirleyin. Bu seçeneği seçerseniz, tarihi seçin veya girin.

1. **Tamam**'ı seçin.
1. **Tamam**'ı seçin.

## <a name="warranty-policies"></a>Garanti ilkeleri

Genişletilmiş bir garanti satıldığında, otomatik olarak garanti ilkesi varlığı oluşturulur. Garanti İlkesi numaraları müşterilerle paylaşılabilir, böylece müşterilerin satın aldıkları garanti maddesi için bir referansı olur. Garanti ilkelerinin özellikleri, garantinin geçerli başlangıç tarihini ve bitiş tarihini, hüküm ve koşulları, garantinin satıldığı garanti verilebilir maddenin seri numarasını içerir.

> [!NOTE]
> Garanti ilkesi özellikleri, garanti ilkesi varlıkları oluşturulduğunda otomatik olarak oluşturulur. Şu anda, el ile yapılandırılamaz veya düzenlenemez.

Aşağıdaki tabloda, garanti ilkesi özellikleri ve bunların değerleri açıklanmıştır. Commerce Headquarters'da, veritabanı tablosu WARRANTYPOLICY olarak adlandırılır.

| Özellik adı | Değer | Tanım |
|---------------|-------|-------------|
| PolicyNumber | Bir karakter dizesi (maksimum 20 karakter) | Garanti İlkesi numarası |
| WarrantiedItemId | Bir karakter dizesi (maksimum 20 karakter) | Garanti verilebilir maddenin kodu |
| WarrantiedInventoryLotId | Bir karakter dizesi (maksimum 20 karakter) | Garanti verilebilir maddenin stok lot kodu |
| WarrantiedSerialNumber | Bir karakter dizesi (maksimum 20 karakter) | Garanti verilebilir maddenin seri numarası |
| WarrantiedFulfilledDate | Bir tarih | Garanti verilebilir maddenin karşılanma tarihi |
| WarrantyItemId | Bir karakter dizesi (maksimum 20 karakter) | Garanti maddesinin kodu |
| WarrantyInventoryLotId | Bir karakter dizesi (maksimum 20 karakter) | Garanti maddesinin stok lot kodu |
| WarrantySalesDate | Bir tarih | Garanti maddesinin satış tarihi |
| WarrantyEffectiveDate | Bir tarih | Garanti ilkesinin geçerlilik tarihi |
| WarrantyExpirationDate | Bir tarih | Garanti ilkesinin sona erme tarihi |
| CustAccount | Bir karakter dizesi (maksimum 20 karakter) | Müşteri hesap numarası |
| Durum | **Oluşturuldu**, **Hükümsüz kılında**, **Etkin** veya **Süresi doldu** | Garanti ilkesinin durumu |
| Notlar | Bir karakter dizesi (maksimum 255 karakter) | Hükümler ve koşullar gibi garanti ilkesiyle ilgili notlar |

## <a name="frequently-asked-questions-faq"></a>Sık sorulan sorular (SSS)

**Neden POS'ta bir garanti istemini göremiyorum?**

Garanti maddesinin kanala tahsis edildiğinden emin olun. Ayrıca, garanti grubunun ilgili kanalı içerecek şekilde yapılandırıldığından emin olun.

**Mevcut bir harekete garanti eklemeye ve müşteri siparişi makbuz numarasını girmeye çalıştığımda, neden hiçbir hareket satırı öğesini göremiyorum?**

Makbuzlar yalnızca, makbuzları Commerce Headquarters'a yüklemek için bir çekme işi (P işi) çalıştırıldığında bulunur. P işini çalıştırmak için, **Retail ve Commerce \>Retail ve Commerce BT \> Dağıtım planlaması**'na gidin, **P-0001** işini ve **Şimdi çalıştır**'ı seçin.

**Garanti özelliği neden yalnızca serileştirilmiş ürünler için geçerlidir?**

Garanti belirli, benzersiz bir ürün için sağlanan bir hizmettir. Dynamics 365'te, bir ürün yalnızca bir seri numarası ile benzersiz olarak tanımlanabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Perakende ürünlerini ayarlama](set-up-retail-products.md)

[Ürün çeşitlerini ayarlama](set-up-assortments.md)

[Numara serilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]