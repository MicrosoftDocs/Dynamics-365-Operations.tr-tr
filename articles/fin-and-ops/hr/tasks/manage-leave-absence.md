--- 
title: "Devamsızlıkları yönetme"
description: "Bu yordam çalışan izin kayıtlarının oluşturulmasıyla ilgili bilgi içerir."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: fc16d2aefcb52493e72e78def5b86b9da9673914
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="manage-leaves-of-absence"></a><span data-ttu-id="2da63-103">Devamsızlıkları yönetme</span><span class="sxs-lookup"><span data-stu-id="2da63-103">Manage leaves of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2da63-104">Bu yordam çalışan izin kayıtlarının oluşturulmasıyla ilgili bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="2da63-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="2da63-105">Tıbbi, eğitim veya ebeveynlik etkinliklerini kapsayan nedenler için izin süresini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2da63-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="2da63-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="2da63-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2da63-107">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2da63-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="2da63-108">Listeden bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="2da63-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="2da63-109">Çalışan adını seçerek seçili çalışanla ilgili ayrıntılı bilgileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="2da63-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="2da63-110">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2da63-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="2da63-111">İzin öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2da63-111">Click Leave.</span></span>
6. <span data-ttu-id="2da63-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2da63-112">Click New.</span></span>
7. <span data-ttu-id="2da63-113">İzin türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2da63-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2da63-114">İzin türleri formunda bir izin türünü bir kazanç koduyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2da63-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="2da63-115">İzin türü bir kazanç koduyla ilişkilendirilirse, girdiğiniz izin dönemi süresince ilişkilendirilen kazanç koduyla bir kazanç satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2da63-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="2da63-116">Listeden izin türü seçin.</span><span class="sxs-lookup"><span data-stu-id="2da63-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="2da63-117">Örneğin: Benimseme</span><span class="sxs-lookup"><span data-stu-id="2da63-117">For example: Adoption</span></span>  
9. <span data-ttu-id="2da63-118">İznin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="2da63-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="2da63-119">Örnek: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="2da63-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="2da63-120">Örneğin: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="2da63-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="2da63-121">İznin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="2da63-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="2da63-122">Örneğin: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="2da63-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="2da63-123">Not alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="2da63-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="2da63-124">Örneğin: Benimseme için izin</span><span class="sxs-lookup"><span data-stu-id="2da63-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="2da63-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2da63-125">Click Save.</span></span>


