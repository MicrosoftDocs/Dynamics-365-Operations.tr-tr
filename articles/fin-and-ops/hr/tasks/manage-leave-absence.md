--- 
title: "Devamsızlıkları yönetme"
description: "Bu yordam çalışan izin kayıtlarının oluşturulmasıyla ilgili bilgi içerir."
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7687d31fbf73a02b1b924d092e77ac28b573e694
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="ac927-103">Devamsızlıkları yönetme</span><span class="sxs-lookup"><span data-stu-id="ac927-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac927-104">Bu yordam çalışan izin kayıtlarının oluşturulmasıyla ilgili bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="ac927-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="ac927-105">Tıbbi, eğitim veya ebeveynlik etkinliklerini kapsayan nedenler için izin süresini izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac927-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="ac927-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ac927-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ac927-107">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ac927-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="ac927-108">Listeden bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="ac927-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="ac927-109">Çalışan adını seçerek seçili çalışanla ilgili ayrıntılı bilgileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ac927-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="ac927-110">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac927-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="ac927-111">İzin öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac927-111">Click Leave.</span></span>
6. <span data-ttu-id="ac927-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac927-112">Click New.</span></span>
7. <span data-ttu-id="ac927-113">İzin türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac927-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ac927-114">İzin türleri formunda bir izin türünü bir kazanç koduyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac927-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="ac927-115">İzin türü bir kazanç koduyla ilişkilendirilirse, girdiğiniz izin dönemi süresince ilişkilendirilen kazanç koduyla bir kazanç satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ac927-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="ac927-116">Listeden izin türü seçin.</span><span class="sxs-lookup"><span data-stu-id="ac927-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="ac927-117">Örneğin: Benimseme</span><span class="sxs-lookup"><span data-stu-id="ac927-117">For example: Adoption</span></span>  
9. <span data-ttu-id="ac927-118">İznin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="ac927-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="ac927-119">Örnek: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="ac927-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="ac927-120">Örneğin: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="ac927-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="ac927-121">İznin başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="ac927-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="ac927-122">Örneğin: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="ac927-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="ac927-123">Not alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ac927-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="ac927-124">Örneğin: Benimseme için izin</span><span class="sxs-lookup"><span data-stu-id="ac927-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="ac927-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ac927-125">Click Save.</span></span>


