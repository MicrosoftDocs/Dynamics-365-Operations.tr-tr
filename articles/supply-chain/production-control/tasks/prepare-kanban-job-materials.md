--- 
title: "Malzemeler iş hücresi için kullanılabilir olduğunda bir süreç kanban işi hazırlama"
description: "Bu görev, tüm malzemeler iş hücresi için kullanılabilir olduğunda bir kanban işi hazırlamaya odaklanır."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 62f3f71cc5e47f0fb027211a911e61673ca2e375
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="27872-103">Malzemeler iş hücresi için kullanılabilir olduğunda bir süreç kanban işi hazırlama</span><span class="sxs-lookup"><span data-stu-id="27872-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27872-104">Bu görev, tüm malzemeler iş hücresi için kullanılabilir olduğunda bir kanban işi hazırlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="27872-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="27872-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="27872-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="27872-106">Bu görev makine operatörü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="27872-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="27872-107">İşleme işleri için kanban panosuna gidin.</span><span class="sxs-lookup"><span data-stu-id="27872-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="27872-108">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="27872-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="27872-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27872-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="27872-110">İş hücresi 1250'yi seçin ve Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27872-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="27872-111">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="27872-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="27872-112">Temiz demo şirketinde henüz tamamlanmamış olan ilk iş Kanban 000329, satır 4'tedir.</span><span class="sxs-lookup"><span data-stu-id="27872-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="27872-113">Malzeme çekme listesi bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="27872-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="27872-114">Malzeme çekme listesindeki tüm öğeler için tedarik durumunun mevcut olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="27872-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="27872-115">Eğer birden fazla işi seçtiyseniz, malzeme çekme listesi, seçili projeler için gerekli tüm maddelerin toplamını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27872-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="27872-116">Hazırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27872-116">Click Prepare.</span></span>
    * <span data-ttu-id="27872-117">Hazırlama işlemi şimdi tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="27872-117">The preparation process is now completed.</span></span> <span data-ttu-id="27872-118">Seçili malzeme çekme listesindeki tüm satırlar için seçili onay kutusu, tedarik durumunun çekilmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="27872-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  


