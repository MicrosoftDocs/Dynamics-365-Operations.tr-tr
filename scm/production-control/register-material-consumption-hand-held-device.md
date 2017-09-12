---
title: "Mobil cihaz kullanarak malzeme tüketimini kaydetme"
description: "Bu konu, bir taşınabilir aygıt kullanarak üretimdeki ham madde tüketimini kaydetmeyi sağlayan bir iş akışını açıklar."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: tr-tr
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="6c286-103">Mobil cihaz kullanarak malzeme tüketimini kaydetme</span><span class="sxs-lookup"><span data-stu-id="6c286-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="6c286-104">Bu konu, bir taşınabilir aygıt kullanarak üretimdeki ham madde tüketimini kaydetmeyi sağlayan bir iş akışını açıklar.</span><span class="sxs-lookup"><span data-stu-id="6c286-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="6c286-105">Giriş</span><span class="sxs-lookup"><span data-stu-id="6c286-105">Introduction</span></span>
------------

<span data-ttu-id="6c286-106">Bu iş akışı malzeme izlenebilirlik için katı bir gereksinim varsa geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6c286-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="6c286-107">Bu gibi durumlarda, malzemelerin izlenebilirliğini korumak için tam saat ve miktar tüketim için bildirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6c286-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="6c286-108">Bu işlem, kayıt zamanı ile gerçek tüketimin gerçekleştiği zaman arasında bir denkleştirme bulunan önce veya sonra otomatik tüketim işleminin tersi olarak görülebilir.</span><span class="sxs-lookup"><span data-stu-id="6c286-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="6c286-109">Bu, izlenebilirlik gereksinimleri olan bazı maddeler için neden otomatik tüketimi stratejisi kullanılamayacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="6c286-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="6c286-110">Taşınabilir aygıt kullanarak üretimdeki ham madde tüketimi kaydını etkinleştirmek için bir iş akışının nasıl ayarlanacağını açıklayana basit bir senaryoya bakalım.</span><span class="sxs-lookup"><span data-stu-id="6c286-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="6c286-111">Senaryo ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="6c286-111">Scenario details</span></span>

<span data-ttu-id="6c286-112">Sürekli üretim işlemi (5) toplu işlem tarafından denetlenen hammadde RM-100 tüketir.</span><span class="sxs-lookup"><span data-stu-id="6c286-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="6c286-113">Yerleşimde PL-1 plakası üzerinde eldeki malzeme Toplu-001 (1)'dir, her birinin miktarı 100 lbs olan B1 ve B2 toplu işleri mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="6c286-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="6c286-114">Ambar işi (2) RM-100 için serbest bırakılır ve işlenir ve malzeme plaka denetimsiz olarak tanımlanan PIL-01(3) imalat giriş yerleşimine Toplu-001'den çekilir.</span><span class="sxs-lookup"><span data-stu-id="6c286-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="6c286-115">Makine operatörü üretim giriş yerinden (3) gelen malzemeyi tartar ve ağırlığı ve toplu iş numarasını (4) tüketildi olarak kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6c286-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="6c286-116">Üretim giriş yerleşiminden, malzemenin bir bölümü tanımlanan zaman aralıklarına el ile üretim işlemine eklenir.</span><span class="sxs-lookup"><span data-stu-id="6c286-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="6c286-117">Makine operatörü malzemeyi eklediği zaman, tartıda ölçülür ve toplu iş numarası kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6c286-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="6c286-118">Taşınabilir bir cihaz kullanarak tüketimi kaydetmek için iş akışı ayarlama</span><span class="sxs-lookup"><span data-stu-id="6c286-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="6c286-119">Ürün reçetesinde toplu iş denetimli ham madde RM-100 bulunan bir tamamlanmış bir ürün oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6c286-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="6c286-120">Yerleşime miktarı 100 olan iki RM-100 toplu işi (B1 ve B2) ekleyin: PL-1 plakasında Toplu-001</span><span class="sxs-lookup"><span data-stu-id="6c286-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="6c286-121">RM-100 için ürün reçetesi satırındaki otomatik tüketim ilkesi **El ile** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="6c286-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="6c286-122">Üretim girişi yerleşimini PIL-01 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6c286-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="6c286-123">Bunu, ambar 51'de bu yerleşimi varsayılan üretim giriş yerleşimi olarak seçerek yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c286-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="6c286-124">Yeni bir mobil cihaz menü öğesi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="6c286-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="6c286-125">**Menü öğesi adı** - Malzeme tüketimini kaydet.</span><span class="sxs-lookup"><span data-stu-id="6c286-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="6c286-126">**Başlık** - Malzeme tüketimini kaydet.</span><span class="sxs-lookup"><span data-stu-id="6c286-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="6c286-127">**Mod** - Dolaylı.</span><span class="sxs-lookup"><span data-stu-id="6c286-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="6c286-128">**Etkinllik kodu** - Malzeme tüketimini kaydet.</span><span class="sxs-lookup"><span data-stu-id="6c286-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="6c286-129">Menü öğesini **Üretim Mobil** cihaz menüsüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6c286-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="6c286-130">Bitmiş ürün için bir üretim emri oluşturun:</span><span class="sxs-lookup"><span data-stu-id="6c286-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="6c286-131">**Madde numarası** - FG-100</span><span class="sxs-lookup"><span data-stu-id="6c286-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="6c286-132">**Tesis** - 5</span><span class="sxs-lookup"><span data-stu-id="6c286-132">**Site** - 5</span></span> 
-    <span data-ttu-id="6c286-133">**Ambar** - 51</span><span class="sxs-lookup"><span data-stu-id="6c286-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="6c286-134">**Miktar** - 150</span><span class="sxs-lookup"><span data-stu-id="6c286-134">**Quantity** - 150</span></span>

<span data-ttu-id="6c286-135">Üretim emri **Tahmini** ve **Serbest bırakıldı** olur ve ambar işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6c286-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="6c286-136">Taşınabilir cihaz için ham madde çekme iş akışını kullanarak işi tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="6c286-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="6c286-137">Bu malzemeyi toplu yerleşimden üretim giriş yerleşimi PIL-01'e getirir.</span><span class="sxs-lookup"><span data-stu-id="6c286-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="6c286-138">İş tamamlandığında, malzemenin durumu **Üretim giriş yerleşiminde çekildi** olur.</span><span class="sxs-lookup"><span data-stu-id="6c286-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="6c286-139">İş işlendikten sonra durum **Çekildi** veya **Fiziksel olarak rezerve** olabilir.</span><span class="sxs-lookup"><span data-stu-id="6c286-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="6c286-140">Bu **Ambar formuna koyduktan sonra çıkış durumu** parametresiyle yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="6c286-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="6c286-141">Üretim emrini istemciden veya taşınabilir cihazdan **Üretim başlangıcı** menü öğesini kullanarak başlatın.</span><span class="sxs-lookup"><span data-stu-id="6c286-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="6c286-142">Üretim emri başlatıldıktan sonra, taşınabilir cihaz için malzeme tüketimini iş akışıyla kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c286-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="6c286-143">Toplu işin B1 25 lbs tüketim kaydederek başlayalım.</span><span class="sxs-lookup"><span data-stu-id="6c286-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="6c286-144">Taşınabilir cihaz menüsünden **Malzeme** **tüketimini kaydet** menü öğesini seçip aşağıdaki ayrıntıları girin:</span><span class="sxs-lookup"><span data-stu-id="6c286-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="6c286-145">Üretim emri numarası.</span><span class="sxs-lookup"><span data-stu-id="6c286-145">The production order number.</span></span> 
-    <span data-ttu-id="6c286-146">Malzemenin tüketileceği yerleşim, burada PIL-01.</span><span class="sxs-lookup"><span data-stu-id="6c286-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="6c286-147">Madde numarası RM-100.</span><span class="sxs-lookup"><span data-stu-id="6c286-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="6c286-148">Toplu iş numarası B1.</span><span class="sxs-lookup"><span data-stu-id="6c286-148">Batch number B1.</span></span> 
-    <span data-ttu-id="6c286-149">Miktar 25.</span><span class="sxs-lookup"><span data-stu-id="6c286-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="6c286-150">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6c286-150">Select **OK**.</span></span>

<span data-ttu-id="6c286-151">"Günlük satırı oluşturuldu" iletisi ekranda görünür.</span><span class="sxs-lookup"><span data-stu-id="6c286-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="6c286-152">Üretim emrinde, RM-100 madde numarası ve B1 toplu iş numarası için **Üretim malzeme çekme listesi** türünde açık bir günlük bulunur.</span><span class="sxs-lookup"><span data-stu-id="6c286-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="6c286-153">Şimdi kaydınıza (örneğin toplu iş numarası B2'de) devam etmeyi seçebilirsiniz ve **Tamam**'ı her seçtiğinizde açık günlüğe yeni bir günlük satırı eklenir.</span><span class="sxs-lookup"><span data-stu-id="6c286-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="6c286-154">Kaydınız tamamladıktan sonra günlüğü deftere nakletmek ve iş akışını sonlandırmak için **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6c286-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="6c286-155">Ek açıklamalar</span><span class="sxs-lookup"><span data-stu-id="6c286-155">Additional comments</span></span> 

-   <span data-ttu-id="6c286-156">Bir günlük satırı oluşturulduktan sonra kullanıcı bir iş akışını iptal ederse, günlük deftere nakledilmemiş durumda kalır ancak ilerleyen bir noktada kullanıcı aynı üretim emri için iş akışını kullanırsa, satırlar yeni bir günlük yerine açık günlüğe eklenir.</span><span class="sxs-lookup"><span data-stu-id="6c286-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="6c286-157">Yeni iş akışı seri numaraları kaydını da destekler.</span><span class="sxs-lookup"><span data-stu-id="6c286-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="6c286-158">Seçilen üretim emri veya toplu iş emri için yalnızca ürün reçetesinde veya formülde tanımlanan bir madde numarası kaydetmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="6c286-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="6c286-159">Malzeme fazla tüketilebilir.</span><span class="sxs-lookup"><span data-stu-id="6c286-159">Material can be overconsumed.</span></span> <span data-ttu-id="6c286-160">Örneğin, malzemenin 100 libre miktarında tüketileceği tahmin edilirse, ürün daha fazla miktarda (örneğin 105 libre) tüketilebilir.</span><span class="sxs-lookup"><span data-stu-id="6c286-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



