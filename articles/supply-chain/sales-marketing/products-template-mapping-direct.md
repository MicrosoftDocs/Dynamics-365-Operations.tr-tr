---
title: Supply Chain Management'taki ürünleri doğrudan Sales'daki ürünlerle eşitleme
description: Bu konuda, ürünleri Dynamics 365 Sales'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.
author: ChristianRytt
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817833"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="38933-103">Supply Chain Management'taki ürünleri doğrudan Sales'daki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="38933-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="38933-104">Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="38933-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="38933-105">Bu konuda, ürünleri doğrudan Dynamics 365 Sales'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="38933-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="38933-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="38933-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="38933-107">Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="38933-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="38933-108">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="38933-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="38933-109">Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38933-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="38933-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="38933-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="38933-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="38933-111">Templates and tasks</span></span>

<span data-ttu-id="38933-112">Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="38933-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="38933-113">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="38933-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="38933-114">Aşağıdaki şablon ve temel görevler, ürünleri Supply Chain Management'tan Sales'a eşitlemek için kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="38933-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="38933-115">**Veri tümleştirmede şablonun adı:** Ürünler (Supply Chain Management'tan Sales'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="38933-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="38933-116">**Veri tümleştirme projesindeki görevin adı:** Ürünler</span><span class="sxs-lookup"><span data-stu-id="38933-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="38933-117">Ürün eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="38933-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="38933-118">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="38933-118">Entity set</span></span>

| <span data-ttu-id="38933-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="38933-119">Supply Chain Management</span></span>    | <span data-ttu-id="38933-120">Satışlar</span><span class="sxs-lookup"><span data-stu-id="38933-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="38933-121">Satış yapılabilir serbest bırakılan ürünler</span><span class="sxs-lookup"><span data-stu-id="38933-121">Sellable released products</span></span> | <span data-ttu-id="38933-122">Ürünler</span><span class="sxs-lookup"><span data-stu-id="38933-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="38933-123">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="38933-123">Entity flow</span></span>

<span data-ttu-id="38933-124">Ürünler, Supply Chain Management'ta yönetilir ve Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="38933-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="38933-125">Supply Chain Management'taki **Satılabilir serbest bırakılan ürünler** veri varlığı, yalnızca *satılabilir* ürünleri dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="38933-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="38933-126">Satış yapılabilir ürünler, bir satış siparişinde kullanılmak üzere gerekli bilgilere sahip olan ürünlerdir.</span><span class="sxs-lookup"><span data-stu-id="38933-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="38933-127">Aynı kurallar, bir ürün **Serbest bırakılan ürün** sayfasında **Doğrula** işleviyle doğrulanıyorsa da geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="38933-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="38933-128">Ürün numarası anahtar olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38933-128">The product number is used as a key.</span></span> <span data-ttu-id="38933-129">Bu nedenle, ürün çeşitleri Sales'e eşitlendiğinde her ürün çeşidinin ayrı bir ürün kimliği vardır.</span><span class="sxs-lookup"><span data-stu-id="38933-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="38933-130">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="38933-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="38933-131">Sales'ta ürünlere, ürünün dışarıda tutulduğunu belirten yeni bir **Dışarıda tutulan** alanı eklenir.</span><span class="sxs-lookup"><span data-stu-id="38933-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="38933-132">Varsayılan olarak değer Sales'a içe aktarma sırasında **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="38933-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="38933-133">Aşağıdaki değerler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="38933-133">The following values are available:</span></span>

- <span data-ttu-id="38933-134">**Evet** – Ürün, Supply Chain Management'tan gelir ve Sales'da düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="38933-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="38933-135">**Hayır** – Ürün doğrudan Sales içinden girilmiştir.</span><span class="sxs-lookup"><span data-stu-id="38933-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="38933-136">**(Boş)** – Aday müşteriden nakde çözümü etkinleştirilmeden önce ürün Sales içinde vardır.</span><span class="sxs-lookup"><span data-stu-id="38933-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="38933-137">**Dışarıda Tutulan** alanı, yalnızca dışarıda tutulan ürünler bulunan teklif ve satış siparişlerinin Supply Chain Management ile eşitlenmesini sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="38933-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="38933-138">Dışarıda tutulan ürünler otomatik olarak aynı para birimine sahip ilk geçerli fiyat listesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="38933-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="38933-139">Fiyat listeleri ada göre alfabetik olarak düzenlenir.</span><span class="sxs-lookup"><span data-stu-id="38933-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="38933-140">Supply Chain Management'taki ürün satış fiyatı, fiyat listesindeki fiyat olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38933-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="38933-141">Bu nedenle, Supply Chain Management'taki her ürün satış para birimi için Sales'da bir fiyat listesi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="38933-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="38933-142">Serbest bırakılmış satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="38933-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="38933-143">Eşleşen para birimine sahip bir fiyat listesi olmadığı sürece ürün eşitleme başarılı olmaz.</span><span class="sxs-lookup"><span data-stu-id="38933-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="38933-144">Tümleştirmeyle kullanılan fiyat listesini, Veri Tümleştirme projesindeki pricelevelid.name [Varsayılan Fiyat Listesi (Ad)] ile eşleştirerek denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38933-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="38933-145">Girişin tamamen küçük harflerden oluşması gerekir.</span><span class="sxs-lookup"><span data-stu-id="38933-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="38933-146">Örneğin Satışta "Standard" adlı bir fiyat listesi varsayılanı şöyle olur: Hedef alan: pricelevelid.name [Varsayılan Fiyat Listesi (Ad)] ve Eşleşme türü: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="38933-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="38933-147">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="38933-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="38933-148">Eşitlemeyi ilk kez çalıştırmadan önce Farklı ürün tablosu'nu Supply Chain Management'taki mevcut ürünler için doldurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="38933-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="38933-149">Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="38933-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="38933-150">Supply Chain Management'ta **Farklı ürün tablosunu doldur**'u aramak için Arama'yı kullanın.</span><span class="sxs-lookup"><span data-stu-id="38933-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="38933-151">İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="38933-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="38933-152">Bu işlemin yalnızca bir kez çalıştırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="38933-152">This job must be run only one time.</span></span>

- <span data-ttu-id="38933-153">Supply Chain Management ile Sales arasındaki satış ölçü birimi (UOM) için gerekli değer eşlemesinin **SalesUnitSymbol** ile **DefaultUnit (Ad)** eşlemesinde var olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="38933-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="38933-154">**Birim gurubu** (**defaultuomscheduleid.name**) için değer eşlemesini güncelleştirin, böylece bu eşleme Sales'deki **Birim grupları** ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="38933-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="38933-155">Varsayılan şablon değeri **Varsayılan birim**'dir.</span><span class="sxs-lookup"><span data-stu-id="38933-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="38933-156">Supply Chain Management'taki tüm ürünlerin satış UOM'larının Sales'da mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="38933-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="38933-157">Fiyat listelerinin Supply Chain Management'taki her ürün satış para birimi için Sales'da mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="38933-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="38933-158">Sales'de ürünler oluşturulduğunda, durumları **Taslak** veya **Etkin** olabilir.</span><span class="sxs-lookup"><span data-stu-id="38933-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="38933-159">Davranış Sales'deki **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altından kontrol edilebilir.</span><span class="sxs-lookup"><span data-stu-id="38933-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="38933-160">**Taslak** durumuna sahip olan ürünler oluşturulduğunda, satış siparişleri veya tekliflere eklenmeleri için etkinleştirilmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="38933-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="38933-161">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="38933-161">Template mapping in Data integration</span></span>

<span data-ttu-id="38933-162">Aşağıdaki görsel, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="38933-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="38933-163">Eşleme hangi alan bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="38933-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="38933-165">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="38933-165">Related topics</span></span>

[<span data-ttu-id="38933-166">Aday müşteriden nakde</span><span class="sxs-lookup"><span data-stu-id="38933-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="38933-167">Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="38933-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="38933-168">Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="38933-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="38933-169">Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="38933-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="38933-170">Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="38933-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]