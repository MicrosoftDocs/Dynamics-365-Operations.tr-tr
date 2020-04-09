---
title: " Süreklilik zamanlamaları tanımlama"
description: Bu konu süreklilik programının ayarlanmasını gösterir (aksi takdirde tekrarlanan siparişler olarak bilinir).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06fd1e23ad84fdc5e94e309717d5a96fbff45035
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140911"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="456da-103"> Süreklilik zamanlamaları tanımlama</span><span class="sxs-lookup"><span data-stu-id="456da-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="456da-104">Bu konu süreklilik programının ayarlanmasını gösterir (aksi takdirde tekrarlanan siparişler olarak bilinir).</span><span class="sxs-lookup"><span data-stu-id="456da-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="456da-105">Bu konu, demo verilerinde USRT şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="456da-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="456da-106">Süreklilik programı oluşturma</span><span class="sxs-lookup"><span data-stu-id="456da-106">Create continuity program</span></span>
1. <span data-ttu-id="456da-107">Retail and Commerce > Süreklilik > Süreklilik programları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="456da-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="456da-108">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="456da-108">Click New.</span></span>
3. <span data-ttu-id="456da-109">Planlama kodu alanına süreklilik planı kodunu yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="456da-110">Sipariş başlangıç alanında 'İlk olay'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="456da-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="456da-111">Bir müşteri süreklilik programı için yeni bir sipariş verirse, ürünü nakliye edileceği iki yol vardır:  1.</span><span class="sxs-lookup"><span data-stu-id="456da-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="456da-112">İlk olay: süreklilik programındaki ilk ürün sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="456da-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="456da-113">2.</span><span class="sxs-lookup"><span data-stu-id="456da-113">2.</span></span> <span data-ttu-id="456da-114">Geçerli olay: Geçerli ürün sevk edilir.</span><span class="sxs-lookup"><span data-stu-id="456da-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="456da-115">Örneğin,</span><span class="sxs-lookup"><span data-stu-id="456da-115">For example.</span></span> <span data-ttu-id="456da-116">programdaki üç ay içinde müşteri programdaki üçüncüyü alır.</span><span class="sxs-lookup"><span data-stu-id="456da-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="456da-117">Sipariş başlangıç tarihi komutu için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="456da-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="456da-118">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-118">Click Add line.</span></span>
7. <span data-ttu-id="456da-119">Madde numarası alanında ilk ürün için madde numarasını ('0013') girin.</span><span class="sxs-lookup"><span data-stu-id="456da-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="456da-120">"CP" yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-120">Type 'CP'.</span></span>
9. <span data-ttu-id="456da-121">İlk ürünün sipariş için kullanılabilir olacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="456da-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="456da-122">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-122">Click Add line.</span></span>
11. <span data-ttu-id="456da-123">Madde numarası alanına '0014' yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="456da-124">Tarih aralık kodu alanında değeri temizleyerek alanı boşaltın.</span><span class="sxs-lookup"><span data-stu-id="456da-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="456da-125">Bu yordam için tarih aralığını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="456da-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="456da-126">Tarihi ilk öğenin başlangıç tarihinden artırımlı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="456da-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="456da-127">Buraya ürünlerin sevk edildiği aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="456da-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="456da-128">"30" yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-128">Type '30'.</span></span>
    * <span data-ttu-id="456da-129">Aylık program için aralık olarak 30 gün girin.</span><span class="sxs-lookup"><span data-stu-id="456da-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="456da-130">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-130">Click Add line.</span></span>
15. <span data-ttu-id="456da-131">Madde numarası alanına '0015' yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="456da-132">"Son" yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-132">Type 'End'.</span></span>
17. <span data-ttu-id="456da-133">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="456da-134">Süreklilik maddesine atama</span><span class="sxs-lookup"><span data-stu-id="456da-134">Assign to continuity item</span></span>
1. <span data-ttu-id="456da-135">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="456da-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="456da-136">'0016' maddesini seçin.</span><span class="sxs-lookup"><span data-stu-id="456da-136">Select item '0016'.</span></span>
    * <span data-ttu-id="456da-137">Bu yordam için 0016 madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="456da-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="456da-138">Normalde çağrı merkezinde bir satış siparişi verildiğinde uygulanan ek süreklilik iş mantığı olan bir serbest bırakılan ürünü oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="456da-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="456da-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="456da-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-140">Click Edit.</span></span>
5. <span data-ttu-id="456da-141">Satış bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="456da-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="456da-142">Bu maddenin temsil ettiği süreklilik programını buraya girin.</span><span class="sxs-lookup"><span data-stu-id="456da-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="456da-143">Daha önce oluşturduğunuz Planlama kodunu yazın.</span><span class="sxs-lookup"><span data-stu-id="456da-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="456da-144">Bu madde bir çağrı merkezinde satıldığında, seçili süreklilik programından ek iş mantığı uygulanır.</span><span class="sxs-lookup"><span data-stu-id="456da-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="456da-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="456da-145">Click Save.</span></span>

