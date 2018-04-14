---
title: "Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme"
description: "Bu konu, ürünleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Sales'e eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 84366a26f69a651146648d4a9bdb139fc6d2cffe
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="82da7-103">Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="82da7-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="82da7-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="82da7-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="82da7-105">Bu konu, ürünleri doğrudan Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Sales'e eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="82da7-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="82da7-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="82da7-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="82da7-107">Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="82da7-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="82da7-108">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="82da7-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="82da7-109">Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="82da7-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="82da7-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="82da7-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="82da7-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="82da7-111">Templates and tasks</span></span>

<span data-ttu-id="82da7-112">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="82da7-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="82da7-113">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="82da7-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="82da7-114">Aşağıdaki şablon ve altta yatan görevler, ürünleri Finance and Operations'dan Sales'e eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="82da7-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="82da7-115">**Veri tümleştirmedeki şablonun adı:** Ürünler (Fin and Ops'dan Sales'e) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="82da7-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="82da7-116">**Veri tümleştirme projesindeki görevin adı:** Ürünler</span><span class="sxs-lookup"><span data-stu-id="82da7-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="82da7-117">Ürün eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="82da7-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="82da7-118">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="82da7-118">Entity set</span></span>

| <span data-ttu-id="82da7-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="82da7-119">Finance and Operations</span></span>     | <span data-ttu-id="82da7-120">Satış</span><span class="sxs-lookup"><span data-stu-id="82da7-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="82da7-121">Satış yapılabilir serbest bırakılan ürünler</span><span class="sxs-lookup"><span data-stu-id="82da7-121">Sellable released products</span></span> | <span data-ttu-id="82da7-122">Ürünler</span><span class="sxs-lookup"><span data-stu-id="82da7-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="82da7-123">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="82da7-123">Entity flow</span></span>

<span data-ttu-id="82da7-124">Ürünler Finance and Operations'ta yönetilir ve Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="82da7-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="82da7-125">Finance and Operations'da **Satış yapılabilir serbest bırakılan ürünler** veri varlığı yalnızca *satış yapılabilir* ürünleri dışa aktarır.</span><span class="sxs-lookup"><span data-stu-id="82da7-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="82da7-126">Satış yapılabilir ürünler, bir satış siparişinde kullanılmak üzere gerekli bilgilere sahip olan ürünlerdir.</span><span class="sxs-lookup"><span data-stu-id="82da7-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="82da7-127">Aynı kurallar, bir ürün **Serbest bırakılan ürün** sayfasında **Doğrula** işleviyle doğrulanıyorsa da geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="82da7-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="82da7-128">Ürün numarası anahtar olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="82da7-128">The product number is used as a key.</span></span> <span data-ttu-id="82da7-129">Bu nedenle, ürün çeşitleri Sales'e eşitlendiğinde her ürün çeşidinin ayrı bir ürün kimliği vardır.</span><span class="sxs-lookup"><span data-stu-id="82da7-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="82da7-130">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="82da7-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="82da7-131">Sales'ta ürünlere, ürünün dışarıda tutulduğunu belirten yeni bir **Dışarıda tutulan** alanı eklenir.</span><span class="sxs-lookup"><span data-stu-id="82da7-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="82da7-132">Varsayılan olarak değer Sales'a içe aktarma sırasında **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="82da7-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="82da7-133">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="82da7-133">The following values are available:</span></span>

- <span data-ttu-id="82da7-134">**Evet** – Ürün Finance and Operations'tan gelir ve Sales'ta düzenlenebilir olmaz.</span><span class="sxs-lookup"><span data-stu-id="82da7-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="82da7-135">**Hayır** – Ürün doğrudan Sales içinden girilmiştir.</span><span class="sxs-lookup"><span data-stu-id="82da7-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="82da7-136">**(Boş)** – Aday müşteriden nakde çözümü etkinleştirilmeden önce ürün Sales içinde vardır.</span><span class="sxs-lookup"><span data-stu-id="82da7-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="82da7-137">**Dışarıda Tutulan** alanı yalnızca dışarıda tutulan ürünleri bulunan tekliflerin ve satış siparişlerinin Finance and Operations ile eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="82da7-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="82da7-138">Dışarıda tutulan ürünler otomatik olarak aynı para birimine sahip ilk geçerli fiyat listesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="82da7-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="82da7-139">Fiyat listeleri ada göre alfabetik olarak düzenlenir.</span><span class="sxs-lookup"><span data-stu-id="82da7-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="82da7-140">Finance and Operations'taki ürün satış fiyatı, fiyat listesindeki fiyat olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="82da7-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="82da7-141">Bu nedenle, Sales içerisinde, Finance and Operations içindeki her bir ürün satış para birimi için bir fiyat listesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="82da7-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="82da7-142">Serbest bırakılmış satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="82da7-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="82da7-143">Eşleşen para birimine sahip bir fiyat listesi olmadığı sürece ürün eşitleme başarılı olmaz.</span><span class="sxs-lookup"><span data-stu-id="82da7-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="82da7-144">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="82da7-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="82da7-145">Eşitlemeyi ilk kez çalıştırmadan önce Farklı ürün tablosu'nu Finance and Operation içindeki mevcut ürünler için doldurmalısınız.</span><span class="sxs-lookup"><span data-stu-id="82da7-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="82da7-146">Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="82da7-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="82da7-147">Finance and Operations'ta, **Farklı ürün tablolarını doldur**'u aramak için Arama'yı kullanın.</span><span class="sxs-lookup"><span data-stu-id="82da7-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="82da7-148">İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="82da7-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="82da7-149">Bu işlemin yalnızca bir kez çalıştırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="82da7-149">This job must be run only one time.</span></span>

- <span data-ttu-id="82da7-150">Finance and Operations ile Sales arasındaki satış ölçü birimi (UOM) için gerekli değer eşlemesinin **SalesUnitSymbol** ile **DefaultUnit (Name)** eşlemesinde var olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="82da7-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="82da7-151">**Birim gurubu** (**defaultuomscheduleid.name**) için değer eşlemesini güncelleştirin, böylece bu eşleme Sales'deki **Birim grupları** ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="82da7-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="82da7-152">Varsayılan şablon değeri **Varsayılan birim**'dir.</span><span class="sxs-lookup"><span data-stu-id="82da7-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="82da7-153">Finance and Operations'daki tüm ürünlerin satış UOM'larının Sales'de mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="82da7-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="82da7-154">Fiyat listelerinin Sales içerisinde, Finance and Operations içindeki her bir ürün satış para birimi için mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="82da7-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="82da7-155">Sales'de ürünler oluşturulduğunda, durumları **Taslak** veya **Etkin** olabilir.</span><span class="sxs-lookup"><span data-stu-id="82da7-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="82da7-156">Davranış Sales'deki **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altından kontrol edilebilir.</span><span class="sxs-lookup"><span data-stu-id="82da7-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="82da7-157">**Taslak** durumuna sahip olan ürünler oluşturulduğunda, satış siparişleri veya tekliflere eklenmeleri için etkinleştirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="82da7-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="82da7-158">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="82da7-158">Template mapping in Data integration</span></span>

<span data-ttu-id="82da7-159">Aşağıdaki görsel, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="82da7-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="82da7-160">Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="82da7-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="82da7-162">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="82da7-162">Related topics</span></span>

[<span data-ttu-id="82da7-163">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="82da7-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="82da7-164">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="82da7-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="82da7-165">Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="82da7-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="82da7-166">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="82da7-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="82da7-167">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="82da7-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




