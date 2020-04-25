---
title: Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme
description: Bu konu, satış faturası başlıklarını ve satırlarını Dynamics 365 Supply Chain Management'tan Dynamics 365 Sales'e eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215988"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Finance and Operations'taki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme

[!include [banner](../includes/banner.md)]

Bu konu, satış faturası başlıklarını ve satırlarını Dynamics 365 Supply Chain Management'tan Dynamics 365 Sales'e eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir. Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve temel görevler, fatura başlıklarını ve satırlarını 'Supply Chain Management'tan Sales'e doğrudan eşitlemede kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Satış Faturaları (Fin and Ops'dan Sales'e) - Doğrudan
- **Veri tümleştirme projesindeki görevlerin adları:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Supply Chain Management'tan Sales'e) - Doğrudan
- Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)
- İlgili Kişiler (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)
- Satış siparişi başlığı ve satırları (Supply Chain Management'tan Sales'e) - Doğrudan

## <a name="entity-set"></a>Varlık kümesi

| Supply Chain Management                              | Satışlar          |
|------------------------------------------------------|----------------|
| Harici olarak korunan müşteri satış faturası başlıkları | Faturalar       |
| Harici olarak korunan müşteri satış faturası satırları   | InvoiceDetails |

## <a name="entity-flow"></a>Varlık akışı

Satış faturaları Supply Chain Management'ta oluşturulur ve Sales'e eşitlenir.

> [!NOTE]
> Şu anda, satış faturası başlığı üzerindeki masraflarla ilişkili vergiler, Supply Chain Management'tan Sales'e eşitlemeye dahil değildir. Sales vergi bilgisini başlık düzeyinde desteklemez. Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

- Bir **Fatura numarası** alanı **Fatura** varlığına eklenmiştir ve sayfada görüntülenir.
- **Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Supply Chain Management'ta oluşturulacak ve Sales'e eşitlenecektir. **Fatura** sayfası düzenlenemez çünkü faturalar Supply Chain Management'tan eşitlenecektir.
- **Satış siparişi durumu** değeri ilgili fatura Supply Chain Management'tan Sales'e eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir. Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır. Bu nedenle, satış siparişinin sahibi faturayı görebilir.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış faturalarını eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:

- **Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.
- **İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.

### <a name="setup-in-the-data-integration-project"></a>Veri tümleştirme projesinde kurulum

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader görevi

- **InvoiceCountryRegionId** ile **BillingAddress\_Country** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.

    Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.

- Fiyat listesi Sales içerisinde faturalar oluşturmak için gereklidir. **pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin. Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz. Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.

    **pricelevelid.name \[Fiyat listesi adı\]** için şablon değeri USD = CRM Hizmeti ABD (örnek) ile para birimini temel alan bir değer eşlemesidir.  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine görevi

- **Ölçüm birimi** için gerekli eşlemenin mevcut olduğundan emin olun.
- Supply Chain Management'ta **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.

    Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>İlgili konular

[Aday müşteriden nakde](prospect-to-cash.md)

[Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Supply Chain Management'daki ürünleri doğrudan Sales'deki ürünlerle eşitleme](products-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)
