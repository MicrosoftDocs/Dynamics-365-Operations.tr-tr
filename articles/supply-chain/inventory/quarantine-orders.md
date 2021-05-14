---
title: Karantina emirleri
description: Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956194"
---
# <a name="quarantine-orders"></a><span data-ttu-id="b4b0e-103">Karantina emirleri</span><span class="sxs-lookup"><span data-stu-id="b4b0e-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4b0e-104">Bu konuda, karantina emirlerinin stok durdurma için nasıl kullanıldığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="b4b0e-105">Karantina emirleri, stoğu durdurmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="b4b0e-106">Örneğin, maddeleri kalite kontrol nedeniyle karantinaya almak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="b4b0e-107">Karantinaya alınan stok bir karantina ambarına transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="b4b0e-108">(Ambar yönetiminde) gelişmiş ambar yönetimi işlemleri kullanıyorsanız, karantina emri işleme yalnızca iade satış siparişleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="b4b0e-109">Eldeki stok maddelerini karantinaya alın</span><span class="sxs-lookup"><span data-stu-id="b4b0e-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="b4b0e-110">Maddeleri karantinaya aldığınızda, karantina emirlerini el ile oluşturabilirsiniz veya gelen işleme sırasında karantina emirlerini otomatik olarak oluşturmak için sistemi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="b4b0e-111">Sistemi karantina emirlerini otomatik olarak üretecek şekilde ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="b4b0e-112">**Stok yönetimi \> Kurulum \> Stok \> Madde modeli grupları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="b4b0e-113">Liste bölmesinde ilgili bir model grubu seçin veya yeni bir model grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="b4b0e-114">**Stok ilkeleri** hızlı sekmesinde, **Karantina yönetimi** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="b4b0e-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-115">Close the page.</span></span>
1. <span data-ttu-id="b4b0e-116">Teslim alma ambarları için **Ambarı karantinaya al** alanında varsayılan bir ambar alanı belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="b4b0e-117">Ambarda alındı olarak kaydedilen bir madde **Karantina yönetimi** onay kutusunun seçildiği bir model grubuna aitse sistem bunun için bir karantina emiri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="b4b0e-118">Karantina emiri, çalışanların maddeyi karantina ambarına taşıması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="b4b0e-119">Karantina emirlerini el ile oluşturduğunuzda, **Karantina emirleri** sayfasında ilişkili madde model grubunda karantina yönetimi için maddenin ayarlanmasına gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="b4b0e-120">Bu işlem için karantinaya alınması gereken eldeki stoğu ve kullanılması gereken karantina ambarını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="b4b0e-121">Süreci planlamaya yardımcı olması için karantina emri durumlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="b4b0e-122">Karantina emri durumları</span><span class="sxs-lookup"><span data-stu-id="b4b0e-122">Quarantine order statuses</span></span>

<span data-ttu-id="b4b0e-123">Karantina siparişleri aşağıdaki durumlarda olabilir:</span><span class="sxs-lookup"><span data-stu-id="b4b0e-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="b4b0e-124">Oluşturulma</span><span class="sxs-lookup"><span data-stu-id="b4b0e-124">Created</span></span>
- <span data-ttu-id="b4b0e-125">Başladı</span><span class="sxs-lookup"><span data-stu-id="b4b0e-125">Started</span></span>
- <span data-ttu-id="b4b0e-126">Bitirildi olarak bildirildi</span><span class="sxs-lookup"><span data-stu-id="b4b0e-126">Reported as finished</span></span>
- <span data-ttu-id="b4b0e-127">Bitti</span><span class="sxs-lookup"><span data-stu-id="b4b0e-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="b4b0e-128">Oluşturulma</span><span class="sxs-lookup"><span data-stu-id="b4b0e-128">Created</span></span>

<span data-ttu-id="b4b0e-129">Karantina emri el ile oluşturulduğunda, fakat madde henüz karantina ambarına yerleştirilmediğinde karantina emrinin durumu **Oluşturuldu** olur.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="b4b0e-130">İki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="b4b0e-131">Bir hareket, durumu **Siparişte**, **Fiziksel olarak ayrıldı** veya **Çekildi** olan çıkış hareketidir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="b4b0e-132">Diğer hareket ise karantina ambarında durumu **Sipariş edildi** veya **Kayıtlı** olan giriş hareketidir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="b4b0e-133">Normal işlemleri kullanarak stok güncelleştirmelerini ayırabilir, seçebilir ve kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="b4b0e-134">Başladı</span><span class="sxs-lookup"><span data-stu-id="b4b0e-134">Started</span></span>

<span data-ttu-id="b4b0e-135">Bir karantina emrinin durumu **Başlatıldı** ise, stok normal ambardan karantina ambarına taşınır ve iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="b4b0e-136">Bir hareketin durumu **kesinti yapıldı** ve diğer hareket durumu **alınan**.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="b4b0e-137">Aynı zamanda, iade aktarımının işlenmesi için iki stok hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="b4b0e-138">Bu hareketler tarihli değildir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-138">These transactions aren't dated.</span></span> <span data-ttu-id="b4b0e-139">Bir hareketin durumu **Ayrıldı fiziksel** ve diğer hareket durumu **sipariş edildi**.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="b4b0e-140">Tamamlandığı bildirildi</span><span class="sxs-lookup"><span data-stu-id="b4b0e-140">Reported as finished</span></span>

<span data-ttu-id="b4b0e-141">Başlatılan bir karantina emrini tamamlandı olarak bildirmek için, emiri açın ve Eylem Bölmesinde **Tamamlandı olarak bildir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="b4b0e-142">Madde karantinadan serbest bırakılır fakat henüz normal ambara geri taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="b4b0e-143">Normal ambara taşıma rapor sırasında başlatılabilen madde varış günlüğü ile tamamlanmış olarak işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="b4b0e-144">Bitti</span><span class="sxs-lookup"><span data-stu-id="b4b0e-144">Ended</span></span>

<span data-ttu-id="b4b0e-145">Karantina emri sonlandırıldığında, madde karantina ambarından normal ambara geri taşınır.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="b4b0e-146">Madde hareketinin durumu karantina ambarında *satıldı* ve normal ambarda *satın alınan* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="b4b0e-147">Karantina siparişi hurda</span><span class="sxs-lookup"><span data-stu-id="b4b0e-147">Quarantine order scrap</span></span>

<span data-ttu-id="b4b0e-148">Karantina emri işleminin bir parçası olarak stoğu hurdaya çıkartabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="b4b0e-149">Hurdayı işlerken, stoğun durumu karantina ambarından çıkış hareketi tarafından *Satıldı* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4b0e-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b4b0e-150">Additional resources</span></span>

- [<span data-ttu-id="b4b0e-151">Stok durdurma</span><span class="sxs-lookup"><span data-stu-id="b4b0e-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
