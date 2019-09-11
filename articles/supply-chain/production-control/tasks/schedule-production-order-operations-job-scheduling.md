---
title: İşlemler ve iş planlaması olan bir üretim emri planlama
description: Bu konu operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3023d6a6fe09c84b47839a2c4b78c37907754ded
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914896"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="43171-103">İşlemler ve iş planlaması olan bir üretim emri planlama</span><span class="sxs-lookup"><span data-stu-id="43171-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43171-104">Bu konu operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="43171-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="43171-105">İşler iş planlama ile oluşturulurken, operasyon planlama ile iş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="43171-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="43171-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="43171-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="43171-107">Bu yordam üretim müdürü, üretim planlayıcısı veya ayrı bir üretim ortamında çalışan atölye gözetmenine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="43171-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="43171-108">Üretim emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="43171-108">Create a production order</span></span>
1. <span data-ttu-id="43171-109">Gezinti bölmesinde **Modüller > Üretim denetimi > Üretim emirleri > Tüm üretim emirleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="43171-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="43171-110">**Yeni üretim emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-110">Select **New production order**.</span></span>
3. <span data-ttu-id="43171-111">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="43171-112">Madde numarası **D0001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="43171-113">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="43171-114">Üretim emri için işlemleri planlama</span><span class="sxs-lookup"><span data-stu-id="43171-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="43171-115">Yeni oluşturulan satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="43171-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="43171-116">Eylem Bölmesinde, **Planlama** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43171-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="43171-117">**Operasyonları planla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="43171-118">**Planlama yönü** alanında **Planlama tarihinden ileriye doğru** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="43171-119">**Planlama tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="43171-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="43171-120">Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="43171-121">Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.</span><span class="sxs-lookup"><span data-stu-id="43171-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="43171-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-122">Select **OK**.</span></span>
7. <span data-ttu-id="43171-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="43171-123">In the list, mark the selected row.</span></span> <span data-ttu-id="43171-124">Durumun **Planlandı** olarak değiştiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="43171-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="43171-125">**Tüm işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-125">Select **All jobs**.</span></span> <span data-ttu-id="43171-126">Operasyon planlaması ile bir iş oluşturulmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="43171-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="43171-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="43171-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="43171-128">Üretim emri için işleri planlama</span><span class="sxs-lookup"><span data-stu-id="43171-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="43171-129">Eylem Bölmesinde, **Planlama** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43171-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="43171-130">**İşleri zamanla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="43171-131">**Planlama yönü** alanında **Planlama tarihinden ileriye doğru** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="43171-132">**Planlama tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="43171-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="43171-133">Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="43171-134">Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.</span><span class="sxs-lookup"><span data-stu-id="43171-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="43171-135">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-135">Select **OK**.</span></span>
6. <span data-ttu-id="43171-136">Eylem Bölmesinde **Üretim emri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="43171-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="43171-137">**Tüm işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="43171-137">Select **All jobs**.</span></span> <span data-ttu-id="43171-138">Etkin yola göre, iş planlamasında 5 işin oluşturulduğunda dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="43171-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

