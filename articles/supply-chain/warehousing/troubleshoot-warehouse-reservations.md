---
title: Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645132"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="a4ade-103">Ambar yönetiminde rezervasyonlarla ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="a4ade-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4ade-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta ambar rezervasyonları ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a4ade-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="a4ade-105">Şu hata iletisini alıyorum: "Rezervasyonlara dayanan iş oluşturulduğu için rezervasyonlar silinemedi."</span><span class="sxs-lookup"><span data-stu-id="a4ade-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a4ade-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="a4ade-106">Issue description</span></span>

<span data-ttu-id="a4ade-107">Satır karşılığında açık iş bulunduğundan bir satış satırındaki stok ayırmayı geri alamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a4ade-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a4ade-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="a4ade-108">Issue resolution</span></span>

<span data-ttu-id="a4ade-109">Maddeyi bir paketleme istasyonundan başka bir konuma (*Baydoor* gibi) getirmek için açık paketleme grubu işinin bulunup bulunmadığını araştırın.</span><span class="sxs-lookup"><span data-stu-id="a4ade-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="a4ade-110">Stok ayırma işlemini fiziksel olarak neyin yaptığını belirlemek için **İş oluşturma geçmişi günlüğü** ve **İş ayrıntıları** sayfalarındaki kayıtları gözden geçirin ve daha sonra ayırmayı geri almak için işi tamamlayın veya silin.</span><span class="sxs-lookup"><span data-stu-id="a4ade-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="a4ade-111">Şu hata iletisini alıyorum: "Stok miktarı %1, %2 maddesi için yetersiz stok hareketi nedeniyle güncelleştirilemedi..."</span><span class="sxs-lookup"><span data-stu-id="a4ade-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a4ade-112">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="a4ade-112">Issue description</span></span>

<span data-ttu-id="a4ade-113">Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="a4ade-114">Tam hata iletisinin tüm metni şöyledir:</span><span class="sxs-lookup"><span data-stu-id="a4ade-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="a4ade-115">%12 Lot Kimliği ve %11 başvuru kodu için boyutları Boyut=%3, Renk=%4, Ekler=%5, Tesis=%6, Ambar=%7, Konum=%8, Stok durumu=Mevcut, Plaka=%9, Parti numarası=%10 olan %2 maddesi için yeterli stok hareketi olmadığından %1 stok miktarı güncelleştirilemedi.</span><span class="sxs-lookup"><span data-stu-id="a4ade-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a4ade-116">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="a4ade-116">Issue resolution</span></span>

<span data-ttu-id="a4ade-117">Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a4ade-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="a4ade-118">Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="a4ade-119">Şu hata iletisini alıyorum: "Fiziksel eldeki miktar... stokta yalnızca 0,00 mevcut olduğundan ayrılamaz."</span><span class="sxs-lookup"><span data-stu-id="a4ade-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a4ade-120">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="a4ade-120">Issue description</span></span>

<span data-ttu-id="a4ade-121">Bu sorun, belirtilen boyutlara sahip yeterli stok hareketi bulunmadığından, sistem bir stok miktarını güncelleştiremediği takdirde oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="a4ade-122">Tam hata iletisinin tüm metni şöyledir:</span><span class="sxs-lookup"><span data-stu-id="a4ade-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="a4ade-123">Fiziksel eldeki miktar Tesis=%1, Ambar=%2, Stok durumu = Mevcut, Parti numarası=%3, Sahip=%4: Stokta yalnızca 0,00 mevcut olduğundan %5 ayrılamaz.</span><span class="sxs-lookup"><span data-stu-id="a4ade-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a4ade-124">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="a4ade-124">Issue resolution</span></span>

<span data-ttu-id="a4ade-125">Bu sorun büyük olasılıkla açık olan bir iş nedeniyle oluşur.</span><span class="sxs-lookup"><span data-stu-id="a4ade-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="a4ade-126">İşi tamamlayın ya da iş oluşturma işlemi olmadan alın.</span><span class="sxs-lookup"><span data-stu-id="a4ade-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="a4ade-127">Hiçbir stok hareketinin fiziksel olarak miktar ayırmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a4ade-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="a4ade-128">Örneğin, bu hareketler açık kalite emirleri, stok bloke kayıtları veya çıkış emirleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="a4ade-129">Şu hata iletisini alıyorum: "Dalgaya atanması için yük satırlarının konum üzerindeki boyutları belirtmelidir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="a4ade-130">Bu boyutları atamak için yük satırını ayırın ve yeniden oluşturun."</span><span class="sxs-lookup"><span data-stu-id="a4ade-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a4ade-131">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="a4ade-131">Issue description</span></span>

<span data-ttu-id="a4ade-132">"Yukarıdaki parti" rezervasyon hiyerarşisine sahip bir madde kullandığınızda (**Konum** boyutunun *üzerine* yerleştirilen **Parti numarası** boyutu ile), Kısmi bir miktar için **Yük planlama çalışma ekranı** sayfasındaki **Ambara serbest bırak** komutu çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4ade-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="a4ade-133">Bu hata iletisini alırsınız ve kısmi miktar için hiçbir iş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="a4ade-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="a4ade-134">Ancak, "aşağıdaki parti" ayırma hiyerarşisine sahip bir madde kullandığınızda (**Konum** boyutunun *altına* yerleştirilen **Parti numarası** boyutu ile), kısmi bir miktar için **Yük planlama çalışma ekranı** sayfasından bir yükü ambara serbest bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4ade-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a4ade-135">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="a4ade-135">Issue resolution</span></span>

<span data-ttu-id="a4ade-136">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="a4ade-136">This behavior is by design.</span></span> <span data-ttu-id="a4ade-137">Ayırma hiyerarşisindeki **Konum** boyutunun üzerine bir boyut eklerseniz ambara serbest bırakma işlemi öncesinde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="a4ade-138">Microsoft bu sorunu değerlendirmiş ve yük planlama çalışma ekranından ambara serbest bırakma sırasında bir özellik kısıtlaması oluştuğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="a4ade-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="a4ade-139">**Konum** üzerinde bir veya daha fazla boyut belirtilmemişse kısmi miktarlar serbest bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="a4ade-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="a4ade-140">Daha fazla bilgi için bkz. [Esnek ambar düzeyi boyut rezervasyonu ilkesi](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="a4ade-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
