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

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="5e9c2-103">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="5e9c2-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5e9c2-104">Bu konu, satış faturası başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için temel görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5e9c2-105">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="5e9c2-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5e9c2-106">Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="5e9c2-107">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="5e9c2-108">Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="5e9c2-109">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5e9c2-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5e9c2-110">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="5e9c2-110">Templates and tasks</span></span>

<span data-ttu-id="5e9c2-111">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5e9c2-112">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5e9c2-113">Aşağıdaki şablon ve altta yatan görevler, satış faturası başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="5e9c2-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="5e9c2-114">**Veri tümleştirmedeki şablonun adı:** Satış Faturaları (Fin and Ops'dan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5e9c2-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5e9c2-115">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="5e9c2-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="5e9c2-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="5e9c2-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="5e9c2-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="5e9c2-117">SalesInvoiceLine</span></span>

<span data-ttu-id="5e9c2-118">Aşağıdaki eşitleme görevleri, satış faturası başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="5e9c2-119">Ürünler (Fin and Ops'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5e9c2-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5e9c2-120">Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="5e9c2-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="5e9c2-121">İlgili kişiler (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)</span><span class="sxs-lookup"><span data-stu-id="5e9c2-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="5e9c2-122">Satış siparişi başlığı ve satırları (Fin and Ops'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5e9c2-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="5e9c2-123">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="5e9c2-123">Entity set</span></span>

| <span data-ttu-id="5e9c2-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5e9c2-124">Finance and Operations</span></span>                               | <span data-ttu-id="5e9c2-125">Satış</span><span class="sxs-lookup"><span data-stu-id="5e9c2-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="5e9c2-126">Harici olarak korunan müşteri satış faturası başlıkları</span><span class="sxs-lookup"><span data-stu-id="5e9c2-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="5e9c2-127">Faturalar</span><span class="sxs-lookup"><span data-stu-id="5e9c2-127">Invoices</span></span>       |
| <span data-ttu-id="5e9c2-128">Harici olarak korunan müşteri satış faturası satırları</span><span class="sxs-lookup"><span data-stu-id="5e9c2-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="5e9c2-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="5e9c2-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5e9c2-130">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="5e9c2-130">Entity flow</span></span>

<span data-ttu-id="5e9c2-131">Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış faturaları.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="5e9c2-132">Şu anda, satış faturası başlığı üzerindeki masraflarla ilişkili vergiler, Finance and Operations'tan Sales'a eşitlemeye dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="5e9c2-133">Sales vergi bilgisini başlık düzeyinde desteklemez.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="5e9c2-134">Bununla birlikte, satır düzeyinde masraflarla ilgili vergi eşitlemeye dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5e9c2-135">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="5e9c2-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="5e9c2-136">Bir **Fatura numarası** alanı **Fatura** varlığına eklenmiştir ve sayfada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="5e9c2-137">**Satış siparişi** sayfasındaki **Fatura oluştur** düğmesi gizlidir çünkü faturalar Finance and Operations'ta oluşturulacak ve Sales'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="5e9c2-138">**Fatura** sayfası düzenlenemez çünkü faturalar Finance and Operations'tan eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="5e9c2-139">**Satış siparişi durumu** değeri ilgili fatura Finance and Operations'tan Sales'a eşitlendiğinde otomatik olarak **Faturalandı** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="5e9c2-140">Ayrıca, faturanın oluşturulduğu satış siparişinin sahibi, faturanın sahibi olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="5e9c2-141">Bu nedenle, satış siparişinin sahibi faturayı görebilir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5e9c2-142">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="5e9c2-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="5e9c2-143">Satış faturalarını eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:</span><span class="sxs-lookup"><span data-stu-id="5e9c2-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5e9c2-144">Sales içinde kurulum</span><span class="sxs-lookup"><span data-stu-id="5e9c2-144">Setup in Sales</span></span>

<span data-ttu-id="5e9c2-145">**Ayarlar** > **Yönetim** > **Sistem ayarları** > **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="5e9c2-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="5e9c2-146">**Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="5e9c2-147">**İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5e9c2-148">Veri tümleştirme projesinde kurulum</span><span class="sxs-lookup"><span data-stu-id="5e9c2-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="5e9c2-149">SalesInvoiceHeader görevi</span><span class="sxs-lookup"><span data-stu-id="5e9c2-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="5e9c2-150">**InvoiceCountryRegionId** ile **BillingAddress\_Country** arasında gerekli eşleştirmenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="5e9c2-151">Şablon değeri, birçok ülkenin veya bölgenin eşleştirildiği bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="5e9c2-152">Fiyat listesi Sales içerisinde faturalar oluşturmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="5e9c2-153">**pricelevelid.name \[Fiyat listesi adı\]** için değer eşlemesini para birimi başına Sales'ta kullanılan fiyat listesine güncelleştirin. </span><span class="sxs-lookup"><span data-stu-id="5e9c2-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="5e9c2-154">Tek bir para birimi için varsayılan fiyat listesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="5e9c2-155">Bunun yerine, birden fazla para biriminde fiyat listeleriniz varsa, bir değer eşlemesi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="5e9c2-156">**pricelevelid.name \[Fiyat listesi adı\]** için şablon değeri USD = CRM Hizmeti ABD (örnek) ile para birimini temel alan bir değer eşlemesidir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="5e9c2-157">SalesInvoiceLine görevi</span><span class="sxs-lookup"><span data-stu-id="5e9c2-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="5e9c2-158">**Ölçüm birimi** için gerekli eşlemenin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="5e9c2-159">Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="5e9c2-160">Bir değer eşlemesi bulunan şablon değeri **SalesUnitSymbol** için **Quantity\_UOM** olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5e9c2-161">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="5e9c2-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="5e9c2-162">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="5e9c2-163">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5e9c2-164">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5e9c2-165">Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e9c2-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="5e9c2-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="5e9c2-166">SalesInvoiceHeader</span></span>

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="5e9c2-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="5e9c2-168">SalesInvoiceLine</span></span>

![Veri tümleştirmede şablon eşleme](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="5e9c2-170">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="5e9c2-170">Related topics</span></span>

[<span data-ttu-id="5e9c2-171">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="5e9c2-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5e9c2-172">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5e9c2-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5e9c2-173">Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5e9c2-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="5e9c2-174">Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5e9c2-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5e9c2-175">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="5e9c2-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)






