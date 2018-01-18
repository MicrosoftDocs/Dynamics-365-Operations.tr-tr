---
title: "Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme"
description: "Bu konu, satış faturası başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, satış faturası başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar. 

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Aşağıdaki şablonlar ve altta yatan görevler, satış faturası başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:

- **Veri tümleştirmesindeki şablonun adı** 

     - Satış Faturaları (Fin and Ops'tan Sales'a)

- **Veri tümleştirme projesindeki görevlerin adları**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Satış faturası başlığı ve satırları eşitlemesinden önce gerekli eşitleme görevleri:
-   Ürünler (Fin and Ops'tan Sales'a)
-   Hesaplar (Sales'tan Fin and Ops'a) (kullanılıyorsa)
-   İlgili Kişiler (Sales'tan Fin and Ops'a) (kullanılıyorsa)
-   Satış siparişi başlıkları ve satırları (Fin and Ops'tan Sales'a)

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations                               | Ortak Veri Servisi (CDS)              | Satış          |
|------------------------------------------------------|------------------|----------------|
| Harici olarak korunan müşteri satış faturası başlıkları | SalesInvoice     | Faturalar       |
| Harici olarak korunan müşteri satış faturası satırları   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Varlık akışı

Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış faturaları.

> [!NOTE]
> **Satış faturası başlığı** üzerindeki masraflarla ilişkili vergiler, şu anda Finance and Operations'tan Sales'a eşitlemeye dahil değildir. Bu, Sales vergi bilgisini başlık düzeyinde desteklemediği içindir. Satır düzeyi giderleri ile ilgili vergiler dahildir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

-  Bir **Fatura numarası alanı** **Fatura** varlığına eklenir ve sayfada görüntülenir.
 
-  **Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Finance and Operations'ta oluşturulacak ve Sales'a eşitlenecektir. **Fatura** sayfası düzenlenemez çünkü faturalar Finance and Operations'tan eşitlenecektir.
 
-  **Satış siparişi durumu**, ilgili fatura Finance and Operations'tan Sales'a eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir. Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır. Bu, satış siparişinin sahibine faturayı görüntüleme olanağı sağlar.
 
## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış faturalarını eşitlemeden önce, sistemleri aşağıdaki ayarla güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **Sistem fiyatlama hesaplama sistemini kullan**'ın **Evet** olarak ayarlandığından emin olun. 

- **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **İndirim hesaplama yöntemi**'nin **Satır maddesi** olarak ayarlandığından emin olun. 

### <a name="setup-in-the-data-integration-project"></a>Veri tümleştirme projesinde kurulum

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader görevi

- **Kaynak** > **CDS** içerisinde **CDS Kuruluş Kodu** eşleşmeyi güncelleştir. 

    -  **SalesOrder_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
    -  **Account_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
    -  **Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.

- Gerekli eşleşmenin **Kaynak** > **InvoiceCountryRegionId için CDS** üzerinden **BillingAddress_Country** üzerine için mevcut olduğundan emin olun.

    -  Şablon değeri, eşlenmiş ülkelerin sayısı ile **ValueMap**'dir.

- **Fiyat listesi** Sales içerisinde faturalar oluşturmak için gereklidir. **ValueMap**'i **CDS** > **pricelevelid.name [Fiyat Listesi Adı] için Hedef** için **Fiyat listesi**'ne, Sales'ta para birimi başına kullanılmak üzere güncelleştirin. İster varsayılan **Fiyat listesi**'ni tek bir para birimi için kullanabilir veya birden fazla para biriminde **Fiyat listeleri** mevcutsa **ValueMap** kullanabilirsiniz.

    -  **pricelevelid.name [Fiyat Listesi Adı]** için şablon değeri **Para birimine** dayalı olarak **ValueMap**'dir.
    -  usd: CRM Service USA (örnek). 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine görevi

- Gerekli eşleşmenin **Kaynak** > **Ölçü birimi için CDS** içinde mevcut olduğundan emi olun.

- Finance and Operations içerisinde **SalesUnitSymbol** için gereken **ValueMap**'in **Kaynak** > **CDS eşleme** içinde mevcut olduğundan emin olun. 
    
    - **ValueMap** ile şablon değeri **SalesUnitSymbol to Quantity_UOM** için tanımlanmıştır.
    
-  **Kaynakta CDS Kuruluş Kodu** > **CDS** için eşleşmeyi güncelleştir. 

    -  **SalesInvoicer_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
    -  **Product_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
 
## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** varsayılan eşlemelerin parçası değildir. Bu alanların eşlenmesi, değer eşlenmesinin kurulmuş olmasını gerektirir; bu, varlığın eşitleneceği kuruluşlardaki veriye özeldir.

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>İlgili konular

[Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme](products-template-mapping.md)

[Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping.md)

[Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping.md)

[Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme](sales-quotation-template-mapping.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme](sales-order-template-mapping.md)


