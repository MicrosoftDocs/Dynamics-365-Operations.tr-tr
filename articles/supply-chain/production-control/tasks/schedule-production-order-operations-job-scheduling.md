--- 
title: "İşlemler ve iş planlaması olan bir üretim emri planlama"
description: "Bu yordam operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="8dad5-103">İşlemler ve iş planlaması olan bir üretim emri planlama</span><span class="sxs-lookup"><span data-stu-id="8dad5-103">Schedule a production order with operations and job scheduling</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8dad5-104">Bu yordam operasyon planlama ve iş planlama ile bir üretim emri planlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="8dad5-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="8dad5-105">İşler iş planlama ile oluşturulurken, operasyon planlama ile iş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="8dad5-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="8dad5-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8dad5-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="8dad5-107">Bu yordam üretim müdürü, üretim planlayıcısı veya ayrı bir üretim ortamında çalışan atölye gözetmenine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="8dad5-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="8dad5-108">Üretim emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="8dad5-108">Create a production order</span></span>
1. <span data-ttu-id="8dad5-109">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="8dad5-110">Yeni üretim emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-110">Click New production order.</span></span>
3. <span data-ttu-id="8dad5-111">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="8dad5-112">Madde numarası D0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="8dad5-113">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="8dad5-114">Üretim emri için işlemleri planlama</span><span class="sxs-lookup"><span data-stu-id="8dad5-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="8dad5-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8dad5-116">Yeni oluşturduğunuz üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-116">Select the production order that you have just created.</span></span> <span data-ttu-id="8dad5-117">Bu emir listenin en üstünde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8dad5-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="8dad5-118">Eylem Bölmesinde, Planla öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="8dad5-119">Operasyonları planla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="8dad5-120">İş planlama çizelgeleme yönü alanında 'Planlama tarihinden ileriye doğru' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="8dad5-121">Planlama tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="8dad5-122">Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="8dad5-123">Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.</span><span class="sxs-lookup"><span data-stu-id="8dad5-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="8dad5-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-124">Click OK.</span></span>
7. <span data-ttu-id="8dad5-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8dad5-126">Durumun Planlandı olarak değiştiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="8dad5-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8dad5-128">Tüm işleri çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-128">Click All jobs.</span></span>
    * <span data-ttu-id="8dad5-129">Operasyon planlaması ile bir iş oluşturulmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="8dad5-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="8dad5-131">Üretim emri için işleri planlama</span><span class="sxs-lookup"><span data-stu-id="8dad5-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="8dad5-132">Eylem Bölmesinde, Planla öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="8dad5-133">İşleri planla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="8dad5-134">İş planlama çizelgeleme yönü alanında 'Planlama tarihinden ileriye doğru' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="8dad5-135">Planlama tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="8dad5-136">Gelecekteki bir tarihi, örneğin bugünden itibaren bir hafta sonrasını seçin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="8dad5-137">Seçili Planlama yönü ile üretim emri bu tarihten ileriye doğru planlanır.</span><span class="sxs-lookup"><span data-stu-id="8dad5-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="8dad5-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-138">Click OK.</span></span>
6. <span data-ttu-id="8dad5-139">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="8dad5-140">Tüm işleri çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8dad5-140">Click All jobs.</span></span>
    * <span data-ttu-id="8dad5-141">Etkin yola göre, iş planlamasında 5 işin oluşturulduğunda dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="8dad5-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


