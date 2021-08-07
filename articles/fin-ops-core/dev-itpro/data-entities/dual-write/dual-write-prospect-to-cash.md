---
title: Çift yazmada aday müşteriden nakde
description: Bu konu, çift yazmadan aday müşteriden nakde hakkında bilgi sağlar.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0fcbc5b0f571e9f2cf7f1ad7c1e976d022199b47
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542283"
---
# <a name="prospect-to-cash-in-dual-write"></a>Çift yazmada aday müşteriden nakde

[!include [banner](../../includes/banner.md)]

Birçok işletmenin önemli bir hedefi, aday müşterileri müşterilere dönüştürmek ve bu müşterilerle devam eden bir iş ilişkisi sürdürmektir. Microsoft Dynamics 365 uygulamalarında, aday müşteriden nakde süreci teklifler veya sipariş işleme iş akışları aracılığıyla gerçekleştirilir ve mali değerler için mutabakat sağlanır ve kabul edilir. Çift yazma ile aday müşteriden nakde tümleştirmesi, Dynamics 365 Sales veya Dynamics 365 Supply Chain Management'ta oluşturulan bir teklif ve sipariş alır ve teklif ve siparişi her iki uygulamada da kullanılabilir duruma getirir.

Uygulama arabirimlerinde, işleme durumlarına ve fatura bilgilerine gerçek zamanlı olarak erişebilirsiniz. Bu nedenle, teklif ve siparişleri yeniden oluşturmak zorunda kalmadan ürün stoklama, stok işleme ve Supply Chain Management'ta karşılama gibi işlevleri daha kolay yönetebilirsiniz.

![Aday müşteriden nakde için çift yazma veri akışı.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Müşteri ve ilgili kişi tümleştirmesi hakkında bilgi için bkz. [Tümleşik müşteri aslı](customer-mapping.md). Ürün tümleştirmesi hakkında bilgi için bkz. [Birleşik ürün deneyimi](product-mapping.md).

> [!NOTE]
> Dynamics 365 Sales'da, hem aday müşteri hem de müşteri, **RelationshipType** sütununun **Aday Müşteri** ya da **Müşteri** olduğu bir **Hesap** tablosundaki kayda başvurur. İş mantığınız, **Hesap** kaydının önce aday müşteri olarak ve sonra müşteri olarak oluşturulup nitelendirildiği bir **Hesap** niteleme işlemi içeriyorsa, söz konusu kayıt yalnızca müşteriyse (`RelationshipType=Customer`) Finance and Operations uygulamasıyla eşitlenir. **Hesap** satırının aday müşteri olarak eşitlenmesini istiyorsanız, aday müşteri verilerini tümleştirmek için özel bir eşlemeye ihtiyacınız vardır.

## <a name="prerequisites-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış tekliflerini eşitleyebilmeniz için önce aşağıdaki ayarları güncelleştirmeniz gerekir.

### <a name="setup-in-sales"></a>Sales içinde kurulum

Sales'de **Ayarlar \> Yönetim \> Sistem ayarları \> Sales**'e gidin ve aşağıdaki ayarların kullanıldığından emin olun:

- **Sistem fiyatlama hesaplamasını kullan** sistem seçeneğini **Evet** olarak ayarlayın.
- **İndirim hesaplama yöntemi** sütunu **Satır maddesi** olarak ayarlanmalıdır.

### <a name="sites-and-warehouses"></a>Tesisler ve ambarlar

Supply Chain Management'ta, **Tesis** ve **ambar** sütunlar teklif satırları ve sipariş satırları için gereklidir. Tesis ve ambarı varsayılan sipariş ayarlarında ayarlarsanız, teklif satırına veya sipariş satırına bir ürün eklediğinizde bu sütunlar otomatik olarak ayarlanır. 

### <a name="number-sequences-for-quotations-and-orders"></a>Teklifler ve siparişler için numara serileri

Supply Chain Management ve Sales için numara serileri teklifler ve siparişler oluşturulduğunda ve Sales ile Supply Chain Management'ta eşitlendiğinde bağlı değildir. Sales'de oluşturulan bir satış siparişi Supply Chain Management ile eşitlenirse, Supply Chain Management'ta aynı satış siparişi numarasına sahip olur. Satış siparişi numarasının yinelenmemesini sağlamaya yardımcı olmak için iki uygulama içinde farklı numara serisi sistemleri kullanmanız gerekir.

Örneğin, Supply Chain Management'taki numara serisi **1, 2, 3, 4, 5 ,...** Sales'deki numaras serisi **100, 99, 98, ...** olur. Sales içinde 100 satış siparişi oluşturursanız, Supply Chain Management'ta zaten varolan bir sipariş numarası oluşturulur. Başka bir deyişle, Supply Chain Management ve Sales'de satış siparişleri oluşturulurken, iki numara serisi çakışacaktır. Bunun yerine, Supply Chain Management'ta **F1, F2, F3 ,...** ve Sales'de **C1, C2, C3, ...** gibi bir numara serisi kullanabilirsiniz. Bu numara serileri asla tekrarlanan satış siparişi numaraları oluşturmaz.

## <a name="sales-quotations"></a>Satış teklifleri

Satış teklifleri Sales veya Supply Chain Management'ta oluşturulabilir. Sales'de bir teklif oluşturursanız, bu gerçek zamanlı olarak Supply Chain Management ile eşitlenir. Aynı şekilde Supply Chain Management'ta bir teklif oluşturursanız, bu gerçek zamanlı olarak Sales ile eşitlenir. Aaşağıdaki noktaları unutmayın:

+ Teklifte ürüne iskonto ekleyebilirsiniz. Bu durumda, iskonto Supply Chain Management ile eşitlenecektir. Üst bilgideki **İskonto**, **Masraflar** ve **Vergi** sütunları Supply Chain Management'taki bir ayar tarafından denetlenir. Bu kurulum hiçbir tümleştirme eşlemesini desteklemez. Bunun yerine; **Fiyat**, **İskonto**, **Masraf** ve **Vergi** sütunları Supply Chain Management'ta korunur ve işlenir.
+ Satış teklifi üst bilgisindeki **İskonto oranı**, **İskonto** ve **Navlun Tutarı** sütunları salt okunur sütunlardır.
+ **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** sütunları varsayılan eşlemelerin parçası değildir. Bu sütunları eşleştirmek için, tablonun aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşlemesi ayarlamanız gerekir.

Field Service çözümünü de kullanıyorsanız, **Teklif Satırı Hızlı Oluştur** parametresini yeniden etkinleştirdiğinizden emin olun. Parametrenin yeniden etkinleştirilmesi, hızlı oluştur işlevini kullanarak teklif satırları oluşturmaya devam etmenize olanak tanır.

1. Dynamics 365 Sales uygulamanıza gidin.
2. Üst gezinti çubuğunda ayarlar simgesini seçin.
3. **Gelişmiş Ayarlar**'ı seçin.
4. **Sistemi Özelleştir** seçeneğini belirleyin.
5. **Teklif Satırı** menü öğesini seçin.
6. **Veri Hizmetleri** bölümüne gidin ve **Hızlı oluşturmaya izin ver** onay kutusunu seçin.

## <a name="sales-orders"></a>Satış siparişleri

Satış siparişleri Sales veya Supply Chain Management'ta oluşturulabilir. Sales'de bir satış siparişi oluşturursanız, bu gerçek zamanlı olarak Supply Chain Management ile eşitlenir. Aynı şekilde Supply Chain Management'ta bir satış siparişi oluşturursanız, bu gerçek zamanlı olarak Sales ile eşitlenir. Aaşağıdaki noktaları unutmayın:

+ Dynamics 365 Sales'deki serbest ürün eklemeler, Dynamics 365 Supply Chain Management'ta ürün kategorileri olarak görünür.
+ İskonto hesaplama ve yuvarlama:

    - Sales'taki iskonto hesaplama modeli Supply Chain Management'taki iskonto hesaplama modelinden farklıdır. Supply Chain Management'ta, satış satırındaki nihai iskonto tutarı iskonto tutarları ile iskonto yüzdeleri kombinasyonun sonucu olabilir. Nihai iskonto tutarı satırdaki miktara bölünürse, yuvarlama oluşabilir. Bununla birlikte, bu yuvarlama yuvarlanan bir birim başına iskonto tutarı Sales'a eşitlenirse dikkate alınmaz. Supply Chain Management'taki bir satış satırından gelen tam iskonto tutarının Sales'e doğru şekilde eşitlenmesini sağlamak için, tam tutarın satır miktarına bölünmeden eşitlenmesi gerekir. Bu nedenle, Sales'ta iskonto hesaplama yöntemini **Satır maddesi** olarak tanımlamanız gerekir.
    - Bir satış siparişi satırı Sales'den Supply Chain Management'a eşitlendiğinde tam satır iskontosu tutarı kullanılır. Supply Chain Management'ta bir satır için tam iskonto tutarının saklanabileceği bir sütun bulunmadığından tutar miktara bölünür ve **Satır iskontosu** sütununda saklanır. Bu bölme işlemi sırasında gerçekleşen yuvarlamalar satış satırındaki **Satış masrafları** sütununda saklanır.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Örnek: Sales'ten Supply Chain Management'a eşitleme

Aşağıdaki satış siparişine sahipsiniz:

+ **Sales:** Miktar = 3, satır başına iskonto = 10,00 TL
+ **Supply Chain Management:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış masrafı = -0,01 TL

Supply Chain Management'tan Sales'e eşitleme yaparsanız, aşağıdaki sonucu alırsınız:

+ **Supply Chain Management:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış masrafı = -0,01 TL
+ **Sales:** Miktar = 3, satır başına iskonto = (3 x 3,33 TL) + 0,01 TL = 10,00 TL

## <a name="dual-write-solution-for-sales"></a>Sales için çift yazma çözümü

**Sipariş** tablosuna yeni sütunlar eklenmiştir ve bunlar sayfada görüntülenir: Bu sütunların çoğu Sales'daki **Tümleştirme** sekmesinde görünür. Durum sütunlarının nasıl eşlendikleri hakkında daha fazla bilgi edinmek için [Satış siparişi durum sütunlarıyla ilgili eşlemeyi ayarlama](sales-status-map.md) konusuna bakın.

+ Sales'de **Satış siparişi** sayfasındaki **Fatura Oluştur** ve **Siparişi İptal Et** düğmeleri gizlidir.
+ **Satış siparişi durumu** değeri, Supply Chain Management'tan gelen değişikliklerin Sales'de satış siparişine aktığından emin olunması için **Etkin** kalacaktır. Bu davranışı kontrol etmek için, varsayılan **Statecode\[Status\]** değerini **Etkin** olarak ayarlayın.

## <a name="invoices"></a>Faturalar

Satış faturaları Supply Chain Management'ta oluşturulur ve Sales'e eşitlenir. Aaşağıdaki noktaları unutmayın:

+ Bir **Fatura numarası** sütunu **Fatura** tablosuna eklenmiştir ve sayfada görüntülenir.
+ **Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Supply Chain Management'ta oluşturulacak ve Sales'e eşitlenecektir. **Fatura** sayfası düzenlenemez çünkü faturalar Supply Chain Management'tan eşitlenecektir.
+ **Satış siparişi durumu** değeri ilgili fatura Supply Chain Management'tan Sales'e eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir. Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır. Bu nedenle, satış siparişinin sahibi faturayı görebilir.
+ **Navlun koşulları**, **Teslimat koşulları** ve **Teslimat şekli** sütunları varsayılan eşlemelere dahil değildir. Bu sütunları eşleştirmek için, tablonun aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşlemesi ayarlamanız gerekir.

## <a name="templates"></a>Şablonlar

Aday müşteriden nakde, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir temel tablo eşlemeleri koleksiyonudur.

| Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları | Tanım |
|-----------------------------|-----------------------------------|-------------|
[Tüm ürünler](mapping-reference.md#138) | msdyn_globalproducts | |
[Müşteriler V3](mapping-reference.md#101) | hesaplar | |
[Müşteriler V3](mapping-reference.md#116) | ilgili kişiler | |
[İlgili Kişiler V2](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS satış siparişi başlıkları](mapping-reference.md#217) | salesorders | |
[CDS satış siparişi satırları](mapping-reference.md#216) | salesorderdetails | |
[CDS satış teklifi başlığı](mapping-reference.md#215) | teklifler | |
[CDS satış teklifi satırları](mapping-reference.md#214) | quotedetails | |
[Serbest bırakılan ürünler V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Satış faturası başlıkları V2](mapping-reference.md#118) | faturalar | Finance and Operations uygulamasındaki Satış faturası başlıkları V2 tablosu, satış siparişleri için faturalar ve serbest metin faturaları içerir. Dataverse'te çift yazma için serbest metin fatura belgelerini filtreleyecek bir filtre uygulanır. |
[Satış faturası satırları V2](mapping-reference.md#117) | invoicedetails | |
[Satış siparişi kaynak kodları](mapping-reference.md#186) | msdyn_salesorderorigins | |

Fiyat listeleri hakkında bilgi için bkz. [Birleşik ürün deneyimi](product-mapping.md).

## <a name="limitations"></a>Sınırlamalar

- İade siparişleri desteklenmez.
- Alacak dekontları desteklenmez.
- Ana veriler için müşteri veya satıcı gibi mali boyutlar ayarlanmalıdır. Bir teklife veya satış siparişine müşteri eklendiğinde müşteri kaydıyla ilişkilendirilmiş mali boyutlar otomatik olarak siparişe aktarılır. Şu anda çift yazma, ana veriler için mali boyut verilerini içermez.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
