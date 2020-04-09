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
ms.openlocfilehash: 2181a84aea08aac0ddb202f7211dbda6330a3d49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148849"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="f3b6b-103">İşlemler ve iş planlaması olan bir üretim emri planlama</span><span class="sxs-lookup"><span data-stu-id="f3b6b-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3b6b-104">Bu konu operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="f3b6b-105">İşler iş planlama ile oluşturulurken, operasyon planlama ile iş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="f3b6b-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f3b6b-107">Bu yordam üretim müdürü, üretim planlayıcısı veya ayrı bir üretim ortamında çalışan atölye gözetmenine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="f3b6b-108">Üretim emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="f3b6b-108">Create a production order</span></span>
1. <span data-ttu-id="f3b6b-109">Gezinti bölmesinde **Modüller > Üretim denetimi > Üretim emirleri > Tüm üretim emirleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="f3b6b-110">**Yeni üretim emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-110">Select **New production order**.</span></span>
3. <span data-ttu-id="f3b6b-111">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="f3b6b-112">Madde numarası **D0001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="f3b6b-113">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="f3b6b-114">Üretim emri için işlemleri planlama</span><span class="sxs-lookup"><span data-stu-id="f3b6b-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="f3b6b-115">Yeni oluşturulan satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="f3b6b-116">Eylem Bölmesinde, **Planlama** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="f3b6b-117">**Operasyonları planla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="f3b6b-118">**Planlama yönü** alanında **Planlama tarihinden ileriye doğru** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="f3b6b-119">**Planlama tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="f3b6b-120">Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="f3b6b-121">Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="f3b6b-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-122">Select **OK**.</span></span>
7. <span data-ttu-id="f3b6b-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-123">In the list, mark the selected row.</span></span> <span data-ttu-id="f3b6b-124">Durumun **Planlandı** olarak değiştiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="f3b6b-125">**Tüm işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-125">Select **All jobs**.</span></span> <span data-ttu-id="f3b6b-126">Operasyon planlaması ile bir iş oluşturulmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="f3b6b-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="f3b6b-128">Üretim emri için işleri planlama</span><span class="sxs-lookup"><span data-stu-id="f3b6b-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="f3b6b-129">Eylem Bölmesinde, **Planlama** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="f3b6b-130">**İşleri zamanla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="f3b6b-131">**Planlama yönü** alanında **Planlama tarihinden ileriye doğru** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="f3b6b-132">**Planlama tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="f3b6b-133">Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="f3b6b-134">Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="f3b6b-135">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-135">Select **OK**.</span></span>
6. <span data-ttu-id="f3b6b-136">Eylem Bölmesinde **Üretim emri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="f3b6b-137">**Tüm işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-137">Select **All jobs**.</span></span> <span data-ttu-id="f3b6b-138">Etkin yola göre, iş planlamasında 5 işin oluşturulduğunda dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="f3b6b-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

