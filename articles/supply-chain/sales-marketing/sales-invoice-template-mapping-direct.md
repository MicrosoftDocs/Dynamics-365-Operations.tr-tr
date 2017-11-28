---
title: "Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme"
description: "Bu konu, satış faturası başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e9d7e756c56932372ed931620016973c794fb3fc
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, satış faturası başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir. Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve altta yatan görevler, satış faturası başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Satış Faturaları (Fin and Ops'dan Sales'e) - Doğrudan
- **Veri tümleştirme projesindeki görevlerin adları:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Fin and Ops'tan Sales'a) - Doğrudan
- Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)
- İlgili kişiler (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)
- Satış siparişi başlığı ve satırları (Fin and Ops'tan Sales'a) - Doğrudan

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations                               | Satış          |
|------------------------------------------------------|----------------|
| Harici olarak korunan müşteri satış faturası başlıkları | Faturalar       |
| Harici olarak korunan müşteri satış faturası satırları   | InvoiceDetails |

## <a name="entity-flow"></a>Varlık akışı

Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış faturaları.

> [!NOTE]
> Şu anda, satış faturası başlığı üzerindeki masraflarla ilişkili vergiler, Finance and Operations'tan Sales'a eşitlemeye dahil değildir. Sales vergi bilgisini başlık düzeyinde desteklemez. Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

- Bir **Fatura numarası** alanı **Fatura** varlığına eklenmiştir ve sayfada görüntülenir.
- **Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Finance and Operations'ta oluşturulacak ve Sales'a eşitlenecektir. **Fatura** sayfası düzenlenemez çünkü faturalar Finance and Operations'tan eşitlenecektir.
- **Satış siparişi durumu** değeri ilgili fatura Finance and Operations'tan Sales'a eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir. Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır. Bu nedenle, satış siparişinin sahibi faturayı görebilir.

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

- Fiyat listesi Sales içerisinde faturalar oluşturmak için gereklidir. **pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin.  Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz. Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.

    **pricelevelid.name \[Fiyat listesi adı\]** için şablon değeri USD = CRM Hizmeti ABD (örnek) ile para birimini temel alan bir değer eşlemesidir.  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine görevi

- **Ölçüm birimi** için gerekli eşlemenin mevcut olduğundan emin olun.
- Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.

    Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)

[Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme](products-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-order-template-mapping-direct.md)







