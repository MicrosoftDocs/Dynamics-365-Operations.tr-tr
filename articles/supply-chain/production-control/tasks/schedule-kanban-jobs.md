--- 
title: "Kanban işlerini planlama"
description: "Bu prosedür, belirli bir iş hücresi için kanban işlerini zamanlama işlemine odaklanmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fd6349c0da71a7fcf4429e7f6a2ef366afda6678
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="65b20-103">Kanban işlerini planlama</span><span class="sxs-lookup"><span data-stu-id="65b20-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65b20-104">Bu prosedür, belirli bir iş hücresi için kanban işlerini zamanlama işlemine odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="65b20-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="65b20-105">"Malzemeler kullanılabilir olmadığında bir kanban işi hazırla" prosedürü, bu prosedürü oluşturmanın bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="65b20-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="65b20-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="65b20-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="65b20-107">Bu görev, kanbanlarla çalışan atölye gözetmenlerine ve üretim planlayıcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="65b20-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="65b20-108">Bir iş hücresi için kanban işlerini seçin</span><span class="sxs-lookup"><span data-stu-id="65b20-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="65b20-109">Üretim denetimi > Kanban > Kanban işi planlaması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="65b20-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="65b20-110">Dönem kapasitesi olgu kutusunu genişletin</span><span class="sxs-lookup"><span data-stu-id="65b20-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="65b20-111">Kanban bilgi kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="65b20-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="65b20-112">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="65b20-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="65b20-113">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="65b20-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="65b20-114">İş hücresi 1250'yi seç</span><span class="sxs-lookup"><span data-stu-id="65b20-114">Select work cell 1250.</span></span> <span data-ttu-id="65b20-115">Bu, görünümü filtreleyerek sadece 1250 iş hücresi için olan işler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="65b20-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="65b20-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="65b20-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="65b20-117">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="65b20-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="65b20-118">Kanban işini ilk kullanılabilir dönemde zamanlayın.</span><span class="sxs-lookup"><span data-stu-id="65b20-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="65b20-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="65b20-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="65b20-120">Listede "Planlanmadı" durumunda olan ilk satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="65b20-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="65b20-121">İş durumu alanındaki noktalı simge Planlanmadı durumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="65b20-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="65b20-122">Planla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="65b20-122">Click Schedule.</span></span>
    * <span data-ttu-id="65b20-123">Bu, kanban işini ilk kullanılabilir dönemde zamanlar.</span><span class="sxs-lookup"><span data-stu-id="65b20-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="65b20-124">Kanban işinin listede son sıraya taşındığına dikkat edin çünkü bugünden başlayan döneme eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="65b20-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="65b20-125">Dönem bugünden başlayarak tamamen doluysa, iş ilk kullanılabilir döneme taşınır.</span><span class="sxs-lookup"><span data-stu-id="65b20-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="65b20-126">Belirli bir gün için iki kanban işini zamanlayın</span><span class="sxs-lookup"><span data-stu-id="65b20-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="65b20-127">Listede satır 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65b20-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="65b20-128">İlk satırın İş durumu alanındaki değerinin Planlanmadı olduğunu göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="65b20-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="65b20-129">Listede satır 2'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65b20-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="65b20-130">İkinci satırın İş durumu alanındaki değerinin Planlanmadı olduğunu göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="65b20-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="65b20-131">Şimdi ilk iki işi seçmiş durumdasınız.</span><span class="sxs-lookup"><span data-stu-id="65b20-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="65b20-132">Zaman çizelgesi başlangıç tarihi'ne tıklayarak, açılır iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="65b20-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="65b20-133">Kapasite eksikliği tepkisini geçersiz kıl kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="65b20-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="65b20-134">Bu seçenek, varsayılan kapasite eksikliğine tepkiyi geçersiz kılmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="65b20-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="65b20-135">Kapasite eksikliğine tepki alanında, "Talep edilen döneme ekle"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65b20-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="65b20-136">Bu seçenek, iş hücresinin aşırı yüklü olup olmamasına bakılmaksızın, işin istenen döneme eklenmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="65b20-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="65b20-137">Planla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="65b20-137">Click Schedule.</span></span>
    * <span data-ttu-id="65b20-138">Her iki işin istenen öneme eklendiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="65b20-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="65b20-139">Dönem kapasitesi bölümünde, her bir dönemin yükünü görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65b20-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="65b20-140">Tüketim alanı bu dönemde zamanlanan tüketimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="65b20-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="65b20-141">Zamanlanmış tüketim bu dönemdeki kullanılabilir kapasiteden daha yüksekse, aşırı yüklenmiş tüketim seçilecektir.</span><span class="sxs-lookup"><span data-stu-id="65b20-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  


