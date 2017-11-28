---
title: "Sales ile Finance and Operations arasında satış siparişlerini doğrudan eşitleme"
description: "Bu konu, satış siparişi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Sales ile Microsoft Dynamics 365 for Finance and Operations, Enterprise edition arasında iki yönlü eşitleme çalıştırmak için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 568c33a63efdc58a179dadcb617634dcf533fd4b
ms.openlocfilehash: c31d65328250539fbe172f220272eec9d8b59bbf
ms.contentlocale: tr-tr
ms.lasthandoff: 11/13/2017

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Sales ile Finance and Operations arasında satış siparişlerini doğrudan eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, satış siparişi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Sales ile Microsoft Dynamics 365 for Finance and Operations, Enterprise edition arasında iki yönlü eşitleme çalıştırmak için temel görevleri ve şablonları açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablonlar ve temel görevler, satış siparişi başlıklarını ve satırlarını doğrudan Sales ile Finance and Operations arasında iki yönlü eşitlemek için kullanılır:

- **Veri tümleştirmesindeki şablonların adları:** 

    - Satış Siparişleri (Sales'tan Fin and Ops'a) - Doğrudan
    - Satış Siparişleri (Fin and Ops'tan Sales'a) - Doğrudan

- **Veri tümleştirme projesindeki görevlerin adları:**

    - OrderHeader
    - OrderLine

Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Fin and Ops'tan Sales'a) - Doğrudan
- Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)
- İlgili kişilerden Müşterilere (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations  | Satış             |
|-------------------------|-------------------|
| CDS satışları sipariş başlıkları | SalesOrders       |
| CDS satış siparişi satırları   | SalesOrderDetails |

## <a name="entity-flow"></a>Varlık akışı

Satış siparişleri Sales içinde oluşturulur ve bir proje için **Satış Siparişleri (Sales'tan Fin and Ops'a) - Doğrudan** şablonu temel alınarak **Proje çalıştır** tetiklendiğinde Finance and Operations'a eşitlenir. Yalnızca tüm **Sipariş Ürünleri**'nin dışarıda tutulan ürünlerden oluşması durumunda siparişlerini Sales'tan etkinleştirebilir ve eşitleyebilirsiniz. Bu nedenle, serbest olmayan ürünler olabilir. Sipariş etkinleştirildikten sonra satış siparişi kullanıcı arabiriminde (UI) salt okunur olur. Bu noktada, güncelleştirmeler Finance and Operations'dan yapılır. Bir satış siparişi **Onaylandı** olduğunda, **Satış Siparişleri (Fin and Ops'tan Sales'a) - Doğrudan** şablonunu temel alan bir proje, güncelleştirmeleri veya karşılama durumunu Finance and Operations'tan Sales'a eşitlemek için kullanılabilir.

Sales içinde siparişler oluşturmanız gerekmez. Bunun yerine, yeni satış siparişlerini Finance and Operations'da oluşturabilirsiniz. Bir satış siparişi durumunu **Onaylandı** olduğunda, önceki paragrafta açıklanan şekilde Sales'a eşitlenir.

Finance and Operations'da şablondaki filtreler yalnızca ilgili satış siparişlerinin eşitlemeye dahil edilmesini sağlar:

- Satış siparişinde, siparişi veren müşteri ile faturalanan müşteri Sales'tan geliyorsa, eşitlemeye dahil edilir. Finance and Operations'da **OrderingCustomerIsExternallyMaintained** ve **InvoiceCustomerIsExternallyMaintained** alanları, veri varlıklarından gelen satış siparişlerini filtrelemek için kullanılır.
- Finance and Operations içindeki satış siparişinin onaylanması gerekir. Yalnızca onaylanmış satış siparişleri veya daha yüksek işleme durumuna sahip satış siparişler (örneğin **Sevk edildi** veya **Faturalandı** durumları) Sales'a eşitlenir.
- Bir satış siparişi oluşturulduktan veya değiştirildikten sonra, Finance and Operations'da **Satış toplamlarını hesapla** toplu işinin çalıştırılması gerekir. Yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir.

## <a name="freight-tax"></a>Navlun vergisi

Sales vergiyi başlık düzeyinde desteklemez çünkü vergi satır düzeyinde saklanır. Finance and Operations'dan vergiyi başlık düzeyinde desteklemek için (navlun vergisi gibi), sistem veriyi Sales'a serbest ürün olarak eşitler, **Navlun Vergisi** olarak adlandırır ve Finance and Operations'taki vergi tutarına sahip olur. Bu şekilde, Sales'taki standart fiyat hesaplaması, Finance and Operations'dan gelen başlık düzeyinde bir vergi olsa bile, toplamlar için kullanılabilir.

## <a name="discount-calculation-and-rounding"></a>İskonto hesaplama ve yuvarlama

Sales'taki iskonto hesaplama modeli Finance and Operations'taki iskonto hesaplama modelinden farklıdır. Finance and Operations'da, satış satırındaki nihai iskonto tutarı iskonto tutarları ile iskonto yüzdeleri kombinasyonun sonucu olabilir. Nihai iskonto tutarı satırdaki miktara bölünürse, yuvarlama oluşabilir. Bununla birlikte, bu yuvarlama yuvarlanan bir birim başına iskonto tutarı Sales'a eşitlenirse dikkate alınmaz. Finance and Operations'taki bir satış satırından gelen tam iskonto tutarının Sales'a doğru şekilde eşitlenmesini sağlamak için, tam tutarın satır miktarına bölünmeden eşitlenmesi gerekir. Bu nedenle, Sales'ta **İskonto hesaplama yöntemi**'ni **Satır maddesi** olarak tanımlamanız gerekir.

Bir satış siparişi satırı Sales'tan Finance and Operations'a eşitlendiğinde tam satır iskontosu tutarı kullanılır. Finance and Operations'da bir satır için tam iskonto tutarının saklanabileceği bir alan bulunmadığından tutar miktara bölünür ve **Satır iskontosu** alanında saklanır. Bu bölme işlemi sırasında gerçekleşen yuvarlamalar satış satırındaki **Satış masrafları** alanında saklanır.

### <a name="example"></a>Örnek

**Sales'tan Finance and Operations'a eşitleme**

- **Sales:** Miktar = 3, satır başına iskonto = 10,00 TL
- **Finance and Operations:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış masrafı =-0,01 TL 

**Finance and Operations'tan Sales'a eşitleme**

- **Finance and Operations:** Miktar = 3, satır iskonto tutarı = 3,33 TL, satış masrafı =-0,01 TL
- **Sales:** Miktar = 3, satır başına iskonto = (3 x 3,33 TL) + 0,01 TL = 10,00 TL

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yeni alanlar **Sipariş** varlığına eklenir ve sayfada görüntülenir:

- **Dışarıda Tutulan** – Sipariş Finance and Operations'tan geliyorsa bu seçeneği **Evet** olarak ayarlayın.
- **İşleme durumu** – Bu alan siparişin Finance and Operations'taki işleme durumunu gösterir. Aşağıdaki değerler kullanılabilir:

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

**Yalnızca Dışarıda Tutulan Ürünleri Var** ayarı, sipariş etkinleştirme sırasında satış siparişinin tümüyle dışarıda tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için kullanılır. Bir satış siparişi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta korunur. Bu ayar, Finance and Operations tarafından bilenmeyen ürünlere sahip satış siparişi satırlarını etkinleştirmemenizi ve eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.

Dışarıda tutulan siparişler için **Satış siparişi** sayfasındaki **Fatura Oluştur**, **Siparişi İptal Et**, **Yeniden hesapla**, **Ürünleri Al** ve **Arama Adresi** düğmeleri gizlenmiştir çünkü faturalar Finance and Operations içerisinde oluşturulacak ve Sales'a eşitlenecektir. Bu siparişler düzenlenemez çünkü satış siparişi bilgisi etkinleştirmeden sonra Finance and Operations'tan eşitlenecektir.

Satış siparişi durumu, Finance and Operations'tan gelen değişikliklerin Sales içerisinde satış siparişi içine aktığından emin olunması için **Etkin** kalacaktır. Bu davranışı kontrol etmek için, varsayılan **Statecode\[Durum\]** değerini Veri tümleştirme projesinde **Etkin** olarak ayarlayın.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış siparişlerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun. Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir. Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.

    **Ayarlar** &gt; **Güvenlik** &gt; **Ekipler**'e gidin, ilgili ekibi seçin, **Rolleri Yönet**'i ve istenilen izinlere sahip bir rolü seçin; örn. **Sistem Yöneticisi**.

- **Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:

    - **Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.
    - **İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.

### <a name="setup-in-finance-and-operations"></a>Finance and Operations'ta kurulum

- **Satış ve pazarlama** &gt; **Periyodik görevler** &gt; **Satış toplamlarını hesapla**'ya gidin ve işi bir toplu iş olarak çalışacak şekilde ayarlayın. **Satış siparişleri için toplamları hesapla** seçeneğini **Evet** olarak ayarlayın. Bu adım önemlidir çünkü yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir. Toplu işin sıklığı, satış siparişi eşitlemesinin sıklığı ile uyumlu olmalıdır.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Satış Siparişlerinde Ayarlama (Sales'tan Fin and Ops'a) - Doğrudan Veri tümleştirme projesi

- **Shipto\_country** ile **DeliveryAddressCountryRegionISOCode** arasında gerekli eşleştirmenin mevcut olduğundan emin olun. Ulusal siparişler için ülke girmemek için değer eşlemesinde varsayılan değeri boş olarak ayarlayabilirsiniz. Sol tarafı 'Boş' bırakın ve sağ tarafı istenen ülkeye veya bölgeye ayarlayın.

    Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir; burada 'Boş' = ABD.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Satış Siparişlerinde Ayarlama (Fin and Ops'tan Sales'a) - Doğrudan Veri tümleştirme projesi

#### <a name="salesheader-task"></a>SalesHeader görevi

- Sales'ta siparişler oluşturmak için bir fiyat listesi gereklidir. **pricelevelid.name \[Fiyat Listesi Adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin. Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz. Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.

    **pricelevelid.name \[Fiyat Listesi Adı\]** için varsayılan şablon değeri **CRM Hizmeti ABD (örnek)**'dir.

#### <a name="salesline-task"></a>SalesLine görevi

- Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.
- Gerekli birimlerin Sales'ta tanımlandığından emin olun.

    Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **oumid.name** olarak tanımlanır.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a veya Finance and Operations'tan Sales'a eşitleneceğini gösterir.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Satış Siparişleri (Fin and Ops'tan Sales'a) - Doğrudan: OrderHeader

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Satış Siparişleri (Fin and Ops'tan Sales'a) - Doğrudan: OrderLine

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Satış Siparişleri (Sales'tan Fin and Ops'a) - Doğrudan: OrderHeader

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Satış Siparişleri (Sales'tan Fin and Ops'a) - Doğrudan: OrderLine

[![Veri tümleştirmede şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)

