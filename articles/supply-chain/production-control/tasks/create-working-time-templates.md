---
title: Çalışma süresi şablonları oluşturma
description: Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c1e871133b51105386ac3b647432d0c36a6998
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "322778"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="23d1e-103">Çalışma süresi şablonları oluşturma</span><span class="sxs-lookup"><span data-stu-id="23d1e-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23d1e-104">Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="23d1e-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="23d1e-105">Bu yordam, çalışma zaman aralıklarını kategorilere ayırmak için çalışma zamanı planlama özelliklerini kullanarak bir çalışma zamanı şablonunun nasıl tanımlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23d1e-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="23d1e-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23d1e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="23d1e-107">Tüm çalışma alanları > Kaynak yaşam döngüsü yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="23d1e-108">Çalışma zamanı şablonları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="23d1e-109">Çalışma zamanı şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="23d1e-109">Create working time template</span></span>
1. <span data-ttu-id="23d1e-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-110">Click New.</span></span>
2. <span data-ttu-id="23d1e-111">Çalışma zamanı şablonu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="23d1e-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="23d1e-113">Pazartesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="23d1e-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-114">Click Add.</span></span>
6. <span data-ttu-id="23d1e-115">Başlangıç alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="23d1e-116">İşin sabah başlayacağı saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="23d1e-117">Bitiş alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="23d1e-118">Çalışanların öğle yemeği saatini belirtin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="23d1e-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-119">Click Add.</span></span>
9. <span data-ttu-id="23d1e-120">Başlangıç alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="23d1e-121">Öğle yemeğinin ardından işin başlayacağı saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="23d1e-122">Bitiş alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="23d1e-123">İşin bitiş tarihini belirtin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="23d1e-124">Çalışma saatlerini haftanın tüm günleri için çoğaltma</span><span class="sxs-lookup"><span data-stu-id="23d1e-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="23d1e-125">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-125">Click Copy day.</span></span>
    * <span data-ttu-id="23d1e-126">Çalışma saati tanımlarını Pazartesi gününden Salı gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="23d1e-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-127">Click OK.</span></span>
3. <span data-ttu-id="23d1e-128">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-128">Click Copy day.</span></span>
    * <span data-ttu-id="23d1e-129">Çalışma saati tanımlarını Pazartesi gününden Çarşamba gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="23d1e-130">Hafta içi bitiş tarihi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="23d1e-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-131">Click OK.</span></span>
6. <span data-ttu-id="23d1e-132">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-132">Click Copy day.</span></span>
    * <span data-ttu-id="23d1e-133">Çalışma saati tanımlarını Pazartesi gününden Perşembe gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="23d1e-134">Hafta içi bitiş tarihi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="23d1e-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-135">Click OK.</span></span>
9. <span data-ttu-id="23d1e-136">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-136">Click Copy day.</span></span>
    * <span data-ttu-id="23d1e-137">Çalışma saati tanımlarını Pazartesi gününden Cuma gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="23d1e-138">Hafta içi bitiş tarihi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="23d1e-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23d1e-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="23d1e-140">Özel işlemler için zaman dilimi tanımlama</span><span class="sxs-lookup"><span data-stu-id="23d1e-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="23d1e-141">Cuma bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="23d1e-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="23d1e-143">Özellik alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="23d1e-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="23d1e-145">Özellik alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="23d1e-146">Haftasonlarını malzeme çekme için kapatıldı olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="23d1e-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="23d1e-147">Cumartesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="23d1e-148">Malzeme çekme için Kapatıldı alanında Evet seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="23d1e-149">Pazar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="23d1e-150">Malzeme çekme için Kapatıldı alanında Evet seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23d1e-150">Select Yes in the Closed for pickup field.</span></span>

