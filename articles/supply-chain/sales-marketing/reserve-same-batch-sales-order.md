---
title: Satış siparişi için aynı toplu işi rezerve etme
description: Bu makalede, bir ürünün, tek bir stok toplu işine karşılık stok rezervasyonuna izin verecek şekilde nasıl ayarlandığı açıklanmaktadır.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c7745b1306142678760318cc47f54b93d6f727a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231828"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="c3782-103">Satış siparişi için aynı toplu işi rezerve etme</span><span class="sxs-lookup"><span data-stu-id="c3782-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3782-104">Bu makalede, bir ürünün, tek bir stok toplu işine karşılık stok rezervasyonuna izin verecek şekilde nasıl ayarlandığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c3782-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="c3782-105">Aynı toplu iş rezervasyonu, tek bir stok toplu işine karşılık bir satış siparişi satırı için stok rezerve etmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c3782-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="c3782-106">Örneğin, duvar kağıdı sipariş eden bir müşteri, kağıt ruloları arasında tutarsızlıklar olmaması için tüm siparişin aynı toplu iş veya lottan karşılanmasını talep edebilir.</span><span class="sxs-lookup"><span data-stu-id="c3782-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="c3782-107">Bir ürünü aynı toplu rezervasyonu kullanacak şekilde ayarlamak için, ürüne atadığınız madde model grubunda, etkin izleme boyut grubunda ve depolama boyut grubunda aşağıdaki ayarların etkin olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="c3782-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="c3782-108">**Madde model grupları** – Madde model grubu için, stok ilkelerine ilişkin **Rezervasyon** alan grubunda **Aynı toplu iş seçimi** ve **Gereksinimi konsolide et** alanları seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c3782-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="c3782-109">**İzleme boyutu grupları** – İzleme boyutu grubu için, toplu iş numarasına ilişkin **Boyuta göre tedarik planı** alanı seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c3782-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="c3782-110">**Depolama boyutu grupları** – Depolama boyutu grubu için, **Tesis** ve **Ambar** için **Boyuta göre tedarik planı** alanı seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c3782-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="c3782-111">Aynı toplu iş seçimi için bir satış siparişi satırında bir ürüne ilişkin stok rezerve ettiğiniz zaman, sistem, sipariş edilen miktarı tek bir stok toplu işinden rezerve etmeyi dener.</span><span class="sxs-lookup"><span data-stu-id="c3782-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="c3782-112">Tüm özel toplu iş özniteliği gereksinimleri de dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="c3782-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="c3782-113">Miktar tek bir toplu işleminden doldurulamıyorsa, **Aynı toplu iş rezervasyon çakışması** sayfası görünür.</span><span class="sxs-lookup"><span data-stu-id="c3782-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="c3782-114">Bu sayfada sorunlar ve rezervasyon işlemine devam etmek için alabileceğiniz önlemler açıklanır.</span><span class="sxs-lookup"><span data-stu-id="c3782-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="c3782-115">Aşağıdaki koşullar, toplu işin rezerve edilmesini engelleyebilir:</span><span class="sxs-lookup"><span data-stu-id="c3782-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="c3782-116">Toplu iş değerlendirme kodunda, satış için **Engellendi** olarak işaretlenmiş **Rezervasyonu engelle** uyarısı vardır.</span><span class="sxs-lookup"><span data-stu-id="c3782-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="c3782-117">Bitiş tarihine ve varsa müşterinin ilgili satış yapılabilir gün sayısına göre, toplu işin tarihi geçmiştir.</span><span class="sxs-lookup"><span data-stu-id="c3782-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="c3782-118">Madde için madde model grubu FEFO (İlk Sona Eren İlk Çıkar) tarih denetimliyse ve malzeme çekme ölçütü olarak bitiş tarihi seçilmişse madde yine rezervasyon için değerlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c3782-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="c3782-119">Bitiş tarihi/son kullanma tarihi ve varsa müşterinin satış yapılabilir gün sayısına göre toplu işin raf ömrü kalan gün sayısı yeterli değildir.</span><span class="sxs-lookup"><span data-stu-id="c3782-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="c3782-120">**Etkin ambar yönetimi işlemleri** kullanan bir depolama boyutu grubuyla ilişkilendirilmiş maddeler için, yerleşim boyutunun üstünde tanımlanan toplu iş numarası stok boyutuna sahip bir rezervasyon hiyerarşisi kullanarak belirli toplu iş numaralarını rezerve edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3782-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="c3782-121">Satış ve transfer emri satırları için **toplu rezervasyon** sayfası, kullanılabilir toplu iş numaralarına dayalı olarak çoklu satırları seçmenizi ve rezerve etmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c3782-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="c3782-122">Yerin altında toplu iş numarası boyutu olan bir rezervasyon hiyerarşisi kullanıyorsanız ne yapmanız gerektiğini öğrenmek için [esnek Ambar düzeyi boyut rezervasyon ilkesi](../warehousing/flexible-warehouse-level-dimension-reservation.md) 'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="c3782-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]