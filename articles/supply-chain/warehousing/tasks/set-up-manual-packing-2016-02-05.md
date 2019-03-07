---
title: Manuel ambalajlamayı ayarlama (Şubat 2016 ve Mayıs 2016)
description: Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b90b4a71e2447e942dbb4a9645ef93064da630d3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "347733"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="7933b-103">Manuel ambalajlamayı ayarlama (Şubat 2016 ve Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="7933b-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7933b-104">Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="7933b-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="7933b-105">Bu süreçte ambar çalışanları ürünleri depolama konumlarından çeker ve onları ürün miktarları ve türlerini denetledikleri bir paketleme istasyonuna taşır ve daha sonra onları uygun konteynerlere atar.</span><span class="sxs-lookup"><span data-stu-id="7933b-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="7933b-106">Bir konteyner tam olarak paketlendiğinde, bunu kapatıp çıkış noktalarına taşıyabilirler ve böylece ürünler sevk edilmeye hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="7933b-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="7933b-107">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7933b-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="7933b-108">Bu yordam yalnızca Dynamics 365 for Operations'ın Şubat 2016 ve Mayıs 2016 ve Mayıs 2016 sürümleri içindir.</span><span class="sxs-lookup"><span data-stu-id="7933b-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="7933b-109">Yerleşim profillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="7933b-109">Set up location profiles</span></span>
1. <span data-ttu-id="7933b-110">Ambar yönetimi > Kurulum > Ambar > Konum profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7933b-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="7933b-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-111">Click New.</span></span>
    * <span data-ttu-id="7933b-112">Konum profili paketleme istasyonları için kullanılır ve bir konum için bilgiler ve kurallar içerir.</span><span class="sxs-lookup"><span data-stu-id="7933b-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="7933b-113">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7933b-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="7933b-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7933b-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7933b-115">Konum biçimi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="7933b-116">Konum türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="7933b-117">Karışık öğelere izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="7933b-118">Karışık stok durumlarına izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="7933b-119">Toplu iş günleri alanı için geçersiz kılma kurallarında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="7933b-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7933b-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="7933b-121">Ambar yönetimi parametreleri ayarla</span><span class="sxs-lookup"><span data-stu-id="7933b-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="7933b-122">Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7933b-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="7933b-123">Paketleme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="7933b-124">Paketleme konumu için profil kimliği alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="7933b-125">Paketleme için kullanmak istediğiniz konum profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="7933b-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7933b-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="7933b-127">Konteyner türlerini ayarla</span><span class="sxs-lookup"><span data-stu-id="7933b-127">Set up container types</span></span>
1. <span data-ttu-id="7933b-128">Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7933b-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="7933b-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-129">Click New.</span></span>
    * <span data-ttu-id="7933b-130">Kullanılacak konteyner türlerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7933b-130">You can define the types of containers to use.</span></span> <span data-ttu-id="7933b-131">Konteynerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve ağırlık da dahil olmak üzere belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7933b-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="7933b-132">Öznitelikler, konteyner türüne ek boyutlar eklemenize olanak sağlayan özelleştirilmiş alanlardır.</span><span class="sxs-lookup"><span data-stu-id="7933b-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="7933b-133">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="7933b-134">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7933b-135">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="7933b-136">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="7933b-137">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="7933b-138">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="7933b-139">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="7933b-140">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="7933b-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-141">Click Save.</span></span>
12. <span data-ttu-id="7933b-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7933b-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="7933b-143">Paketleme profilleri ayarla</span><span class="sxs-lookup"><span data-stu-id="7933b-143">Set up packing profiles</span></span>
1. <span data-ttu-id="7933b-144">Ambar yönetimi > Kurulum > Sevk > Sevk profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7933b-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="7933b-145">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-145">Click New.</span></span>
3. <span data-ttu-id="7933b-146">Paketleme profili kimliği alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="7933b-147">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7933b-148">Konteyner kapatma profili kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="7933b-149">Bir konteyner kapatma profil kimliği isteğe bağlıdır ve bu paketleme profili için varsayılan konteyner kapatma profilidir.</span><span class="sxs-lookup"><span data-stu-id="7933b-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="7933b-150">Konteyner kimliği modu alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="7933b-151">Bu seçenek, bir konteyner oluşturulduğunda bir konteyner kimliğinin otomatik olarak mı oluşturulacağını yoksa konteyner kimliğinin el ile mi oluşturulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="7933b-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="7933b-152">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="7933b-153">Yeni konteyner türü oluşturulduğunda varsayılan olarak bu konteyner türü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7933b-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="7933b-154">Konteyner kapatmada konteyneri otomatik oluştur onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="7933b-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-155">Click Save.</span></span>
10. <span data-ttu-id="7933b-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7933b-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="7933b-157">Konteyner kapanış profilleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="7933b-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="7933b-158">Ambar yönetimi > Kurulum > Konteynerler > Konteyner kapanış profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7933b-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="7933b-159">Konteyner kapanış profilleri, bir konteyner kapandığında ne olacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7933b-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="7933b-160">Birden fazla konteyner kapatma profili ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7933b-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="7933b-161">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-161">Click New.</span></span>
3. <span data-ttu-id="7933b-162">Konteyner kapanış profili kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="7933b-163">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7933b-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7933b-164">Manifesto yeri alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="7933b-165">Sevk irsaliyesinin konteyner kapatmasında mı yoksa sevkiyatın onaylanmasında mı gerçekleşeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7933b-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="7933b-166">Manifestolamak Taşımacılık yönetimini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7933b-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="7933b-167">Manifestolamanın çalışması için taşımacılık motorunda uygulanmış olması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7933b-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="7933b-168">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="7933b-169">Son sevkiyat alanı için varsayılan konum alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="7933b-170">Bu, konteynerler kapatıldıktan sonra ürünlerin taşınacağı konum olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7933b-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="7933b-171">Bu konumun Ambar parametrelerinde tanımlanmış bir konum profili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7933b-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="7933b-172">Ağırlık birimi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7933b-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="7933b-173">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7933b-173">Click Save.</span></span>

