---
title: Personel saat ve işe devam için bordro işlemini etkinleştirme
description: Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560198"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="ad60a-103">Personel saat ve işe devam için bordro işlemini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ad60a-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad60a-104">Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ad60a-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="ad60a-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ad60a-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="ad60a-106">İlgili ödeme oranıyla ödeme türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad60a-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="ad60a-107">Saat ve işe devam > Kurulum > Bordro > Ödeme türleri</span><span class="sxs-lookup"><span data-stu-id="ad60a-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="ad60a-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-108">Click New.</span></span>
3. <span data-ttu-id="ad60a-109">Ödeme türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="ad60a-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ad60a-111">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-111">Click Save.</span></span>
6. <span data-ttu-id="ad60a-112">Oranlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-112">Click Rates.</span></span>
    * <span data-ttu-id="ad60a-113">Ödeme türleri için oranlar belirli zaman aralıkları için ayarlanır ve çalışanlar için bireysel oranlar oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ad60a-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="ad60a-114">Saat ve işe devamdaki ödeme türleri için oran oluşturmak her zaman gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="ad60a-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="ad60a-115">Bu bilgi, ücretleri oluşturmak için kullanılan bordro sisteminde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="ad60a-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="ad60a-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-116">Click New.</span></span>
8. <span data-ttu-id="ad60a-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ad60a-118">Oran alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="ad60a-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="ad60a-120">Ödeme anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad60a-120">Create a pay agreement</span></span>
1. <span data-ttu-id="ad60a-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-121">Close the page.</span></span>
2. <span data-ttu-id="ad60a-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-122">Close the page.</span></span>
3. <span data-ttu-id="ad60a-123">Ödeme anlaşmalarına gidin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="ad60a-124">Saat ve işe devam > Kurulum > Ödeme anlaşmaları</span><span class="sxs-lookup"><span data-stu-id="ad60a-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="ad60a-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-125">Click New.</span></span>
5. <span data-ttu-id="ad60a-126">Ödeme anlaşması alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="ad60a-127">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="ad60a-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-128">Click Save.</span></span>
8. <span data-ttu-id="ad60a-129">Anlaşma satırlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="ad60a-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-130">Click New.</span></span>
10. <span data-ttu-id="ad60a-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ad60a-132">Profil türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="ad60a-133">Ödeme türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="ad60a-134">Süre ve kayıtlı çalışan için ödeme anlaşması ayarlama</span><span class="sxs-lookup"><span data-stu-id="ad60a-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="ad60a-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-135">Close the page.</span></span>
2. <span data-ttu-id="ad60a-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-136">Close the page.</span></span>
3. <span data-ttu-id="ad60a-137">Zaman kayıtlı çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="ad60a-138">Saat ve işe devam > Kurulum > Zaman kayıtlı çalışanlar</span><span class="sxs-lookup"><span data-stu-id="ad60a-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="ad60a-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ad60a-140">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="ad60a-141">Zaman kaydı bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="ad60a-142">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad60a-142">Click Edit.</span></span>
8. <span data-ttu-id="ad60a-143">Ödeme anlaşması alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad60a-143">In the Pay agreement field, enter or select a value.</span></span>

