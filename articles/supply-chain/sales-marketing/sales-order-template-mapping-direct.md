---
title: "Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme"
description: "Bu konu, satış siparişi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, satış siparişi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir. Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve altta yatan görevler, satış siparişi başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Satış Siparişleri (Fin and Ops'dan Sales'e) - Doğrudan
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

Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış siparişleri.

Şablondaki filtreler yalnızca ilgili satış siparişlerinin eşitlemeye dahil edilmesini sağlar:

- Satış siparişinde, siparişi veren müşteri ile faturalanan müşteri Sales'tan geliyorsa, eşitlemeye dahil edilir. Finance and Operations'da **OrderingCustomerIsExternallyMaintained** ve **InvoiceCustomerIsExternallyMaintained** alanları, veri varlıkları içindeki eşitlemeyi izlemek için kullanılır.
- Finance and Operations içindeki satış siparişinin onaylanması gerekir. Yalnızca onaylanmış satış siparişleri veya daha yüksek işleme durumuna sahip satış siparişler (örneğin **Sevk edildi** veya **Faturalandı** durumları) Sales'a eşitlenir.
- Bir satış siparişi oluşturulduktan veya değiştirildikten sonra, Finance and Operations'da **Satış toplamlarını hesapla** toplu işinin çalıştırılması gerekir. Yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir.

> [!NOTE]
> Şu anda, satış faturası siparişi üzerindeki masraflarla ilişkili vergiler, Finance and Operations'tan Sales'a eşitlemeye dahil değildir. Sales vergi bilgisini başlık düzeyinde desteklemez. Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yeni alanlar **Sipariş** varlığına eklenir ve sayfada görüntülenir:

- **Dışarıda Tutulan** – Sipariş Finance and Operations'tan geliyorsa bu seçeneği **Evet** olarak ayarlayın.
- **İşleme durumu** – Bu alan siparişin Finance and Operations'taki işleme durumunu gösterir. Aşağıdaki değerler kullanılabilir:

    - Etkin
    - Onaylandı
    - Sevk İrsaliyesi
    - Faturalanan
    - Malzeme çekildi
    - Kısmen Çekildi
    - Kısmen Paketlendi
    - Sevk Edildi
    - Kısmen Sevk Edildi
    - Kısmen Faturalandı
    - İptal edildi

Yalnızca **Dışarıda Tutulan Ürünlere Sahip** ayarı, diğer satış siparişi senaryolarında (örneğin Sales'tan Finance and Operations'a eşitleme), satış siparişinin tümüyle dışarıda tutulan ürünlerden mi oluştuğunu izlemek için kullanılır. Bir satış siparişi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta korunur. Bu ayar, Finance and Operations tarafından bilenmeyen ürünlere sahip satış siparişi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.

Dışarıda tutulan siparişler için **Satış siparişi** sayfasındaki **Fatura Oluştur**, **Siparişi İptal Et**, **Yeniden hesapla**, **Ürünleri Al** ve **Arama Adresi** düğmeleri gizlenmiştir çünkü faturalar Finance and Operations içerisinde oluşturulacak ve Sales'a eşitlenecektir. Sipariş sayfası düzenlenemez çünkü satış siparişi bilgisi Finance and Operations'tan eşitlenecektir.

Satış siparişi durumu, Finance and Operations'tan gelen değişikliklerin Sales içerisinde satış siparişi içine aktığından emin olunması için **Etkin** kalacaktır. Bu davranışı kontrol etmek için, varsayılan **Statecode\[Durum\]** değerini Veri tümleştirme projesinde **Etkin** olarak ayarlayın.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış siparişlerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun. Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir. Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine de sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.

    **Ayarlar** > **Güvenlik** > **Ekipler**'e gidin, ilgili ekibi seçin, **Rolleri Yönet**'i ve istenilen izinlere sahip bir rolü seçin; örn. **Sistem Yöneticisi**.

- **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:

    - **Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.
    - **İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.

### <a name="setup-in-finance-and-operations"></a>Finance and Operations'ta kurulum

**Satış ve pazarlama** > **Periyodik görevler** > **Satış toplamlarını hesapla**'ya gidin ve işi bir toplu iş olarak çalışacak şekilde ayarlayın. **Satış siparişleri için toplamları hesapla** seçeneğini **Evet** olarak ayarlayın. Bu adım önemlidir çünkü yalnızca satış toplamlarının hesaplandığı satış siparişleri Sales'a eşitlenir. Toplu işin sıklığı, satış siparişi eşitlemesinin sıklığı ile uyumlu olmalıdır.

### <a name="setup-in-the-data-integration-project"></a>Veri tümleştirme projesinde kurulum

#### <a name="salesheader-task"></a>SalesHeader görevi

- Gerekli eşleşmenin **InvoiceCountryRegionId** ile **BillingAddress\_Country** arasında ve **DeliveryCountryRegionId** ile **DeliveryAddress\_Country** arasında mevcut olduğundan emin olun.

    Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.

- Sales'ta siparişler oluşturmak için bir fiyat listesi gereklidir. **pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin.  Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz. Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.

    **pricelevelid.name \[Fiyat listesi adı\]** için varsayılan şablon değeri **CRM Hizmeti ABD (örnek)**'dir.

#### <a name="salesline-task"></a>SalesLine görevi

- **DeliveryCountryRegionId** ile **DeliveryAddress\_Country** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.

    Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.

- Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.

    Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.

### <a name="orderheader"></a>OrderHeader

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)

[Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme](products-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)




