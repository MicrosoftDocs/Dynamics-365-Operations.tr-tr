---
title: Karantina emirleri
description: "Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 515f14e72137f7299093cc6e75cb8e6eec2893fb
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="quarantine-orders"></a><span data-ttu-id="d105b-103">Karantina emirleri</span><span class="sxs-lookup"><span data-stu-id="d105b-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d105b-104">Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d105b-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="d105b-105">Karantina emirleri stok durdurma için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d105b-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="d105b-106">Örneğin, maddeleri kalite kontrol nedeniyle karantinaya almak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d105b-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="d105b-107">Karantinaya alınan stok bir karantina ambarına transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="d105b-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="d105b-108">**Not:** (Ambar yönetiminde) gelişmiş ambar yönetimi işlemleri kullanıyorsanız, karantina emri işleme yalnızca iade satış siparişleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d105b-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="d105b-109">Eldeki stok maddelerini karantinaya alın</span><span class="sxs-lookup"><span data-stu-id="d105b-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="d105b-110">Maddeleri karantinaya aldığınızda, karantina emirlerini el ile oluşturabilirsiniz veya gelen işleme sırasında karantina emirlerini otomatik olarak oluşturmak için sistemi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d105b-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="d105b-111">Karantina emirlerini otomatik olarak oluşturmak için **Madde modeli grupları** sayfasındaki **Stok ilkeleri** sekmesinde **Karantina yönetimi** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d105b-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="d105b-112">Teslim alma ambarları için **Ambarı karantinaya al** alanında varsayılan bir ambar belirtmeniz de gerekir.</span><span class="sxs-lookup"><span data-stu-id="d105b-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="d105b-113">Eldeki fiziksel stok satınalma siparişi veya üretim emrinde kaydedildiğinde, karantinaya alınan maddeler otomatik olarak Microsoft Dynamics 365 for Finance and Operations içindeki karantina ambarına taşınır.</span><span class="sxs-lookup"><span data-stu-id="d105b-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="d105b-114">Bu taşımanın gerçekleşmesinin nedeni karantina emrinin durumunun **Başladı** olarak değişmesidir.</span><span class="sxs-lookup"><span data-stu-id="d105b-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="d105b-115">Karantina emirlerini el ile oluşturduğunuzda, ilişkili madde model grubunda karantina yönetimi için maddenin ayarlanmasına gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="d105b-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="d105b-116">Bu işlem için karantinaya alınması gereken eldeki stoğu ve kullanılması gereken karantina ambarını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d105b-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="d105b-117">Süreci planlamaya yardımcı olması için karantina emri durumlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d105b-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="d105b-118">Karantina emri durumları</span><span class="sxs-lookup"><span data-stu-id="d105b-118">Quarantine order statuses</span></span>
<span data-ttu-id="d105b-119">Karantina siparişleri aşağıdaki durumlarda olabilir:</span><span class="sxs-lookup"><span data-stu-id="d105b-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="d105b-120">Oluşturulma</span><span class="sxs-lookup"><span data-stu-id="d105b-120">Created</span></span>
-   <span data-ttu-id="d105b-121">Başladı</span><span class="sxs-lookup"><span data-stu-id="d105b-121">Started</span></span>
-   <span data-ttu-id="d105b-122">Bitirildi olarak bildirildi</span><span class="sxs-lookup"><span data-stu-id="d105b-122">Reported as finished</span></span>
-   <span data-ttu-id="d105b-123">Bitti</span><span class="sxs-lookup"><span data-stu-id="d105b-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="d105b-124">Oluşturulma</span><span class="sxs-lookup"><span data-stu-id="d105b-124">Created</span></span>

<span data-ttu-id="d105b-125">Karantina emri el ile oluşturulduğunda, fakat madde henüz karantina ambarına yerleştirilmediğinde karantina emrinin durumu **Oluşturuldu** olur.</span><span class="sxs-lookup"><span data-stu-id="d105b-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="d105b-126">İki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d105b-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="d105b-127">Bir hareket, durumu **Siparişte**, **Fiziksel olarak ayrıldı** veya **Çekildi** olan çıkış hareketidir.</span><span class="sxs-lookup"><span data-stu-id="d105b-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="d105b-128">Diğer hareket ise karantina ambarında durumu **Sipariş edildi** veya **Kayıtlı** olan giriş hareketidir.</span><span class="sxs-lookup"><span data-stu-id="d105b-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="d105b-129">Normal işlemleri kullanarak stok güncelleştirmelerini ayırabilir, seçebilir ve kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d105b-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="d105b-130">Başladı</span><span class="sxs-lookup"><span data-stu-id="d105b-130">Started</span></span>

<span data-ttu-id="d105b-131">Bir karantina emrinin durumu **Başlatıldı** ise, stok normal ambardan karantina ambarına taşınır ve iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d105b-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="d105b-132">Bir hareketin durumu **kesinti yapıldı** ve diğer hareket durumu **alınan**.</span><span class="sxs-lookup"><span data-stu-id="d105b-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="d105b-133">Aynı zamanda, iade aktarımının işlenmesi için iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d105b-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="d105b-134">Bu hareketler tarihli değildir.</span><span class="sxs-lookup"><span data-stu-id="d105b-134">These transactions aren't dated.</span></span> <span data-ttu-id="d105b-135">Bir hareketin durumu **Ayrıldı fiziksel** ve diğer hareket durumu **sipariş edildi**.</span><span class="sxs-lookup"><span data-stu-id="d105b-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="d105b-136">Bitirildi olarak bildirildi</span><span class="sxs-lookup"><span data-stu-id="d105b-136">Reported as finished</span></span>

<span data-ttu-id="d105b-137">**Tamamlandı olarak bildir**'e tıklayarak başlatılan bir karantina siparişinin tamamlandığını bildirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d105b-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="d105b-138">Madde karantinadan serbest bırakılır fakat henüz normal ambara geri taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="d105b-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="d105b-139">Normal ambara taşıma Rapor sırasında başlatılabilen Madde varış günlüğü ile tamamlanmış olarak işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="d105b-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="d105b-140">Bitti</span><span class="sxs-lookup"><span data-stu-id="d105b-140">Ended</span></span>

<span data-ttu-id="d105b-141">Karantina emri sonlandırıldığında, madde karantina ambarından normal ambara geri taşınır.</span><span class="sxs-lookup"><span data-stu-id="d105b-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="d105b-142">Madde hareketinin durumu karantina ambarında **satıldı** ve normal ambarda **satın alınan** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="d105b-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="d105b-143">Karantina siparişi hurda</span><span class="sxs-lookup"><span data-stu-id="d105b-143">Quarantine order scrap</span></span>
<span data-ttu-id="d105b-144">Karantina emri işleminin bir parçası olarak stoğu hurdaya çıkartabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d105b-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="d105b-145">Hurdayı işlerken, stoğun durumu karantina ambarından çıkış hareketi tarafından **Satıldı** olarak ayarlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="d105b-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="d105b-146">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d105b-146">See also</span></span>
--------

[<span data-ttu-id="d105b-147">Stok durdurma</span><span class="sxs-lookup"><span data-stu-id="d105b-147">Inventory blocking</span></span>](inventory-blocking.md)

