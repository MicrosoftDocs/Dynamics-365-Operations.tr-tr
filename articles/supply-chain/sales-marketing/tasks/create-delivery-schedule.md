---
title: Teslimat planı oluşturun
description: Bu prosedür, satış siparişi için teslimat oluşturmayı göstermektedir.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af983b30530a7f5d0a82f98deeb12180c42d86cd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215827"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="a89cd-103">Teslimat planı oluşturun</span><span class="sxs-lookup"><span data-stu-id="a89cd-103">Create delivery schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a89cd-104">Bu prosedür, satış siparişi için teslimat oluşturmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a89cd-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="a89cd-105">Teslimat planı, bir siparişteki veya teklifteki miktarın birden fazla sevkiyatlar halinde teslim edilmesi istendiği zaman kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a89cd-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="a89cd-106">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a89cd-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="a89cd-107">Teslimat planı oluşturun</span><span class="sxs-lookup"><span data-stu-id="a89cd-107">Create delivery schedule</span></span>
1. <span data-ttu-id="a89cd-108">Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="a89cd-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-109">Click New.</span></span>
3. <span data-ttu-id="a89cd-110">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="a89cd-111">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-111">Click OK.</span></span>
5. <span data-ttu-id="a89cd-112">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="a89cd-113">Miktar alanına 1'den büyük bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="a89cd-114">Satış siparişi satırına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-114">Click Sales order line.</span></span>
8. <span data-ttu-id="a89cd-115">Teslimat planı öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="a89cd-116">Teslimat planı sayfası, sipariş satırı toplam miktarının müşteriye teslim edileceği sevkiyat sayısını belirtebildiğiniz yerdir.</span><span class="sxs-lookup"><span data-stu-id="a89cd-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="a89cd-117">Varsayılan olarak, sistem orijinal satış satırının toplam miktarını ve diğer teslimat ayrıntılarını ilk teslimat planı satırına kopyalar.</span><span class="sxs-lookup"><span data-stu-id="a89cd-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="a89cd-118">Bu örnekte iki sevkiyat planı oluşturacağız ve ikinci sevkiyatın tarihi, ilkinden bir hafta sonra olacak.</span><span class="sxs-lookup"><span data-stu-id="a89cd-118">In this example, we'll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="a89cd-119">Miktar alanına toplam miktarın bir kısmı olan bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="a89cd-120">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-120">Click New.</span></span>
11. <span data-ttu-id="a89cd-121">Miktar alanına, kalan miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="a89cd-122">Talep edilen sevk tarihi alanına, ilk teslimat satırı tarihinden bir hafta sonrasına denk gelen tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="a89cd-123">Masraf dönüştürme hızlı sekmesindeki iki seçenek, masrafların, orijinal sipariş satırına atandıktan sonra teslimat planı satırlarına nasıl dağıtılmasını istediğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="a89cd-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they've been assigned to the original order line.</span></span> <span data-ttu-id="a89cd-124">Brüt tutarları kopyala'yı seçerseniz, her satıra aynı masraf tutarı kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="a89cd-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="a89cd-125">Teslimat satırlarına tahsis et seçeneği, masrafı teslimat satırlarına eşit olarak böler.</span><span class="sxs-lookup"><span data-stu-id="a89cd-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="a89cd-126">Yalnızca sabit masraflar bölünebilir, ancak değişken masraflar satırlara kopyalanmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="a89cd-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="a89cd-127">İmleci ikinci teslimat satırından uzaklaştırarak sayfayı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="a89cd-128">Toplam ve Kalan alanlarına bakarak, teslimat planı satırlarına tahsis edilen toplam miktarı izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a89cd-128">You can keep track of the total quantity that's allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="a89cd-129">Kalan miktar sıfır olduğunda, orijinal satırdan alınan tüm miktar plana tahsis edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a89cd-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="a89cd-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-130">Click OK.</span></span>
    * <span data-ttu-id="a89cd-131">Teslimat planı artık diğer sipariş satırlarına kopyalandı.</span><span class="sxs-lookup"><span data-stu-id="a89cd-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="a89cd-132">Ticari satırı olarak anılan orijinal sipariş satırı, birden fazla teslimatlı bir Siparişe dönüştürülmüştür.</span><span class="sxs-lookup"><span data-stu-id="a89cd-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="a89cd-133">Farklı bir simgeyle işaretlenir ve teslimat satırlar için üst bilgi işlevi görür.</span><span class="sxs-lookup"><span data-stu-id="a89cd-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="a89cd-134">Teslimat satırları olarak başvurulan iki yeni satır bir teslimat planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a89cd-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="a89cd-135">Sipariş orijinal satıra göre değil, bu satırlara göre işlenir.</span><span class="sxs-lookup"><span data-stu-id="a89cd-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="a89cd-136">Onay makbuzu, malzeme çekme listesi, sevk irsaliyesi, fatura gibi belgeler yazdırılırken yalnızca teslimat satırları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a89cd-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="a89cd-137">Teslimat satırları farklı teslim tarihleri; miktarları; teslimat şekilleri; tesis ve ambar gibi depolama boyutları içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a89cd-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="a89cd-138">Ancak, ürün boyutları mutlaka ticari satırındaki boyutlarla eşleşmek zorundadır ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="a89cd-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="a89cd-139">Miktar alanına, mevcut sayıdan daha büyük bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="a89cd-140">Miktarın yeniden hesaplanmasının etkisini görmek için ticari satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="a89cd-141">Eylem Bölmesinde, Çek ve paketle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="a89cd-142">Sevk irsaliyesini deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="a89cd-143">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="a89cd-144">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="a89cd-145">Sevk irsaliyesinin orijinal sipariş satırı için değil, bu iki teslimat planı satırı için oluşturulacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="a89cd-146">Sevk irsaliyesi yazdır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a89cd-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="a89cd-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-147">Click OK.</span></span>
23. <span data-ttu-id="a89cd-148">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-148">Click Yes.</span></span>
24. <span data-ttu-id="a89cd-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a89cd-149">Close the page.</span></span>

