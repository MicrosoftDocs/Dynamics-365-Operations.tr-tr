---
title: "Personel saat ve işe devam için bordro işlemini etkinleştirme"
description: "Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8d80e9be7ded9adb5aa75b3fba9468e58ecb4b4a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="0b864-103">Personel saat ve işe devam için bordro işlemini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0b864-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b864-104">Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0b864-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="0b864-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="0b864-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="0b864-106">İlgili ödeme oranıyla ödeme türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b864-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="0b864-107">Saat ve işe devam > Kurulum > Bordro > Ödeme türleri</span><span class="sxs-lookup"><span data-stu-id="0b864-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="0b864-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-108">Click New.</span></span>
3. <span data-ttu-id="0b864-109">Ödeme türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0b864-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="0b864-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0b864-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0b864-111">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-111">Click Save.</span></span>
6. <span data-ttu-id="0b864-112">Oranlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-112">Click Rates.</span></span>
    * <span data-ttu-id="0b864-113">Ödeme türleri için oranlar belirli zaman aralıkları için ayarlanır ve çalışanlar için bireysel oranlar oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="0b864-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="0b864-114">Saat ve işe devamdaki ödeme türleri için oran oluşturmak her zaman gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="0b864-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="0b864-115">Bu bilgi, ücretleri oluşturmak için kullanılan bordro sisteminde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="0b864-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="0b864-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-116">Click New.</span></span>
8. <span data-ttu-id="0b864-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0b864-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0b864-118">Oran alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0b864-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="0b864-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="0b864-120">Ödeme anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="0b864-120">Create a pay agreement</span></span>
1. <span data-ttu-id="0b864-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b864-121">Close the page.</span></span>
2. <span data-ttu-id="0b864-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b864-122">Close the page.</span></span>
3. <span data-ttu-id="0b864-123">Ödeme anlaşmalarına gidin.</span><span class="sxs-lookup"><span data-stu-id="0b864-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="0b864-124">Saat ve işe devam > Kurulum > Ödeme anlaşmaları</span><span class="sxs-lookup"><span data-stu-id="0b864-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="0b864-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-125">Click New.</span></span>
5. <span data-ttu-id="0b864-126">Ödeme anlaşması alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0b864-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="0b864-127">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0b864-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="0b864-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-128">Click Save.</span></span>
8. <span data-ttu-id="0b864-129">Anlaşma satırlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="0b864-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-130">Click New.</span></span>
10. <span data-ttu-id="0b864-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0b864-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="0b864-132">Profil türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0b864-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="0b864-133">Ödeme türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0b864-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="0b864-134">Süre ve kayıtlı çalışan için ödeme anlaşması ayarlama</span><span class="sxs-lookup"><span data-stu-id="0b864-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="0b864-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b864-135">Close the page.</span></span>
2. <span data-ttu-id="0b864-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b864-136">Close the page.</span></span>
3. <span data-ttu-id="0b864-137">Zaman kayıtlı çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0b864-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="0b864-138">Saat ve işe devam > Kurulum > Zaman kayıtlı çalışanlar</span><span class="sxs-lookup"><span data-stu-id="0b864-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="0b864-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0b864-140">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="0b864-141">Zaman kaydı bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b864-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="0b864-142">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b864-142">Click Edit.</span></span>
8. <span data-ttu-id="0b864-143">Ödeme anlaşması alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0b864-143">In the Pay agreement field, enter or select a value.</span></span>

