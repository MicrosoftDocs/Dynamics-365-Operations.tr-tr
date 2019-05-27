---
title: Üretim akışını ve sürümünü doğrulama
description: Bu yordam, yalın imalat için yeni bir üretim akışının ve bir ilk sürümün nasıl oluşturulacağını gösterir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae4c5f55d317a99e23ba6e76fc50ddece1e55a1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571416"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="4a0ee-103">Üretim akışını ve sürümünü doğrulama</span><span class="sxs-lookup"><span data-stu-id="4a0ee-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a0ee-104">Bu yordam, yalın imalat için yeni bir üretim akışının ve bir ilk sürümün nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="4a0ee-105">Önkoşullar: Yalın imalat için üretim parametreleri ve sınıf zamanı için ölçü birimleri tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="4a0ee-106">Bir Değer akışı ve Üretim grubu tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="4a0ee-107">Üretim akışları ve faaliyetleri kavramlarını öğrenmek üzere Yalın imalat hakkındaki teknik incelemelere bakın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="4a0ee-108">Bu yordam, demo verilerindeki USMF tüzel kişiliğini referans alır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="4a0ee-109">Ancak, tüzel kişiliklerin Yalın imalat için yapılandırıldığı varsayılarak diğer tüzel kişilikler de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="4a0ee-110">Üretim akışı oluşturun</span><span class="sxs-lookup"><span data-stu-id="4a0ee-110">Create a production flow</span></span>
1. <span data-ttu-id="4a0ee-111">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="4a0ee-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-112">Click New.</span></span>
3. <span data-ttu-id="4a0ee-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4a0ee-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4a0ee-115">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4a0ee-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4a0ee-117">Bir değer akışı, değer akışının tüm faaliyetlerini ve hareketlerini kapsayan faaliyet birimidir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="4a0ee-118">Bu aşamada, işletme birimleri bir tüzel varlık ile sınırlıdır ve hiçbir ek işlevselliğe sahip değildirler.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="4a0ee-119">Üretim grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4a0ee-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4a0ee-121">Üretim grupları, bir üretim işlemi için malzeme, işçilik ve Süren iş hesaplarını tanımlamayı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="4a0ee-122">Üretim akışını bir hesap bağlamıyla ilişkilendirmek için bir üretim grubu seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="4a0ee-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="4a0ee-124">Üretim akışı sürümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="4a0ee-124">Create a production flow version</span></span>
1. <span data-ttu-id="4a0ee-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-125">Click Add.</span></span>
2. <span data-ttu-id="4a0ee-126">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="4a0ee-127">Sürümün bitiş tarihini, etkin sürümler için bile, istediğiniz zaman güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="4a0ee-128">Sürüm dışında bir aşama planlamak için sürümün bitiş tarihini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="4a0ee-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-129">Click OK.</span></span>
4. <span data-ttu-id="4a0ee-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="4a0ee-131">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="4a0ee-132">Takt birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="4a0ee-133">Ortalama takt zamanı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="4a0ee-134">Üretim akışı sürümünün takt denetimi için hedeflenen ortalama takt zamanını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="4a0ee-135">Takt, zaman aralığına düşen miktar olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="4a0ee-136">Verilen örnekte, takt zamanı 10 parça başına 0,2 saattir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="4a0ee-137">8 saatlik bir çalışma zamanı için, günlük 400 parçalık üretim kapasitesine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="4a0ee-138">Miktar esası döngüsü alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="4a0ee-139">Sürümler detayları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="4a0ee-140">Minimum takt zamanı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="4a0ee-141">Minimum takt zamanı ortalama takt süresine eşit veya daha küçük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="4a0ee-142">Maksimum takt zamanı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="4a0ee-143">Maksimum takt zamanı ortalama takt süresine eşit veya daha büyük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="4a0ee-144">Gerçek döngü süresi için dönem alanında bir gün sayısı gir</span><span class="sxs-lookup"><span data-stu-id="4a0ee-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="4a0ee-145">Döneme ait gerçek döngü süresi, güncel dakikadan geriye yönelik toplanarak hesaplanan gerçek döngü süresinin gün olarak sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="4a0ee-146">Değer herhangi bir zamanda değiştirilebilir ve yalnızca gerçek döngü zamanının hesaplanması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="4a0ee-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4a0ee-147">Click Save.</span></span>

