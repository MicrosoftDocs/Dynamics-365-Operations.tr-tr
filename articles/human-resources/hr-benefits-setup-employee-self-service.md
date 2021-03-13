---
title: Personel self servisini yapılandırma
description: Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114590"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="bc968-103">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bc968-103">Configure employee self service</span></span>

<span data-ttu-id="bc968-104">Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bc968-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="bc968-105">Kazanç planı kutucukları kullanıcıları uygun oldukları kazanç planlarına yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="bc968-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="bc968-106">Kazanç planları kutucuğu ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc968-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="bc968-107">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bc968-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bc968-108">**Kazanç planları kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bc968-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bc968-109">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="bc968-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bc968-110">Alan</span><span class="sxs-lookup"><span data-stu-id="bc968-110">Field</span></span> | <span data-ttu-id="bc968-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc968-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bc968-112">**Kutucuk kodu**</span><span class="sxs-lookup"><span data-stu-id="bc968-112">**Tile ID**</span></span> | <span data-ttu-id="bc968-113">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="bc968-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bc968-114">**Kutucuk etiketi metni**</span><span class="sxs-lookup"><span data-stu-id="bc968-114">**Tile label text**</span></span> | <span data-ttu-id="bc968-115">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="bc968-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="bc968-116">**Tanım**</span><span class="sxs-lookup"><span data-stu-id="bc968-116">**Description**</span></span> | <span data-ttu-id="bc968-117">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="bc968-117">A description of the tile.</span></span> |
   | <span data-ttu-id="bc968-118">**Internet adresi**</span><span class="sxs-lookup"><span data-stu-id="bc968-118">**Internet address**</span></span> | <span data-ttu-id="bc968-119">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="bc968-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bc968-120">**Kutucuk boyutu**</span><span class="sxs-lookup"><span data-stu-id="bc968-120">**Tile size**</span></span> | <span data-ttu-id="bc968-121">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="bc968-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bc968-122">**Hedef**</span><span class="sxs-lookup"><span data-stu-id="bc968-122">**Target**</span></span> | <span data-ttu-id="bc968-123">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc968-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bc968-124">**Kutucuk arka plan görüntüsü**</span><span class="sxs-lookup"><span data-stu-id="bc968-124">**Tile background image**</span></span> | <span data-ttu-id="bc968-125">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="bc968-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bc968-126">**Başlangıç**</span><span class="sxs-lookup"><span data-stu-id="bc968-126">**Start**</span></span> | <span data-ttu-id="bc968-127">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc968-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bc968-128">**End**</span><span class="sxs-lookup"><span data-stu-id="bc968-128">**End**</span></span> | <span data-ttu-id="bc968-129">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc968-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bc968-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bc968-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="bc968-131">Esnek kredi planı kutucuğu ayarla</span><span class="sxs-lookup"><span data-stu-id="bc968-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="bc968-132">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bc968-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="bc968-133">**Esnek kredi planı kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bc968-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="bc968-134">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="bc968-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bc968-135">Alan</span><span class="sxs-lookup"><span data-stu-id="bc968-135">Field</span></span> | <span data-ttu-id="bc968-136">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc968-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bc968-137">**Kutucuk kodu**</span><span class="sxs-lookup"><span data-stu-id="bc968-137">**Tile ID**</span></span> | <span data-ttu-id="bc968-138">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="bc968-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="bc968-139">**Kutucuk etiketi metni**</span><span class="sxs-lookup"><span data-stu-id="bc968-139">**Tile label text**</span></span> | <span data-ttu-id="bc968-140">Self serviste kutucuk için görüntülenecek metin.</span><span class="sxs-lookup"><span data-stu-id="bc968-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="bc968-141">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="bc968-141">**Description**</span></span> | <span data-ttu-id="bc968-142">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="bc968-142">A description of the tile.</span></span> |
   | <span data-ttu-id="bc968-143">**Internet adresi**</span><span class="sxs-lookup"><span data-stu-id="bc968-143">**Internet address**</span></span> | <span data-ttu-id="bc968-144">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="bc968-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="bc968-145">**Kutucuk boyutu**</span><span class="sxs-lookup"><span data-stu-id="bc968-145">**Tile size**</span></span> | <span data-ttu-id="bc968-146">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="bc968-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="bc968-147">**Hedef**</span><span class="sxs-lookup"><span data-stu-id="bc968-147">**Target**</span></span> | <span data-ttu-id="bc968-148">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc968-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="bc968-149">**Kutucuk arka plan görüntüsü**</span><span class="sxs-lookup"><span data-stu-id="bc968-149">**Tile background image**</span></span> | <span data-ttu-id="bc968-150">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="bc968-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="bc968-151">**Başlangıç**</span><span class="sxs-lookup"><span data-stu-id="bc968-151">**Start**</span></span> | <span data-ttu-id="bc968-152">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc968-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="bc968-153">**End**</span><span class="sxs-lookup"><span data-stu-id="bc968-153">**End**</span></span> | <span data-ttu-id="bc968-154">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bc968-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="bc968-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bc968-155">Select **Save**.</span></span>
