---
title: Çalışan yararları programı teslim et
description: Bu makale, yeni bir kazanç oluştururken kullanılacak kazanç öğelerini nasıl oluşturacağınızı gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010930"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="8d377-103">Çalışan yararları programı teslim et</span><span class="sxs-lookup"><span data-stu-id="8d377-103">Deliver employee benefits program</span></span>

<span data-ttu-id="8d377-104">Bu makale, yeni bir kazanç oluştururken kullanılacak kazanç öğelerini nasıl oluşturacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="8d377-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="8d377-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8d377-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="8d377-106">Bu görev Ücret ve Kazançlar yöneticisine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="8d377-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="8d377-107">Kazanç öğeleri oluştur</span><span class="sxs-lookup"><span data-stu-id="8d377-107">Create benefit elements</span></span>
1. <span data-ttu-id="8d377-108">Bu görev Kazanç listesi sayfasından başlar.</span><span class="sxs-lookup"><span data-stu-id="8d377-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="8d377-109">Görevi sayfayı açarak veya Kazanç listesi sayfasında arama yaparak başlatın.</span><span class="sxs-lookup"><span data-stu-id="8d377-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="8d377-110">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8d377-110">Click New.</span></span>
3. <span data-ttu-id="8d377-111">Tür alanına, oluşturmakta olduğunuz kazanç türünün adını girin.</span><span class="sxs-lookup"><span data-stu-id="8d377-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="8d377-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8d377-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8d377-113">Eşzamanlı kayıt alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="8d377-114">Çalışanların birden fazla sağlık planına kaydolma olanağını sınırlamak için Tür başına bir kayıt seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="8d377-115">Bordro kategorisi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="8d377-116">Planlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="8d377-117">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8d377-117">Click New.</span></span>
9. <span data-ttu-id="8d377-118">Plan alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8d377-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="8d377-119">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8d377-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="8d377-120">Tür alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="8d377-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="8d377-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="8d377-123">Bordro etkisi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="8d377-124">Seçenekler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-124">Click the Options tab.</span></span>
16. <span data-ttu-id="8d377-125">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8d377-125">Click New.</span></span>
17. <span data-ttu-id="8d377-126">Seçenek alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8d377-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="8d377-127">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8d377-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="8d377-128">Kazanç oluşturma</span><span class="sxs-lookup"><span data-stu-id="8d377-128">Create a benefit</span></span>
1. <span data-ttu-id="8d377-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8d377-129">Close the page.</span></span>
2. <span data-ttu-id="8d377-130">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="8d377-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="8d377-131">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="8d377-132">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8d377-133">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="8d377-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8d377-135">Seçenek alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8d377-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="8d377-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8d377-138">Yürürlük alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="8d377-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="8d377-139">Kazanç oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-139">Click Create benefit.</span></span>
12. <span data-ttu-id="8d377-140">Bordro detayları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="8d377-141">Sıklık alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8d377-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8d377-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d377-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8d377-144">Temel alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="8d377-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="8d377-145">Tutar veya oran alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8d377-145">In the Amount or rate field, enter a number.</span></span>

