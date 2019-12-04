---
title: Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme
description: Bu konu, satış faturası başlıklarını ve satırlarını Dynamics 365 Supply Chain Management'tan Dynamics 365 Sales'e eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fb5073fe8db0b51c4ea378cac57097e15e88bf83
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814064"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="5692d-103">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="5692d-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5692d-104">Bu konu, satış faturası başlıklarını ve satırlarını Dynamics 365 Supply Chain Management'tan Dynamics 365 Sales'e eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5692d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5692d-105">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="5692d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5692d-106">Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5692d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="5692d-107">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="5692d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5692d-108">Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5692d-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5692d-109">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5692d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5692d-110">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="5692d-110">Templates and tasks</span></span>

<span data-ttu-id="5692d-111">Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="5692d-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5692d-112">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5692d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5692d-113">Aşağıdaki şablon ve temel görevler, fatura başlıklarını ve satırlarını 'Supply Chain Management'tan Sales'e doğrudan eşitlemede kullanılır:</span><span class="sxs-lookup"><span data-stu-id="5692d-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="5692d-114">**Veri tümleştirmedeki şablonun adı:** Satış Faturaları (Fin and Ops'dan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5692d-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5692d-115">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="5692d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="5692d-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="5692d-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="5692d-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="5692d-117">SalesInvoiceLine</span></span>

<span data-ttu-id="5692d-118">Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5692d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="5692d-119">Ürünler (Supply Chain Management'tan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5692d-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="5692d-120">Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="5692d-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="5692d-121">İlgili Kişiler (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="5692d-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="5692d-122">Satış siparişi başlığı ve satırları (Supply Chain Management'tan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5692d-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="5692d-123">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="5692d-123">Entity set</span></span>

| <span data-ttu-id="5692d-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5692d-124">Supply Chain Management</span></span>                              | <span data-ttu-id="5692d-125">Satışlar</span><span class="sxs-lookup"><span data-stu-id="5692d-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="5692d-126">Harici olarak korunan müşteri satış faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="5692d-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="5692d-127">Faturalar</span><span class="sxs-lookup"><span data-stu-id="5692d-127">Invoices</span></span>       |
| <span data-ttu-id="5692d-128">Harici olarak korunan müşteri satış faturası satırları</span><span class="sxs-lookup"><span data-stu-id="5692d-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="5692d-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="5692d-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5692d-130">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="5692d-130">Entity flow</span></span>

<span data-ttu-id="5692d-131">Satış faturaları Supply Chain Management'ta oluşturulur ve Sales'e eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="5692d-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="5692d-132">Şu anda, satış faturası başlığı üzerindeki masraflarla ilişkili vergiler, Supply Chain Management'tan Sales'e eşitlemeye dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="5692d-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="5692d-133">Sales vergi bilgisini başlık düzeyinde desteklemez.</span><span class="sxs-lookup"><span data-stu-id="5692d-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="5692d-134">Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="5692d-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5692d-135">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="5692d-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="5692d-136">Bir **Fatura numarası** alanı **Fatura** varlığına eklenmiştir ve sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5692d-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="5692d-137">**Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Supply Chain Management'ta oluşturulacak ve Sales'e eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="5692d-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="5692d-138">**Fatura** sayfası düzenlenemez çünkü faturalar Supply Chain Management'tan eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="5692d-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="5692d-139">**Satış siparişi durumu** değeri ilgili fatura Supply Chain Management'tan Sales'e eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="5692d-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="5692d-140">Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="5692d-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="5692d-141">Bu nedenle, satış siparişinin sahibi faturayı görebilir.</span><span class="sxs-lookup"><span data-stu-id="5692d-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5692d-142">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="5692d-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="5692d-143">Satış faturalarını eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="5692d-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5692d-144">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="5692d-144">Setup in Sales</span></span>

<span data-ttu-id="5692d-145">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="5692d-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="5692d-146">**Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5692d-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="5692d-147">**İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5692d-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5692d-148">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="5692d-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="5692d-149">SalesInvoiceHeader görevi</span><span class="sxs-lookup"><span data-stu-id="5692d-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="5692d-150">**InvoiceCountryRegionId** ile **BillingAddress\_Country** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5692d-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="5692d-151">Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="5692d-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="5692d-152">Fiyat listesi Sales içerisinde faturalar oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5692d-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="5692d-153">**pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5692d-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="5692d-154">Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5692d-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="5692d-155">Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5692d-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="5692d-156">**pricelevelid.name \[Fiyat listesi adı\]** için şablon değeri USD = CRM Hizmeti ABD (örnek) ile para birimini temel alan bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="5692d-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="5692d-157">SalesInvoiceLine görevi</span><span class="sxs-lookup"><span data-stu-id="5692d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="5692d-158">**Ölçüm birimi** için gerekli eşlemenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5692d-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="5692d-159">Supply Chain Management'ta **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5692d-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="5692d-160">Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="5692d-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5692d-161">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="5692d-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="5692d-162">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="5692d-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="5692d-163">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5692d-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5692d-164">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5692d-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5692d-165">Eşleme hangi alan bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5692d-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="5692d-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="5692d-166">SalesInvoiceHeader</span></span>

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="5692d-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="5692d-168">SalesInvoiceLine</span></span>

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="5692d-170">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="5692d-170">Related topics</span></span>

[<span data-ttu-id="5692d-171">Aday müşteriden nakde</span><span class="sxs-lookup"><span data-stu-id="5692d-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5692d-172">Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5692d-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5692d-173">Supply Chain Management'daki ürünleri doğrudan Sales'deki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5692d-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="5692d-174">Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5692d-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5692d-175">Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="5692d-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
