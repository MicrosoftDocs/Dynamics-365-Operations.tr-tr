---
title: Tedarik kataloğu oluşturma
description: Bu kılavuzda bir tedarik kataloğunu nasıl oluşturacağınız gösterilir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f2a010e21f16b3908a6ee5f18d8f144c5130be7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547664"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="ca80c-103">Tedarik kataloğu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca80c-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca80c-104">Bu kılavuzda bir tedarik kataloğunu nasıl oluşturacağınız gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="ca80c-105">Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="ca80c-106">Ayrıca talep oluşturduklarında çalışanların kataloğu nasıl kullanabileceğini öğreneceksiniz.</span><span class="sxs-lookup"><span data-stu-id="ca80c-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="ca80c-107">Katalog oluşturmadan önce sisteminizde bir tedarik kategorisi hiyerarşisi olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="ca80c-108">Hiyerarşi, dahil olan tüm ürünlerle birlikte yeni katalog tarafından devralınır.</span><span class="sxs-lookup"><span data-stu-id="ca80c-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="ca80c-109">Bu kılavuzu tedarik kategorisinin kullanılabilir olduğu demo veri şirketi USMF'de ve prosedür adımlarında kullanılan örneklerde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca80c-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="ca80c-110">Tedarik kategorisi hiyerarşisinin var olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="ca80c-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="ca80c-111">Tedarik ve kaynak > Tedarik kategorileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="ca80c-112">Tedarik kategorisi hiyerarşisi USMF demo veri şirketinde kullanılabilir ve ürünler Ofis makineleri/Bilgisayarlar kategorisine eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="ca80c-113">Bu prosedürü bir görev kılavuzu olarak çalıştırıyorsanız kategoride gezinmek istediğinizde kılavuzun kilidini açmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="ca80c-114">Bir hiyerarşi kullanılabilir değilse Yeni'ye tıklayarak oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca80c-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="ca80c-115">Bu yalnızca bir defa yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-115">This can only be done once.</span></span>  
2. <span data-ttu-id="ca80c-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="ca80c-117">Katalog oluşturma</span><span class="sxs-lookup"><span data-stu-id="ca80c-117">Create a catalog</span></span>
1. <span data-ttu-id="ca80c-118">Tedarik ve kaynak atama > Kataloglar > Tedarik katalogları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="ca80c-119">Açılır iletişim kutusunu açmak için Yeni tedarik kataloğu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="ca80c-120">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ca80c-121">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-121">Click OK.</span></span>
5. <span data-ttu-id="ca80c-122">Ağaçtan 'CORP PROCUREMENT CATEGORIES'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="ca80c-123">Ağaçtan, 'OFFICE MACHINES'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="ca80c-124">Ağaçtan 'Bilgisayarlar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="ca80c-125">Tedarik kategorisindeki ürünler listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="ca80c-126">Kategoriye bir ürün eklemek isterseniz bunu Tedarik kategorisi hiyerarşisi sayfasından veya Madde ayrıntıları sayfasından yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="ca80c-127">Varsayılan güncelleştirme türü, tedarik kategorisi hiyerarşisine eklenen yeni ürünlerin katalogda anında görünür olup olmayacaklarını belirler.</span><span class="sxs-lookup"><span data-stu-id="ca80c-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="ca80c-128">Güncelleştirme türü Dinamik olarak ayarlanmışsa değişiklikler anında görünür.</span><span class="sxs-lookup"><span data-stu-id="ca80c-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="ca80c-129">Güncelleştirme türü Statik ise yeni ürünler, yalnızca katalog yeniden yayınlandıktan sonra kataloğu kullanan kişilerce görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="ca80c-130">Yayımla eylemi sayfanın en üstündeki Eylem Bölmesi'nden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="ca80c-131">Ürünler tedarik kategorisi hiyerarşisinden kaldırılırsa Varsayılan güncelleştirme türü alanındaki değerden bağımsız olarak değişiklik hemen görünür.</span><span class="sxs-lookup"><span data-stu-id="ca80c-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="ca80c-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ca80c-133">Gizle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-133">Click Hide.</span></span>
10. <span data-ttu-id="ca80c-134">Eylem Bölmesi'nde, Kategori gezinmesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="ca80c-135">Devre dışı bırak'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-135">Click Disable.</span></span>
12. <span data-ttu-id="ca80c-136">Eylem Bölmesi'nde, Kategori gezinmesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="ca80c-137">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-137">Click Enable.</span></span>
14. <span data-ttu-id="ca80c-138">Kataloğu etkinleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="ca80c-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="ca80c-140">Kataloğu görünür yapın</span><span class="sxs-lookup"><span data-stu-id="ca80c-140">Make the catalog visible</span></span>
1. <span data-ttu-id="ca80c-141">Tedarik ve kaynak atama > Ayarlar > İlkeler > Satınalma ilkeleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="ca80c-142">Tedarik İlkesi USMF'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="ca80c-143">Tüzel kişilik için kullanıcı profilinize bağlanan çalışanın profilinizdeki ürünleri sipariş etmesine izin veren satınalma ilkesini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca80c-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="ca80c-144">USMF demo verilerinde Yönetici kullanıcı Julia Funderburk adlı çalışana bağlanır ve USMF'de varsayılan olarak ürünleri sipariş eder.</span><span class="sxs-lookup"><span data-stu-id="ca80c-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="ca80c-145">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ca80c-146">Yeni oluşturduğunuz kataloğu seçin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="ca80c-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-147">Click OK.</span></span>
6. <span data-ttu-id="ca80c-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-148">Close the page.</span></span>
7. <span data-ttu-id="ca80c-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="ca80c-150">Kataloğu kullanın</span><span class="sxs-lookup"><span data-stu-id="ca80c-150">Use the catalog</span></span>
1. <span data-ttu-id="ca80c-151">Tedarik ve kaynak atama > Satınalma talepleri > Tüm satınalma talepleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="ca80c-152">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-152">Click New.</span></span>
3. <span data-ttu-id="ca80c-153">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ca80c-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-154">Click OK.</span></span>
5. <span data-ttu-id="ca80c-155">Ürünler ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-155">Click Add products.</span></span>
6. <span data-ttu-id="ca80c-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ca80c-157">Ürünleri filtrelemek için soldaki kategori hiyerarşisini veya listenin en üstündeki filtreyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca80c-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="ca80c-158">Satırlara ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-158">Click Add to lines.</span></span>
8. <span data-ttu-id="ca80c-159">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ca80c-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ca80c-160">Satırlara ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-160">Click Add to lines.</span></span>
10. <span data-ttu-id="ca80c-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca80c-161">Click OK.</span></span>

