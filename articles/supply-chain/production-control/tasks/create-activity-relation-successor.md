---
title: 'Faaliyet ilişkisi oluşturma: - Ardıl'
description: Bir yalın imalat akışındaki faaliyetlerin akışı etkinlik ilişkileri üzerinden belgelenir.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f10ecb8e579975327440ede6ea383226645c8cf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255313"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="ed707-103">Faaliyet ilişkisi oluşturma: - Ardıl</span><span class="sxs-lookup"><span data-stu-id="ed707-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed707-104">Bir yalın imalat akışındaki faaliyetlerin akışı etkinlik ilişkileri üzerinden belgelenir.</span><span class="sxs-lookup"><span data-stu-id="ed707-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="ed707-105">Bu kayıt, bir etkinlik ilişkisinin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed707-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="ed707-106">Ön koşullar:</span><span class="sxs-lookup"><span data-stu-id="ed707-106">Prerequisites:</span></span>

- <span data-ttu-id="ed707-107">Taslak modunda bir üretim akışı ve sürüm.</span><span class="sxs-lookup"><span data-stu-id="ed707-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="ed707-108">Üretim akışında birbirini izleyen iki faaliyet oluşturulur ancak ilişkilendirilmez.</span><span class="sxs-lookup"><span data-stu-id="ed707-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="ed707-109">Üretim akışı sürümünü bul</span><span class="sxs-lookup"><span data-stu-id="ed707-109">Find the production flow version</span></span> 
1. <span data-ttu-id="ed707-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="ed707-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="ed707-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ed707-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ed707-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed707-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ed707-113">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ed707-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="ed707-114">Listede bir taslak sürüm seçin.</span><span class="sxs-lookup"><span data-stu-id="ed707-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="ed707-115">Faaliyet ilişkileri, üretim akışının hem taslak hem de etkin sürümlerine eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ed707-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="ed707-116">Faaliyet genel bakışını aç</span><span class="sxs-lookup"><span data-stu-id="ed707-116">Open the activity overview</span></span>
1. <span data-ttu-id="ed707-117">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed707-117">Click Activities.</span></span>
    * <span data-ttu-id="ed707-118">Formun, çalışmakta olduğunuz üretim akışı Sürümü için ayrılan tüm üretim akışı faaliyetlerini gösterdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ed707-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="ed707-119">Bir Ardıl ekle</span><span class="sxs-lookup"><span data-stu-id="ed707-119">Add a Successor</span></span>
1. <span data-ttu-id="ed707-120">Ardıl ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed707-120">Click Add successor.</span></span>
2. <span data-ttu-id="ed707-121">Faaliyet alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed707-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ed707-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ed707-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ed707-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed707-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ed707-124">Sınırlama onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ed707-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="ed707-125">Sınırlama değeri alanında bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="ed707-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="ed707-126">Sınırlama süresi, öncelin zamanlanmış bitiş (vade tarihi ve saati) ve ardılın zamanlanmış başlangıç süresi arasında zamanlanacak süredir.</span><span class="sxs-lookup"><span data-stu-id="ed707-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="ed707-127">Birimler alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ed707-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="ed707-128">Döngü süresi oranı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ed707-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="ed707-129">Her iki etkinlik de aynı takt'ta çalışırsa, döngü zamanı oranı 1 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed707-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="ed707-130">Öncül, ardılın iki katı hızda çalışıyorsa, oran 2 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed707-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="ed707-131">Döngü zamanı oranları, üretim akışı etkinliklerinin ayrı ayrı döngü zamanlarını hesaplamakta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ed707-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="ed707-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ed707-132">Click OK.</span></span>
10. <span data-ttu-id="ed707-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ed707-133">Close the page.</span></span>
11. <span data-ttu-id="ed707-134">GridPanel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ed707-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="ed707-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ed707-135">Close the page.</span></span>
13. <span data-ttu-id="ed707-136">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="ed707-136">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]