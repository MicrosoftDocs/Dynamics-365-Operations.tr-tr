---
title: Malzemeler iş hücresi için kullanılabilir olduğunda bir süreç kanban işi hazırlama
description: Bu görev, tüm malzemeler iş hücresi için kullanılabilir olduğunda bir kanban işi hazırlamaya odaklanır.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bde7a52e092723f9c6a686cb79080656c8de964c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204604"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="fb448-103">Malzemeler iş hücresi için kullanılabilir olduğunda bir süreç kanban işi hazırlama</span><span class="sxs-lookup"><span data-stu-id="fb448-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb448-104">Bu görev, tüm malzemeler iş hücresi için kullanılabilir olduğunda bir kanban işi hazırlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="fb448-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="fb448-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="fb448-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="fb448-106">Bu görev makine operatörü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fb448-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="fb448-107">İşleme işleri için kanban panosuna gidin.</span><span class="sxs-lookup"><span data-stu-id="fb448-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="fb448-108">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="fb448-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fb448-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb448-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fb448-110">İş hücresi 1250'yi seçin ve Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fb448-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="fb448-111">Listede satır 4'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="fb448-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="fb448-112">Temiz demo şirketinde henüz tamamlanmamış olan ilk iş Kanban 000329, satır 4'tedir.</span><span class="sxs-lookup"><span data-stu-id="fb448-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="fb448-113">Malzeme çekme listesi bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="fb448-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="fb448-114">Malzeme çekme listesindeki tüm öğeler için tedarik durumunun mevcut olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="fb448-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="fb448-115">Eğer birden fazla işi seçtiyseniz, malzeme çekme listesi, seçili projeler için gerekli tüm maddelerin toplamını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb448-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="fb448-116">Hazırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb448-116">Click Prepare.</span></span>
    * <span data-ttu-id="fb448-117">Hazırlama işlemi şimdi tamamlandı.</span><span class="sxs-lookup"><span data-stu-id="fb448-117">The preparation process is now completed.</span></span> <span data-ttu-id="fb448-118">Seçili malzeme çekme listesindeki tüm satırlar için seçili onay kutusu, tedarik durumunun çekilmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb448-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]