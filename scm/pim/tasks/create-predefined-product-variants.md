--- 
title: "Önceden tanımlanmış ürün çeşitleri oluşturma"
description: "Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır."
author: BibiSp
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa23f1449e750b4ed1c0f631a98c42b18b7dbb40
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="af262-103">Önceden tanımlanmış ürün çeşitleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="af262-103">Create predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af262-104">Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="af262-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="af262-105">Bu yöntemi oluşturmak için kullanılan demo şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="af262-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="af262-106">Ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="af262-106">Create a product master</span></span>
1. <span data-ttu-id="af262-107">Ürün bilgi yönetimi > Ürünler > Ana ürünler'e git.</span><span class="sxs-lookup"><span data-stu-id="af262-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="af262-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-108">Click New.</span></span>
3. <span data-ttu-id="af262-109">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="af262-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="af262-110">Bir ürün numarasının el ile girilmesi sadece ürün numarası alanı için hiçbir numarası dizisi ayarlanmamışsa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="af262-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="af262-111">Diğer bir deyişle, alan için bir numara serisi ayarlanmışsa bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="af262-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="af262-112">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="af262-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="af262-113">Ürün boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="af262-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="af262-114">SizeCol (Boyut ve Renk) ürün boyut grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="af262-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="af262-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="af262-116">Ürün boyutları ekleme</span><span class="sxs-lookup"><span data-stu-id="af262-116">Add product dimensions</span></span>
1. <span data-ttu-id="af262-117">Ürün boyutları öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="af262-118">Bu örnekte ürün boyutlarının nasıl el ile girileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="af262-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="af262-119">Ayrıca, kullanmak istediğiniz ürün boyutu değerlerini içeren boyut, renk veya tarz grubunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af262-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="af262-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-120">Click New.</span></span>
3. <span data-ttu-id="af262-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af262-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="af262-122">Ebat alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="af262-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="af262-123">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af262-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="af262-124">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="af262-124">Click New.</span></span>
7. <span data-ttu-id="af262-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af262-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="af262-126">Ebat alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="af262-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="af262-127">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af262-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="af262-128">Renkler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="af262-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="af262-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-129">Click New.</span></span>
12. <span data-ttu-id="af262-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af262-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="af262-131">Renk alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="af262-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="af262-132">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af262-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="af262-133">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="af262-133">Click New.</span></span>
16. <span data-ttu-id="af262-134">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af262-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="af262-135">Renk alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="af262-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="af262-136">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af262-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="af262-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-137">Click Save.</span></span>
20. <span data-ttu-id="af262-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="af262-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="af262-139">Ürün seçenekleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="af262-139">Generate product variants</span></span>
1. <span data-ttu-id="af262-140">Ürün çeşitleri öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-140">Click Product variants.</span></span>
2. <span data-ttu-id="af262-141">Çeşit önerilerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="af262-142">Tümünü seç'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="af262-142">Click Select all.</span></span>
    * <span data-ttu-id="af262-143">Bu örnekte tüm olası seçenekler dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="af262-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="af262-144">Bu seçeneklerin oluşturulması için sadece olası ürün boyutu kombinasyonlarının bir alt kümesi kullanılacaksa, bireysel girişleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af262-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="af262-145">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-145">Click Create.</span></span>
    * <span data-ttu-id="af262-146">Ürün boyutu değerlerinin kombinasyonuna dayalı olarak tüm seçenekleriniz için açıklamalar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af262-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="af262-147">Açıklamalar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="af262-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="af262-148">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af262-148">Click Save.</span></span>


