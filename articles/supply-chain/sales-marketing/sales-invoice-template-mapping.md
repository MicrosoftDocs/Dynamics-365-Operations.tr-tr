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
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6db68236f512cc720e75c0d576ce4c49d6c87882
ms.contentlocale: tr-tr
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="151cf-103">Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="151cf-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="151cf-104">Bu konu, satış faturası başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="151cf-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="151cf-105">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="151cf-105">Templates and tasks</span></span>

<span data-ttu-id="151cf-106">Aşağıdaki şablonlar ve altta yatan görevler, satış faturası başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="151cf-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="151cf-107">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="151cf-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="151cf-108">Satış Faturaları (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="151cf-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="151cf-109">**Veri tümleştirme projesindeki görevlerin adları**</span><span class="sxs-lookup"><span data-stu-id="151cf-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="151cf-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="151cf-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="151cf-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="151cf-111">SalesInvoiceLine</span></span>

<span data-ttu-id="151cf-112">Satış faturası başlığı ve satırları eşitlemesinden önce gerekli eşitleme görevleri:</span><span class="sxs-lookup"><span data-stu-id="151cf-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="151cf-113">Ürünler (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="151cf-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="151cf-114">Hesaplar (Sales'tan Fin and Ops'a) (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="151cf-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="151cf-115">İlgili Kişiler (Sales'tan Fin and Ops'a) (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="151cf-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="151cf-116">Satış siparişi başlıkları ve satırları (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="151cf-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="151cf-117">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="151cf-117">Entity set</span></span>

| <span data-ttu-id="151cf-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="151cf-118">Finance and Operations</span></span>                               | <span data-ttu-id="151cf-119">Ortak Veri Servisi (CDS)</span><span class="sxs-lookup"><span data-stu-id="151cf-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="151cf-120">Satış</span><span class="sxs-lookup"><span data-stu-id="151cf-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="151cf-121">Harici olarak korunan müşteri satış faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="151cf-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="151cf-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="151cf-122">SalesInvoice</span></span>     | <span data-ttu-id="151cf-123">Faturalar</span><span class="sxs-lookup"><span data-stu-id="151cf-123">Invoices</span></span>       |
| <span data-ttu-id="151cf-124">Harici olarak korunan müşteri satış faturası satırları</span><span class="sxs-lookup"><span data-stu-id="151cf-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="151cf-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="151cf-125">SalesInvoiceLine</span></span> | <span data-ttu-id="151cf-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="151cf-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="151cf-127">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="151cf-127">Entity flow</span></span>

<span data-ttu-id="151cf-128">Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış faturaları.</span><span class="sxs-lookup"><span data-stu-id="151cf-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="151cf-129">**Satış faturası başlığı** üzerindeki masraflarla ilişkili vergiler, şu anda Finance and Operations'tan Sales'a eşitlemeye dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="151cf-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="151cf-130">Bu, Sales vergi bilgisini başlık düzeyinde desteklemediği içindir.</span><span class="sxs-lookup"><span data-stu-id="151cf-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="151cf-131">Satır düzeyi giderleri ile ilgili vergiler dahildir.</span><span class="sxs-lookup"><span data-stu-id="151cf-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="151cf-132">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="151cf-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="151cf-133">Bir **Fatura numarası alanı** **Fatura** varlığına eklenir ve sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="151cf-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="151cf-134">**Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Finance and Operations'ta oluşturulacak ve Sales'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="151cf-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="151cf-135">**Fatura** sayfası düzenlenemez çünkü faturalar Finance and Operations'tan eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="151cf-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="151cf-136">**Satış siparişi durumu**, ilgili fatura Finance and Operations'tan Sales'a eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="151cf-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="151cf-137">Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="151cf-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="151cf-138">Bu, satış siparişinin sahibine faturayı görüntüleme olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="151cf-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="151cf-139">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="151cf-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="151cf-140">Satış faturalarını eşitlemeden önce, sistemleri aşağıdaki ayarla güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="151cf-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="151cf-141">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="151cf-141">Setup in Sales</span></span>

- <span data-ttu-id="151cf-142">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **Sistem fiyatlama hesaplama sistemini kullan**'ın **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="151cf-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="151cf-143">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **İndirim hesaplama yöntemi**'nin **Satır maddesi** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="151cf-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="151cf-144">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="151cf-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="151cf-145">SalesInvoiceHeader görevi</span><span class="sxs-lookup"><span data-stu-id="151cf-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="151cf-146">**Kaynak** > **CDS** içerisinde **CDS Kuruluş Kodu** eşleşmeyi güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="151cf-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="151cf-147">**SalesOrder_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="151cf-148">**Account_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="151cf-149">**Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="151cf-150">Gerekli eşleşmenin **Kaynak** > **InvoiceCountryRegionId için CDS** üzerinden **BillingAddress_Country** üzerine için mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="151cf-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="151cf-151">Şablon değeri, eşlenmiş ülkelerin sayısı ile **ValueMap**'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="151cf-152">**Fiyat listesi** Sales içerisinde faturalar oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="151cf-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="151cf-153">**ValueMap**'i **CDS** > **pricelevelid.name [Fiyat Listesi Adı] için Hedef** için **Fiyat listesi**'ne, Sales'ta para birimi başına kullanılmak üzere güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="151cf-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="151cf-154">İster varsayılan **Fiyat listesi**'ni tek bir para birimi için kullanabilir veya birden fazla para biriminde **Fiyat listeleri** mevcutsa **ValueMap** kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="151cf-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="151cf-155">**pricelevelid.name [Fiyat Listesi Adı]** için şablon değeri **Para birimine** dayalı olarak **ValueMap**'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="151cf-156">usd: CRM Service USA (örnek).</span><span class="sxs-lookup"><span data-stu-id="151cf-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="151cf-157">SalesInvoiceLine görevi</span><span class="sxs-lookup"><span data-stu-id="151cf-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="151cf-158">Gerekli eşleşmenin **Kaynak** > **Ölçü birimi için CDS** içinde mevcut olduğundan emi olun.</span><span class="sxs-lookup"><span data-stu-id="151cf-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="151cf-159">Finance and Operations içerisinde **SalesUnitSymbol** için gereken **ValueMap**'in **Kaynak** > **CDS eşleme** içinde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="151cf-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="151cf-160">**ValueMap** ile şablon değeri **SalesUnitSymbol to Quantity_UOM** için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="151cf-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="151cf-161">**Kaynakta CDS Kuruluş Kodu** > **CDS** için eşleşmeyi güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="151cf-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="151cf-162">**SalesInvoicer_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="151cf-163">**Product_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.</span><span class="sxs-lookup"><span data-stu-id="151cf-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="151cf-164">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="151cf-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="151cf-165">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** varsayılan eşlemelerin parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="151cf-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="151cf-166">Bu alanların eşlenmesi, değer eşlenmesinin kurulmuş olmasını gerektirir; bu, varlığın eşitleneceği kuruluşlardaki veriye özeldir.</span><span class="sxs-lookup"><span data-stu-id="151cf-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="151cf-167">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="151cf-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="151cf-172">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="151cf-172">Related topics</span></span>

[<span data-ttu-id="151cf-173">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="151cf-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="151cf-174">Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="151cf-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="151cf-175">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="151cf-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="151cf-176">Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="151cf-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="151cf-177">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="151cf-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


