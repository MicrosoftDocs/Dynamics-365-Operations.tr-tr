---
title: Tüketim esasına göre amortisman
description: Bu makalede, amortismanın Tüketim yöntemi hakkında genel bir bakış verilmektedir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840709"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="4d7ef-103">Tüketim esasına göre amortisman</span><span class="sxs-lookup"><span data-stu-id="4d7ef-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d7ef-104">Bu makalede, amortismanın Tüketim yöntemi hakkında genel bir bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="4d7ef-105">Sabit kıymetler için bir amortisman profili ayarladıysanız ve **Amortisman profilleri** sayfasındaki **Yöntem** alanında **Tüketim** seçeneğini işaretlerseniz, sabit kıymetler kullanımlarına göre amortisman profili atanır.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="4d7ef-106">**Amortisman profilleri** sayfasında yüzdeleri ve aralıkları ayarlamak zorunda değilsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="4d7ef-107">Tüketim yöntemini kullanan bir amortisman profili oluşturduktan sonra yöntemi çeşitli şekillerde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="4d7ef-108">Tüketim amortismanını ayarlayın ve kullanın</span><span class="sxs-lookup"><span data-stu-id="4d7ef-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="4d7ef-109">**Amortisman profilleri** sayfasında, bir amortisman profili oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="4d7ef-110">Tüketim hesaplamaları için amortisman profilinin bir kimlik ve bir adı olmalıdır ve **Yöntemi** alanından **Tüketim** seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="4d7ef-111">**Tüketim faktörleri** sayfasında, tüketim faktörlerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="4d7ef-112">Her tüketim faktörünün bir kimliği ve bir adı ve bir yüzde ya da bir miktar olarak belirtilmiş bir tüketim faktörü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="4d7ef-113">**Tüketim birimleri** sayfası, tüketim birimleri ayarlama.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="4d7ef-114">Her tüketim biriminin bir kimliği ve bir adı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="4d7ef-115">Amortisman birimleri, **Tüketim amortismanı** sayfasında tüketim amortismanını hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="4d7ef-116">Birimlere örnek olarak, kilometre (km), kilogram (kg) ve saat verilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="4d7ef-117">**Sabit kıymetler** sayfası üzerinde, sabit kıymetleri tek ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="4d7ef-118">Her bir sabit kıymet için değer modelleri ve amortisman profilleri olan amortisman defterleri seçin.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="4d7ef-119">Eğer sabit kıymetlerinizden herhangi biri Tüketim yöntemine dayalı amortisman modelleri kullanıyorsa, tüketim amortismanı için değer modelleri ve amortisman defterleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="4d7ef-120">Bu ayar ya **Değer modelleri** sayfasındaki **Amortisman** sekmesinde ya da **Amortisman profili** sayfasında **Genel** hızlı sekmesinde yapılır..</span><span class="sxs-lookup"><span data-stu-id="4d7ef-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="4d7ef-121">Çok sayıda sabit kıymet için aynı değer modelini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="4d7ef-122">Amortisman profilleri, her sabit kıymet için seçtiğiniz değer modeli veya amortisman defterinin bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="4d7ef-123">Amortisman profillerini doğrudan **Sabit kıymetler** sayfasında ekleyemez veya değiştirmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="4d7ef-124">Amortisman profillerini yalnızca **amortisman defterleri** sayfa değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="4d7ef-125">**Değer modelleri** sayfasi veya **Amortisman defterleri** sayfasında, **Tüketim esasına göre amortisman** alan grubunda, aşağıdaki alanlara bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="4d7ef-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="4d7ef-126">Tüketim faktörü</span><span class="sxs-lookup"><span data-stu-id="4d7ef-126">Consumption factor</span></span>
    -   <span data-ttu-id="4d7ef-127">Birim</span><span class="sxs-lookup"><span data-stu-id="4d7ef-127">Unit</span></span>
    -   <span data-ttu-id="4d7ef-128">Birim amortisman</span><span class="sxs-lookup"><span data-stu-id="4d7ef-128">Unit depreciation</span></span>
    -   <span data-ttu-id="4d7ef-129">Tahmini tüketim</span><span class="sxs-lookup"><span data-stu-id="4d7ef-129">Estimated consumption</span></span>

    <span data-ttu-id="4d7ef-130">**Deftere nakledilen tüketim** alanı deftere sabit kıymet ve değer modelinin birleşimi için veya amortisman defter için nakledilmiş tüketim amortismanını birimleriyle gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="4d7ef-131">Bu alandaki değeri el ile güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="4d7ef-132">Örnekler</span><span class="sxs-lookup"><span data-stu-id="4d7ef-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="4d7ef-133">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4d7ef-133">Example 1</span></span>

<span data-ttu-id="4d7ef-134">Aşağıdaki tüketim faktörü 31 Ocak için oluşturulmuştur:</span><span class="sxs-lookup"><span data-stu-id="4d7ef-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="4d7ef-135">Miktar 1,000'dir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="4d7ef-136">Sabit kıymet için belirtilmiş birim amortisman fiyatı 1,5'tur.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="4d7ef-137">31 Ocak Amortisman teklifi aşağıdaki gibidir: Miktar × Birim amortismanı 1.000 × 1,5 = 1.500 Eğer sabit kıymet için belirtilen faktör bir yüzde faktörüyse, **Tüketim tahmini** alanındaki sabit kıymet için değer modeli tahminin miktarı, seçilen bitiş tarihi için ayarlanmış oran ile çarpılır.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="4d7ef-138">Sonuçta elde edilen miktar sonra dönem için amortisman miktarı olarak önerilir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="4d7ef-139">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4d7ef-139">Example 2</span></span>

<span data-ttu-id="4d7ef-140">Aşağıdaki tüketim amortismanına yönelik faktör, 31 Ocak için oluşturulmuştur:</span><span class="sxs-lookup"><span data-stu-id="4d7ef-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="4d7ef-141">Yüzde, yüzde 10'dur.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="4d7ef-142">Sabit kıymet için belirtilmiş birim amortisman fiyatı 1,5'tur.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="4d7ef-143">Sabit kıymetin tahmini miktarı 2.000'dir.</span><span class="sxs-lookup"><span data-stu-id="4d7ef-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="4d7ef-144">31 Ocak tarihindeki amortisman teklifi aşağıdaki gibidir: Tahmini miktarı x Yüzde × Birim amortisman 2,000 × ,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="4d7ef-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



