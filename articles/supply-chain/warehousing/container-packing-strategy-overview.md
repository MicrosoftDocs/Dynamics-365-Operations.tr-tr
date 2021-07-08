---
title: Konteyner paketleme stratejileri
description: Bu konuda konteyner paketleme stratejileri arasındaki farklar açıklanmakta ve örnekler verilmektedir.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292773"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="5c56d-103">Konteyner paketleme stratejileri</span><span class="sxs-lookup"><span data-stu-id="5c56d-103">Container packing strategies</span></span>

<span data-ttu-id="5c56d-104">*Konteyner paketleme stratejisi*, konteynerler arasında madde tahsisatlarını tanımlamak için kullanabileceğiniz bir stratejidir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="5c56d-105">Bu konuda, *Tüm açık konteynerlere paketle* ve *Yalnızca geçerli konteynerde paketle* stratejileri arasındaki farklar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="5c56d-106">**Tüm açık konteynerlere paketle** - Sistem, maddenin bunlardan birine uygun olacağından emin olmak için konteyner kullanımı döngüsü sırasında zaten oluşturulmuş olan tüm açık konteynerleri kontrol etmelidir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="5c56d-107">Paketleme sırasında sistem, önceden oluşturulmuş konteynerlerden herhangi birine uyup uymayacağını belirlemek için her maddeyi denetler.</span><span class="sxs-lookup"><span data-stu-id="5c56d-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="5c56d-108">Madde mevcut bir konteynere uymuyorsa, sistem yeni bir konteyner oluşturur ve tüm siparişi paketlemeyi tamamlayana kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="5c56d-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="5c56d-109">Örneğin, sipariş edilmiş *n* madde için konteyner kullanımı gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="5c56d-110">En kötü durumda, sistem mevcut herhangi bir konteynere uygun olmayan bir maddeyi her işlediğinde, maddenin mevcut konteynerlere uyup uymadını değerlendirmek için toplam (\[(*n* – 1) × (*n* + 1)\] ÷ 2) denetim yapacaktır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="5c56d-111">**Yalnızca geçerli konteynere paketle**: Sistemin, maddenin uygun olup olmadığından emin olmak için yalnızca en son oluşturulan konteyneri kontrol etmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="5c56d-112">Paketleme sırasında sistem, en son oluşturulan konteynere uyup uymayacağını belirlemek için her maddeyi denetler.</span><span class="sxs-lookup"><span data-stu-id="5c56d-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="5c56d-113">Madde bu konteynere uymuyorsa, sistem yeni bir konteyner oluşturur ve tüm siparişi paketlemeyi tamamlayana kadar devam eder.</span><span class="sxs-lookup"><span data-stu-id="5c56d-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="5c56d-114">Örneğin, sipariş edilmiş *n* madde için konteyner kullanımı gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="5c56d-115">En kötü durumda, sistem maddenin kapsayıcılara uygun olup olmadığını değerlendirmek için toplam (*n* – 1) denetim yapar.</span><span class="sxs-lookup"><span data-stu-id="5c56d-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="5c56d-116">Konteyner paketleme stratejileri için akış örneği</span><span class="sxs-lookup"><span data-stu-id="5c56d-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="5c56d-117">Konteynet oluşturma için aşağıdaki öğeleri ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5c56d-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="5c56d-118">Ürün</span><span class="sxs-lookup"><span data-stu-id="5c56d-118">Item</span></span> | <span data-ttu-id="5c56d-119">Fiziksel boyutlar (genişlik × derinlik × yükseklik)</span><span class="sxs-lookup"><span data-stu-id="5c56d-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="5c56d-120">Ağırlık</span><span class="sxs-lookup"><span data-stu-id="5c56d-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="5c56d-121">HDMI Kablosu 6'</span><span class="sxs-lookup"><span data-stu-id="5c56d-121">HDMI Cable 6'</span></span> | <span data-ttu-id="5c56d-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="5c56d-122">1 × 1 × 1</span></span> | <span data-ttu-id="5c56d-123">1</span><span class="sxs-lookup"><span data-stu-id="5c56d-123">1</span></span> |
| <span data-ttu-id="5c56d-124">HDMI Kablosu 12'</span><span class="sxs-lookup"><span data-stu-id="5c56d-124">HDMI Cable 12'</span></span> | <span data-ttu-id="5c56d-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="5c56d-125">2 × 1 × 1</span></span> | <span data-ttu-id="5c56d-126">1</span><span class="sxs-lookup"><span data-stu-id="5c56d-126">1</span></span> |
| <span data-ttu-id="5c56d-127">HDMI Kablosu 18'</span><span class="sxs-lookup"><span data-stu-id="5c56d-127">HDMI Cable 18'</span></span> | <span data-ttu-id="5c56d-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="5c56d-128">3 × 1 × 1</span></span> | <span data-ttu-id="5c56d-129">2</span><span class="sxs-lookup"><span data-stu-id="5c56d-129">2</span></span> |

<span data-ttu-id="5c56d-130">Ayrıca, paketleme için kullanılacak aşağıdaki kutuyu da ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5c56d-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="5c56d-131">Konteyner</span><span class="sxs-lookup"><span data-stu-id="5c56d-131">Container</span></span> | <span data-ttu-id="5c56d-132">Fiziksel boyutlar (uzunluk × genişlik × yükseklik)</span><span class="sxs-lookup"><span data-stu-id="5c56d-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="5c56d-133">Ağırlık</span><span class="sxs-lookup"><span data-stu-id="5c56d-133">Weight</span></span> | <span data-ttu-id="5c56d-134">Hacim</span><span class="sxs-lookup"><span data-stu-id="5c56d-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="5c56d-135">Orta Kutu</span><span class="sxs-lookup"><span data-stu-id="5c56d-135">Medium Box</span></span> | <span data-ttu-id="5c56d-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="5c56d-136">6 × 3 × 2</span></span> | <span data-ttu-id="5c56d-137">10</span><span class="sxs-lookup"><span data-stu-id="5c56d-137">10</span></span> | <span data-ttu-id="5c56d-138">100</span><span class="sxs-lookup"><span data-stu-id="5c56d-138">100</span></span> |

<span data-ttu-id="5c56d-139">Son olarak, aşağıdaki ürün ve miktarlara sahip bir sipariş ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5c56d-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="5c56d-140">Satış sipariş satırı</span><span class="sxs-lookup"><span data-stu-id="5c56d-140">Sales order line</span></span> | <span data-ttu-id="5c56d-141">Miktar</span><span class="sxs-lookup"><span data-stu-id="5c56d-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="5c56d-142">HDMI Kablosu 12'</span><span class="sxs-lookup"><span data-stu-id="5c56d-142">HDMI Cable 12'</span></span> | <span data-ttu-id="5c56d-143">9</span><span class="sxs-lookup"><span data-stu-id="5c56d-143">9</span></span> |
| <span data-ttu-id="5c56d-144">HDMI Kablosu 18'</span><span class="sxs-lookup"><span data-stu-id="5c56d-144">HDMI Cable 18'</span></span> | <span data-ttu-id="5c56d-145">8</span><span class="sxs-lookup"><span data-stu-id="5c56d-145">8</span></span> |
| <span data-ttu-id="5c56d-146">HDMI Kablosu 6'</span><span class="sxs-lookup"><span data-stu-id="5c56d-146">HDMI Cable 6'</span></span> | <span data-ttu-id="5c56d-147">13</span><span class="sxs-lookup"><span data-stu-id="5c56d-147">13</span></span> |

<span data-ttu-id="5c56d-148">Aşağıdaki tabloda, *Tüm açık konteynerlere paketle* stratejisini ve *Yalnızca geçerli kontenyere paketle* stratejisini kullandığınızda konteyner kullanımının nasıl çalıştığı özetlenmektedir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="5c56d-149">Tüm açık konteynerlere ambalajla</span><span class="sxs-lookup"><span data-stu-id="5c56d-149">Pack into all open containers</span></span> | <span data-ttu-id="5c56d-150">Geçerli konteynere paketle</span><span class="sxs-lookup"><span data-stu-id="5c56d-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="5c56d-151">HDMI Kablosu 12':</span><span class="sxs-lookup"><span data-stu-id="5c56d-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="5c56d-152">Yeni konteyner (CONT0001) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="5c56d-153">CONT0001 kontenyerine 9 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="5c56d-154">HDMI Kablosu 12':</span><span class="sxs-lookup"><span data-stu-id="5c56d-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="5c56d-155">Yeni konteyner (CONT0001) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="5c56d-156">CONT0001 kontenyerine 9 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="5c56d-157">HDMI Kablosu 18':</span><span class="sxs-lookup"><span data-stu-id="5c56d-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="5c56d-158">Maddenin CONT0001 konteynerine uyup uymadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="5c56d-159">Yeni konteyner (CONT0002) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="5c56d-160">CONT0002 kontenyerine 5 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="5c56d-161">Yeni konteyner (CONT0003) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="5c56d-162">CONT0003 kontenyerine 3 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="5c56d-163">HDMI Kablosu 18':</span><span class="sxs-lookup"><span data-stu-id="5c56d-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="5c56d-164">Maddenin CONT0001 konteynerine uyup uymadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="5c56d-165">Yeni konteyner (CONT0002) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="5c56d-166">CONT0002 kontenyerine 5 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="5c56d-167">Yeni konteyner (CONT0003) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="5c56d-168">CONT0003 kontenyerine 3 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="5c56d-169">HDMI Kablosu 6':</span><span class="sxs-lookup"><span data-stu-id="5c56d-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="5c56d-170">Maddenin CONT0001 konteynerine uyup uymadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="5c56d-171">CONT0001 kontenyerine 1 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="5c56d-172">Maddenin CONT0002 konteynerine uyup uymadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="5c56d-173">Maddenin CONT0003 konteynerine uyup uymadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="5c56d-174">CONT0003 kontenyerine 4 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="5c56d-175">Yeni konteyner (CONT0004) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="5c56d-176">CONT0004 kontenyerine 8 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="5c56d-177">HDMI Kablosu 6':</span><span class="sxs-lookup"><span data-stu-id="5c56d-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="5c56d-178">Maddenin CONT0003 konteynerine uyup uymadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="5c56d-179">CONT0003 kontenyerine 4 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="5c56d-180">Yeni konteyner (CONT0004) oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="5c56d-181">CONT0004 kontenyerine 9 ea koyun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="5c56d-182">Örnek senaryo: Her konteynere tekli siparişleri paketleme</span><span class="sxs-lookup"><span data-stu-id="5c56d-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="5c56d-183">Bu bölüm, sistemin birden çok siparişi tek bir sevk sevkiyatta birleştirmek üzere ayarlandığı bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="5c56d-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="5c56d-184">Bu nedenle, birden fazla ürün içeren her siparişin kendi konteynerine paketlenmesi için konteynerleme satış siparişinden yapılacaktır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="5c56d-185">Bu işlev, dağıtım merkezinin tam konteynerlerin perakende mağazaları arasında çapraz sevkini yapabilmesi için her konteynere yalnızca bir satış siparişi paketlemeniz gereken senaryoları uygulamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="5c56d-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="5c56d-186">Perakende senaryolarına ek olarak (perakende mağazası başına sipariş ve çapraz sevkiyat için dağıtım merkezine sevkiyat) bu teknik yalın tedarik zincirlerinde de yaygın olarak kullanılır (tam zamanında üretim hattı başına satış siparişi).</span><span class="sxs-lookup"><span data-stu-id="5c56d-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="5c56d-187">Bu senaryo, konteynerleme için *Yalnızca geçerli konteynere paketle* stratejisi kullanıarak paketleme sırasında değerlendirilen kenteyner sayısını nasıl düşürebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5c56d-188">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="5c56d-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="5c56d-189">Sisteminizde Sevkiyatları konsolide et özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="5c56d-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="5c56d-190">Bu senaryo *Sevkiyatları konsolide et* özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="5c56d-191">Bu özellik sisteminizde kullanılmıyorsa, [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanarak açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="5c56d-192">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="5c56d-192">Make demo data available</span></span>

<span data-ttu-id="5c56d-193">Bu senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="5c56d-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="5c56d-194">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="5c56d-195">Konteyner türlerini inceleme veya oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c56d-195">Inspect or create container types</span></span>

<span data-ttu-id="5c56d-196">Konteyner türlerinizi incelemek veya gerekirse yeni kapsayıcı türleri oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-197">**Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="5c56d-198">Aşağıdaki konteyner türlerinin her birinin tanıtım verilerinizde kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="5c56d-199">Konteyner türlerini gerektiği gibi düzenleyin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="5c56d-200">Konteyner türü 1:</span><span class="sxs-lookup"><span data-stu-id="5c56d-200">Container type 1:</span></span>

        - <span data-ttu-id="5c56d-201">**Konteyner türü kodu:** *Kutu-Büyük*</span><span class="sxs-lookup"><span data-stu-id="5c56d-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="5c56d-202">**Açıklama:** *Büyük Kutu*</span><span class="sxs-lookup"><span data-stu-id="5c56d-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="5c56d-203">**Maksimum net ağırlık:** *100*</span><span class="sxs-lookup"><span data-stu-id="5c56d-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="5c56d-204">**Hacim:** *400*</span><span class="sxs-lookup"><span data-stu-id="5c56d-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="5c56d-205">**Uzunluk:** *4*</span><span class="sxs-lookup"><span data-stu-id="5c56d-205">**Length:** *4*</span></span>
        - <span data-ttu-id="5c56d-206">**Genişlik:** *10*</span><span class="sxs-lookup"><span data-stu-id="5c56d-206">**Width:** *10*</span></span>
        - <span data-ttu-id="5c56d-207">**Yükseklik:** *10*</span><span class="sxs-lookup"><span data-stu-id="5c56d-207">**Height:** *10*</span></span>

    - <span data-ttu-id="5c56d-208">Konteyner türü 2:</span><span class="sxs-lookup"><span data-stu-id="5c56d-208">Container type 2:</span></span>

        - <span data-ttu-id="5c56d-209">**Konteyner türü kodu:** *Kutu-Orta*</span><span class="sxs-lookup"><span data-stu-id="5c56d-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="5c56d-210">**Açıklama:** *Orta Kutu*</span><span class="sxs-lookup"><span data-stu-id="5c56d-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="5c56d-211">**Maksimum net ağırlık:** *50*</span><span class="sxs-lookup"><span data-stu-id="5c56d-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="5c56d-212">**Hacim:** *200*</span><span class="sxs-lookup"><span data-stu-id="5c56d-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="5c56d-213">**Uzunluk:** *2*</span><span class="sxs-lookup"><span data-stu-id="5c56d-213">**Length:** *2*</span></span>
        - <span data-ttu-id="5c56d-214">**Genişlik:** *10*</span><span class="sxs-lookup"><span data-stu-id="5c56d-214">**Width:** *10*</span></span>
        - <span data-ttu-id="5c56d-215">**Yükseklik:** *10*</span><span class="sxs-lookup"><span data-stu-id="5c56d-215">**Height:** *10*</span></span>

    - <span data-ttu-id="5c56d-216">Konteyner türü 3:</span><span class="sxs-lookup"><span data-stu-id="5c56d-216">Container type 3:</span></span>

        - <span data-ttu-id="5c56d-217">**Konteyner türü kodu:** *Kutu-Küçük*</span><span class="sxs-lookup"><span data-stu-id="5c56d-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="5c56d-218">**Açıklama:** *Küçük Kutu*</span><span class="sxs-lookup"><span data-stu-id="5c56d-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="5c56d-219">**Maksimum net ağırlık:** *20*</span><span class="sxs-lookup"><span data-stu-id="5c56d-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="5c56d-220">**Hacim:** *100*</span><span class="sxs-lookup"><span data-stu-id="5c56d-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="5c56d-221">**Uzunluk:** *1*</span><span class="sxs-lookup"><span data-stu-id="5c56d-221">**Length:** *1*</span></span>
        - <span data-ttu-id="5c56d-222">**Genişlik:** *10*</span><span class="sxs-lookup"><span data-stu-id="5c56d-222">**Width:** *10*</span></span>
        - <span data-ttu-id="5c56d-223">**Yükseklik:** *10*</span><span class="sxs-lookup"><span data-stu-id="5c56d-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="5c56d-224">Konteyner gruplarını inceleme veya oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c56d-224">Inspect or create container groups</span></span>

<span data-ttu-id="5c56d-225">Konteyner gruplarınızı incelemek veya gerekirse yeni konteyner grupları oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-226">**Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner grupları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="5c56d-227">Aşağıdaki konteyner grubunun tanıtım verilerinizde kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="5c56d-228">Kullanılamıyorsa, oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="5c56d-229">**Konteyner grubu kodu:** *Kutular*</span><span class="sxs-lookup"><span data-stu-id="5c56d-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="5c56d-230">**Açıklama:** *Kutu boyutları*</span><span class="sxs-lookup"><span data-stu-id="5c56d-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="5c56d-231">**Kutular** konteyner grubunun *Ayrıntılar* hızlı sekmesinde, aşağıdaki satırların varoldğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5c56d-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="5c56d-232">Yoksa, eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="5c56d-233">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="5c56d-233">Line 1:</span></span>

        - <span data-ttu-id="5c56d-234">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="5c56d-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="5c56d-235">**Konteyner türü:** *Kutu-Büyük*</span><span class="sxs-lookup"><span data-stu-id="5c56d-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="5c56d-236">**Konteyner kullanım yüzdesi:** *100*</span><span class="sxs-lookup"><span data-stu-id="5c56d-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="5c56d-237">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="5c56d-237">Line 2:</span></span>

        - <span data-ttu-id="5c56d-238">**Sıra numarası:** *2*</span><span class="sxs-lookup"><span data-stu-id="5c56d-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="5c56d-239">**Konteyner türü:** *Kutu-Orta*</span><span class="sxs-lookup"><span data-stu-id="5c56d-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="5c56d-240">**Konteyner kullanım yüzdesi:** *100*</span><span class="sxs-lookup"><span data-stu-id="5c56d-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="5c56d-241">Satır 3:</span><span class="sxs-lookup"><span data-stu-id="5c56d-241">Line 3:</span></span>

        - <span data-ttu-id="5c56d-242">**Sıra numarası:** *3*</span><span class="sxs-lookup"><span data-stu-id="5c56d-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="5c56d-243">**Konteyner türü:** *Kutu-Küçük*</span><span class="sxs-lookup"><span data-stu-id="5c56d-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="5c56d-244">**Konteyner kullanım yüzdesi:** *100*</span><span class="sxs-lookup"><span data-stu-id="5c56d-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="5c56d-245">Yeni bir konteyner oluşturma şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c56d-245">Create a new container build template</span></span>

<span data-ttu-id="5c56d-246">Yeni konteyner oluşturma şablonu oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-247">**Ambar yönetimi** \> **Kurulum** \> **Konteynerler** \> **Konteyner yapı şablonu** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="5c56d-248">Aşağıdaki ayarlara sahip bir konteyner oluşturma şablonu oluşturmak için **Yeni**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="5c56d-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="5c56d-249">**Sıra numarası:** *1*</span><span class="sxs-lookup"><span data-stu-id="5c56d-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="5c56d-250">**Konteyner şablonu kodu:** *Kutu*</span><span class="sxs-lookup"><span data-stu-id="5c56d-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="5c56d-251">**Konteyner grubu kodu:** *Kutular*</span><span class="sxs-lookup"><span data-stu-id="5c56d-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="5c56d-252">**Temel sorgu türleri:** *Satış tahsisat satırı*</span><span class="sxs-lookup"><span data-stu-id="5c56d-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="5c56d-253">**Dalga adım kodu:** *234*</span><span class="sxs-lookup"><span data-stu-id="5c56d-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="5c56d-254">**Bölünmüş çekmelere izin ver:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="5c56d-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="5c56d-255">**Konteyner paketleme stratejisi:** *Yalnızca geçerli konteynere paketle*</span><span class="sxs-lookup"><span data-stu-id="5c56d-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="5c56d-256">**Yönerge birimine göre paketle:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="5c56d-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="5c56d-257">Yeni şablon için satır seçiliyken, Eylem Bölmesinde **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="5c56d-258">Standart sorgu düzenleyicisi iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="5c56d-259">Aşağıdaki ayarlara sahip bir satır eklemek için **Tasnif** sekmesinde **Ekle**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="5c56d-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="5c56d-260">**Tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="5c56d-261">**Türetilmiş tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="5c56d-262">**Alan:** *Sipariş numarası*</span><span class="sxs-lookup"><span data-stu-id="5c56d-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="5c56d-263">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="5c56d-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="5c56d-264">Diğer tüm açık konteynerlerde döngü yapılmasını önlemek ve bir kerede tek bir konteyneri denetleyerek işlemi hızlandırmak için, sipariş numarasına göre sıralamaya ek olarak *Yalnızca geçerli konteynere paketle* stratejisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="5c56d-265">Bu birleşim, bir iş şablonundaki bir iş sonu gibi çalışır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="5c56d-266">Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="5c56d-267">Yeni şablon için satır seçiliyken, Eylem Bölmesinde **Konteyner karıştırma sınırlamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="5c56d-268">Şimdi, maddeleri tek bir siparişten tek bir kapsayıcıya koyan bir sınırlama ekleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="5c56d-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="5c56d-269">Başka bir siparişten gelen maddeler ayrı bir konteynere konulacaktır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="5c56d-270">Aşağıdaki ayarlara sahip bir karıştırma sınırlaması oluşturmak için **Yeni**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="5c56d-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="5c56d-271">**Tablo:** *Satış siparişleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="5c56d-272">**Alan seçimi:** *SalesId* (Alan, ızgarada *Satış siparişi* olarak görünecektir.)</span><span class="sxs-lookup"><span data-stu-id="5c56d-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="5c56d-273">Sınırlamayı eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="5c56d-274">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="5c56d-275">Konteynerleme için dalga şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c56d-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="5c56d-276">Dalga şablonu ayarlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-277">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5c56d-278">Liste bölmesinde, **Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="5c56d-279">Listeden **63 Konteynerleme** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="5c56d-280">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5c56d-281">**Yöntemler** hızlı sekmesinde, **Seçili yöntemler** sütununda, aşağıdaki satırı bulun:</span><span class="sxs-lookup"><span data-stu-id="5c56d-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="5c56d-282">**Yöntem adı:** *konteynerleme*</span><span class="sxs-lookup"><span data-stu-id="5c56d-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="5c56d-283">**Ad:** *Konteynerleme*</span><span class="sxs-lookup"><span data-stu-id="5c56d-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="5c56d-284">Satır için **Dalga adımı kodu** alanını *234* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="5c56d-285">İş şablonu ayarla</span><span class="sxs-lookup"><span data-stu-id="5c56d-285">Set up a work template</span></span>

<span data-ttu-id="5c56d-286">İş şablonu ayarlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-287">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="5c56d-288">**İş emri türü** alanını,*Satış siparişleri* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="5c56d-289">**Genel bakış** ızgarasında, konteyner başına tekli siparişleri paketleme için kullanılması gereken iş şablonunu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="5c56d-290">Bu senaryo için **63 Konteynere çekme** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="5c56d-291">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="5c56d-292">Standart sorgu düzenleyicisi iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="5c56d-293">**Tasnif** sekmesinde, aşağıdaki satırları ekleyin:</span><span class="sxs-lookup"><span data-stu-id="5c56d-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="5c56d-294">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="5c56d-294">Line 1:</span></span>

        - <span data-ttu-id="5c56d-295">**Tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="5c56d-296">**Türetilmiş tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="5c56d-297">**Alan:** *Sevkiyat kodu*</span><span class="sxs-lookup"><span data-stu-id="5c56d-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="5c56d-298">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="5c56d-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="5c56d-299">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="5c56d-299">Line 2:</span></span>

        - <span data-ttu-id="5c56d-300">**Tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="5c56d-301">**Türetilmiş tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="5c56d-302">**Alan:** *Sipariş numarası*</span><span class="sxs-lookup"><span data-stu-id="5c56d-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="5c56d-303">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="5c56d-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="5c56d-304">Satır 3:</span><span class="sxs-lookup"><span data-stu-id="5c56d-304">Line 3:</span></span>

        - <span data-ttu-id="5c56d-305">**Tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="5c56d-306">**Türetilmiş tablo:** *geçici iş hareketleri*</span><span class="sxs-lookup"><span data-stu-id="5c56d-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="5c56d-307">**Alan:** *Konteyner Kimliği*</span><span class="sxs-lookup"><span data-stu-id="5c56d-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="5c56d-308">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="5c56d-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5c56d-309">Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="5c56d-310">Aşağıdaki iletiyi alırsınız: "Gruplama sıfırlanacak, devam edilsin mi?"</span><span class="sxs-lookup"><span data-stu-id="5c56d-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="5c56d-311">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="5c56d-312">**63 Konteynere çekme** hala seçiliyken, Eylem Bölmesinde **İş başlığı sonları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="5c56d-313">Şimdi, siparişteki her konteynerin bir iş emrine bağlanması için işi bölmek üzere ayarları uygulayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="5c56d-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="5c56d-314">**Çalışma başlığı sonları** sayfasındaki her satır için **Bu alana göre grupla** onay kutusunu seçin  (**Sevkiyat kodu**, **Sipariş numarası** ve **Konteyner kodu**).</span><span class="sxs-lookup"><span data-stu-id="5c56d-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="5c56d-315">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="5c56d-316">Sevkiyat konsolidasyonu ilkelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5c56d-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="5c56d-317">Sevkiyat konsolidasyonu ilkesi ayralamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-318">**Ambar yönetimi \> Kurulum \> Ambara serbest bırakma \> Sevkiyat konsolidasyon ilkeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="5c56d-319">Liste bölmesinde **İlke türü** alanını *Satış siparişleri* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="5c56d-320">Listeden **Varsayılan** ilkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="5c56d-321">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5c56d-322">**Konsolidasyon alanları** hızlı sekmesinde **Seçili alanlar** listesinde, **Alan adı** alanının *Sipariş numarası* olarak ayarlandığı satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="5c56d-323">Alanı **Kalan alanlar** listesine taşımak için **Kaldır** düğmesini ![Sol ok](media/backward-button.png) seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="5c56d-324">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="5c56d-325">Ürün için fiziksel boyutlar ayarlama</span><span class="sxs-lookup"><span data-stu-id="5c56d-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="5c56d-326">Bu senaryoda kullanılacak ürünlerle ilgili fiziksel boyutları ayarlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-327">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5c56d-328">**Madde numarası** alanının *A0001* olarak ayarlandığı ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="5c56d-329">Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Ambar** grubunda, **Fiziksel boyutlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="5c56d-330">**Fiziksel boyutlar** sayfasında, ızgarada aşağıdaki satırı görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="5c56d-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="5c56d-331">**Birim:** *adet*</span><span class="sxs-lookup"><span data-stu-id="5c56d-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="5c56d-332">**Brüt ağırlık:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="5c56d-333">**Genişlik:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="5c56d-334">**Derinlik:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="5c56d-335">**Yükseklik:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="5c56d-336">**Hacim:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="5c56d-337">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-337">Close the page.</span></span>
1. <span data-ttu-id="5c56d-338">**Madde numarası** alanının *A0002* olarak ayarlandığı ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="5c56d-339">Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Ambar** grubunda, **Fiziksel boyutlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="5c56d-340">**Fiziksel boyutlar** sayfasında, ızgarada aşağıdaki satırı görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="5c56d-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="5c56d-341">**Birim:** *adet*</span><span class="sxs-lookup"><span data-stu-id="5c56d-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="5c56d-342">**Brüt ağırlık:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="5c56d-343">**Genişlik:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="5c56d-344">**Derinlik:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="5c56d-345">**Yükseklik:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="5c56d-346">**Hacim:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="5c56d-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="5c56d-347">Satış siparişi oluşturma 1</span><span class="sxs-lookup"><span data-stu-id="5c56d-347">Create sales order 1</span></span>

<span data-ttu-id="5c56d-348">Bir satış siparişi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-349">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5c56d-350">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5c56d-351">Yeni bir satış siparişi oluşturmak için bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="5c56d-352">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="5c56d-352">Set the following values:</span></span>

    - <span data-ttu-id="5c56d-353">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5c56d-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5c56d-354">**Ambar:** *63*</span><span class="sxs-lookup"><span data-stu-id="5c56d-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="5c56d-355">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="5c56d-356">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-356">The new sales order is opened.</span></span> <span data-ttu-id="5c56d-357">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki satış satırlarını ekleyin:</span><span class="sxs-lookup"><span data-stu-id="5c56d-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="5c56d-358">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="5c56d-358">Line 1:</span></span>

        - <span data-ttu-id="5c56d-359">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5c56d-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="5c56d-360">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="5c56d-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="5c56d-361">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="5c56d-361">Line 2:</span></span>

        - <span data-ttu-id="5c56d-362">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5c56d-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="5c56d-363">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="5c56d-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="5c56d-364">İlk satırı seçin ve **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="5c56d-365">**Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="5c56d-366">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-366">Then close the page.</span></span>
1. <span data-ttu-id="5c56d-367">İkinci satır için önceki iki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="5c56d-368">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="5c56d-369">Satış siparişi oluşturma 2</span><span class="sxs-lookup"><span data-stu-id="5c56d-369">Create sales order 2</span></span>

<span data-ttu-id="5c56d-370">İkinci bir satış siparişi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-371">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5c56d-372">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5c56d-373">Yeni bir satış siparişi oluşturmak için bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="5c56d-374">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="5c56d-374">Set the following values:</span></span>

    - <span data-ttu-id="5c56d-375">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="5c56d-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="5c56d-376">**Ambar:** *63*</span><span class="sxs-lookup"><span data-stu-id="5c56d-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="5c56d-377">Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="5c56d-378">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="5c56d-378">The new sales order is opened.</span></span> <span data-ttu-id="5c56d-379">**Satış siparişi satırları** hızlı sekmesinde, aşağıdaki satış satırlarını ekleyin:</span><span class="sxs-lookup"><span data-stu-id="5c56d-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="5c56d-380">Satır 1:</span><span class="sxs-lookup"><span data-stu-id="5c56d-380">Line 1:</span></span>

        - <span data-ttu-id="5c56d-381">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5c56d-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="5c56d-382">**Miktar:** *4*</span><span class="sxs-lookup"><span data-stu-id="5c56d-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="5c56d-383">Satır 2:</span><span class="sxs-lookup"><span data-stu-id="5c56d-383">Line 2:</span></span>

        - <span data-ttu-id="5c56d-384">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5c56d-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="5c56d-385">**Miktar:** *4*</span><span class="sxs-lookup"><span data-stu-id="5c56d-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="5c56d-386">İlk satırı seçin ve **Stok \> Rezervasyon**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="5c56d-387">**Rezervasyon** sayfasında, **Lot rezerve et** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="5c56d-388">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-388">Then close the page.</span></span>
1. <span data-ttu-id="5c56d-389">İkinci satır için önceki iki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="5c56d-390">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="5c56d-391">Yük oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c56d-391">Create the load</span></span>

<span data-ttu-id="5c56d-392">Bu senaryo için oluşturduğunuz her sipariş için bir yük oluşturmak ve sonra bunu ambara serbest bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="5c56d-393">**Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="5c56d-394">**Satış satırları** sekmesinde, bu senaryo için oluşturduğunuz  satış siparişlerindeki tüm satış siparişi satırlarını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="5c56d-395">Eylem Bölmesinde **Arz ve talep** sekmesindeki **Ekle** grubunda **Yeni yüke**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="5c56d-396">Seçili sipariş satırları yeni bir yüke eklenir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="5c56d-397">**Yük şablonu ataması** iletişim kutusundaki **Yük şablonu kimliği** alanında, *40' Konteyner* gibi bir yük şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="5c56d-398">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5c56d-399">**Yükler** bölümünde, az önce oluşturduğunuz yükü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="5c56d-400">**Serbest bırak \> Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="5c56d-401">Seçili yükü ambara serbest bırakmak için **Ambara serbest bırak** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="5c56d-402">Sevkiyatları ve konteynerleri doğrulama</span><span class="sxs-lookup"><span data-stu-id="5c56d-402">Verify the shipments and containers</span></span>

<span data-ttu-id="5c56d-403">Aşağıdaki prosedür, oluşturulan sevkiyatları doğrulamanıza olanak verir.</span><span class="sxs-lookup"><span data-stu-id="5c56d-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="5c56d-404">İstenen sonuçları elde ettiğinizden emin olmak için bu senaryo için oluşturduğunuz siparişi incelemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="5c56d-405">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="5c56d-406">Az önce serbest bıraktığınız yük için oluşturulan sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="5c56d-407">Eylem Bölmesinde, **Taşıma** sekmesinde **Konteynerleri görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c56d-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="5c56d-408">Satış siparişlerindeki maddelerin iki farklı konteynere yerleştirildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="5c56d-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c56d-409">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5c56d-409">Additional resources</span></span>

- [<span data-ttu-id="5c56d-410">Konteyner kullanımı</span><span class="sxs-lookup"><span data-stu-id="5c56d-410">Containerization</span></span>](wave-containerization.md)
