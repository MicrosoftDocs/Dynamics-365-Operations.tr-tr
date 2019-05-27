---
title: Kanban işini planlamadan kaldırma
description: Bu prosedür, bir planlanan işlem kanban işini, durumu Planlanmadı'ya döndürerek planlamadan kaldırmaya odaklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4d994be5c6bb1edc6f0fc64494a19a5babf72ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571991"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="88a29-103">Kanban işini planlamadan kaldırma</span><span class="sxs-lookup"><span data-stu-id="88a29-103">Remove a kanban job from the schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88a29-104">Bu prosedür, bir planlanan işlem kanban işini, durumu Planlanmadı'ya döndürerek planlamadan kaldırmaya odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="88a29-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="88a29-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="88a29-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="88a29-106">Bu prosedür atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="88a29-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="88a29-107">Planlanmış bir kanban işi bulun</span><span class="sxs-lookup"><span data-stu-id="88a29-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="88a29-108">Üretim denetimi > Kanban > Kanban işi planlaması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="88a29-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="88a29-109">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="88a29-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="88a29-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88a29-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="88a29-111">İş hücresi 1250'yi seç</span><span class="sxs-lookup"><span data-stu-id="88a29-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="88a29-112">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88a29-112">Click Select.</span></span>
5. <span data-ttu-id="88a29-113">İş durumunu görüntüle alanında "Planlandı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="88a29-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="88a29-114">Planlanmış kanban işini planlamadan kaldırın</span><span class="sxs-lookup"><span data-stu-id="88a29-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="88a29-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="88a29-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="88a29-116">Örneğin, 19 Aralık 2012'den, Planlandı durumunda olan bir işi seçin.</span><span class="sxs-lookup"><span data-stu-id="88a29-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="88a29-117">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88a29-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="88a29-118">İş durumunu geri al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88a29-118">Click Revert job status.</span></span>
4. <span data-ttu-id="88a29-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88a29-119">Click OK.</span></span>
    * <span data-ttu-id="88a29-120">Bu, geçerli işin "Planlandı" olan durumunu "Planlanmadı"ya döndürür ve işlem panosundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="88a29-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

