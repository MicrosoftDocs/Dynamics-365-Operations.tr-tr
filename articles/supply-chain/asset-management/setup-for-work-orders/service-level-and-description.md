---
title: Servis düzeyi ve açıklaması
description: Bu konuda Varlık Yönetimi'ndeki düzeyleri ve açıklamaları açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874659"
---
# <a name="service-level-and-description"></a><span data-ttu-id="1ac0c-103">Servis düzeyi ve açıklaması</span><span class="sxs-lookup"><span data-stu-id="1ac0c-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1ac0c-104">Bir iş emri oluşturduğunuzda, ilgili servis düzeylerini tanımlamak ve buna genel bir açıklama eklemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="1ac0c-105">**İş emri servis düzeyleri** sayfasında iş emri servis düzeylerini ve **İş emri açıklama** sayfasıyla ilgili açıklamaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="1ac0c-106">Servis düzeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ac0c-106">Create a service level</span></span>

1. <span data-ttu-id="1ac0c-107">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Servis düzeyi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="1ac0c-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-108">Select **New**.</span></span>
3. <span data-ttu-id="1ac0c-109">**Servis düzeyi** alanına, servis düzeyini (örneğin bir sayı) girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="1ac0c-110">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="1ac0c-111">**İş emirleri** hızlı sekmesinde, beklenen başlangıç ve bitiş tarihleri ile saatlerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="1ac0c-112">Bu hızlı sekmedeki alanlar, iş emirlerinin başlaması gereken ve sona erdirildiği dönemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="1ac0c-113">El ile oluşturulan ve bakım taleplerinde oluşturulan iş emirlerinin bulunduğu iş emirleri için kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="1ac0c-114">**Başlangıç günü** alanına, iş emrinin başlaması gereken dönemi tanımlamak için bir gün sayısı girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="1ac0c-115">Gün sayısı, iş emrinin yaratılış tarihinden itibaren hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="1ac0c-116">Örneğin, iş emri oluşturulurken başlaması gerekiyorsa **0** girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="1ac0c-117">İş emri oluşturulduktan sonraki bir hafta içinde başlaması gerekirse, **7** girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="1ac0c-118">Başlangıç tarihine ek olarak, iş emri başlangıç saatini ayarlamak için **Başlangıç saatini ayarla** seçeneğini **Evet**olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="1ac0c-119">Sonra **Başlangıç saati** alanına başlangıç saatini girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="1ac0c-120">Seçeneği **Hayır**olarak ayarlarsanız günün geçerli saati kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="1ac0c-121">**Bitiş günü** alanına, iş emrinin bitmesi gereken dönemi tanımlamak için bir gün sayısı girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="1ac0c-122">Gün sayısı, iş emrinin başlangıç tarihinden itibaren hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="1ac0c-123">Örneğin, iş emrinin başlangıç tarihinin bir hafta içinde bitmesi gerekiyorsa, **7**girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="1ac0c-124">Bitiş tarihine ek olarak, iş emri bitiş saatini ayarlamak için **Bitiş saatini ayarla** seçeneğini **Evet**olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="1ac0c-125">Sonra **Bitiş saati** alanına bitiş saatini girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="1ac0c-126">Seçeneği **Hayır**olarak ayarlarsanız günün geçerli saati kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="1ac0c-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-127">Select **Save**.</span></span>

![Şekil 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="1ac0c-129">Açıklama oluştur</span><span class="sxs-lookup"><span data-stu-id="1ac0c-129">Create a description</span></span>

1. <span data-ttu-id="1ac0c-130">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Açıklamalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="1ac0c-131">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-131">Select **New**.</span></span>
3. <span data-ttu-id="1ac0c-132">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="1ac0c-133">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1ac0c-133">Select **Save**.</span></span>
