---
title: Personel Self Servisi yapılandır
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010873"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="3c092-102">Personel Self Servisi yapılandır</span><span class="sxs-lookup"><span data-stu-id="3c092-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3c092-103">Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3c092-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="3c092-104">Kazanç planı, doğrudan kullanıcıları kaydolmaya uygun oldukları kazanç planlarına göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="3c092-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="3c092-105">Bir rol merkezi kutucuğu ayarla</span><span class="sxs-lookup"><span data-stu-id="3c092-105">Set up a role center tile</span></span>

1. <span data-ttu-id="3c092-106">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3c092-107">**Rol merkezi kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3c092-108">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="3c092-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3c092-109">Alan</span><span class="sxs-lookup"><span data-stu-id="3c092-109">Field</span></span> | <span data-ttu-id="3c092-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c092-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3c092-111">Kutucuk kodu</span><span class="sxs-lookup"><span data-stu-id="3c092-111">Tile ID</span></span> | <span data-ttu-id="3c092-112">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3c092-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3c092-113">Kutucuk etiketi metni</span><span class="sxs-lookup"><span data-stu-id="3c092-113">Tile label text</span></span> | <span data-ttu-id="3c092-114">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="3c092-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="3c092-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c092-115">Description</span></span> | <span data-ttu-id="3c092-116">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3c092-116">A description of the tile.</span></span> |
   | <span data-ttu-id="3c092-117">Internet adresi</span><span class="sxs-lookup"><span data-stu-id="3c092-117">Internet address</span></span> | <span data-ttu-id="3c092-118">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="3c092-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3c092-119">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="3c092-119">Tile size</span></span> | <span data-ttu-id="3c092-120">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="3c092-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3c092-121">Hedef</span><span class="sxs-lookup"><span data-stu-id="3c092-121">Target</span></span> | <span data-ttu-id="3c092-122">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c092-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3c092-123">Kutucuk arka plan görüntüsü</span><span class="sxs-lookup"><span data-stu-id="3c092-123">Tile background image</span></span> | <span data-ttu-id="3c092-124">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="3c092-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3c092-125">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="3c092-125">Start</span></span> | <span data-ttu-id="3c092-126">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c092-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3c092-127">End</span><span class="sxs-lookup"><span data-stu-id="3c092-127">End</span></span> | <span data-ttu-id="3c092-128">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c092-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3c092-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="3c092-130">Kazanç planları kutucuğu ayarlama</span><span class="sxs-lookup"><span data-stu-id="3c092-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="3c092-131">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3c092-132">**Kazanç planları kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3c092-133">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="3c092-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3c092-134">Alan</span><span class="sxs-lookup"><span data-stu-id="3c092-134">Field</span></span> | <span data-ttu-id="3c092-135">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c092-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3c092-136">Kutucuk kodu</span><span class="sxs-lookup"><span data-stu-id="3c092-136">Tile ID</span></span> | <span data-ttu-id="3c092-137">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3c092-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3c092-138">Kutucuk etiketi metni</span><span class="sxs-lookup"><span data-stu-id="3c092-138">Tile label text</span></span> | <span data-ttu-id="3c092-139">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="3c092-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="3c092-140">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c092-140">Description</span></span> | <span data-ttu-id="3c092-141">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3c092-141">A description of the tile.</span></span> |
   | <span data-ttu-id="3c092-142">Internet adresi</span><span class="sxs-lookup"><span data-stu-id="3c092-142">Internet address</span></span> | <span data-ttu-id="3c092-143">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="3c092-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3c092-144">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="3c092-144">Tile size</span></span> | <span data-ttu-id="3c092-145">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="3c092-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3c092-146">Hedef</span><span class="sxs-lookup"><span data-stu-id="3c092-146">Target</span></span> | <span data-ttu-id="3c092-147">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c092-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3c092-148">Kutucuk arka plan görüntüsü</span><span class="sxs-lookup"><span data-stu-id="3c092-148">Tile background image</span></span> | <span data-ttu-id="3c092-149">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="3c092-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3c092-150">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="3c092-150">Start</span></span> | <span data-ttu-id="3c092-151">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c092-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3c092-152">End</span><span class="sxs-lookup"><span data-stu-id="3c092-152">End</span></span> | <span data-ttu-id="3c092-153">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c092-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3c092-154">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="3c092-155">Esnek kredi planı kutucuğu ayarla</span><span class="sxs-lookup"><span data-stu-id="3c092-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="3c092-156">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3c092-157">**Esnek kredi planı kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3c092-158">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="3c092-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3c092-159">Alan</span><span class="sxs-lookup"><span data-stu-id="3c092-159">Field</span></span> | <span data-ttu-id="3c092-160">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c092-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3c092-161">Kutucuk kodu</span><span class="sxs-lookup"><span data-stu-id="3c092-161">Tile ID</span></span> | <span data-ttu-id="3c092-162">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3c092-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3c092-163">Kutucuk etiketi metni</span><span class="sxs-lookup"><span data-stu-id="3c092-163">Tile label text</span></span> | <span data-ttu-id="3c092-164">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="3c092-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="3c092-165">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c092-165">Description</span></span> | <span data-ttu-id="3c092-166">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3c092-166">A description of the tile.</span></span> |
   | <span data-ttu-id="3c092-167">Internet adresi</span><span class="sxs-lookup"><span data-stu-id="3c092-167">Internet address</span></span> | <span data-ttu-id="3c092-168">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="3c092-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3c092-169">Kutucuk boyutu</span><span class="sxs-lookup"><span data-stu-id="3c092-169">Tile size</span></span> | <span data-ttu-id="3c092-170">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="3c092-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3c092-171">Hedef</span><span class="sxs-lookup"><span data-stu-id="3c092-171">Target</span></span> | <span data-ttu-id="3c092-172">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c092-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3c092-173">Kutucuk arka plan görüntüsü</span><span class="sxs-lookup"><span data-stu-id="3c092-173">Tile background image</span></span> | <span data-ttu-id="3c092-174">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="3c092-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3c092-175">Başlangıç</span><span class="sxs-lookup"><span data-stu-id="3c092-175">Start</span></span> | <span data-ttu-id="3c092-176">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c092-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3c092-177">End</span><span class="sxs-lookup"><span data-stu-id="3c092-177">End</span></span> | <span data-ttu-id="3c092-178">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3c092-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3c092-179">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3c092-179">Select **Save**.</span></span>
