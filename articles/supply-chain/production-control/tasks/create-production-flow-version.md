---
title: Üretim akışı sürümü oluşturma
description: Bu yordam, yeni bir üretim akışı sürümünü oluşturmaya odaklanır.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5512c30be586c75d2571d60588a1179c0d47570b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147009"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="585eb-103">Üretim akışı sürümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="585eb-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="585eb-104">Bu yordam, yeni bir üretim akışı sürümünü oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="585eb-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="585eb-105">Bu yordam için yalın üretim ve sınıf zaman ölçümü birimleri için üretim parametreleri tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="585eb-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="585eb-106">Ayrıca bir değer akışı ve üretim grubu tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="585eb-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="585eb-107">Üretim akışları ve yalın üretim faaliyetleri hakkında daha fazla bilgi için Microsoft Dynamics AX için yalın üretim teknik incelemelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="585eb-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="585eb-108">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="585eb-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="585eb-109">Üretim akışı oluşturun</span><span class="sxs-lookup"><span data-stu-id="585eb-109">Create a production flow</span></span>
1. <span data-ttu-id="585eb-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="585eb-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="585eb-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-111">Click New.</span></span>
3. <span data-ttu-id="585eb-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="585eb-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="585eb-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="585eb-114">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="585eb-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="585eb-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="585eb-116">Değer akış türünde bir işletme birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="585eb-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="585eb-117">Bir değer akışı, değer akışının tüm aktivitelerini ve hareketlerini kapsayan işletme bir birimidir.</span><span class="sxs-lookup"><span data-stu-id="585eb-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="585eb-118">Bu aşamada, işletme birimleri bir tüzel varlık ile sınırlıdır ve hiçbir ek işlevselliğe sahip değildirler.</span><span class="sxs-lookup"><span data-stu-id="585eb-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="585eb-119">Üretim grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="585eb-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="585eb-121">Üretim akışı için bir üretim grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="585eb-121">Select a production group for the production flow.</span></span> <span data-ttu-id="585eb-122">Üretim grupları, bir üretim işlemi için malzeme, işçilik ve Süren iş hesaplarını tanımlamayı sağlar.</span><span class="sxs-lookup"><span data-stu-id="585eb-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="585eb-123">Üretim akışını bir hesap bağlamıyla ilişkilendirmek için bir üretim grubu seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="585eb-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="585eb-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="585eb-125">Üretim akışı sürümü oluşturma</span><span class="sxs-lookup"><span data-stu-id="585eb-125">Create a production flow version</span></span>
1. <span data-ttu-id="585eb-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="585eb-126">Click Add.</span></span>
2. <span data-ttu-id="585eb-127">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="585eb-128">Gerekirse, sürüm için bir sona erme tarihi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="585eb-129">Etkin versiyonlar için bile verilen istediğiniz zaman güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="585eb-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="585eb-130">Aşama bir sürümünü planlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="585eb-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="585eb-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-131">Click OK.</span></span>
4. <span data-ttu-id="585eb-132">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="585eb-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="585eb-133">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="585eb-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="585eb-134">Takt birimini ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="585eb-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="585eb-135">Ortalama takt zamanı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="585eb-136">Sürümün ortalama takt süresini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="585eb-137">Üretim akışı sürümünün takt denetimi için hedeflenen ortalama takt zamanını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="585eb-138">Takt, zaman aralığına düşen miktar olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="585eb-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="585eb-139">Örnekte, takt zamanı 10 parça başına 0.2 saattir.</span><span class="sxs-lookup"><span data-stu-id="585eb-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="585eb-140">8 saatlik bir çalışma zamanı için, günlük 400 parçalık üretim kapasitesine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="585eb-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="585eb-141">Miktar esası döngüsü alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="585eb-142">Ortalama takt zamanına düşen döngü başına miktarı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="585eb-143">Sürüm detayları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="585eb-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="585eb-144">Minimum takt zamanı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="585eb-145">Minimum takt zamanını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-145">Define the minimum takt time.</span></span> <span data-ttu-id="585eb-146">Minimum takt zamanı ortalama takt süresine eşit veya daha küçük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="585eb-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="585eb-147">Maksimum takt zamanı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="585eb-148">Maksimum takt zamanı ortalama takt süresine eşit veya daha büyük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="585eb-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="585eb-149">Döneme ait gerçek döngü süresi (gün) alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="585eb-150">Döneme ait gerçek döngü süresini, gün sayısı olarak girin.</span><span class="sxs-lookup"><span data-stu-id="585eb-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="585eb-151">Döneme ait gerçek döngü süresi, güncel dakikadan geriye yönelik toplanarak hesaplanan gerçek döngü süresinin gün olarak sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="585eb-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="585eb-152">Değer herhangi bir zamanda değiştirilebilir ve yalnızca gerçek döngü zamanının hesaplanması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="585eb-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="585eb-153">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="585eb-153">Click Save.</span></span>

