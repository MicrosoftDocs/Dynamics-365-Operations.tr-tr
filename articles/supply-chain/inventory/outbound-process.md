---
title: Giden işleme genel bakış
description: Bu konu, Stok Yönetimi'nde giden işlemine genel bakış sağlar.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: db1a6887e7742700dd3451c9a877b948b5ab691b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207290"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="9f237-103">Giden işleme genel bakış</span><span class="sxs-lookup"><span data-stu-id="9f237-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f237-104">Bu konu, Stok Yönetimi'nde giden işlemine genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="9f237-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="9f237-105">Çıkış emirleri</span><span class="sxs-lookup"><span data-stu-id="9f237-105">Output orders</span></span>

<span data-ttu-id="9f237-106">Çıkış siparişleri, satış siparişi satırlarını ve transfer siparişi satırlarını giden çekme listelerini kullanan çekme işlemleri ile bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9f237-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="9f237-107">Çekme listeleri satış siparişleri veya nakil siparişlerinden oluşturulduğunda, çıkış emirleri ve sevkiyatlar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9f237-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="9f237-108">Bir çekme listesinin bir sevkiyat ile birebir bir ilişkisi vardır.</span><span class="sxs-lookup"><span data-stu-id="9f237-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="9f237-109">Bir transfer emri sevkiyatı veya satış siparişi sevk irsaliyesi, sevkiyattan işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9f237-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="9f237-110">Aşağıdaki diyagram, giden siparişler için işlemin genel bakışını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f237-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="9f237-111">[![Giden sipariş işleminin genel bakışı](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="9f237-112">Programın çıkış sürecini nasıl uygulanacağını tanımlamak için çıkış kuralları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f237-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="9f237-113">Sevkiyat sürecini denetlemek için bu kuralları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f237-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="9f237-114">Özellikle, bir sevkiyatın gönderilebileceği işlemin aşamasını denetlemek için bu kuralları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f237-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="9f237-115">Aşağıdaki ayarlar, giden işlemlerin nasıl işleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9f237-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="9f237-116">Satış siparişleri ve transfer emirleri için çekme rotası</span><span class="sxs-lookup"><span data-stu-id="9f237-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="9f237-117">**Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin ve sonra **Güncelleştirmeler** sekmesinde, **Çekme rotası durumu** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9f237-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="9f237-118">[![Satış siparişleri için çekme rotası durum alanı](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="9f237-119">**Çekme rotası durumu** alanı **Tamamlandı** olarak ayarlandıysa, çekme işlemi çekme listesi oluşturma işleminin parçası olarak otomatik gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="9f237-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="9f237-120">Alan **Etkinleştirildi** olarak ayarlandıysa, malzeme çekme listesi satırlarının el ile güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9f237-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="9f237-121">Aynı kurulum transfer emirlerine de uygulanır.</span><span class="sxs-lookup"><span data-stu-id="9f237-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="9f237-122">**Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetim parametreleri**'ne gidin ve sonra **Taşıma** sekmesinde, **Çekme rotası durumu** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9f237-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="9f237-123">[![Transfer emirleri için çekme rotası durum alanı](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="9f237-124">Stok çıkış emirlerini sonlandır</span><span class="sxs-lookup"><span data-stu-id="9f237-124">End output inventory orders</span></span>

<span data-ttu-id="9f237-125">**Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetimi parametreleri**'ne gidin ve sonra **Genel** sekmesinde, **Çıkış stok siparişini sonlandır** seçeneğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9f237-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="9f237-126">[![Stok çıkış emrini sonlandır seçeneği](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="9f237-127">Ambar çalışanı malzeme çekme listesi miktarlarını azalttığında, karşılık gelen stok sipariş miktarları sevkiyattan çıkarılır.</span><span class="sxs-lookup"><span data-stu-id="9f237-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="9f237-128">Malzeme çekme listesi belirli bir zamanda güncelleştirildiğinde, **Stok çıkış siparişini sonlandır** seçeneği **Evet** olarak ayarlanmışsa kalan miktarlar siparişe geri bildirilir.</span><span class="sxs-lookup"><span data-stu-id="9f237-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="9f237-129">**Stok çıkış siparişini sonlandır** seçeneği **Hayır** olarak ayarlanmışsa, kalan miktarlar açık çıkış siparişi miktarı olarak tutulur ve yeni bir malzeme çekme listesine **Açık çıkış siparişleri** işlevinin bir parçası olarak eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="9f237-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="9f237-130">[![İşlevler menüsünde açık çıkış emirleri komutu](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="9f237-131">[![Açık çıkış emirleri sayfasındaki İşlevler menüsü](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="9f237-132">Miktarı azalt</span><span class="sxs-lookup"><span data-stu-id="9f237-132">Reduce quantity</span></span>

<span data-ttu-id="9f237-133">Malzeme çekme listelerini oluşturmak işleminin parçası olarak kullanabileceğiniz üçüncü parametre **Miktarı azalt** parametresidir.</span><span class="sxs-lookup"><span data-stu-id="9f237-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="9f237-134">Bu parametreyi ayarlamak, ambara serbest bırakmayı rezervasyon işlemini tetikleyen **Rezervasyon** ayarı ile birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="9f237-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="9f237-135">[![Miktar azaltma parametresi](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="9f237-136">Bir satış siparişi için çıkan işleme örnek</span><span class="sxs-lookup"><span data-stu-id="9f237-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="9f237-137">Bu örnekte, iki madde için bir satış siparişi vardır.</span><span class="sxs-lookup"><span data-stu-id="9f237-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="9f237-138">Malzeme çekme listesi oluşturulmasında **Miktarı azalt** parametresini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f237-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="9f237-139">Bu nedenle, yalnızca eldeki stok için serbest bırakır ve çekme satırlarını oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="9f237-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="9f237-140">Çekme, malzeme çekme listeleri için bir kayıt işlemi olarak raporlanması gerekir (**Çekme rotası durumu** = **Etkinleştirildi**).</span><span class="sxs-lookup"><span data-stu-id="9f237-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="9f237-141">Malzeme çekme listesi oluşturulması sırasında halihazırda rezerve edilmemiş olan stok.</span><span class="sxs-lookup"><span data-stu-id="9f237-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="9f237-142">Kullanılabilir stok satış siparişinden çıkartılabilir veya çekmek için kullanılabilir olduğunda daha sonra işlenmek üzere ambara serbest bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="9f237-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="9f237-143">[![Malzeme çekme listesini güncelleştirmek](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="9f237-144">Tüm çekme satırları **Çekme listesi kayıt** sayfası üzerinde çekildikten sonra, ilişkilendirilen sevkiyat tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="9f237-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="9f237-145">Daha sonra satış siparişi sevk irsaliyeleri için işlem, çekilen stoka dayalı olarak başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="9f237-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="9f237-146">[![Giden sevkiyatları güncelleştirmek](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="9f237-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
