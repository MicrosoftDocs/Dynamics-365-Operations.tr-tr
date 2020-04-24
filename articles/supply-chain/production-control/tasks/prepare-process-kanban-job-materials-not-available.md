---
title: Malzemeler iş hücresi için kullanılamadığında bir süreç kanban işi hazırlama
description: Bu yordam, bazı malzemeler için iş hücre kullanılamadığında bir süreç kanban işi hazırlanmasına odaklanır, bu nedenle ambardan malzeme çekme gerekli.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d57df6188aacc2f8a56a7ba91c4ab50a90901a7e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206924"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="49647-103">Malzemeler iş hücresi için kullanılamadığında bir süreç kanban işi hazırlama</span><span class="sxs-lookup"><span data-stu-id="49647-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49647-104">Bu yordam, bazı malzemeler için iş hücre kullanılamadığında bir süreç kanban işi hazırlanmasına odaklanır, bu nedenle ambardan malzeme çekme gerekli.</span><span class="sxs-lookup"><span data-stu-id="49647-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="49647-105">"Malzeme hazır olduğunda bir süreç kanban işi hazırla" yordamı, bu yordamı oluşturmak için bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="49647-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="49647-106">Bu yordam makine operatörü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="49647-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="49647-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="49647-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="49647-108">Üretim kontrolü > Kanban > İş işlemleri için kanban kartı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="49647-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="49647-109">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="49647-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="49647-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49647-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="49647-111">İş hücresi 1250'yi seç</span><span class="sxs-lookup"><span data-stu-id="49647-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="49647-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49647-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49647-113">Kanban 000356'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="49647-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="49647-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49647-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49647-115">Listede satır 4'ün seçimini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="49647-115">In the list, deselect row 4.</span></span> <span data-ttu-id="49647-116">ya da "Malzeme hazır olduğunda bir süreç kanban işi hazırlayın" görevini tamamlamadıysanız satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="49647-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="49647-117">Malzeme çekme listesi bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="49647-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="49647-118">Tedarik durumundaki Giriş yok simgesi, madde P0002'nin 48 ea iş hücresinden eksik olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="49647-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="49647-119">Malzemeleri iş hücresine nakledin</span><span class="sxs-lookup"><span data-stu-id="49647-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="49647-120">Transfer işleri bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="49647-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="49647-121">Madde numarası alanında 'P0002' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="49647-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="49647-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49647-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="49647-123">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49647-123">Click Start.</span></span>
    * <span data-ttu-id="49647-124">Transfer devam ediyor.</span><span class="sxs-lookup"><span data-stu-id="49647-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="49647-125">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49647-125">Click Complete.</span></span>
    * <span data-ttu-id="49647-126">Madde P0002 kanban işi için malzeme çekme listesinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="49647-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="49647-127">Başka bir deyişle, gerekli tüm malzemelerle kanban hazırlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49647-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="49647-128">Hazırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49647-128">Click Prepare.</span></span>
    * <span data-ttu-id="49647-129">İş durumu'ndaki bir simgenin işin şimdi hazır olduğunu belirttiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="49647-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

