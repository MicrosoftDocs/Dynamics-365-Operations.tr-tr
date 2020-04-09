---
title: Malzemeler iş hücresi için kullanılabilir olduğunda bir süreç kanban işi hazırlama
description: Bu görev, tüm malzemeler iş hücresi için kullanılabilir olduğunda bir kanban işi hazırlamaya odaklanır.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf163968474e91da7e3d47fd638a857a76179645
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149003"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="27ecf-103">Malzemeler iş hücresi için kullanılabilir olduğunda bir süreç kanban işi hazırlama</span><span class="sxs-lookup"><span data-stu-id="27ecf-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27ecf-104">Bu görev, tüm malzemeler iş hücresi için kullanılabilir olduğunda bir kanban işi hazırlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="27ecf-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="27ecf-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="27ecf-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="27ecf-106">Bu görev makine operatörü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="27ecf-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="27ecf-107">İşleme işleri için kanban panosuna gidin.</span><span class="sxs-lookup"><span data-stu-id="27ecf-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="27ecf-108">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="27ecf-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="27ecf-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27ecf-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="27ecf-110">İş hücresi 1250'yi seçin ve Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="27ecf-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="27ecf-111">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="27ecf-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="27ecf-112">Temiz demo şirketinde henüz tamamlanmamış olan ilk iş Kanban 000329, satır 4'tedir.</span><span class="sxs-lookup"><span data-stu-id="27ecf-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="27ecf-113">Malzeme çekme listesi bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="27ecf-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="27ecf-114">Malzeme çekme listesindeki tüm öğeler için tedarik durumunun mevcut olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="27ecf-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="27ecf-115">Eğer birden fazla işi seçtiyseniz, malzeme çekme listesi, seçili projeler için gerekli tüm maddelerin toplamını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27ecf-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="27ecf-116">Hazırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27ecf-116">Click Prepare.</span></span>
    * <span data-ttu-id="27ecf-117">Hazırlama işlemi şimdi tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="27ecf-117">The preparation process is now completed.</span></span> <span data-ttu-id="27ecf-118">Seçili malzeme çekme listesindeki tüm satırlar için seçili onay kutusu, tedarik durumunun çekilmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="27ecf-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

