---
title: Yeni kazanç oluştur
description: Bu görev, yeni bir kazanç oluştururken kullanılacak kazanç öğelerini nasıl oluşturacağınızı gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a74900f288fb5ce145f89e0ccad509deaac505cb
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507878"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="3d759-103">Yeni kazanç oluştur</span><span class="sxs-lookup"><span data-stu-id="3d759-103">Create a new benefit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d759-104">Bu görev, yeni bir kazanç oluştururken kullanılacak kazanç öğelerini nasıl oluşturacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d759-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="3d759-105">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="3d759-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="3d759-106">Bu görev Ücret ve Kazançlar yöneticisine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="3d759-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="3d759-107">Kazanç öğeleri oluştur</span><span class="sxs-lookup"><span data-stu-id="3d759-107">Create benefit elements</span></span>
1. <span data-ttu-id="3d759-108">Sırasıyla İnsan Kaynakları > Faydalar > Kurulum > Faydalar seçimlerini yapın.</span><span class="sxs-lookup"><span data-stu-id="3d759-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="3d759-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d759-109">Click New.</span></span>
3. <span data-ttu-id="3d759-110">Tür alanına, oluşturmakta olduğunuz kazanç türünün adını girin.</span><span class="sxs-lookup"><span data-stu-id="3d759-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="3d759-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3d759-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3d759-112">Eşzamanlı kayıt alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="3d759-113">Çalışanların birden fazla sağlık planına kaydolma olanağını sınırlamak için Tür başına bir kayıt seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="3d759-114">Bordro kategorisi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="3d759-115">Planlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d759-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="3d759-116">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3d759-116">Click New.</span></span>
9. <span data-ttu-id="3d759-117">Plan alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3d759-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="3d759-118">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3d759-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="3d759-119">Tür alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="3d759-120">Bordro etkisi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="3d759-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d759-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="3d759-122">Kazanç oluşturma</span><span class="sxs-lookup"><span data-stu-id="3d759-122">Create a benefit</span></span>
1. <span data-ttu-id="3d759-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d759-123">Close the page.</span></span>
2. <span data-ttu-id="3d759-124">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="3d759-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="3d759-125">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d759-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="3d759-126">Plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="3d759-127">Seçenek alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3d759-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="3d759-128">Yürürlük alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="3d759-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="3d759-129">Kazanç oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d759-129">Click Create benefit.</span></span>

