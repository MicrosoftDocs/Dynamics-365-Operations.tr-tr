---
title: Ambar stoku düzeltmesi
description: Bu konu, Ambar stoğu ayarlama günlüğü ve ölçek birimleri kullanırken işleme hakkında bilgi sağlar.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026145"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="29202-103">Ambar stoku düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="29202-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="29202-104">Ambar stoğu ayarlama özelliği, [üretim iş yükleri](cloud-edge-workload-manufacturing.md) ve [ambar yönetimi iş yükleri](cloud-edge-workload-warehousing.md) için bulut ve kenar ölçek birimleri çalıştırıldığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="29202-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="29202-105">Bir çalışan, bir ölçek birimi ambar yönetimi iş yüküne karşı ambar uygulamasını kullanarak stok ayarlaması yaptığında eldeki fiziksel güncelleştirmesi **Ambar stok ayarlaması günlüğü** toplu işlemi tarafından işlenmelidir. Bu özelliği, **Ambar yönetimi > Periyodik görevler > Ambar stoğu ayarlama günlüğü**'ne giderek çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29202-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="29202-106">Şu anda aşağıdaki ambar uygulaması iş süreçleri, ölçek birimi iş yükleri üzerinde **Ambar stok ayarlama günlüğü**'nü kullanır:</span><span class="sxs-lookup"><span data-stu-id="29202-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="29202-107">Ayarlama giriş/çıkış</span><span class="sxs-lookup"><span data-stu-id="29202-107">Adjustment in/out</span></span>
- <span data-ttu-id="29202-108">Döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="29202-108">Cycle counting</span></span>
- <span data-ttu-id="29202-109">Plaka yükleme</span><span class="sxs-lookup"><span data-stu-id="29202-109">License plate loading</span></span>

<span data-ttu-id="29202-110">Merkez ve ölçek birimi dağıtımları stok kayıtlarını paylaştığı için her bir stok ayarlama işleminin bir parçası olarak çeşitli stok hareketleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29202-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="29202-111">Stok ayarlama örneği</span><span class="sxs-lookup"><span data-stu-id="29202-111">Inventory adjustment example</span></span>

<span data-ttu-id="29202-112">Bu örnekte, ambar çalışanı eldeki stok eklenmesini kaydetmek için ambar uygulamasını kullandı.</span><span class="sxs-lookup"><span data-stu-id="29202-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="29202-113">İlk olarak, ölçek birimi iş yükü, pozitif fiziksel ayarlama için bir ambar stoğu ayarlama hareketi oluşturur ve bu durum daha sonra merkez ile eşitlenir ve merkezde eldeki stok artışına neden olur.</span><span class="sxs-lookup"><span data-stu-id="29202-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="29202-114">Türü</span><span class="sxs-lookup"><span data-stu-id="29202-114">Type</span></span>                                    | <span data-ttu-id="29202-115">Ölçek birimi</span><span class="sxs-lookup"><span data-stu-id="29202-115">Scale unit</span></span> | <span data-ttu-id="29202-116">Yön</span><span class="sxs-lookup"><span data-stu-id="29202-116">Direction</span></span> | <span data-ttu-id="29202-117">Hub</span><span class="sxs-lookup"><span data-stu-id="29202-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="29202-118">Ambar stoku düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="29202-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="29202-119">+1</span><span class="sxs-lookup"><span data-stu-id="29202-119">+1</span></span>         | ->        | <span data-ttu-id="29202-120">+1</span><span class="sxs-lookup"><span data-stu-id="29202-120">+1</span></span>  |

<span data-ttu-id="29202-121">Daha sonra merkez, [ileti işlemcisi iletileri](cloud-edge-message-processor-messages.md) üzerinden alınan bir sayım günlüğü deftere nakil işlemini işler.</span><span class="sxs-lookup"><span data-stu-id="29202-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="29202-122">Bu, ek eldeki stoğu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="29202-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="29202-123">Eldeki stoğun çift olmasını engellemek için, merkez bu işlemin bir parçası olarak mahsup hareket oluşturur ve ambar stok ayarlamasıyla ilişkili daha önceden kaydedilen eldeki stoğu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="29202-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="29202-124">Türü</span><span class="sxs-lookup"><span data-stu-id="29202-124">Type</span></span>                                    | <span data-ttu-id="29202-125">Ölçek birimi</span><span class="sxs-lookup"><span data-stu-id="29202-125">Scale unit</span></span> | <span data-ttu-id="29202-126">Yön</span><span class="sxs-lookup"><span data-stu-id="29202-126">Direction</span></span> | <span data-ttu-id="29202-127">Hub</span><span class="sxs-lookup"><span data-stu-id="29202-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="29202-128">Sayım</span><span class="sxs-lookup"><span data-stu-id="29202-128">Counting</span></span>                                | <span data-ttu-id="29202-129">+1</span><span class="sxs-lookup"><span data-stu-id="29202-129">+1</span></span>         | <-        | <span data-ttu-id="29202-130">+1</span><span class="sxs-lookup"><span data-stu-id="29202-130">+1</span></span>  |
| <span data-ttu-id="29202-131">Ambar stok ayarlaması (Mahsup)</span><span class="sxs-lookup"><span data-stu-id="29202-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="29202-132">-1</span><span class="sxs-lookup"><span data-stu-id="29202-132">-1</span></span>         | <-        | <span data-ttu-id="29202-133">-1</span><span class="sxs-lookup"><span data-stu-id="29202-133">-1</span></span>  |

<span data-ttu-id="29202-134">Bir ölçek birimi bir merkez üzerinde **Ambar stoğu ayarlama günlüğü** oluşturduktan sonra, hem **Sayım günlüğü**'nü hem de **Mahsup günlük**'ü inceleyebilirsiniz (bunların ikisi de merkez tarafından düzeltme işleminin bir parçası olarak oluşturulur).</span><span class="sxs-lookup"><span data-stu-id="29202-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="29202-135">Aşağıdaki adımları gerçekleştirerek, Supply Chain Management'taki bu günlük girişlerini inceleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="29202-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="29202-136">Ölçek biriminde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="29202-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="29202-137">**Ambar yönetimi \> Periyodik görevler \> Ambar stok ayarlaması günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="29202-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="29202-138">**Ambar stoğu düzeltme günlüğü** sayfasında, eldeki stok değişikliğini kaydeden günlüğü bulun ve açın.</span><span class="sxs-lookup"><span data-stu-id="29202-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="29202-139">**Günlük satırları** bölümü, bu günlük tarafından kaydedilen düzeltmeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="29202-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="29202-140">Merkezde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="29202-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="29202-141">**Ambar yönetimi \> Periyodik görevler \> Ambar stok ayarlaması günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="29202-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="29202-142">Merkez ve ölçek birimi eşitlendiyse **Ambar stoğu ayarlama günlüğü** sayfasında aynı günlüğün listelendiğini görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="29202-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="29202-143">Günlüğü açın.</span><span class="sxs-lookup"><span data-stu-id="29202-143">Open the journal.</span></span> <span data-ttu-id="29202-144">[İleti işlemci iletileri](cloud-edge-message-processor-messages.md) işlendiyse başlıkta **Sayım günlüğü** ve **Mahsup günlük** bağlantılarını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="29202-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="29202-145">**Sayım günlüğü**, günlük satırlarıyla aynı boyut değerlerini göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="29202-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="29202-146">**Mahsup günlük**, çift stok ayarlamasını kaldıran mahsup değeri göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="29202-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="29202-147">Tüm eşitleme ve işleme işlemleri tamamlandığında, **Sayım günlüğü** ve **Mahsup günlük** ölçek birimiyle geri eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="29202-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="29202-148">Bunlar ayrıca ilgili **Ambar stok ayarlama günlüğü** sayfasından da görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="29202-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
