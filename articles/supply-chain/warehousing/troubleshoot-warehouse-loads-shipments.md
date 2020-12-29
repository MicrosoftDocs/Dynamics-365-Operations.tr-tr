---
title: Yük oluşturma ve sevkiyatlar ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta yük oluşturma ve sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645344"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="90295-103">Yük oluşturma ve sevkiyatlar ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="90295-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90295-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta yük oluşturma ve sevkiyatlarla çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="90295-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="90295-105">Şu hata iletisini alıyorum: "Sipariş satırı, geçersiz stok boyutları içerdiğinden bu sipariş için yükleme satırı oluşturamazsınız..."</span><span class="sxs-lookup"><span data-stu-id="90295-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="90295-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="90295-106">Issue description</span></span>

<span data-ttu-id="90295-107">Ambara bir iade satış siparişini serbest bırakmaya çalıştığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="90295-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="90295-108">Sipariş satırı, geçersiz stok boyutları içerdiğinden bu sipariş için yükleme satırı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="90295-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="90295-109">Rezervasyon hiyerarşisinde konum boyutunun altında bulunan stok boyutlarına referans veremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="90295-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="90295-110">Sipariş satırından geçersiz boyutları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="90295-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="90295-111">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="90295-111">Issue resolution</span></span>

<span data-ttu-id="90295-112">Ne yazık ki, ürün bir satış iade işlemi için yük işlemeyi desteklemiyor.</span><span class="sxs-lookup"><span data-stu-id="90295-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="90295-113">Bu nedenle, iade satış siparişini ambara serbest bırakamazsınız.</span><span class="sxs-lookup"><span data-stu-id="90295-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="90295-114">Satış siparişi hareketlerinde, rezervasyon hiyerarşisinde **Konum** boyutunun altında bulunan stok boyutlarına referans veremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="90295-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="90295-115">Çözüm, sipariş satırından geçersiz boyutları kaldırmaktadır.</span><span class="sxs-lookup"><span data-stu-id="90295-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="90295-116">Şu hata iletisini alıyorum: "Satırlardan biri zaten bir yükte yer alıyor.</span><span class="sxs-lookup"><span data-stu-id="90295-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="90295-117">Ambara serbest bırakılamıyor."</span><span class="sxs-lookup"><span data-stu-id="90295-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="90295-118">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="90295-118">Issue description</span></span>

<span data-ttu-id="90295-119">Yükleri el ile oluşturursanız veya süreci satış siparişi satırı girişi gerçekleşmeden önce yükler oluşturulacak şekilde ayarlarsanız sonraki serbest bırakmanın el ile yapılacağı ve yükün rotası ve değerlendirmesinin kullanılacağı varsayılır.</span><span class="sxs-lookup"><span data-stu-id="90295-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="90295-120">Başka bir olası senaryoda, ambara otomatik olarak serbest bırakma işlemi yapmaya çalışırsınız ancak dalga süreci işi oluşturamaz.</span><span class="sxs-lookup"><span data-stu-id="90295-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="90295-121">Bu nedenle, açık bir sevkiyat veya yük yine de oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90295-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="90295-122">Bu açık sevkiyat veya yük, açık sevkiyatı ya da yükü silinceye veya dalgayı el ile yeniden işleyinceye kadar, siparişin otomatik olarak serbest bırakılmasını deneyen sonraki girişimleri engeller.</span><span class="sxs-lookup"><span data-stu-id="90295-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="90295-123">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="90295-123">Issue resolution</span></span>

<span data-ttu-id="90295-124">Yalnızca ambara serbest bırakmadan önce yük yoksa, satış siparişi sayfasından serbest bırakabilirsiniz veya otomatik serbest bırakma oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="90295-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="90295-125">Dalga işlendikten sonra yük otomatik olarak oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="90295-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="90295-126">Şu hata iletisini alıyorum: "Teslim notu düzeltmesi işlenemiyor.</span><span class="sxs-lookup"><span data-stu-id="90295-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="90295-127">Teslimat notu yalnızca Teslimat Notu Düzeltmesi tarafından desteklenmeyen, ambar yönetim süreçlerine tabi olan maddeleri içerir."</span><span class="sxs-lookup"><span data-stu-id="90295-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="90295-128">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="90295-128">Issue description</span></span>

<span data-ttu-id="90295-129">Teslim notunu deftere naklettikten sonra iptal edemiyorsunuz çünkü **İptal** düğmesi kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="90295-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="90295-130">Teslim notunu da düzeltemiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="90295-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="90295-131">Denerseniz bu hata iletisini alıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="90295-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="90295-132">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="90295-132">Issue resolution</span></span>

<span data-ttu-id="90295-133">Gelişmiş ambar yönetimi (WMS) için etkinleştirilen maddelere ait deftere nakledilen sevk irsaliyelerini düzeltmek için deftere nakletme işlemini doğrudan siparişten değil, yükten yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="90295-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="90295-134">Dalgalar yerine giden yüklerden nasıl iş oluşturabilirim?</span><span class="sxs-lookup"><span data-stu-id="90295-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="90295-135">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="90295-135">Issue description</span></span>

<span data-ttu-id="90295-136">Bu sorunu yeniden oluşturmanın bir yolu aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="90295-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="90295-137">Satış siparişi veya transfer emri kullanarak bir giden yük oluşturun.</span><span class="sxs-lookup"><span data-stu-id="90295-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="90295-138">Yükü ambara serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="90295-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="90295-139">Henüz malzeme çekme işi oluşturulmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="90295-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="90295-140">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="90295-140">Issue resolution</span></span>

<span data-ttu-id="90295-141">İşin yük serbest bırakıldığında hemen oluşturulması gerekiyorsa dalga şablonunu buna göre yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="90295-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="90295-142">Dalga şablonunda, aşağıdaki seçenekleri *Evet* olarak ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="90295-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="90295-143">Dalga oluşturmayı otomatik hale getir</span><span class="sxs-lookup"><span data-stu-id="90295-143">Automate wave creation</span></span>
- <span data-ttu-id="90295-144">Dalgayı ambara serbest bırakma sırasında işle</span><span class="sxs-lookup"><span data-stu-id="90295-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="90295-145">Dalga serbest bırakma işlemini otomatikleştir</span><span class="sxs-lookup"><span data-stu-id="90295-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="90295-146">Kısmen sevk edilen bir yükü yeniden serbest bırakamıyorum.</span><span class="sxs-lookup"><span data-stu-id="90295-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="90295-147">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="90295-147">Issue description</span></span>

<span data-ttu-id="90295-148">Kısmen sevk edilen bir yükü ambara serbest bırakamazsınız.</span><span class="sxs-lookup"><span data-stu-id="90295-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="90295-149">Ambarın serbest bırakılması işlemini gerçekleştirdiğinizde, bir "İşlem tamamlandı" iletisi görüntülenir, ancak hiçbir şey olmaz ve kalan miktar için hiçbir iş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="90295-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="90295-150">Bu sorun, taşıma yükü işlevini kullandığınızda ve eksik bir ayırma varsa oluşur.</span><span class="sxs-lookup"><span data-stu-id="90295-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="90295-151">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="90295-151">Issue resolution</span></span>

<span data-ttu-id="90295-152">[KB sorunu 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Kısmen sevk edilen yükler yeniden dalgaya eklenebilir ve yeniden işlenebilir"), [sürüm 10.0.15](../get-started/whats-new-scm-10-0-15.md)'te düzeltilmiştir.</span><span class="sxs-lookup"><span data-stu-id="90295-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
