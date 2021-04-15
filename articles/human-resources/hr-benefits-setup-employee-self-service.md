---
title: Personel self servisini yapılandırma
description: Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797948"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="88f61-103">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="88f61-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88f61-104">Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="88f61-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="88f61-105">Kazanç planı kutucukları kullanıcıları uygun oldukları kazanç planlarına yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="88f61-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="88f61-106">Kazanç planları kutucuğu ayarlama</span><span class="sxs-lookup"><span data-stu-id="88f61-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="88f61-107">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="88f61-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="88f61-108">**Kazanç planları kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88f61-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="88f61-109">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="88f61-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="88f61-110">Alan</span><span class="sxs-lookup"><span data-stu-id="88f61-110">Field</span></span> | <span data-ttu-id="88f61-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="88f61-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="88f61-112">**Kutucuk kodu**</span><span class="sxs-lookup"><span data-stu-id="88f61-112">**Tile ID**</span></span> | <span data-ttu-id="88f61-113">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="88f61-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="88f61-114">**Kutucuk etiketi metni**</span><span class="sxs-lookup"><span data-stu-id="88f61-114">**Tile label text**</span></span> | <span data-ttu-id="88f61-115">Self serviste kutucuk için görüntülenecek metin</span><span class="sxs-lookup"><span data-stu-id="88f61-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="88f61-116">**Tanım**</span><span class="sxs-lookup"><span data-stu-id="88f61-116">**Description**</span></span> | <span data-ttu-id="88f61-117">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="88f61-117">A description of the tile.</span></span> |
   | <span data-ttu-id="88f61-118">**Internet adresi**</span><span class="sxs-lookup"><span data-stu-id="88f61-118">**Internet address**</span></span> | <span data-ttu-id="88f61-119">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="88f61-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="88f61-120">**Kutucuk boyutu**</span><span class="sxs-lookup"><span data-stu-id="88f61-120">**Tile size**</span></span> | <span data-ttu-id="88f61-121">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="88f61-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="88f61-122">**Hedef**</span><span class="sxs-lookup"><span data-stu-id="88f61-122">**Target**</span></span> | <span data-ttu-id="88f61-123">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88f61-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="88f61-124">**Kutucuk arka plan görüntüsü**</span><span class="sxs-lookup"><span data-stu-id="88f61-124">**Tile background image**</span></span> | <span data-ttu-id="88f61-125">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="88f61-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="88f61-126">**Başlangıç**</span><span class="sxs-lookup"><span data-stu-id="88f61-126">**Start**</span></span> | <span data-ttu-id="88f61-127">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="88f61-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="88f61-128">**End**</span><span class="sxs-lookup"><span data-stu-id="88f61-128">**End**</span></span> | <span data-ttu-id="88f61-129">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="88f61-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="88f61-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="88f61-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="88f61-131">Esnek kredi planı kutucuğu ayarla</span><span class="sxs-lookup"><span data-stu-id="88f61-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="88f61-132">**Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="88f61-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="88f61-133">**Esnek kredi planı kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88f61-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="88f61-134">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="88f61-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="88f61-135">Alan</span><span class="sxs-lookup"><span data-stu-id="88f61-135">Field</span></span> | <span data-ttu-id="88f61-136">Tanım</span><span class="sxs-lookup"><span data-stu-id="88f61-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="88f61-137">**Kutucuk kodu**</span><span class="sxs-lookup"><span data-stu-id="88f61-137">**Tile ID**</span></span> | <span data-ttu-id="88f61-138">Kutucuk için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="88f61-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="88f61-139">**Kutucuk etiketi metni**</span><span class="sxs-lookup"><span data-stu-id="88f61-139">**Tile label text**</span></span> | <span data-ttu-id="88f61-140">Self serviste kutucuk için görüntülenecek metin.</span><span class="sxs-lookup"><span data-stu-id="88f61-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="88f61-141">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="88f61-141">**Description**</span></span> | <span data-ttu-id="88f61-142">Kutucuğun bir açıklaması.</span><span class="sxs-lookup"><span data-stu-id="88f61-142">A description of the tile.</span></span> |
   | <span data-ttu-id="88f61-143">**Internet adresi**</span><span class="sxs-lookup"><span data-stu-id="88f61-143">**Internet address**</span></span> | <span data-ttu-id="88f61-144">Çalışan Self Servis sayfasının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="88f61-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="88f61-145">**Kutucuk boyutu**</span><span class="sxs-lookup"><span data-stu-id="88f61-145">**Tile size**</span></span> | <span data-ttu-id="88f61-146">Döşemenin boyutu: küçük, orta veya büyük.</span><span class="sxs-lookup"><span data-stu-id="88f61-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="88f61-147">**Hedef**</span><span class="sxs-lookup"><span data-stu-id="88f61-147">**Target**</span></span> | <span data-ttu-id="88f61-148">Sayfanın yeni bir pencerede mi yoksa geçerli pencerede mi açılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88f61-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="88f61-149">**Kutucuk arka plan görüntüsü**</span><span class="sxs-lookup"><span data-stu-id="88f61-149">**Tile background image**</span></span> | <span data-ttu-id="88f61-150">Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="88f61-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="88f61-151">**Başlangıç**</span><span class="sxs-lookup"><span data-stu-id="88f61-151">**Start**</span></span> | <span data-ttu-id="88f61-152">Döşemenin başlangıç tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="88f61-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="88f61-153">**End**</span><span class="sxs-lookup"><span data-stu-id="88f61-153">**End**</span></span> | <span data-ttu-id="88f61-154">Döşemenin bitiş tarihi ve saati kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="88f61-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="88f61-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="88f61-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]