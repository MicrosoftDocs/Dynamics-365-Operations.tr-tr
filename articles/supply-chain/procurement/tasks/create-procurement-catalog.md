---
title: Tedarik kataloğu oluşturma
description: Bu konu tedarik kataloğunun nasıl oluşturulacağını açıklar.
author: mkirknel
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20966291ce6297561514ce9d9f7e945859997351
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439242"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="d64f2-103">Tedarik kataloğu oluşturma</span><span class="sxs-lookup"><span data-stu-id="d64f2-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d64f2-104">Bu konu tedarik kataloğunun nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d64f2-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="d64f2-105">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="d64f2-106">Ayrıca talep oluşturduklarında çalışanların kataloğu nasıl kullanabileceğini öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="d64f2-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="d64f2-107">Katalog oluşturmadan önce sisteminizde bir tedarik kategorisi hiyerarşisi olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="d64f2-108">Hiyerarşi, dahil olan tüm ürünlerle birlikte yeni katalog tarafından devralınır.</span><span class="sxs-lookup"><span data-stu-id="d64f2-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="d64f2-109">Bu kılavuzu tedarik kategorisinin kullanılabilir olduğu demo veri şirketi USMF'de ve prosedür adımlarında kullanılan örneklerde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d64f2-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="d64f2-110">Tedarik kategorisi hiyerarşisinin var olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="d64f2-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="d64f2-111">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Tedarik kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="d64f2-112">Tedarik kategorisi hiyerarşisi USMF demo veri şirketinde kullanılabilir ve ürünler **Ofis makineleri/Bilgisayarlar** kategorisine eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="d64f2-113">Bu prosedürü bir görev kılavuzu olarak çalıştırıyorsanız kategoride gezinmek istediğinizde kılavuzun kilidini açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="d64f2-114">Bir hiyerarşi kullanılabilir değilse **Yeni**'ye tıklayarak oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d64f2-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="d64f2-115">Bu yalnızca bir defa yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-115">This can only be done once.</span></span>  
2. <span data-ttu-id="d64f2-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d64f2-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="d64f2-117">Katalog oluşturma</span><span class="sxs-lookup"><span data-stu-id="d64f2-117">Create a catalog</span></span>
1. <span data-ttu-id="d64f2-118">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Kataloglar > Tedarik katalogları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="d64f2-119">Açılır iletişim kutusunu açmak için **Yeni tedarik kataloğu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="d64f2-120">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d64f2-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d64f2-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-121">Select **OK**.</span></span>
5. <span data-ttu-id="d64f2-122">Ağaçtan **CORP PROCUREMENT CATEGORIES**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="d64f2-123">Ağaçtan, **OFFICE MACHINES**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="d64f2-124">Ağaçtan **Bilgisayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="d64f2-125">Tedarik kategorisindeki ürünler listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="d64f2-126">Kategoriye bir ürün eklemek isterseniz bunu **Tedarik kategorisi hiyerarşisi** sayfasından veya **Madde ayrıntıları** sayfasından yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="d64f2-127">**Varsayılan** güncelleştirme türü, tedarik kategorisi hiyerarşisine eklenen yeni ürünlerin katalogda anında görünür olup olmayacaklarını belirler.</span><span class="sxs-lookup"><span data-stu-id="d64f2-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="d64f2-128">Güncelleştirme türü **Dinamik** olarak ayarlanmışsa değişiklikler anında görünür.</span><span class="sxs-lookup"><span data-stu-id="d64f2-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="d64f2-129">Güncelleştirme türü **Statik** ise yeni ürünler, yalnızca katalog yeniden yayınlandıktan sonra kataloğu kullanan kişilerce görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="d64f2-130">**Yayımla** eylemi sayfanın en üstündeki Eylem Bölmesi'nden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="d64f2-131">Ürünler tedarik kategorisi hiyerarşisinden kaldırılırsa **Varsayılan** güncelleştirme türü alanındaki değerden bağımsız olarak değişiklik hemen görünür.</span><span class="sxs-lookup"><span data-stu-id="d64f2-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="d64f2-132">Eylem bölmesinde **Kategori gezinmesi**'ni seçin ve **Etkin**'in seçili olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="d64f2-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="d64f2-133">**Kataloğı etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="d64f2-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d64f2-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="d64f2-135">Kataloğu görünür yapın</span><span class="sxs-lookup"><span data-stu-id="d64f2-135">Make the catalog visible</span></span>
1. <span data-ttu-id="d64f2-136">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Kurulum > İlkeler > Satın alma ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="d64f2-137">**Tedarik İlkesi USMF**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="d64f2-138">Tüzel kişilik için kullanıcı profilinize bağlanan çalışanın profilinizdeki ürünleri sipariş etmesine izin veren satınalma ilkesini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d64f2-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="d64f2-139">USMF demo verilerinde Yönetici kullanıcı **Julia Funderburk** adlı çalışana bağlanır ve USMF'de varsayılan olarak ürünleri sipariş eder.</span><span class="sxs-lookup"><span data-stu-id="d64f2-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="d64f2-140">Yeni oluşturduğunuz kataloğu seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="d64f2-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="d64f2-142">Kataloğu kullanın</span><span class="sxs-lookup"><span data-stu-id="d64f2-142">Use the catalog</span></span>
1. <span data-ttu-id="d64f2-143">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma talepleri > Tüm satınalma talepleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="d64f2-144">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-144">Select **New**.</span></span>
3. <span data-ttu-id="d64f2-145">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d64f2-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d64f2-146">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-146">Select **OK**.</span></span>
5. <span data-ttu-id="d64f2-147">**Ürün ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-147">Select **Add products**.</span></span>
6. <span data-ttu-id="d64f2-148">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="d64f2-149">Ürünleri filtrelemek için soldaki kategori hiyerarşisini veya listenin en üstündeki filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d64f2-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="d64f2-150">**Satırlara ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="d64f2-151">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d64f2-151">Select **OK**.</span></span>

