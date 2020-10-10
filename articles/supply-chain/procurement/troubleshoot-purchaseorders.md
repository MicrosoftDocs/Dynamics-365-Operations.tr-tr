---
title: Satınalma siparişleri ile ilgili sorun giderme
description: Bu konu, satınalma siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
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
ms.openlocfilehash: e55974f65577170880e60095f1ba74ea7366e592
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834440"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="4e789-103">Satınalma siparişleri ile ilgili sorun giderme</span><span class="sxs-lookup"><span data-stu-id="4e789-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="4e789-104">Bu konu, satınalma siparişleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4e789-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="4e789-105">Eylem, yalnızca satır numarası tam olarak dağıtıldıktan sonra tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4e789-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="4e789-106">Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="4e789-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="4e789-107">Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="4e789-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="4e789-108">Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="4e789-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="4e789-109">Satınalma siparişleri veri yönetimi aracılığıyla içe aktarıldığında, satınalma siparişi satır numaraları sistem parametrelerinde tanımlanan artışı izlemez.</span><span class="sxs-lookup"><span data-stu-id="4e789-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e789-110">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4e789-110">Issue description</span></span>

<span data-ttu-id="4e789-111">Varsayılan olarak, *Satınalma siparişi satırları V2* veri varlığı aracılığıyla içe aktarılan satınalma siparişi satırları için otomatik olarak oluşturulan satır numaraları sistem parametrelerinde belirtilen sistem satır numarası artışını kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="4e789-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="4e789-112">El ile bir satınalma siparişi oluşturur ve kullanıcı arabirimiyle (UI) satır eklerseniz, satır numaraları doğru şekilde artırılır.</span><span class="sxs-lookup"><span data-stu-id="4e789-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="4e789-113">Ancak, Veri yönetimi çerçevesi (DMF) kullanıyorsanız, doğru şekilde arttırılmazlar.</span><span class="sxs-lookup"><span data-stu-id="4e789-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="4e789-114">Bu sorun; satırları DMF ile içe aktardığınızda, içe aktarılan varlıkta satır numaraları atanmış değilse, sistem bu dosyaları atamak için DMF yöntemini kullandığı için oluşur.</span><span class="sxs-lookup"><span data-stu-id="4e789-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="4e789-115">Bu yöntem satır numaralarını her zaman bir sayı kadar arttırır.</span><span class="sxs-lookup"><span data-stu-id="4e789-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="4e789-116">Sorun geçici çözümü</span><span class="sxs-lookup"><span data-stu-id="4e789-116">Issue workaround</span></span>

<span data-ttu-id="4e789-117">Satınalma siparişi satırlarını içe aktardığınızda, gerekli satır numaralarının veri varlığı satır numarası alanlarında zaten verildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="4e789-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="4e789-118">Bu durumda, DMF satır numaralarının üzerine yazmaz.</span><span class="sxs-lookup"><span data-stu-id="4e789-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="4e789-119">Varsayılan bir vergi grubu ve varsayılan nakit iskontosu fatura hesabından doldurulmamış.</span><span class="sxs-lookup"><span data-stu-id="4e789-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="4e789-120">Müşteri hesabından farklı bir fatura hesabı kullanıyorsanız, bir satınalma siparişi oluşturulduğunda varsayılan vergi grubu ve varsayılan nakit iskontosu fatura hesabından doldurulmaz.</span><span class="sxs-lookup"><span data-stu-id="4e789-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="4e789-121">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="4e789-121">This behavior is by design.</span></span> <span data-ttu-id="4e789-122">Vergi grubu, nakit iskontoları ve diğer fiyat bilgilerinin varsayılan değerleri fatura hesabına değil müşteri hesabına dayanır.</span><span class="sxs-lookup"><span data-stu-id="4e789-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="4e789-123">Satınalma siparişi teyidi sırasında "Nesne başvurusu ayarlanmadı" hatasını alıyorum veya satıcı faturasının deftere nakli sırasında "Bir çağrı hedefi tarafından özel durum oluşturuldu" özel durumu oluştu.</span><span class="sxs-lookup"><span data-stu-id="4e789-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="4e789-124">Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="4e789-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="4e789-125">Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="4e789-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="4e789-126">Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="4e789-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="4e789-127">Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış.</span><span class="sxs-lookup"><span data-stu-id="4e789-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e789-128">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4e789-128">Issue description</span></span>

<span data-ttu-id="4e789-129">Şu hatayı alırsınız: "Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış."</span><span class="sxs-lookup"><span data-stu-id="4e789-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e789-130">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4e789-130">Issue resolution</span></span>

<span data-ttu-id="4e789-131">Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="4e789-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="4e789-132">Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="4e789-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="4e789-133">Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="4e789-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="4e789-134">Yalnızca oluşturduğum satınalma siparişlerini görüntüleyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="4e789-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="4e789-135">Bu işlev şu anda kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="4e789-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="4e789-136">Bir satınalma siparişindeki stok rezerve edebilir ve kayıtlı stokla hareket oluşturabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="4e789-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e789-137">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4e789-137">Issue description</span></span>

<span data-ttu-id="4e789-138">Malzemeler bir satınalma siparişi üzerinde *Kayıtlı* durumda olsa bile, yine de stoku rezerve edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e789-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="4e789-139">Başka bir deyişle, kayıtlı stok için hareketler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e789-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="4e789-140">Sorunu yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="4e789-140">Reproduce the issue</span></span>

<span data-ttu-id="4e789-141">Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4e789-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="4e789-142">Bir satınalma siparişi oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="4e789-142">Create a purchase order.</span></span>
2. <span data-ttu-id="4e789-143">Satınalma siparişi satırını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4e789-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="4e789-144">Kayıtlı stok için rezervasyon veya hareket üretebildiğinize dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="4e789-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e789-145">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4e789-145">Issue resolution</span></span>

<span data-ttu-id="4e789-146">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="4e789-146">This behavior is by design.</span></span> <span data-ttu-id="4e789-147">Bu, kayıtlı malzemelerin ambar veya stoka fiziksel olarak ulaşmış olması ve bu nedenle rezervasyon için kullanılabilir durumda olması beklenir.</span><span class="sxs-lookup"><span data-stu-id="4e789-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="4e789-148">Satınalma siparişleri yasal varlığın dil ayarlarını yansıtmaz.</span><span class="sxs-lookup"><span data-stu-id="4e789-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e789-149">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4e789-149">Issue description</span></span>

<span data-ttu-id="4e789-150">Satın alma siparişindeki ürün adı, satınalma siparişinin oluşturulduğu yasal varlık için ayarlanmış dil yerine sistem dilinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4e789-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="4e789-151">Sorunu yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="4e789-151">Reproduce the issue</span></span>

<span data-ttu-id="4e789-152">Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4e789-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="4e789-153">Sistem dilini *en-US* (ABD İngilizcesi) olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4e789-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="4e789-154">Ürün adı çevirileri için *EN-US* ve *DE* (Almanca) dillerinin tutulduğu bir ürün bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4e789-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="4e789-155">Geçerli bir varlığın dilini de *DE* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4e789-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="4e789-156">*DE* dilinin ayarlandığı yasal varlıkta, ürünü içeren bir satınalma siparişi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4e789-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="4e789-157">Ürün adının ABD İngilizcesinde (sistem dili) gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="4e789-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e789-158">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4e789-158">Issue resolution</span></span>

<span data-ttu-id="4e789-159">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="4e789-159">This behavior is by design.</span></span> <span data-ttu-id="4e789-160">Satınalma siparişlerinde, ürün her zaman sistem dilinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4e789-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="4e789-161">Bir onay günlüğü oluşturulduğunda satınalma siparişi dili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4e789-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="4e789-162">Ürün varlığına göre Onaylanan satıcı listesi geçerlilik tarihinin değiştirilmesine izin vermiyor.</span><span class="sxs-lookup"><span data-stu-id="4e789-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e789-163">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4e789-163">Issue description</span></span>

<span data-ttu-id="4e789-164">Bir üründe, örneğin, geçerlilik tarihi 11 Ocak 2018 (*11.01.2018*) ve sona erme tarihi *Hiçbir zaman* olan onaylanmış bir satıcı vardır.</span><span class="sxs-lookup"><span data-stu-id="4e789-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="4e789-165">Geçerlilik tarihini 10 Ocak 2018 (*10.01.2018*) veya 12 Ocak 2018 (*12.01.2018*) olarak değiştirmeye çalışırsanız aşağıdaki hatayı alırsınız:</span><span class="sxs-lookup"><span data-stu-id="4e789-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="4e789-166">Onaylanan tedarikçi listesinde (PdsApproveVendorList) bir kayıt oluşturulamıyor.</span><span class="sxs-lookup"><span data-stu-id="4e789-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="4e789-167">"Geçerlilik süresi" değeri "Geçerli" değerinden büyük veya eşit olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4e789-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e789-168">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4e789-168">Issue resolution</span></span>

<span data-ttu-id="4e789-169">Yalnızca satıcı için onay verilen dönemi uzatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e789-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="4e789-170">Geçerli olan kurallar şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4e789-170">The following rules apply:</span></span>

- <span data-ttu-id="4e789-171">Geçerlilik tarihi, malzeme satıcısı için var olan kayıtlardan (dönemler) önce gelecek şekilde değiştirmek için, yeni dönemin sona erme tarihi var olan kayıtlardaki tüm sona erme tarihlerinden önce olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4e789-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="4e789-172">Sona erme tarihini var olan herhangi bir dönemden daha geç olacak şekilde değiştirmek için, geçerli tarih var olan bir kayıttaki en son sona erme tarihinden sonra olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4e789-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="4e789-173">Satıcının onaylandığı genel dönemi azaltmak için, var olan kayıtları silmeniz veya değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e789-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="4e789-174">Alternatif olarak, içe aktarma sırasında **kısaltma** anahtarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e789-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="4e789-175">Bu anahtar, tabloda onaylanan satıcılar için olan tüm kayıtları malzemeye göre siler.</span><span class="sxs-lookup"><span data-stu-id="4e789-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="4e789-176">Bir kaydın geçerlilik tarihi *11.01.2018* ve sona erme tarihi *Hiçbir zaman* olduğunda sorun açıklamasında açıklanan örnek senaryo için, geçerlilik tarihi *10.01.2018* ve sona erme tarihi *Hiçbir zaman* olan yeni bir kaydı içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e789-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="4e789-177">Ancak, geçerlilik tarihi veri yönetimi aracılığıyla *12.01.2018* olarak güncelleştirilecek şekilde dönemi azaltamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4e789-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="4e789-178">Bu değişikliği kullanıcı arayüzü aracılığıyla yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4e789-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="4e789-179">Bir satınalma siparişi başlığındaki teslimat adresini değiştirdikten sonra, teslimat adı eşitlenmemiş.</span><span class="sxs-lookup"><span data-stu-id="4e789-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4e789-180">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4e789-180">Issue description</span></span>

<span data-ttu-id="4e789-181">Bir satınalma siparişinin başlığındaki adres teslimat adresi olmayan bir adresle güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4e789-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="4e789-182">Adres satınalma siparişinde güncelleştirilse de, teslimat adı güncelleştirilmiş adrese göre güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="4e789-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4e789-183">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4e789-183">Issue resolution</span></span>

<span data-ttu-id="4e789-184">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="4e789-184">This behavior is by design.</span></span> <span data-ttu-id="4e789-185">Seçilen adresin teslimat adresi olarak sınıflandırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e789-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="4e789-186">Aksi durumda, teslimat adı seçilen adrese göre güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="4e789-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="4e789-187">Bir satınalma siparişini iptal eden kullanıcıyı bulabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="4e789-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="4e789-188">Bu bilgiler yalnızca satınalma siparişi değişiklik yönetimine tabi olduğunda izlenir.</span><span class="sxs-lookup"><span data-stu-id="4e789-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="4e789-189">Değişiklik yönetimini kullanıyorsanız, değişikliği kimlerin göndermiş olduğunu (iptal) ve kimin onayladığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4e789-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
