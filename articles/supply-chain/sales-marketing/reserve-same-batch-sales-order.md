---
title: Satış siparişi için aynı toplu işi rezerve etme
description: Bu makalede, bir ürünün, tek bir stok toplu işine karşılık stok rezervasyonuna izin verecek şekilde nasıl ayarlandığı açıklanmaktadır.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6089d07b0f8bc1a36703b5b1c2f24af72770d5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568317"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="207bd-103">Satış siparişi için aynı toplu işi rezerve etme</span><span class="sxs-lookup"><span data-stu-id="207bd-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="207bd-104">Bu makalede, bir ürünün, tek bir stok toplu işine karşılık stok rezervasyonuna izin verecek şekilde nasıl ayarlandığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="207bd-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="207bd-105">Aynı toplu iş rezervasyonu, tek bir stok toplu işine karşılık bir satış siparişi satırı için stok rezerve etmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="207bd-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="207bd-106">Örneğin, duvar kağıdı sipariş eden bir müşteri, kağıt ruloları arasında tutarsızlıklar olmaması için tüm siparişin aynı toplu iş veya lottan karşılanmasını talep edebilir.</span><span class="sxs-lookup"><span data-stu-id="207bd-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="207bd-107">Bir ürünü aynı toplu rezervasyonu kullanacak şekilde ayarlamak için, ürüne atadığınız madde model grubunda, etkin izleme boyut grubunda ve depolama boyut grubunda aşağıdaki ayarların etkin olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="207bd-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="207bd-108">**Madde model grupları** – Madde model grubu için, stok ilkelerine ilişkin **Rezervasyon** alan grubunda **Aynı toplu iş seçimi** ve **Gereksinimi konsolide et** alanları seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="207bd-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="207bd-109">**İzleme boyutu grupları** – İzleme boyutu grubu için, toplu iş numarasına ilişkin **Boyuta göre tedarik planı** alanı seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="207bd-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="207bd-110">**Depolama boyutu grupları** – Depolama boyutu grubu için, **Tesis** ve **Ambar** için **Boyuta göre tedarik planı** alanı seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="207bd-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="207bd-111">Aynı toplu iş seçimi için bir satış siparişi satırında bir ürüne ilişkin stok rezerve ettiğiniz zaman, Microsoft Dynamics 365 for Finance and Operations, sipariş edilen miktarı tek bir stok toplu işinden rezerve etmeyi dener.</span><span class="sxs-lookup"><span data-stu-id="207bd-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="207bd-112">Tüm özel toplu iş özniteliği gereksinimleri de dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="207bd-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="207bd-113">Miktar tek bir toplu işleminden doldurulamıyorsa, **Aynı toplu iş rezervasyon çakışması** sayfası görünür.</span><span class="sxs-lookup"><span data-stu-id="207bd-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="207bd-114">Bu sayfada sorunlar ve rezervasyon işlemine devam etmek için alabileceğiniz önlemler açıklanır.</span><span class="sxs-lookup"><span data-stu-id="207bd-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="207bd-115">Aşağıdaki koşullar, toplu işin rezerve edilmesini engelleyebilir:</span><span class="sxs-lookup"><span data-stu-id="207bd-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="207bd-116">Toplu iş değerlendirme kodunda, satış için **Engellendi** olarak işaretlenmiş **Rezervasyonu engelle** uyarısı vardır.</span><span class="sxs-lookup"><span data-stu-id="207bd-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="207bd-117">Bitiş tarihine ve varsa müşterinin ilgili satış yapılabilir gün sayısına göre, toplu işin tarihi geçmiştir.</span><span class="sxs-lookup"><span data-stu-id="207bd-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="207bd-118">Madde için madde model grubu FEFO (İlk Sona Eren İlk Çıkar) tarih denetimliyse ve malzeme çekme ölçütü olarak bitiş tarihi seçilmişse madde yine rezervasyon için değerlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="207bd-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="207bd-119">Bitiş tarihi/son kullanma tarihi ve varsa müşterinin satış yapılabilir gün sayısına göre toplu işin raf ömrü kalan gün sayısı yeterli değildir.</span><span class="sxs-lookup"><span data-stu-id="207bd-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>




