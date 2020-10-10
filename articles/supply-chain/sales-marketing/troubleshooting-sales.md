---
title: Satış siparişleri ile ilgili sorun giderme
description: Bu konu, satış siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6e51723915892f465ce09d09ee9ed622bab9451e
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889469"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="8d27b-103">Satış siparişleri ile ilgili sorun giderme</span><span class="sxs-lookup"><span data-stu-id="8d27b-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="8d27b-104">Bu konu, satış siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8d27b-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="8d27b-105">Satış siparişi başlığındaki konumu değiştirdiğimde vergi bilgileri güncelleştirilmiyor.</span><span class="sxs-lookup"><span data-stu-id="8d27b-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d27b-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="8d27b-106">Issue description</span></span>

<span data-ttu-id="8d27b-107">Bir satış siparişi başlığında veya satır düzeyinde tesis, ambar veya teslimat adresi değiştirilirse, duruma ait vergi bilgileri satırlar için otomatik olarak güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="8d27b-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d27b-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="8d27b-108">Issue resolution</span></span>

<span data-ttu-id="8d27b-109">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="8d27b-109">This behavior is by design.</span></span> <span data-ttu-id="8d27b-110">Bu sorun, teslimat adresi, tesis ve ambarın satır düzeyinde otomatik olarak değiştirilemediğinden de oluşur.</span><span class="sxs-lookup"><span data-stu-id="8d27b-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="8d27b-111">Bunları el ile güncelleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="8d27b-112">Aynı dönem veya çakışan dönemler için iki ticari sözleşme varsa, her zaman aynı sözleşme satırı seçilir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d27b-113">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="8d27b-113">Issue description</span></span>

<span data-ttu-id="8d27b-114">İki ticari sözleşme aynı dönem veya örtüşen dönemler için tanımlanmışsa, bu malzemeleri içeren satış siparişi satırları oluşturduğunuzda, aynı ticari sözleşme her seferinde seçilmiş olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="8d27b-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d27b-115">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="8d27b-115">Issue resolution</span></span>

<span data-ttu-id="8d27b-116">Belirli bir tarihe ait birden fazla ticari sözleşme varsa, en düşük fiyata sahip olan ticari sözleşme her zaman seçilir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="8d27b-117">Daha fazla bilgi için, aşağıdaki teknik incelemeyi karşıdan yükleyin: [Microsoft Dynamics AX 2012'de ticari sözleşmeler](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="8d27b-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="8d27b-118">Talebi karşılamak için bir satınalma siparişini bir satış siparişine bağlayabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="8d27b-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="8d27b-119">Satış siparişinden satınalma siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="8d27b-120">Daha fazla bilgi için, bkz. [Satış siparişinden satınalma siparişi oluşturma](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="8d27b-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="8d27b-121">İade siparişi veya satış siparişini iptal edemiyor veya silemiyorum.</span><span class="sxs-lookup"><span data-stu-id="8d27b-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="8d27b-122">Yalnızca, *Oluşturuldu* durumundaki satış siparişlerini ve iade siparişlerini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="8d27b-123">Daha fazla bilgi için bkz. [İade siparişlerini iptal etme](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="8d27b-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="8d27b-124">Bir satış siparişini iptal etmeyi denediğimde, "Rezervasyonlara dayanan iş oluşturulduğu için rezervasyonlar silinemedi" hatasını alıyorum.</span><span class="sxs-lookup"><span data-stu-id="8d27b-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="8d27b-125">İş bir satış siparişiyle ilişkilendirilmişse, iş iptal edilene ve ters çevrilinceye kadar satış siparişini iptal edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-125">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="8d27b-126">Bu gereksinim, satış siparişiyle ilişkilendirilmiş iş kapatılmış olsa bile geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-126">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="8d27b-127">Bu sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8d27b-127">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="8d27b-128">İşi iptal edin ve stoku istenen konuma geri koyun.</span><span class="sxs-lookup"><span data-stu-id="8d27b-128">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="8d27b-129">Satış siparişinin ilgili yüküne gidin ve yükleme satırında **Çekilen miktarı azalt** ya da Eylem Bölmesi'ndeki **İşi tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8d27b-129">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="8d27b-130">İş artık *İptal edildi* durumunda olur ve yeni stok hareketi işi otomatik olarak oluşturulur stoku ters çevirme işlemi sırasında tanımlanan konuma geri yerleştirmek için işlenir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-130">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="8d27b-131">Yükü silin.</span><span class="sxs-lookup"><span data-stu-id="8d27b-131">Delete the load.</span></span> <span data-ttu-id="8d27b-132">Sevkiyat da silinir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-132">The shipment is also deleted.</span></span>
3. <span data-ttu-id="8d27b-133">Artık satış siparişine gidip iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-133">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="8d27b-134">Bir satış siparişiyle bağlantılı şirketlerarası satınalma siparişini iptal edemiyorum.</span><span class="sxs-lookup"><span data-stu-id="8d27b-134">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d27b-135">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="8d27b-135">Issue description</span></span>

<span data-ttu-id="8d27b-136">Bir satış siparişiyle bağlantılı şirketlerarası satınalma siparişini iptal etmeyi denerseniz, aşağıdaki hata iletisini alabilirsiniz: "Kalan güncelleştirme miktarının işareti değiştiğinden miktar azaltılamaz."</span><span class="sxs-lookup"><span data-stu-id="8d27b-136">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d27b-137">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="8d27b-137">Issue resolution</span></span>

<span data-ttu-id="8d27b-138">Bu sorun Microsoft Dynamics 365 Supply Chain Management 10.0.13 sürümünde giderilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-138">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="8d27b-139">Bu sürümde ve sonraki sürümlerde artık bir satış siparişiyle bağlantılı olan bir şirketlerarası satınalma siparişini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-139">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="8d27b-140">Silinmiş bir faturalandırılmış satış siparişini geri yükleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="8d27b-140">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="8d27b-141">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="8d27b-141">Issue description</span></span>

<span data-ttu-id="8d27b-142">Faturalandırılmış bir satış siparişi yanlışlıkla silindi ve geri yüklemek veya ayrıntılarını görüntülemek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-142">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8d27b-143">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="8d27b-143">Issue resolution</span></span>

<span data-ttu-id="8d27b-144">Silinen satış siparişi zaten faturalanmışsa, **Müşteri hesabı \> Hareketler \> Özgün belge \> Ayrıntıları görüntüle** ögesine gidin.</span><span class="sxs-lookup"><span data-stu-id="8d27b-144">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="8d27b-145">Aradığınız faturayı bulun ve ayrıntılarını görüntülemek için seçin.</span><span class="sxs-lookup"><span data-stu-id="8d27b-145">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="8d27b-146">Bu ayrıntılar satış siparişi referansını içerir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-146">These details include the sales order reference.</span></span> <span data-ttu-id="8d27b-147">Ayrıca, bu sayfadan satış siparişi ayrıntılarına de erişebilmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-147">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="8d27b-148">Satış siparişi başlığının son tarihi SalesOrderHeaderV2Entity veri varlığı içinde bulunamıyor.</span><span class="sxs-lookup"><span data-stu-id="8d27b-148">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="8d27b-149">*SalesOrderHeaderV2Entity* varlığında son tarih alanı yok.</span><span class="sxs-lookup"><span data-stu-id="8d27b-149">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="8d27b-150">Sahipsiz satış siparişi kayıtlarını silmem gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="8d27b-150">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="8d27b-151">Sahipsiz satış siparişi kayıtlarını temizlemek için, aşağıdaki yerlerden birine giderek *Satış siparişi silme* dönemsel işini çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="8d27b-151">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="8d27b-152">Satış ve pazarlama \> Dönemsel görevler \> Temizle \> Satış siparişlerini sil</span><span class="sxs-lookup"><span data-stu-id="8d27b-152">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="8d27b-153">Retail and commerce \> Retail and commerce IT \> Temizleme \> Satış siparişlerini sil</span><span class="sxs-lookup"><span data-stu-id="8d27b-153">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="8d27b-154">Deftere nakledilmiş olan faturalardaki komisyonları hesaplanmanın bir yolu var mı?</span><span class="sxs-lookup"><span data-stu-id="8d27b-154">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="8d27b-155">Supply Chain Management, şu anda deftere nakledilen faturaların komisyonlarını hesaplamayı desteklememektedir.</span><span class="sxs-lookup"><span data-stu-id="8d27b-155">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="8d27b-156">Bir paket malzeme şirketlerarası bir işlemde desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="8d27b-156">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="8d27b-157">Paket satış öğesi satınalma siparişlerinde kullanılmaz; çünkü paket satış öğesi için satış siparişi satırlarını incelerseniz miktarın *0* (sıfır) olduğunu ve durumun *İptal edildi* olduğunu fark edildiğini göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-157">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Cancelled*.</span></span> <span data-ttu-id="8d27b-158">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="8d27b-158">This behavior is by design.</span></span> <span data-ttu-id="8d27b-159">Satış siparişi yalnızca paket satış öğesinin bileşenlerini satın alır.</span><span class="sxs-lookup"><span data-stu-id="8d27b-159">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="8d27b-160">Paket satış öğesinin kendisini satın almaz.</span><span class="sxs-lookup"><span data-stu-id="8d27b-160">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="8d27b-161">Bir paket satın almanız gerekiyorsa, bunu paket satış öğesi olarak işaretlemenizin gerekip gerekmediğiniz gözden geçirin; çünkü bu işlev gerçekte gelir tanıma senaryoları için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="8d27b-161">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is actually designed for revenue recognition scenarios.</span></span> <span data-ttu-id="8d27b-162">Paket satış öğeleri hakkında daha fazla bilgi için bkz. [Paket satış öğeleri](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="8d27b-162">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>
