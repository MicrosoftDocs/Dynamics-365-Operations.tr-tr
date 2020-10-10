---
title: Önceden tanımlanmış ürün çeşitleri oluşturma
description: Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6009f6de76155ea7c2982b28fe4505232447c9c8
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895317"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="58531-103">Önceden tanımlanmış ürün çeşitleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="58531-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58531-104">Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="58531-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="58531-105">Bu yöntemi oluşturmak için kullanılan demo şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="58531-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="58531-106">Ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="58531-106">Create a product master</span></span>
1. <span data-ttu-id="58531-107">Ürün bilgi yönetimi > Ürünler > Ana ürünler'e git.</span><span class="sxs-lookup"><span data-stu-id="58531-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="58531-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-108">Click New.</span></span>
3. <span data-ttu-id="58531-109">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="58531-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="58531-110">Bir ürün numarasının el ile girilmesi sadece ürün numarası alanı için hiçbir numarası dizisi ayarlanmamışsa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="58531-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="58531-111">Diğer bir deyişle, alan için bir numara serisi ayarlanmışsa bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="58531-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="58531-112">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="58531-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="58531-113">Ürün boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="58531-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="58531-114">SizeCol (Boyut ve Renk) ürün boyut grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="58531-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="58531-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="58531-116">Ürün boyutları ekleme</span><span class="sxs-lookup"><span data-stu-id="58531-116">Add product dimensions</span></span>
1. <span data-ttu-id="58531-117">Ürün boyutları öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="58531-118">Bu örnekte ürün boyutlarının nasıl el ile girileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="58531-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="58531-119">Ayrıca, kullanmak istediğiniz ürün boyutu değerlerini içeren boyut, renk veya tarz grubunu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58531-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="58531-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-120">Click New.</span></span>
3. <span data-ttu-id="58531-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="58531-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="58531-122">Ebat alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="58531-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="58531-123">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="58531-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="58531-124">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58531-124">Click New.</span></span>
7. <span data-ttu-id="58531-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="58531-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="58531-126">Ebat alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="58531-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="58531-127">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="58531-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="58531-128">Renkler sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58531-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="58531-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-129">Click New.</span></span>
12. <span data-ttu-id="58531-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="58531-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="58531-131">Renk alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="58531-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="58531-132">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="58531-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="58531-133">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58531-133">Click New.</span></span>
16. <span data-ttu-id="58531-134">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="58531-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="58531-135">Renk alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="58531-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="58531-136">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="58531-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="58531-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-137">Click Save.</span></span>
20. <span data-ttu-id="58531-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="58531-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="58531-139">Ürün seçenekleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="58531-139">Generate product variants</span></span>
1. <span data-ttu-id="58531-140">Ürün çeşitleri öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-140">Click Product variants.</span></span>
2. <span data-ttu-id="58531-141">Çeşit önerilerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="58531-142">Tümünü seç'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="58531-142">Click Select all.</span></span>
    * <span data-ttu-id="58531-143">Bu örnekte tüm olası seçenekler dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="58531-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="58531-144">Bu seçeneklerin oluşturulması için sadece olası ürün boyutu kombinasyonlarının bir alt kümesi kullanılacaksa, bireysel girişleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58531-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="58531-145">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-145">Click Create.</span></span>
    * <span data-ttu-id="58531-146">Ürün boyutu değerlerinin kombinasyonuna dayalı olarak tüm seçenekleriniz için açıklamalar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58531-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="58531-147">Açıklamalar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="58531-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="58531-148">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58531-148">Click Save.</span></span>

