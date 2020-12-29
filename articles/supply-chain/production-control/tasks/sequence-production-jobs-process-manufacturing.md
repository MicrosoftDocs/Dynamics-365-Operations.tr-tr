---
title: Süreç üretimi için üretim işlerini sıralama
description: Bu prosedürde, planlanan siparişlerin renk ve paket boyutu önceliğine göre nasıl sıralanacağının gösterilmesi için örnek olarak boya ürünleri kullanılmıştır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db2c881f60b6e5251e2bcdf198da9e1c9f39a0e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439256"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="e0dfb-103">Süreç üretimi için üretim işlerini sıralama</span><span class="sxs-lookup"><span data-stu-id="e0dfb-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0dfb-104">Bu prosedürde, planlanan siparişlerin renk ve paket boyutu önceliğine göre nasıl sıralanacağının gösterilmesi için örnek olarak boya ürünleri kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="e0dfb-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USPI'dir.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="e0dfb-106">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="e0dfb-107">USPI için master planlama yürüme</span><span class="sxs-lookup"><span data-stu-id="e0dfb-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="e0dfb-108">Master planlama > Master planlama > Çalıştır > Master planlama öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="e0dfb-109">Master plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e0dfb-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e0dfb-111">MasterPlan'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="e0dfb-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-112">Click OK.</span></span>
    * <span data-ttu-id="e0dfb-113">Bu işlem, sıralama işlemi dahil Master Planlamayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="e0dfb-114">Bu işlem birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="e0dfb-115">Boya ürünleri için planlı siparişleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e0dfb-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="e0dfb-116">Master planlama > Master planlama > Planlı siparişler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="e0dfb-117">Madde ayrıntıları Hızlı Kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="e0dfb-118">Zamanlama ayrıntıları Hızlı Kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="e0dfb-119">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e0dfb-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0dfb-121">MasterPlan'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="e0dfb-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e0dfb-123">Madde numarası alanında 'P300' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e0dfb-124">Sipariş tarihini ve teslimat tarihini görmek için sağa doğru kaydırarak kilidi açın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="e0dfb-125">Bu maddelerin sipariş tarihinin Bugün olduğuna ve ürün adında da gösterildiği gibi, planlanan siparişler için teslim tarihlerinin, renk ve paket boyutu önceliğinden sonra sıralanmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="e0dfb-126">Ürün adını ve önceliğini görmek için bir madde numarasının üstüne gelin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="e0dfb-127">Boya için planlı siparişleri sıralama</span><span class="sxs-lookup"><span data-stu-id="e0dfb-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="e0dfb-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-128">Close the page.</span></span>
2. <span data-ttu-id="e0dfb-129">Master planlama > Master planlama > Sıralanan planlı siparişler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="e0dfb-130">Madde ayrıntıları Hızlı Kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e0dfb-131">Zamanlama ayrıntıları Hızlı Kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="e0dfb-132">Not: Burada, planlı siparişler için Başlangıç tarihi/saatinin 28 günlük zaman aralığı dönemi içindeki renk ve paket boyutuna göre sıralandığını görüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="e0dfb-133">Bu dönemler, Kampanya alanındaki bir sayıyla tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="e0dfb-134">Sıralı planlı sipariş formu, tipik bir planlı sipariş formu gibi hareket eder ve üretim planlayıcı, planlanan emirleri burada kesinleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="e0dfb-135">Tüm sıraları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-135">Mark all rows.</span></span>
6. <span data-ttu-id="e0dfb-136">Kabul et düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-136">Click Accept.</span></span>
    * <span data-ttu-id="e0dfb-137">Planlanan emirleri seçilen sıra eylemiyle Ertele veya Öne getir olarak günceller.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="e0dfb-138">Planlı siparişlerin sırasını doğrulama</span><span class="sxs-lookup"><span data-stu-id="e0dfb-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="e0dfb-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-139">Close the page.</span></span>
2. <span data-ttu-id="e0dfb-140">Master planlama > Master planlama > Planlı siparişler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="e0dfb-141">Madde ayrıntıları Hızlı Kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e0dfb-142">Zamanlama ayrıntıları Hızlı Kutusunu genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="e0dfb-143">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e0dfb-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e0dfb-145">MasterPlan'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="e0dfb-146">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0dfb-147">Madde numarası alanında 'P300' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e0dfb-148">Siparişlerin artık, renk ve boyut önceliğine göre sıralanacağına ve planlı siparişlerin ise en erken sipariş tarihinde ve teslim tarihinde bağlayacağına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="e0dfb-149">Sipariş tarihi sütununu veya Başlangıç tarihini Zamanlama Ayrıntıları Hızlı Kutusundan doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="e0dfb-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

