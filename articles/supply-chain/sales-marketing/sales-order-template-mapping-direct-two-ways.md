---
title: Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme
description: Bu konu altında, satış siparişlerini Dynamics 365 Sales ve Dynamics 365 Supply Chain Management arasında eşitlemek için kullanılan temel görevler ve şablonlar açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ddc6159480d1ff9fb823dbd95465c991ae51f9c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974997"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu altında, satış siparişlerini Dynamics 365 Sales ve Dynamics 365 Supply Chain Management arasında eşitlemek için kullanılan temel görevler ve şablonlar açıklanmaktadır.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliğiyle kullanılabilecek Aday müşteriden nakde şablonları; hesaplar, ilgili kişiler, ürünler, satış teklifleri, satış siparişleri ve satış faturaları için Supply Chain Management ve Sales arasında veri akışını etkinleştirir. Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablonlar ve temel görevler, satış siparişlerini doğrudan Sales ve Supply Chain Management arasında eşitlemek için kullanılır.

- **Veri tümleştirmesindeki şablonların adları:** 

    - Satış Siparişleri (Sales'ten Supply Chain Management'a) - Doğrudan
    - Satış Siparişleri (Supply Chain Management'tan Sales'e) - Doğrudan

- **Veri tümleştirme projesindeki görevlerin adları:**

    - OrderHeader
    - OrderLine

Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Supply Chain Management'tan Sales'e) - Doğrudan
- Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)
- İlgili kişilerden Müşterilere (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)

## <a name="entity-set"></a>Varlık kümesi

| Supply Chain Management  | Satışlar             |
|-------------------------|-------------------|
| Dataverse satış siparişi başlıkları | SalesOrders       |
| Dataverse satış siparişi satırları   | SalesOrderDetails |

## <a name="entity-flow"></a>Varlık akışı

Satış siparişleri Sales içinde oluşturulur ve bir proje için **Satış Siparişleri (Sales'ten Supply Chain Management'a) - Doğrudan** şablonu temel alınarak **Proje çalıştır** tetiklendiğinde Supply Chain Management'a eşitlenir. Yalnızca tüm **Sipariş Ürünleri**'nin dışarıda tutulan ürünlerden oluşması durumunda siparişlerini Sales'tan etkinleştirebilir ve eşitleyebilirsiniz. Bu nedenle, serbest olmayan ürünler olabilir. Sipariş etkinleştirildikten sonra satış siparişi kullanıcı arabiriminde (UI) salt okunur olur. Bu noktada, güncelleştirmeler Supply Chain Management'tan yapılır. Bir satış siparişi **Onaylandı** olduğunda, **Satış Siparişleri (Supply Chain Management'tan Sales'e) - Doğrudan** şablonunu temel alan bir proje, güncelleştirmeleri veya karşılama durumunu Supply Chain Management'tan Sales'e eşitlemek için kullanılabilir.

Sales içinde siparişler oluşturmanız gerekmez. Bunun yerine, yeni satış siparişlerini Supply Chain Management'ta oluşturabilirsiniz. Bir satış siparişi durumunu **Onaylandı** olduğunda, önceki paragrafta açıklanan şekilde Sales'a eşitlenir.

Supply Chain Management'ta şablondaki filtreler yalnızca ilgili satış siparişlerinin eşitlemeye dahil edilmesini sağlar:

- Satış siparişinde, siparişi veren müşteri ile faturalanan müşteri Sales'tan geliyorsa, eşitlemeye dahil edilir. Supply Chain Management'ta **OrderingCustomerIsExternallyMaintained** ve **InvoiceCustomerIsExternallyMaintained** sütunları, veri tablolarından gelen satış siparişlerini filtrelemek için kullanılır.
- Supply Chain Management'taki satış siparişinin onaylanması gerekir. Yalnızca onaylanmış satış siparişleri veya daha yüksek işleme durumuna sahip satış siparişler (örneğin **Sevk edildi** veya **Faturalandı** durumları) Sales'a eşitlenir.
- Bir satış siparişi oluşturulduktan veya değiştirildikten sonra, Supply Chain Management'ta **Satış toplamlarını hesapla** toplu işinin çalıştırılması gerekir. Yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir.

## <a name="freight-tax"></a>Navlun vergisi

Sales vergiyi başlık düzeyinde desteklemez çünkü vergi satır düzeyinde saklanır. Supply Chain Management'tan vergiyi başlık düzeyinde desteklemek için (navlun vergisi gibi), sistem veriyi Sales'a serbest ürün olarak eşitler, **Navlun Vergisi** olarak adlandırır ve Supply Chain Management'taki vergi tutarına sahip olur. Bu şekilde, Sales'taki standart fiyat hesaplaması, Supply Chain Management'tan gelen başlık düzeyinde bir vergi olsa bile, toplamlar için kullanılabilir.

## <a name="discount-calculation-and-rounding"></a>İskonto hesaplama ve yuvarlama

Sales'taki iskonto hesaplama modeli Supply Chain Management'taki iskonto hesaplama modelinden farklıdır. Supply Chain Management'ta, satış satırındaki nihai iskonto tutarı iskonto tutarları ile iskonto yüzdeleri kombinasyonun sonucu olabilir. Nihai iskonto tutarı satırdaki miktara bölünürse, yuvarlama oluşabilir. Bununla birlikte, bu yuvarlama yuvarlanan bir birim başına iskonto tutarı Sales'a eşitlenirse dikkate alınmaz. Supply Chain Management'taki bir satış satırından gelen tam iskonto tutarının Sales'e doğru şekilde eşitlenmesini sağlamak için, tam tutarın satır miktarına bölünmeden eşitlenmesi gerekir. Bu nedenle, Sales'ta **İskonto hesaplama yöntemi**'ni **Satır maddesi** olarak tanımlamanız gerekir.

Bir satış siparişi satırı Sales'den Supply Chain Management'a eşitlendiğinde tam satır iskontosu tutarı kullanılır. Supply Chain Management'ta bir satır için tam iskonto tutarının saklanabileceği bir alan bulunmadığından tutar miktara bölünür ve **Satır iskontosu** alanında saklanır. Bu bölme işlemi sırasında gerçekleşen yuvarlamalar satış satırındaki **Satış masrafları** alanında saklanır.

### <a name="example"></a>Örnek

**Sales'ten Supply Chain Management'a eşitleme**

- **Sales:** Miktar = 3, satır başına iskonto = 10,00 TL
- **Supply Chain Management:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış ücreti =-0,01 TL 

**Supply Chain Management'tan Sales'e eşitleme**

- **Supply Chain Management:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış ücreti =-0,01 TL
- **Sales:** Miktar = 3, satır başına iskonto = (3 x 3,33 TL) + 0,01 TL = 10,00 TL

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

**Sipariş** tablosuna yeni sütunlar eklenmiştir ve bunlar sayfada görüntülenir:

- **Dışarıda Tutulan** – Sipariş Supply Chain Management'tan geliyorsa bu seçeneği **Evet** olarak ayarlayın.
- **İşleme durumu**: Bu sütun siparişin Supply Chain Management'taki işleme durumunu gösterir. Aşağıdaki değerler kullanılabilir:

    - **Taslak** – Bir sipariş Sales'ta ilk oluşturulduğundaki durum. Sales'ta yalnızca bu işleme durumuna sahip olan siparişler düzenlenebilir.
    - **Etkin** – Sipariş Sales'taki **Etkinleştir** düğmesi kullanılarak etkinleştirildikten sonraki durum.
    - **Teyit edildi**
    - **Sevk İrsaliyesi**
    - **Faturalandı**
    - **Çekildi**
    - **Kısmen Çekildi**
    - **Kısmen Paketlendi**
    - **Sevk Edildi**
    - **Kısmen Sevk Edildi**
    - **Kısmen Faturalandı**
    - **İptal edildi**

**Yalnızca Dışarıda Tutulan Ürünleri Var** ayarı, sipariş etkinleştirme sırasında satış siparişinin tümüyle dışarıda tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için kullanılır. Bir satış siparişi yalnızca harici tutulan ürünlere sahipse, ürünler Supply Chain Management'ta korunur. Bu ayar, Supply Chain Management tarafından bilinmeyen ürünlere sahip satış siparişi satırlarını etkinleştirmemenizi ve eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.

Dışarıda tutulan siparişler için **Satış siparişi** sayfasındaki **Fatura Oluştur**, **Siparişi İptal Et**, **Yeniden hesapla**, **Ürünleri Al** ve **Arama Adresi** düğmeleri gizlenmiştir çünkü faturalar Supply Chain Management'ta oluşturulacak ve Sales'e eşitlenecektir. Bu siparişler düzenlenemez çünkü satış siparişi bilgisi etkinleştirmeden sonra Supply Chain Management'tan eşitlenecektir.

Satış siparişi durumu, Supply Chain Management'tan gelen değişikliklerin Sales'de satış siparişi içine aktığından emin olunması için **Etkin** kalacaktır. Bu davranışı kontrol etmek için, varsayılan **Statecode\[Durum\]** değerini Veri tümleştirme projesinde **Etkin** olarak ayarlayın.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış siparişlerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun. Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir. Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.

    **Ayarlar** &gt; **Güvenlik** &gt; **Ekipler**'e gidin, ilgili ekibi seçin, **Rolleri Yönet**'i ve istenilen izinlere sahip bir rolü seçin; örn. **Sistem Yöneticisi**.

- Hem Sales hem de Supply Chain Management'ta iskontoların doğru hesaplandığından emin olmak için **İskonto hesaplama yöntemi** **Satır maddesi** olarak ayarlanmalıdır.
- **Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:

    - **Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.
    - **İndirim hesaplama yöntemi** sütunu **Satır maddesi** olarak ayarlanmalıdır.

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management'ta Kurulum

- **Satış ve pazarlama** &gt; **Periyodik görevler** &gt; **Satış toplamlarını hesapla**'ya gidin ve işi bir toplu iş olarak çalışacak şekilde ayarlayın. **Satış siparişleri için toplamları hesapla** seçeneğini **Evet** olarak ayarlayın. Bu adım önemlidir çünkü yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir. Toplu işin sıklığı, satış siparişi eşitlemesinin sıklığı ile uyumlu olmalıdır.

İş emri tümleştirmesini de kullanıyorsanız, satış menşeini ayarlamanız gerekir. Satış kaynağı Supply Chain Management'ta Field Service'taki iş emirlerinden oluşturulmuş olan satış siparişlerinin ayrılması için kullanılır. Satış siparişinin **İş emri tümleştirmesi** türünde bir satış kaynağı olduğunda **Harici iş emri durumu** alanı satış siparişi başlığında görüntülenir. Ayrıca, satış kaynağı Field Service'teki iş emirlerinden oluşturulmuş olan satış siparişlerinin Supply Chain Management'tan Field Service'e satış siparişi eşitlemesi sırasında filtrelenmesini sağlar.

1. **Satış ve pazarlama** \> **Kurulum** \> **Satış siparişleri** \> **Satış kaynağı** seçeneğine gidin.
2. **Yeni**'yi seçerek yeni bir satış kaynağı oluşturun.
3. **Satış kaynağı** sütununa, satış kaynağı için **SalesOrder** gibi bir ad girin.
4. **Açıklama** sütununda, **Sales'dan Satış Siparişi** gibi bir açıklama girin.
5. **Kaynak türü ataması** onay kutusunu seçin.
6. **Satış kaynağı türü** sütununu **Satış siparişi tümleştirmesi** olarak ayarlayın.
7. **Kaydet**'i seçin.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Satış Siparişlerinde Ayarlama (Sales'den Supply Chain Management'a) - Doğrudan Veri tümleştirme projesi

- **Shipto\_country** ile **DeliveryAddressCountryRegionISOCode** arasında gerekli eşleştirmenin mevcut olduğundan emin olun. Ulusal siparişler için ülke/bölge girmemek için değer eşlemesinde varsayılan değeri boş olarak ayarlayabilirsiniz. Sol tarafı 'Boş' bırakın ve sağ tarafı istenen ülkeye veya bölgeye ayarlayın.

    Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir; burada 'Boş' = ABD.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Satış Siparişlerinde Ayarlama (Supply Chain Management'tan Sales'e) - Doğrudan Veri tümleştirme projesi

#### <a name="salesheader-task"></a>SalesHeader görevi

- Sales'ta siparişler oluşturmak için bir fiyat listesi gereklidir. **pricelevelid.name \[Fiyat Listesi Adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin. Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz. Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.

    **pricelevelid.name \[Fiyat Listesi Adı\]** için varsayılan şablon değeri **CRM Hizmeti ABD (örnek)**'dir.

#### <a name="salesline-task"></a>SalesLine görevi

- Supply Chain Management'ta **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.
- Gerekli birimlerin Sales'ta tanımlandığından emin olun.

    Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **oumid.name** olarak tanımlanır.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** sütunları varsayılan eşlemelerin parçası değildir. Bu sütunları eşleştirmek için, tablonun aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşlemesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.

> [!NOTE]
> Eşleme hangi sütun bilgilerinin Sales'dan Supply Chain Management'a veya Supply Chain Management'tan Sales'a eşitleneceğini gösterir.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Satış Siparişleri (Supply Chain Management'tan Sales'e) - Doğrudan: OrderHeader

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Satış Siparişleri (Supply Chain Management'tan Sales'e) - Doğrudan: OrderLine

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Satış Siparişleri (Sales'den Supply Chain Management'a) - Doğrudan: OrderHeader

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Satış Siparişleri (Sales'den Supply Chain Management'a) - Doğrudan: OrderLine

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)
