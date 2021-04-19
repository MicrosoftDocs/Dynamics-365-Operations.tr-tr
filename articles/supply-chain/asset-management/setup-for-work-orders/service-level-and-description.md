---
title: Servis düzeyi ve açıklaması
description: Bu konuda Varlık Yönetimi'ndeki düzeyleri ve açıklamaları açıklanmaktadır.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb342e700c9390e1eb9f2a9e9d67b874b3e19b8e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808268"
---
# <a name="service-level-and-description"></a><span data-ttu-id="d01b4-103">Servis düzeyi ve açıklaması</span><span class="sxs-lookup"><span data-stu-id="d01b4-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d01b4-104">Bir iş emri oluşturduğunuzda, ilgili servis düzeylerini tanımlamak ve buna genel bir açıklama eklemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d01b4-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="d01b4-105">**İş emri servis düzeyleri** sayfasında iş emri servis düzeylerini ve **İş emri açıklama** sayfasıyla ilgili açıklamaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d01b4-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="d01b4-106">Servis düzeyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="d01b4-106">Create a service level</span></span>

1. <span data-ttu-id="d01b4-107">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Servis düzeyi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="d01b4-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-108">Select **New**.</span></span>
3. <span data-ttu-id="d01b4-109">**Servis düzeyi** alanına, servis düzeyini (örneğin bir sayı) girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="d01b4-110">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="d01b4-111">**İş emirleri** hızlı sekmesinde, beklenen başlangıç ve bitiş tarihleri ile saatlerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d01b4-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="d01b4-112">Bu hızlı sekmedeki alanlar, iş emirlerinin başlaması gereken ve sona erdirildiği dönemi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="d01b4-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="d01b4-113">El ile oluşturulan ve bakım taleplerinde oluşturulan iş emirlerinin bulunduğu iş emirleri için kullanılırlar.</span><span class="sxs-lookup"><span data-stu-id="d01b4-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="d01b4-114">**Başlangıç günü** alanına, iş emrinin başlaması gereken dönemi tanımlamak için bir gün sayısı girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="d01b4-115">Gün sayısı, iş emrinin yaratılış tarihinden itibaren hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d01b4-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="d01b4-116">Örneğin, iş emri oluşturulurken başlaması gerekiyorsa **0** girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="d01b4-117">İş emri oluşturulduktan sonraki bir hafta içinde başlaması gerekirse, **7** girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="d01b4-118">Başlangıç tarihine ek olarak, iş emri başlangıç saatini ayarlamak için **Başlangıç saatini ayarla** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d01b4-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="d01b4-119">Sonra **Başlangıç saati** alanına başlangıç saatini girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="d01b4-120">Seçeneği **Hayır** olarak ayarlarsanız günün geçerli saati kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d01b4-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="d01b4-121">**Bitiş günü** alanına, iş emrinin bitmesi gereken dönemi tanımlamak için bir gün sayısı girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="d01b4-122">Gün sayısı, iş emrinin başlangıç tarihinden itibaren hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d01b4-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="d01b4-123">Örneğin, iş emrinin başlangıç tarihinin bir hafta içinde bitmesi gerekiyorsa, **7** girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="d01b4-124">Bitiş tarihine ek olarak, iş emri bitiş saatini ayarlamak için **Bitiş saatini ayarla** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d01b4-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="d01b4-125">Sonra **Bitiş saati** alanına bitiş saatini girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="d01b4-126">Seçeneği **Hayır** olarak ayarlarsanız günün geçerli saati kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d01b4-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="d01b4-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-127">Select **Save**.</span></span>

![İş emri hizmet düzeyi sayfası](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="d01b4-129">Açıklama oluştur</span><span class="sxs-lookup"><span data-stu-id="d01b4-129">Create a description</span></span>

1. <span data-ttu-id="d01b4-130">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Açıklamalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="d01b4-131">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-131">Select **New**.</span></span>
3. <span data-ttu-id="d01b4-132">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="d01b4-133">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d01b4-133">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]