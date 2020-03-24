---
title: Personel self servisini yapılandırma
description: Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092672"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="32e5d-103">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="32e5d-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="32e5d-104">Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="32e5d-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="32e5d-105">Kazanç planı, doğrudan kullanıcıları kaydolmaya uygun oldukları kazanç planlarına göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="32e5d-106">Bir rol merkezi kutucuğu ayarla</span><span class="sxs-lookup"><span data-stu-id="32e5d-106">Set up a role center tile</span></span>

1. <span data-ttu-id="32e5d-107">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="32e5d-108">**Rol merkezi kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="32e5d-109">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="32e5d-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="32e5d-110">Alan</span><span class="sxs-lookup"><span data-stu-id="32e5d-110">Field</span></span> | <span data-ttu-id="32e5d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="32e5d-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="32e5d-112">Kutucuk kodu</span><span class="sxs-lookup"><span data-stu-id="32e5d-112">Tile ID</span></span> | <span data-ttu-id="32e5d-113">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="32e5d-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="32e5d-114">Kutucuk etiketi metni</span><span class="sxs-lookup"><span data-stu-id="32e5d-114">Tile label text</span></span> | <span data-ttu-id="32e5d-115">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="32e5d-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="32e5d-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="32e5d-116">Description</span></span> | <span data-ttu-id="32e5d-117">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="32e5d-117">A description of the tile.</span></span> |
   | <span data-ttu-id="32e5d-118">Internet adresi</span><span class="sxs-lookup"><span data-stu-id="32e5d-118">Internet address</span></span> | <span data-ttu-id="32e5d-119">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="32e5d-120">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="32e5d-120">Tile size</span></span> | <span data-ttu-id="32e5d-121">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="32e5d-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="32e5d-122">Hedef</span><span class="sxs-lookup"><span data-stu-id="32e5d-122">Target</span></span> | <span data-ttu-id="32e5d-123">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32e5d-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="32e5d-124">Kutucuk arka plan görüntüsü</span><span class="sxs-lookup"><span data-stu-id="32e5d-124">Tile background image</span></span> | <span data-ttu-id="32e5d-125">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="32e5d-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="32e5d-126">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="32e5d-126">Start</span></span> | <span data-ttu-id="32e5d-127">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="32e5d-128">End</span><span class="sxs-lookup"><span data-stu-id="32e5d-128">End</span></span> | <span data-ttu-id="32e5d-129">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="32e5d-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="32e5d-131">Kazanç planları kutucuğu ayarlama</span><span class="sxs-lookup"><span data-stu-id="32e5d-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="32e5d-132">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="32e5d-133">**Kazanç planları kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="32e5d-134">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="32e5d-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="32e5d-135">Alan</span><span class="sxs-lookup"><span data-stu-id="32e5d-135">Field</span></span> | <span data-ttu-id="32e5d-136">Tanım</span><span class="sxs-lookup"><span data-stu-id="32e5d-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="32e5d-137">Kutucuk kodu</span><span class="sxs-lookup"><span data-stu-id="32e5d-137">Tile ID</span></span> | <span data-ttu-id="32e5d-138">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="32e5d-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="32e5d-139">Kutucuk etiketi metni</span><span class="sxs-lookup"><span data-stu-id="32e5d-139">Tile label text</span></span> | <span data-ttu-id="32e5d-140">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="32e5d-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="32e5d-141">Tanım</span><span class="sxs-lookup"><span data-stu-id="32e5d-141">Description</span></span> | <span data-ttu-id="32e5d-142">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="32e5d-142">A description of the tile.</span></span> |
   | <span data-ttu-id="32e5d-143">Internet adresi</span><span class="sxs-lookup"><span data-stu-id="32e5d-143">Internet address</span></span> | <span data-ttu-id="32e5d-144">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="32e5d-145">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="32e5d-145">Tile size</span></span> | <span data-ttu-id="32e5d-146">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="32e5d-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="32e5d-147">Hedef</span><span class="sxs-lookup"><span data-stu-id="32e5d-147">Target</span></span> | <span data-ttu-id="32e5d-148">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32e5d-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="32e5d-149">Kutucuk arka plan görüntüsü</span><span class="sxs-lookup"><span data-stu-id="32e5d-149">Tile background image</span></span> | <span data-ttu-id="32e5d-150">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="32e5d-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="32e5d-151">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="32e5d-151">Start</span></span> | <span data-ttu-id="32e5d-152">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="32e5d-153">End</span><span class="sxs-lookup"><span data-stu-id="32e5d-153">End</span></span> | <span data-ttu-id="32e5d-154">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="32e5d-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="32e5d-156">Esnek kredi planı kutucuğu ayarla</span><span class="sxs-lookup"><span data-stu-id="32e5d-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="32e5d-157">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="32e5d-158">**Esnek kredi planı kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="32e5d-159">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="32e5d-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="32e5d-160">Alan</span><span class="sxs-lookup"><span data-stu-id="32e5d-160">Field</span></span> | <span data-ttu-id="32e5d-161">Tanım</span><span class="sxs-lookup"><span data-stu-id="32e5d-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="32e5d-162">Kutucuk kodu</span><span class="sxs-lookup"><span data-stu-id="32e5d-162">Tile ID</span></span> | <span data-ttu-id="32e5d-163">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="32e5d-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="32e5d-164">Kutucuk etiketi metni</span><span class="sxs-lookup"><span data-stu-id="32e5d-164">Tile label text</span></span> | <span data-ttu-id="32e5d-165">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="32e5d-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="32e5d-166">Tanım</span><span class="sxs-lookup"><span data-stu-id="32e5d-166">Description</span></span> | <span data-ttu-id="32e5d-167">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="32e5d-167">A description of the tile.</span></span> |
   | <span data-ttu-id="32e5d-168">Internet adresi</span><span class="sxs-lookup"><span data-stu-id="32e5d-168">Internet address</span></span> | <span data-ttu-id="32e5d-169">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="32e5d-170">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="32e5d-170">Tile size</span></span> | <span data-ttu-id="32e5d-171">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="32e5d-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="32e5d-172">Hedef</span><span class="sxs-lookup"><span data-stu-id="32e5d-172">Target</span></span> | <span data-ttu-id="32e5d-173">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32e5d-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="32e5d-174">Kutucuk arka plan görüntüsü</span><span class="sxs-lookup"><span data-stu-id="32e5d-174">Tile background image</span></span> | <span data-ttu-id="32e5d-175">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="32e5d-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="32e5d-176">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="32e5d-176">Start</span></span> | <span data-ttu-id="32e5d-177">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="32e5d-178">End</span><span class="sxs-lookup"><span data-stu-id="32e5d-178">End</span></span> | <span data-ttu-id="32e5d-179">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32e5d-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="32e5d-180">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32e5d-180">Select **Save**.</span></span>
