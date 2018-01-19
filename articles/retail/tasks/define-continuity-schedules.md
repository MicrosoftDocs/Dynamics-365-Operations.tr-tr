--- 
title: " Süreklilik zamanlamaları tanımlama"
description: "Bu konu süreklilik programının ayarlanmasını gösterir (aksi takdirde tekrarlanan siparişler olarak bilinir)."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 7add873705fd67c80d5d91f870bfa2c2e7952512
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---
# <a name="define-continuity-schedules"></a><span data-ttu-id="ae15a-103"> Süreklilik zamanlamaları tanımlama</span><span class="sxs-lookup"><span data-stu-id="ae15a-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ae15a-104">Bu konu süreklilik programının ayarlanmasını gösterir (aksi takdirde tekrarlanan siparişler olarak bilinir).</span><span class="sxs-lookup"><span data-stu-id="ae15a-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="ae15a-105">Bu konu, demo verilerinde USRT şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ae15a-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="ae15a-106">Süreklilik programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ae15a-106">Create continuity program</span></span>
1. <span data-ttu-id="ae15a-107">Perakende ve ticaret > Süreklilik > Süreklilik programları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-107">Go to Retail and commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="ae15a-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-108">Click New.</span></span>
3. <span data-ttu-id="ae15a-109">Planlama kodu alanına süreklilik planı kodunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="ae15a-110">Sipariş başlangıç alanında 'İlk olay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="ae15a-111">Bir müşteri süreklilik programı için yeni bir sipariş verirse, ürünü nakliye edileceği iki yol vardır:  1.</span><span class="sxs-lookup"><span data-stu-id="ae15a-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="ae15a-112">İlk olay: süreklilik programındaki ilk ürün sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="ae15a-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="ae15a-113">2.</span><span class="sxs-lookup"><span data-stu-id="ae15a-113">2.</span></span> <span data-ttu-id="ae15a-114">Geçerli olay: Geçerli ürün sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="ae15a-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="ae15a-115">Örneğin,</span><span class="sxs-lookup"><span data-stu-id="ae15a-115">For example.</span></span> <span data-ttu-id="ae15a-116">programdaki üç ay içinde müşteri programdaki üçüncüyü alır.</span><span class="sxs-lookup"><span data-stu-id="ae15a-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="ae15a-117">Sipariş başlangıç tarihi komutu için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="ae15a-118">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-118">Click Add line.</span></span>
7. <span data-ttu-id="ae15a-119">Madde numarası alanında ilk ürün için madde numarasını ('0013') girin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="ae15a-120">"CP" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-120">Type 'CP'.</span></span>
9. <span data-ttu-id="ae15a-121">İlk ürünün sipariş için kullanılabilir olacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="ae15a-122">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-122">Click Add line.</span></span>
11. <span data-ttu-id="ae15a-123">Madde numarası alanına '0014' yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="ae15a-124">Tarih aralık kodu alanında değeri temizleyerek alanı boşaltın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="ae15a-125">Bu yordam için tarih aralığını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="ae15a-126">Tarihi ilk öğenin başlangıç tarihinden artırımlı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="ae15a-127">Buraya ürünlerin sevk edildiği aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="ae15a-128">"30" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-128">Type '30'.</span></span>
    * <span data-ttu-id="ae15a-129">Aylık program için aralık olarak 30 gün girin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="ae15a-130">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-130">Click Add line.</span></span>
15. <span data-ttu-id="ae15a-131">Madde numarası alanına '0015' yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="ae15a-132">"Son" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-132">Type 'End'.</span></span>
17. <span data-ttu-id="ae15a-133">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="ae15a-134">Süreklilik maddesine atama</span><span class="sxs-lookup"><span data-stu-id="ae15a-134">Assign to continuity item</span></span>
1. <span data-ttu-id="ae15a-135">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ae15a-136">'0016' maddesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-136">Select item '0016'.</span></span>
    * <span data-ttu-id="ae15a-137">Bu yordam için 0016 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="ae15a-138">Normalde çağrı merkezinde bir satış siparişi verildiğinde uygulanan ek süreklilik iş mantığı olan bir serbest bırakılan ürünü oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="ae15a-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="ae15a-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ae15a-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-140">Click Edit.</span></span>
5. <span data-ttu-id="ae15a-141">Satış bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="ae15a-142">Bu maddenin temsil ettiği süreklilik programını buraya girin.</span><span class="sxs-lookup"><span data-stu-id="ae15a-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="ae15a-143">Daha önce oluşturduğunuz Planlama kodunu yazın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="ae15a-144">Bu madde bir çağrı merkezinde satıldığında, seçili süreklilik programından ek iş mantığı uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ae15a-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="ae15a-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae15a-145">Click Save.</span></span>


