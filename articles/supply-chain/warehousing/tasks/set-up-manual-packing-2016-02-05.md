--- 
title: "El ile ambalajlamayı ayarlama (yalnızca Şubat ve Mayıs 2016)"
description: "Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 31b689b6c31563f24892525eed5911af3a35bd51
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="f7d2e-103">El ile ambalajlamayı ayarlama (yalnızca Şubat ve Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="f7d2e-103">Set up manual packing (February & May 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7d2e-104">Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="f7d2e-105">Bu süreçte ambar çalışanları ürünleri depolama konumlarından çeker ve onları ürün miktarları ve türlerini denetledikleri bir paketleme istasyonuna taşır ve daha sonra onları uygun konteynerlere atar.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="f7d2e-106">Bir konteyner tam olarak paketlendiğinde, bunu kapatıp çıkış noktalarına taşıyabilirler ve böylece ürünler sevk edilmeye hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="f7d2e-107">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="f7d2e-108">Yerleşim profillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="f7d2e-108">Set up location profiles</span></span>
1. <span data-ttu-id="f7d2e-109">Ambar yönetimi > Kurulum > Ambar > Konum profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="f7d2e-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-110">Click New.</span></span>
    * <span data-ttu-id="f7d2e-111">Konum profili paketleme istasyonları için kullanılır ve bir konum için bilgiler ve kurallar içerir.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="f7d2e-112">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="f7d2e-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f7d2e-114">Konum biçimi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="f7d2e-115">Konum türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="f7d2e-116">Karışık öğelere izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="f7d2e-117">Karışık stok durumlarına izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="f7d2e-118">Toplu iş günleri alanı için geçersiz kılma kurallarında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="f7d2e-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="f7d2e-120">Ambar yönetimi parametreleri ayarla</span><span class="sxs-lookup"><span data-stu-id="f7d2e-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="f7d2e-121">Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="f7d2e-122">Paketleme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="f7d2e-123">Paketleme konumu için profil kimliği alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d2e-124">Paketleme için kullanmak istediğiniz konum profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="f7d2e-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="f7d2e-126">Konteyner türlerini ayarla</span><span class="sxs-lookup"><span data-stu-id="f7d2e-126">Set up container types</span></span>
1. <span data-ttu-id="f7d2e-127">Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="f7d2e-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-128">Click New.</span></span>
    * <span data-ttu-id="f7d2e-129">Kullanılacak konteyner türlerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-129">You can define the types of containers to use.</span></span> <span data-ttu-id="f7d2e-130">Konteynerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve ağırlık da dahil olmak üzere belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="f7d2e-131">Öznitelikler, konteyner türüne ek boyutlar eklemenize olanak sağlayan özelleştirilmiş alanlardır.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="f7d2e-132">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="f7d2e-133">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d2e-134">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="f7d2e-135">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="f7d2e-136">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="f7d2e-137">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="f7d2e-138">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="f7d2e-139">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="f7d2e-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-140">Click Save.</span></span>
12. <span data-ttu-id="f7d2e-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="f7d2e-142">Paketleme profilleri ayarla</span><span class="sxs-lookup"><span data-stu-id="f7d2e-142">Set up packing profiles</span></span>
1. <span data-ttu-id="f7d2e-143">Ambar yönetimi > Kurulum > Sevk > Sevk profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="f7d2e-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-144">Click New.</span></span>
3. <span data-ttu-id="f7d2e-145">Paketleme profili kimliği alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="f7d2e-146">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d2e-147">Konteyner kapatma profili kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d2e-148">Bir konteyner kapatma profil kimliği isteğe bağlıdır ve bu paketleme profili için varsayılan konteyner kapatma profilidir.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="f7d2e-149">Konteyner kimliği modu alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="f7d2e-150">Bu seçenek, bir konteyner oluşturulduğunda bir konteyner kimliğinin otomatik olarak mı oluşturulacağını yoksa konteyner kimliğinin el ile mi oluşturulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="f7d2e-151">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d2e-152">Yeni konteyner türü oluşturulduğunda varsayılan olarak bu konteyner türü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="f7d2e-153">Konteyner kapatmada konteyneri otomatik oluştur onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="f7d2e-154">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-154">Click Save.</span></span>
10. <span data-ttu-id="f7d2e-155">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="f7d2e-156">Konteyner kapanış profilleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="f7d2e-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="f7d2e-157">Ambar yönetimi > Kurulum > Konteynerler > Konteyner kapanış profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="f7d2e-158">Konteyner kapanış profilleri, bir konteyner kapandığında ne olacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="f7d2e-159">Birden fazla konteyner kapatma profili ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="f7d2e-160">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-160">Click New.</span></span>
3. <span data-ttu-id="f7d2e-161">Konteyner kapanış profili kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="f7d2e-162">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7d2e-163">Manifesto yeri alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="f7d2e-164">Sevk irsaliyesinin konteyner kapatmasında mı yoksa sevkiyatın onaylanmasında mı gerçekleşeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="f7d2e-165">Manifestolamak Taşımacılık yönetimini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="f7d2e-166">Manifestolamanın çalışması için taşımacılık motorunda uygulanmış olması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="f7d2e-167">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="f7d2e-168">Son sevkiyat alanı için varsayılan konum alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="f7d2e-169">Bu, konteynerler kapatıldıktan sonra ürünlerin taşınacağı konum olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="f7d2e-170">Bu konumun Ambar parametrelerinde tanımlanmış bir konum profili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="f7d2e-171">Ağırlık birimi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="f7d2e-172">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7d2e-172">Click Save.</span></span>


