--- 
title: "Çalışma süresi şablonları oluşturma"
description: "Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="c812d-103">Çalışma süresi şablonları oluşturma</span><span class="sxs-lookup"><span data-stu-id="c812d-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c812d-104">Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c812d-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="c812d-105">Bu yordam, çalışma zaman aralıklarını kategorilere ayırmak için çalışma zamanı planlama özelliklerini kullanarak bir çalışma zamanı şablonunun nasıl tanımlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c812d-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="c812d-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c812d-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="c812d-107">Tüm çalışma alanları > Kaynak yaşam döngüsü yönetimi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c812d-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="c812d-108">Çalışma zamanı şablonları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="c812d-109">Çalışma zamanı şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c812d-109">Create working time template</span></span>
1. <span data-ttu-id="c812d-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-110">Click New.</span></span>
2. <span data-ttu-id="c812d-111">Çalışma zamanı şablonu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c812d-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="c812d-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c812d-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c812d-113">Pazartesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c812d-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="c812d-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-114">Click Add.</span></span>
6. <span data-ttu-id="c812d-115">Başlangıç alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="c812d-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="c812d-116">İşin sabah başlayacağı saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="c812d-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="c812d-117">Bitiş alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="c812d-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="c812d-118">Çalışanların öğle yemeği saatini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c812d-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="c812d-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-119">Click Add.</span></span>
9. <span data-ttu-id="c812d-120">Başlangıç alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="c812d-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="c812d-121">Öğle yemeğinin ardından işin başlayacağı saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="c812d-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="c812d-122">Bitiş alanında bir saat girin.</span><span class="sxs-lookup"><span data-stu-id="c812d-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="c812d-123">İşin bitiş tarihini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c812d-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="c812d-124">Çalışma saatlerini haftanın tüm günleri için çoğaltma</span><span class="sxs-lookup"><span data-stu-id="c812d-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="c812d-125">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-125">Click Copy day.</span></span>
    * <span data-ttu-id="c812d-126">Çalışma saati tanımlarını Pazartesi gününden Salı gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="c812d-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-127">Click OK.</span></span>
3. <span data-ttu-id="c812d-128">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-128">Click Copy day.</span></span>
    * <span data-ttu-id="c812d-129">Çalışma saati tanımlarını Pazartesi gününden Çarşamba gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="c812d-130">Hafta içi bitiş tarihi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c812d-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="c812d-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-131">Click OK.</span></span>
6. <span data-ttu-id="c812d-132">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-132">Click Copy day.</span></span>
    * <span data-ttu-id="c812d-133">Çalışma saati tanımlarını Pazartesi gününden Perşembe gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="c812d-134">Hafta içi bitiş tarihi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c812d-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="c812d-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-135">Click OK.</span></span>
9. <span data-ttu-id="c812d-136">Günü kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c812d-136">Click Copy day.</span></span>
    * <span data-ttu-id="c812d-137">Çalışma saati tanımlarını Pazartesi gününden Cuma gününe kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="c812d-138">Hafta içi bitiş tarihi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c812d-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="c812d-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c812d-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="c812d-140">Özel işlemler için zaman dilimi tanımlama</span><span class="sxs-lookup"><span data-stu-id="c812d-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="c812d-141">Cuma bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c812d-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="c812d-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c812d-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c812d-143">Özellik alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c812d-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="c812d-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c812d-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c812d-145">Özellik alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c812d-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="c812d-146">Haftasonlarını malzeme çekme için kapatıldı olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="c812d-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="c812d-147">Cumartesi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c812d-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="c812d-148">Malzeme çekme için Kapatıldı alanında Evet seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c812d-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="c812d-149">Pazar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c812d-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="c812d-150">Malzeme çekme için Kapatıldı alanında Evet seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c812d-150">Select Yes in the Closed for pickup field.</span></span>


