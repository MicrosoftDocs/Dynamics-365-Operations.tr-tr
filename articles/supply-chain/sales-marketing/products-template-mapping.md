---
title: "Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme"
description: "Bu konu, ürünleri Microsoft Dynamics 365 for Sales'a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 063a20f133a00620bdf389b0a52a90bc61e2f7d4
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="9059a-103">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="9059a-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9059a-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun.</span><span class="sxs-lookup"><span data-stu-id="9059a-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="9059a-105">Bu konu, ürünleri Microsoft Dynamics 365 for Sales'a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="9059a-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="9059a-106">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="9059a-106">Template and task</span></span>

<span data-ttu-id="9059a-107">Ürünleri Microsoft Dynamics 365 for Sales'a (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan (Finance and Operations) eşitlemek için aşağıdaki görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="9059a-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="9059a-108">Şablonun adı: Ürünler (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="9059a-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="9059a-109">Görevin proje içindeki adı: Ürünler</span><span class="sxs-lookup"><span data-stu-id="9059a-109">Name of task in project: Products</span></span>

<span data-ttu-id="9059a-110">Ürün eşitlemesinden önce gerekli görevler: Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="9059a-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="9059a-111">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="9059a-111">Entity set</span></span>

| <span data-ttu-id="9059a-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="9059a-112">**Finance and Operations**</span></span> | <span data-ttu-id="9059a-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="9059a-113">**CDS**</span></span> | <span data-ttu-id="9059a-114">**Satış**</span><span class="sxs-lookup"><span data-stu-id="9059a-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="9059a-115">Satış yapılabilir serbest bırakılan ürünler</span><span class="sxs-lookup"><span data-stu-id="9059a-115">Sellable released products</span></span> | <span data-ttu-id="9059a-116">Ürün</span><span class="sxs-lookup"><span data-stu-id="9059a-116">Product</span></span> | <span data-ttu-id="9059a-117">Ürünler</span><span class="sxs-lookup"><span data-stu-id="9059a-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="9059a-118">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="9059a-118">Entity flow</span></span>

<span data-ttu-id="9059a-119">Ürünler Finance and Operations'ta yönetilir ve Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="9059a-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="9059a-120">Finance and Operations'taki **Satılabilir serbest ürünler** veri varlığı, yalnızca satılabilir olan ürünleri dışa aktarır; bu da bir satış siparişinde kullanılması gereken bilgiye sahip ürünler anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9059a-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="9059a-121">Aynı kurallar, bir ürün **Yayımlanan ürün** sayfasında **Doğrula** işlevi le doğrulanıyorsa da geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9059a-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="9059a-122">**Ürün numarası** bir anahtar olarak kullanılır, bu da ürün çeşitlerinin CDS ve Sales ile **Ürün çeşidi** başına bireysel **Ürün kodları** ile eşitlendiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9059a-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9059a-123">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="9059a-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9059a-124">Sales'ta, ürünlere, ürünün dışarıda tutulduğunu belirten **Harici olarak tutulan** alanı eklenir.</span><span class="sxs-lookup"><span data-stu-id="9059a-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="9059a-125">Değer, Sales'a içe aktarmada varsayılan olarak **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9059a-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="9059a-126">**Dışarıda tutulan = Evet**: Ürün Finance and Operations'tan geliyor ve Sales'ta düzenlenebilir olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="9059a-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="9059a-127">**Dışarıda tutula = Hayır**: Ürün doğrudan Sales'a girildi.</span><span class="sxs-lookup"><span data-stu-id="9059a-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="9059a-128">**Dışarıda tutulan = Boş**: Ürün Sales'ta, Aday müşteriden nakde çözümünü etkinleştirmeden önce mevcuttu.</span><span class="sxs-lookup"><span data-stu-id="9059a-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="9059a-129">**Dışarıda tutulan** bilgisi yalnızca **Dışarıda tutulan ürünler** özelliğine sahip **Tekliflerin** ve **Satış siparişlerinin** Finance and Operations'a eşitleneceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9059a-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="9059a-130">**Dışarıda tutulan ürünler** otomatik olarak ilk geçerli **Fiyat listesine**, aynı para birimi ile eklenir.</span><span class="sxs-lookup"><span data-stu-id="9059a-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="9059a-131">Listenin **Ad** sıralamasına göre alfabetik olarak düzenlendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9059a-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="9059a-132">Finance and Operations'taki ürün satış fiyatı, **Fiyat listesindeki** fiyat olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9059a-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="9059a-133">Bu, Finance and Operations içindeki her bir **Ürün satış para birimi** için Sales içinde bir **Fiyat listesi** bulundurmanın zorunlu olduğu anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9059a-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="9059a-134">Yayımlanan satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9059a-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="9059a-135">Ürün eşitleme, eşleşen para birimine sahip bir **Fiyat listesi** olmadan başarılı olmaz.</span><span class="sxs-lookup"><span data-stu-id="9059a-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9059a-136">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="9059a-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="9059a-137">İlk eşitlemeyi çalıştırmadan önce **Farklı ürün tablosu**'nu Finance and Operation içindeki mevcut ürünler için doldurmalısınız.</span><span class="sxs-lookup"><span data-stu-id="9059a-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="9059a-138">Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="9059a-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="9059a-139">Finance and Operations'ta, **Farklı ürün tablolarını doldur**'u aramak için Arama'yı kullanın.</span><span class="sxs-lookup"><span data-stu-id="9059a-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="9059a-140">İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9059a-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="9059a-141">Bu işin yalnızca bir kere çalıştırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9059a-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="9059a-142">**Ölçü birimi** satmak için ihtiyaç duyulan **ValueMap**'in Finance and Operations'ta **Kaynak-\> CDS eşleme SalesUnitSymbol / DefaultSellingUnitOfMeasure** içinde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9059a-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="9059a-143">**Kaynak -\> CDS** içindeki **CDS Kuruluş Kodu Organization_OrganizationId**.</span><span class="sxs-lookup"><span data-stu-id="9059a-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="9059a-144">Şablon değeri varsayılan olarak ORG001 olur.</span><span class="sxs-lookup"><span data-stu-id="9059a-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="9059a-145">**Unit group** (**defaultuomscheduleid.name**) için **ValueMap**'i **CDS -\> Hedef** içerisinde, Sales içindeki **Birim grupları** ile eşleşmek için güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="9059a-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="9059a-146">Şablon değeri **Varsayılan birim**'e varsayılan olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="9059a-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="9059a-147">Finance and Operations'tan UOM'ler satan tüm ürünlerin Sales içinde **CDS çekme listeleri** değeri ile mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9059a-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="9059a-148">**Fiyat listelerini** Sales içerisinde, Finance and Operations içindeki her bir ürün satış para biriminde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9059a-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="9059a-149">Ürünler Sales'ta **Taslak** veya **Etkin** durumuyla oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="9059a-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="9059a-150">Bu, Sales'ta **Satışlar** altında **Sistem ayarları** içerisinde denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9059a-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="9059a-151">Taslak durumunda oluşturulan ürünlerin **Teklif** veya **Satış siparişi**'ne eklenebilmeden önce etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9059a-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="9059a-152">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="9059a-152">Template mapping in data integrator</span></span>

<span data-ttu-id="9059a-153">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="9059a-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![veri entegratörü içerisindeki şablon eşleme](./media/products-template-mapping-data-integrator-1.png)

![veri entegratörü içerisindeki ürünler için şablon eşleme](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="9059a-156">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="9059a-156">Related topics</span></span>

[<span data-ttu-id="9059a-157">Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="9059a-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="9059a-158">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="9059a-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="9059a-159">Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="9059a-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="9059a-160">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="9059a-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="9059a-161">Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="9059a-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


