---
title: "Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme"
description: "Bu konu, ürünleri Microsoft Dynamics 365 for Sales'a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="44d00-103">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="44d00-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="44d00-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun.</span><span class="sxs-lookup"><span data-stu-id="44d00-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="44d00-105">Bu konu, ürünleri Microsoft Dynamics 365 for Sales'a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="44d00-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="44d00-106">Şablon ve görev</span><span class="sxs-lookup"><span data-stu-id="44d00-106">Template and task</span></span>

<span data-ttu-id="44d00-107">Ürünleri Microsoft Dynamics 365 for Sales'a (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan (Finance and Operations) eşitlemek için aşağıdaki görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="44d00-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="44d00-108">Şablonun adı: Ürünler (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="44d00-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="44d00-109">Görevin proje içindeki adı: Ürünler</span><span class="sxs-lookup"><span data-stu-id="44d00-109">Name of task in project: Products</span></span>

<span data-ttu-id="44d00-110">Ürün eşitlemesinden önce gerekli görevler: Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="44d00-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="44d00-111">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="44d00-111">Entity set</span></span>

| <span data-ttu-id="44d00-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="44d00-112">**Finance and Operations**</span></span> | <span data-ttu-id="44d00-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="44d00-113">**CDS**</span></span> | <span data-ttu-id="44d00-114">**Satış**</span><span class="sxs-lookup"><span data-stu-id="44d00-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="44d00-115">Satış yapılabilir serbest bırakılan ürünler</span><span class="sxs-lookup"><span data-stu-id="44d00-115">Sellable released products</span></span> | <span data-ttu-id="44d00-116">Ürün</span><span class="sxs-lookup"><span data-stu-id="44d00-116">Product</span></span> | <span data-ttu-id="44d00-117">Ürünler</span><span class="sxs-lookup"><span data-stu-id="44d00-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="44d00-118">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="44d00-118">Entity flow</span></span>

<span data-ttu-id="44d00-119">Ürünler Finance and Operations'ta yönetilir ve Sales'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="44d00-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="44d00-120">Finance and Operations'taki **Satılabilir serbest ürünler** veri varlığı, yalnızca satılabilir olan ürünleri dışa aktarır; bu da bir satış siparişinde kullanılması gereken bilgiye sahip ürünler anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="44d00-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="44d00-121">Aynı kurallar, bir ürün **Yayımlanan ürün** sayfasında **Doğrula** işlevi le doğrulanıyorsa da geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="44d00-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="44d00-122">**Ürün numarası** bir anahtar olarak kullanılır, bu da ürün çeşitlerinin CDS ve Sales ile **Ürün çeşidi** başına bireysel **Ürün kodları** ile eşitlendiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="44d00-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="44d00-123">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="44d00-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="44d00-124">Sales'ta, ürünlere, ürünün dışarıda tutulduğunu belirten **Harici olarak tutulan** alanı eklenir.</span><span class="sxs-lookup"><span data-stu-id="44d00-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="44d00-125">Değer, Sales'a içe aktarmada varsayılan olarak **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="44d00-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="44d00-126">**Dışarıda tutulan = Evet**: Ürün Finance and Operations'tan geliyor ve Sales'ta düzenlenebilir olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="44d00-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="44d00-127">**Dışarıda tutula = Hayır**: Ürün doğrudan Sales'a girildi.</span><span class="sxs-lookup"><span data-stu-id="44d00-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="44d00-128">**Dışarıda tutulan = Boş**: Ürün Sales'ta, Aday müşteriden nakde çözümünü etkinleştirmeden önce mevcuttu.</span><span class="sxs-lookup"><span data-stu-id="44d00-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="44d00-129">**Dışarıda tutulan** bilgisi yalnızca **Dışarıda tutulan ürünler** özelliğine sahip **Tekliflerin** ve **Satış siparişlerinin** Finance and Operations'a eşitleneceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="44d00-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="44d00-130">**Dışarıda tutulan ürünler** otomatik olarak ilk geçerli **Fiyat listesine**, aynı para birimi ile eklenir.</span><span class="sxs-lookup"><span data-stu-id="44d00-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="44d00-131">Listenin **Ad** sıralamasına göre alfabetik olarak düzenlendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="44d00-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="44d00-132">Finance and Operations'taki ürün satış fiyatı, **Fiyat listesindeki** fiyat olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="44d00-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="44d00-133">Bu, Finance and Operations içindeki her bir **Ürün satış para birimi** için Sales içinde bir **Fiyat listesi** bulundurmanın zorunlu olduğu anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="44d00-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="44d00-134">Yayımlanan satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="44d00-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="44d00-135">Ürün eşitleme, eşleşen para birimine sahip bir **Fiyat listesi** olmadan başarılı olmaz.</span><span class="sxs-lookup"><span data-stu-id="44d00-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="44d00-136">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="44d00-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="44d00-137">İlk eşitlemeyi çalıştırmadan önce **Farklı ürün tablosu**'nu Finance and Operation içindeki mevcut ürünler için doldurmalısınız.</span><span class="sxs-lookup"><span data-stu-id="44d00-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="44d00-138">Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="44d00-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="44d00-139">Finance and Operations'ta, **Farklı ürün tablolarını doldur**'u aramak için Arama'yı kullanın.</span><span class="sxs-lookup"><span data-stu-id="44d00-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="44d00-140">İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="44d00-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="44d00-141">Bu işin yalnızca bir kere çalıştırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="44d00-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="44d00-142">**Ölçü birimi** satmak için ihtiyaç duyulan **ValueMap**'in Finance and Operations'ta **Kaynak-\> CDS eşleme SalesUnitSymbol / DefaultSellingUnitOfMeasure** içinde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="44d00-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="44d00-143">UOM için **Desteklenen ondalık basamak sayısının**, **CDS -\> Hedef** içindeki gereksinimlerinizle eşleştiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="44d00-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="44d00-144">UOM başına farklı değerlere ihtiyaç duyuyorsanız, bu Birim içinden **ValueMap** ile yapılabilir, örneğin [Her biri : 0] ve [Pound : 2].</span><span class="sxs-lookup"><span data-stu-id="44d00-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="44d00-145">Şablon değeri varsayılan olarak 0 olur.</span><span class="sxs-lookup"><span data-stu-id="44d00-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="44d00-146">**Kaynak -\> CDS** içindeki **CDS Kuruluş Kodu Organization_OrganizationId**.</span><span class="sxs-lookup"><span data-stu-id="44d00-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="44d00-147">Şablon değeri varsayılan olarak ORG001 olur.</span><span class="sxs-lookup"><span data-stu-id="44d00-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="44d00-148">**Unit group** (**defaultuomscheduleid.name**) için **ValueMap**'i **CDS -\> Hedef** içerisinde, Sales içindeki **Birim grupları** ile eşleşmek için güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="44d00-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="44d00-149">Şablon değeri **Varsayılan birim**'e varsayılan olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="44d00-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="44d00-150">Finance and Operations'tan UOM'ler satan tüm ürünlerin Sales içinde **CDS çekme listeleri** değeri ile mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="44d00-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="44d00-151">**Fiyat listelerini** Sales içerisinde, Finance and Operations içindeki her bir ürün satış para biriminde mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="44d00-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="44d00-152">Ürünler Sales'ta **Taslak** veya **Etkin** durumuyla oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="44d00-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="44d00-153">Bu, Sales'ta **Satışlar** altında **Sistem ayarları** içerisinde denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="44d00-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="44d00-154">Taslak durumunda oluşturulan ürünlerin **Teklif** veya **Satış siparişi**'ne eklenebilmeden önce etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="44d00-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="44d00-155">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="44d00-155">Template mapping in data integrator</span></span>

<span data-ttu-id="44d00-156">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="44d00-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![veri entegratörü içerisindeki şablon eşleme](./media/products-template-mapping-data-integrator-1.png)

![veri entegratörü içerisindeki ürünler için şablon eşleme](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="44d00-159">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="44d00-159">Related topics</span></span>

[<span data-ttu-id="44d00-160">Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="44d00-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="44d00-161">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="44d00-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="44d00-162">Sales'teki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="44d00-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


