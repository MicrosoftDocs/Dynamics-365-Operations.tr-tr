---
title: Manuel ambalajlamayı ayarlama (Şubat 2016 ve Mayıs 2016)
description: Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8486ca90da44bb4c05c71a2babfc79445ed2dd12
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216908"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="d88b0-103">Manuel ambalajlamayı ayarlama (Şubat 2016 ve Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="d88b0-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d88b0-104">Paketleme işlemi, doğrulamanıza ve ürünleri konteynerlere yerleştirmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="d88b0-105">Bu süreçte ambar çalışanları ürünleri depolama konumlarından çeker ve onları ürün miktarları ve türlerini denetledikleri bir paketleme istasyonuna taşır ve daha sonra onları uygun konteynerlere atar.</span><span class="sxs-lookup"><span data-stu-id="d88b0-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="d88b0-106">Bir konteyner tam olarak paketlendiğinde, bunu kapatıp çıkış noktalarına taşıyabilirler ve böylece ürünler sevk edilmeye hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="d88b0-107">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d88b0-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="d88b0-108">Bu yordam yalnızca Dynamics 365 for Operations'ın Şubat 2016 ve Mayıs 2016 ve Mayıs 2016 sürümleri içindir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="d88b0-109">Yerleşim profillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="d88b0-109">Set up location profiles</span></span>
1. <span data-ttu-id="d88b0-110">Ambar yönetimi > Kurulum > Ambar > Konum profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="d88b0-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-111">Click New.</span></span>
    * <span data-ttu-id="d88b0-112">Konum profili paketleme istasyonları için kullanılır ve bir konum için bilgiler ve kurallar içerir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="d88b0-113">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="d88b0-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d88b0-115">Konum biçimi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="d88b0-116">Konum türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="d88b0-117">Karışık öğelere izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d88b0-118">Karışık stok durumlarına izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d88b0-119">Toplu iş günleri alanı için geçersiz kılma kurallarında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="d88b0-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="d88b0-121">Ambar yönetimi parametreleri ayarla</span><span class="sxs-lookup"><span data-stu-id="d88b0-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="d88b0-122">Ambar yönetimi > Kurulum > Ambar yönetimi parametreleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="d88b0-123">Paketleme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="d88b0-124">Paketleme konumu için profil kimliği alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="d88b0-125">Paketleme için kullanmak istediğiniz konum profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="d88b0-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="d88b0-127">Konteyner türlerini ayarla</span><span class="sxs-lookup"><span data-stu-id="d88b0-127">Set up container types</span></span>
1. <span data-ttu-id="d88b0-128">Ambar yönetimi > Kurulum > Konteynerler > Konteyner türleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="d88b0-129">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-129">Click New.</span></span>
    * <span data-ttu-id="d88b0-130">Kullanılacak konteyner türlerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88b0-130">You can define the types of containers to use.</span></span> <span data-ttu-id="d88b0-131">Konteynerin fiziksel boyutlarını, dara ağırlığı, maksimum ağırlık, maksimum hacim, uzunluk, genişlik ve ağırlık da dahil olmak üzere belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88b0-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="d88b0-132">Öznitelikler, konteyner türüne ek boyutlar eklemenize olanak sağlayan özelleştirilmiş alanlardır.</span><span class="sxs-lookup"><span data-stu-id="d88b0-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="d88b0-133">Konteyner türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="d88b0-134">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d88b0-135">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="d88b0-136">Maksimum ağırlık alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="d88b0-137">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="d88b0-138">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="d88b0-139">Genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="d88b0-140">Yükseklik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="d88b0-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-141">Click Save.</span></span>
12. <span data-ttu-id="d88b0-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="d88b0-143">Paketleme profilleri ayarla</span><span class="sxs-lookup"><span data-stu-id="d88b0-143">Set up packing profiles</span></span>
1. <span data-ttu-id="d88b0-144">Ambar yönetimi > Kurulum > Sevk > Sevk profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="d88b0-145">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-145">Click New.</span></span>
3. <span data-ttu-id="d88b0-146">Paketleme profili kimliği alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d88b0-147">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d88b0-148">Konteyner kapatma profili kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d88b0-149">Bir konteyner kapatma profil kimliği isteğe bağlıdır ve bu paketleme profili için varsayılan konteyner kapatma profilidir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="d88b0-150">Konteyner kimliği modu alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="d88b0-151">Bu seçenek, bir konteyner oluşturulduğunda bir konteyner kimliğinin otomatik olarak mı oluşturulacağını yoksa konteyner kimliğinin el ile mi oluşturulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="d88b0-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="d88b0-152">Konteyner türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="d88b0-153">Yeni konteyner türü oluşturulduğunda varsayılan olarak bu konteyner türü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d88b0-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="d88b0-154">Konteyner kapatmada konteyneri otomatik oluştur onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="d88b0-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-155">Click Save.</span></span>
10. <span data-ttu-id="d88b0-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="d88b0-157">Konteyner kapanış profilleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="d88b0-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="d88b0-158">Ambar yönetimi > Kurulum > Konteynerler > Konteyner kapanış profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="d88b0-159">Konteyner kapanış profilleri, bir konteyner kapandığında ne olacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d88b0-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="d88b0-160">Birden fazla konteyner kapatma profili ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88b0-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="d88b0-161">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-161">Click New.</span></span>
3. <span data-ttu-id="d88b0-162">Konteyner kapanış profili kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d88b0-163">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d88b0-164">Manifesto yeri alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="d88b0-165">Sevk irsaliyesinin konteyner kapatmasında mı yoksa sevkiyatın onaylanmasında mı gerçekleşeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="d88b0-166">Manifestolamak Taşımacılık yönetimini gerektirir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="d88b0-167">Manifestolamanın çalışması için taşımacılık motorunda uygulanmış olması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d88b0-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="d88b0-168">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="d88b0-169">Son sevkiyat alanı için varsayılan konum alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="d88b0-170">Bu, konteynerler kapatıldıktan sonra ürünlerin taşınacağı konum olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d88b0-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="d88b0-171">Bu konumun Ambar parametrelerinde tanımlanmış bir konum profili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d88b0-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="d88b0-172">Ağırlık birimi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d88b0-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="d88b0-173">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88b0-173">Click Save.</span></span>

