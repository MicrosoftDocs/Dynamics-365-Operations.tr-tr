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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 347509a9556f15e7d880508e36516f04bc6964b7
ms.contentlocale: tr-tr
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="563d8-103">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="563d8-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="563d8-104">Bu konu, satış faturası başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="563d8-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="563d8-105">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="563d8-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="563d8-106">Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="563d8-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="563d8-107">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="563d8-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="563d8-108">Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="563d8-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="563d8-109">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="563d8-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="563d8-110">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="563d8-110">Templates and tasks</span></span>

<span data-ttu-id="563d8-111">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="563d8-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="563d8-112">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="563d8-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="563d8-113">Aşağıdaki şablon ve altta yatan görevler, satış faturası başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="563d8-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="563d8-114">**Veri tümleştirmedeki şablonun adı:** Satış Faturaları (Fin and Ops'dan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="563d8-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="563d8-115">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="563d8-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="563d8-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="563d8-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="563d8-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="563d8-117">SalesInvoiceLine</span></span>

<span data-ttu-id="563d8-118">Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="563d8-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="563d8-119">Ürünler (Fin and Ops'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="563d8-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="563d8-120">Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="563d8-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="563d8-121">İlgili kişiler (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="563d8-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="563d8-122">Satış siparişi başlığı ve satırları (Fin and Ops'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="563d8-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="563d8-123">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="563d8-123">Entity set</span></span>

| <span data-ttu-id="563d8-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="563d8-124">Finance and Operations</span></span>                               | <span data-ttu-id="563d8-125">Satış</span><span class="sxs-lookup"><span data-stu-id="563d8-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="563d8-126">Harici olarak korunan müşteri satış faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="563d8-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="563d8-127">Faturalar</span><span class="sxs-lookup"><span data-stu-id="563d8-127">Invoices</span></span>       |
| <span data-ttu-id="563d8-128">Harici olarak korunan müşteri satış faturası satırları</span><span class="sxs-lookup"><span data-stu-id="563d8-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="563d8-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="563d8-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="563d8-130">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="563d8-130">Entity flow</span></span>

<span data-ttu-id="563d8-131">Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış faturaları.</span><span class="sxs-lookup"><span data-stu-id="563d8-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="563d8-132">Şu anda, satış faturası başlığı üzerindeki masraflarla ilişkili vergiler, Finance and Operations'tan Sales'a eşitlemeye dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="563d8-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="563d8-133">Sales vergi bilgisini başlık düzeyinde desteklemez.</span><span class="sxs-lookup"><span data-stu-id="563d8-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="563d8-134">Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="563d8-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="563d8-135">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="563d8-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="563d8-136">Bir **Fatura numarası** alanı **Fatura** varlığına eklenmiştir ve sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="563d8-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="563d8-137">**Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Finance and Operations'ta oluşturulacak ve Sales'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="563d8-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="563d8-138">**Fatura** sayfası düzenlenemez çünkü faturalar Finance and Operations'tan eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="563d8-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="563d8-139">**Satış siparişi durumu** değeri ilgili fatura Finance and Operations'tan Sales'a eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="563d8-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="563d8-140">Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="563d8-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="563d8-141">Bu nedenle, satış siparişinin sahibi faturayı görebilir.</span><span class="sxs-lookup"><span data-stu-id="563d8-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="563d8-142">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="563d8-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="563d8-143">Satış faturalarını eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="563d8-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="563d8-144">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="563d8-144">Setup in Sales</span></span>

<span data-ttu-id="563d8-145">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="563d8-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="563d8-146">**Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="563d8-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="563d8-147">**İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="563d8-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="563d8-148">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="563d8-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="563d8-149">SalesInvoiceHeader görevi</span><span class="sxs-lookup"><span data-stu-id="563d8-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="563d8-150">**InvoiceCountryRegionId** ile **BillingAddress\_Country** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="563d8-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="563d8-151">Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="563d8-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="563d8-152">Fiyat listesi Sales içerisinde faturalar oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="563d8-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="563d8-153">**pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin. </span><span class="sxs-lookup"><span data-stu-id="563d8-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="563d8-154">Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="563d8-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="563d8-155">Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="563d8-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="563d8-156">**pricelevelid.name \[Fiyat listesi adı\]** için şablon değeri USD = CRM Hizmeti ABD (örnek) ile para birimini temel alan bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="563d8-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="563d8-157">SalesInvoiceLine görevi</span><span class="sxs-lookup"><span data-stu-id="563d8-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="563d8-158">**Ölçüm birimi** için gerekli eşlemenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="563d8-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="563d8-159">Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="563d8-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="563d8-160">Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="563d8-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="563d8-161">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="563d8-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="563d8-162">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="563d8-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="563d8-163">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="563d8-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="563d8-164">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="563d8-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="563d8-165">Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="563d8-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="563d8-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="563d8-166">SalesInvoiceHeader</span></span>

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="563d8-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="563d8-168">SalesInvoiceLine</span></span>

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="563d8-170">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="563d8-170">Related topics</span></span>

[<span data-ttu-id="563d8-171">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="563d8-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="563d8-172">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="563d8-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="563d8-173">Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="563d8-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="563d8-174">Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="563d8-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="563d8-175">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="563d8-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







