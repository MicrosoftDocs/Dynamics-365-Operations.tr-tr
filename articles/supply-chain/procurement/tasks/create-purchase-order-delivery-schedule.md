--- 
title: "Teslimat planı olan satınalma siparişi oluşturma"
description: "Bu prosedür, satınalma siparişi için teslimat oluşturmayı göstermektedir."
author: FrankDahl
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ae57d8e64b4888e6ff4678437d0b3da8eb05867d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="9ef38-103">Teslimat planı olan satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ef38-103">Create a purchase order with a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ef38-104">Bu prosedür, satınalma siparişi için teslimat oluşturmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="9ef38-105">Teslimat planı, bir siparişteki veya günlükteki miktarın birden fazla sevkiyatlar halinde teslim edilmesi istendiği zaman kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="9ef38-106">Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="9ef38-107">Bu prosedür tipik olarak bir satın alma temsilcisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="9ef38-108">Teslimat planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ef38-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="9ef38-109">Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9ef38-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-110">Click New.</span></span>
3. <span data-ttu-id="9ef38-111">Satıcı hesabı alanına, US-101 girin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="9ef38-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-112">Click OK.</span></span>
5. <span data-ttu-id="9ef38-113">Madde numarası alanına M0001 girin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="9ef38-114">Miktar alanına 10 yazın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="9ef38-115">Satınalma siparişi satırına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="9ef38-116">Teslimat planı öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="9ef38-117">Teslimat planı sayfası, sipariş satırı toplam miktarının satıcıdan teslim edileceği sevkiyat sayısını belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="9ef38-118">Varsayılan olarak, sistem orijinal satınalma satırının toplam miktarını ve diğer teslimat ayrıntılarını ilk teslimat planı satırına kopyalar.</span><span class="sxs-lookup"><span data-stu-id="9ef38-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="9ef38-119">Bu örnekte iki sevkiyat planı oluşturacağız ve ikinci sevkiyatın tarihi, ilk sevkiyattan bir hafta sonra olacak.</span><span class="sxs-lookup"><span data-stu-id="9ef38-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="9ef38-120">Miktar alanında miktarı 4 olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="9ef38-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-121">Click New.</span></span>
11. <span data-ttu-id="9ef38-122">Miktar alanına, kalan miktar olarak 6 girin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="9ef38-123">Teslimat tarihi alanında ilk teslimat satırındaki tarihten bir hafta sonraki tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="9ef38-124">Toplam ve Kalan alanlarına bakarak, teslimat planı satırlarına tahsis edilen toplam miktarı izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ef38-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="9ef38-125">Kalan miktar sıfır olduğunda, orijinal satırdan alınan tüm miktar plana tahsis edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="9ef38-126">Gider dönüştürme bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="9ef38-127">Burada seçenekler, teslimat planı satırları üzerinden masrafları nasıl dağıtmak istediğinizi kontrol etmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="9ef38-128">Brüt tutarları kopyala'yı seçerseniz her teslimat satırına orijinal sipariş satırındaki masraf tutarı kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="9ef38-129">Teslimat satırlarına tahsis et seçeneği orijinal satırdaki masrafı her bir teslimat satırındaki miktara göre böler.</span><span class="sxs-lookup"><span data-stu-id="9ef38-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="9ef38-130">Gider dönüştürme bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="9ef38-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-131">Click OK.</span></span>
    * <span data-ttu-id="9ef38-132">Teslimat planı siparişe artık uygulanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="9ef38-133">Ticari satırı olarak anılan orijinal sipariş satırı, birden fazla teslimatlı bir Siparişe dönüştürülmüştür.</span><span class="sxs-lookup"><span data-stu-id="9ef38-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="9ef38-134">Farklı bir simgeyle işaretlenir ve teslimat satırları için başlık olarak işlev görür.</span><span class="sxs-lookup"><span data-stu-id="9ef38-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="9ef38-135">İki teslimat satırının ilki olan ikinci sipariş satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="9ef38-136">Teslimat satırları olarak anılan iki yeni satır bir teslim planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ef38-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="9ef38-137">Sipariş orijinal satıra göre değil, bu satırlara göre işlenir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="9ef38-138">Onaylar, ürün girişi günlükleri veya faturalar gibi belgeler yazdırılırken yalnızca teslimat satırları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="9ef38-139">Teslimat planını değiştirin</span><span class="sxs-lookup"><span data-stu-id="9ef38-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="9ef38-140">Teslimat satırlarında miktarı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ef38-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="9ef38-141">Bunu yaparsanız, ticari satırı otomatik olarak güncelleştirilip, teslimat satırlarındaki toplam miktara çevrilir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="9ef38-142">İlk teslimat satırının miktar alanında miktarı 4'ten 5'e değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="9ef38-143">İlk sipariş satırını (ticari satırı) seçin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="9ef38-144">Ticari satırındaki miktar 11'e değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="9ef38-145">Teslimat planlarını kullanarak ürün girişini işleyin</span><span class="sxs-lookup"><span data-stu-id="9ef38-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="9ef38-146">Satınalma siparişi ürün girişi işlenmeden önce onaylanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="9ef38-147">Bu örnekte giriş doğrudan satınalma siparişi üzerinden kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="9ef38-148">Mallar ambara ulaştığında da giriş kaydedilmiş olur.</span><span class="sxs-lookup"><span data-stu-id="9ef38-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="9ef38-149">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="9ef38-150">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-150">Click Confirm.</span></span>
3. <span data-ttu-id="9ef38-151">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="9ef38-152">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-152">Click Product receipt.</span></span>
5. <span data-ttu-id="9ef38-153">Ürün girişi alanına herhangi bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="9ef38-154">Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ef38-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="9ef38-155">Miktar alanında, 'Sipariş edilen miktar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="9ef38-156">Bu seçenek, sipariş satırlarının birlikte oluşturulduğu miktar için girişin işleneceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="9ef38-157">Ürün girişi yazdır alanının Hayır olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="9ef38-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="9ef38-158">Bu örnekte, yazdırma gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="9ef38-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="9ef38-159">Satırlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="9ef38-160">Ürün girişinin orijinal sipariş satırı değil iki teslimat satırı için oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9ef38-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="9ef38-161">Giriş ambarda kaydedilmişse teslimat planı satırlarında da kaydedilmiş olur.</span><span class="sxs-lookup"><span data-stu-id="9ef38-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="9ef38-162">Satırlar bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="9ef38-163">Girişi nakletmek için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ef38-163">Click OK to post the receipt.</span></span>


