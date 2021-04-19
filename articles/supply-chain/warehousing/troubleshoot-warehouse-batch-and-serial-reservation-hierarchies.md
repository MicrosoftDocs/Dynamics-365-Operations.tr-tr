---
title: Ambar toplu işi ve seri rezervasyon hiyerarşileriyle ilgili sorunları giderme
description: Bu konuda, toplu veya seri boyutlar kullanan rezervasyon hiyerarşileri ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: a1abb6f8657484d43d434076e5ee38d1c63fe2ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838190"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="c9516-103">Ambar toplu işi ve seri rezervasyon hiyerarşileriyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="c9516-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9516-104">Bu konuda, toplu veya seri boyutlar kullanan rezervasyon hiyerarşileri ile çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c9516-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="c9516-105">Daha fazla bilgi için bkz. [Esnek ambar düzeyi boyut rezervasyonu ilkesi](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="c9516-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="c9516-106">Bir maddenin rezervasyon hiyerarşisi, talep siparişine yerleşim atamak için yerine getirilmesi gereken depolama boyutlarının gereksinimini belirler.</span><span class="sxs-lookup"><span data-stu-id="c9516-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="c9516-107">Bu boyutlar , bir yerleşim atanmadan önce karşılanması gereken tüm boyutlar için *konum üzerindeki boyutlar* ve talep emrine bir yerleşim atandıktan sonra tahsis edilebilecek boyutlar için de *konum altındaki boyutlar* olarak açıklanabilir.</span><span class="sxs-lookup"><span data-stu-id="c9516-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="c9516-108">Bu ayırma hiyerarşileri Ayrıca *toplu iş-üstü* ve *toplu iş altı* ayırma hiyerarşileri ya da *seri üstü* ve *seri altı* ayırma hiyerarşileri olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="c9516-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="c9516-109">Yalnızca konum üstü boyutta yer yoksa, stok başarıyla tahsis edilebilir.</span><span class="sxs-lookup"><span data-stu-id="c9516-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="c9516-110">Örneğin, *toplu iş üstü* rezervasyon hiyerarşisinde, **tesis**, **Ambar** ve **toplu iş numarası** boyutlarının talep siparişinde belirtilecek şekilde olmasını beklersiniz.</span><span class="sxs-lookup"><span data-stu-id="c9516-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="c9516-111">Bu boyutlardan herhangi biri eksikse, tahsisat işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="c9516-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="c9516-112">Bunun aksine, *toplu iş altı* veya *seri altı* rezervasyon hiyerarşisinde, bir toplu iş veya seri numara talep siparişinde belirtilebilir, ancak tahsisat süreci bunu gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="c9516-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="c9516-113">Şu hata iletisini alıyorum: "Dalgaya atanması için yük satırlarının konum üzerindeki boyutları belirtmelidir.</span><span class="sxs-lookup"><span data-stu-id="c9516-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="c9516-114">Bu boyutları atamak için yük satırını ayırın ve yeniden oluşturun."</span><span class="sxs-lookup"><span data-stu-id="c9516-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9516-115">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="c9516-115">Issue description</span></span>

<span data-ttu-id="c9516-116">*Toplu iş üstü* rezervasyon hiyerarşisine sahip bir madde kullandığınızda Kısmi bir miktar için Yük serbest bırakmaya çalışıyorsanız **Yük planlama çalışma ekranı** sayfasındaki **Ambara serbest bırak** komutu çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9516-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="c9516-117">Bu hata iletisini alırsınız ve kısmi miktar için hiçbir iş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="c9516-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="c9516-118">Ancak, *toplu iş altı* ayırma hiyerarşisine sahip bir madde kullandığınızda **Yük planlama çalışma ekranı sayfasından** kısmi bir miktar için bir yükü serbest bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9516-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c9516-119">Sorun nedeni</span><span class="sxs-lookup"><span data-stu-id="c9516-119">Issue cause</span></span>

<span data-ttu-id="c9516-120">Boyut, Ayırma hiyerarşisindeki **Konum** boyutunun üzerinde olduğunda ambara serbest bırakma işlemi öncesinde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c9516-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="c9516-121">**Konum** üzerinde bir veya daha fazla boyut belirtilmemişse kısmi miktarlar serbest bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="c9516-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="c9516-122">Kullanılabilir stok olmasına rağmen, bir toplu iş numarası için otomatik rezervasyon istemi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="c9516-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9516-123">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="c9516-123">Issue description</span></span>

<span data-ttu-id="c9516-124">Ambar işlemlerini etkinleştirilmemiş bir ambarda *toplu iş üstü* rezervasyon hiyerarşisine sahip bir madde kullandığınızda ve otomatik rezervasyon etkinleştirildiğinde, malzeme çekme için yalnızca bir toplu iş olsa bile bir toplu iş numarası için otomatik rezervasyon istemi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c9516-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="c9516-125">Ancak, ambar işlemlerinin etkinleştirildiği bir ambarda aynı maddeyi kullandığınızda, otomatik rezervasyon istemi gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="c9516-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c9516-126">Sorun nedeni</span><span class="sxs-lookup"><span data-stu-id="c9516-126">Issue cause</span></span>

<span data-ttu-id="c9516-127">Rezervasyon hiyerarşisi *toplu iş üstü* veya *seri üstü* olarak tanımlanmışsa, referansta bulunulan boyut (**toplu iş numarası** veya **seri numarası**) her zaman talep siparişlerinde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c9516-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="c9516-128">Tek bir toplu iş veya seri numarası varsa, ambar işlemleri bu bilgileri tamamlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="c9516-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="c9516-129">Ancak Ambar, ambar işlemleri için etkinleştirilmediğinden, kullanıcının her zaman **konumun** üzerindeki tüm boyutları belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c9516-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="c9516-130">Eldeki miktarı dikkate al ölçütüne sahip yerleştirme şablonları, toplu iş etkinleştirilmiş maddeler için geçerli eldeki stok envanterini dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="c9516-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="c9516-131">Daha fazla bilgi için bkz. [Ambar yerleştirme](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="c9516-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="c9516-132">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="c9516-132">Issue description</span></span>

<span data-ttu-id="c9516-133">*Eldeki miktarı dikkate al* ölçütüne sahip yerleştirme şablonları, *toplu iş üstü* maddeler için geçerli eldeki stok envanterini dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="c9516-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="c9516-134">Bunlar yalnızca, toplu iş numarası satış siparişi satırında belirtilmişse bunu dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="c9516-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="c9516-135">Ancak, *toplu iş altı* maddeleri kullandığınızda, geçerli eldeki stok beklendiği gibi kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="c9516-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c9516-136">Sorun nedeni</span><span class="sxs-lookup"><span data-stu-id="c9516-136">Issue cause</span></span>

<span data-ttu-id="c9516-137">Yerleştirme şablon başlığı *sipariş edilen*, *rezerve edilen* veya *serbest bırakılan* talep stratejisi için tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c9516-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="c9516-138">*Sipariş edilen* talep stratejisi için, rezervasyon veya ambara serbest bırakma işlemlerine uygulanan aynı rezervasyon hiyerarşisi gereksinimleri geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c9516-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="c9516-139">Bu nedenle, *toplu iş üstü* ve *Seri üstü* ayırma hiyerarşileri bulunan maddeler için, toplu iş veya seri numarasının talep emrinde (satış veya transfer) belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c9516-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="c9516-140">Alternatif olarak, Ambar yerleştirme talebi oluşturulmadan önce toplu iş veya seri numarasını seçmek için *Rezerve edilen* talep stratejisi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c9516-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
