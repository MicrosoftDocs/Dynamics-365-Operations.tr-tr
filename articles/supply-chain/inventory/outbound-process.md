---
title: "Giden işlem"
description: "Bu konu, Stok Yönetimi'nde giden işlemine genel bakış sağlar."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: tr-tr
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="6c0d8-103">Giden işlem</span><span class="sxs-lookup"><span data-stu-id="6c0d8-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6c0d8-104">Bu konu, Stok Yönetimi'nde giden işlemine genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="6c0d8-105">Çıkış emirleri</span><span class="sxs-lookup"><span data-stu-id="6c0d8-105">Output orders</span></span>

<span data-ttu-id="6c0d8-106">Çıkış siparişleri, satış siparişi satırlarını ve transfer siparişi satırlarını giden çekme listelerini kullanan çekme işlemleri ile bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="6c0d8-107">Çekme listeleri satış siparişleri veya nakil siparişlerinden oluşturulduğunda, çıkış emirleri ve sevkiyatlar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="6c0d8-108">Bir çekme listesinin bir sevkiyat ile birebir bir ilişkisi vardır.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="6c0d8-109">Bir transfer emri sevkiyatı veya satış siparişi sevk irsaliyesi, sevkiyattan işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="6c0d8-110">Aşağıdaki diyagram, giden siparişler için işlemin genel bakışını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="6c0d8-111">[![Giden sipariş işleminin genel bakışı](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="6c0d8-112">Programın çıkış sürecini nasıl uygulanacağını tanımlamak için çıkış kuralları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="6c0d8-113">Sevkiyat sürecini denetlemek için bu kuralları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="6c0d8-114">Özellikle, bir sevkiyatın gönderilebileceği işlemin aşamasını denetlemek için bu kuralları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="6c0d8-115">Aşağıdaki ayarlar, giden işlemlerin nasıl işleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="6c0d8-116">Satış siparişleri ve transfer emirleri için çekme rotası</span><span class="sxs-lookup"><span data-stu-id="6c0d8-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="6c0d8-117">**Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin ve sonra **Güncelleştirmeler** sekmesinde, **Çekme rotası durumu** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="6c0d8-118">[![Satış siparişleri için çekme rotası durum alanı](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="6c0d8-119">**Çekme rotası durumu** alanı **Tamamlandı** olarak ayarlandıysa, çekme işlemi çekme listesi oluşturma işleminin parçası olarak otomatik gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="6c0d8-120">Alan **Etkinleştirildi** olarak ayarlandıysa, malzeme çekme listesi satırlarının el ile güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="6c0d8-121">Aynı kurulum transfer emirlerine de uygulanır.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="6c0d8-122">**Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetim parametreleri**'ne gidin ve sonra **Taşıma** sekmesinde, **Çekme rotası durumu** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="6c0d8-123">[![Transfer emirleri için çekme rotası durum alanı](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="6c0d8-124">Stok çıkış emirlerini sonlandır</span><span class="sxs-lookup"><span data-stu-id="6c0d8-124">End output inventory orders</span></span>

<span data-ttu-id="6c0d8-125">**Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetimi parametreleri**'ne gidin ve sonra **Genel** sekmesinde, **Çıkış stok siparişini sonlandır** seçeneğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="6c0d8-126">[![Stok çıkış emrini sonlandır seçeneği](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="6c0d8-127">Bazen, stoktaki bazı maddeler malzeme çekme listesi işleminin bir parçası olarak çekilemez.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="6c0d8-128">Örneği, bu durum bir ambar çalışanı çekme satırlarındaki miktarları azalttığında ve malzeme çekme listesini işlediğinde gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="6c0d8-129">**Stok çıkış emrini sonlandır** seçeneği **Evet** olarak ayarlanmışsa, kalan çekilmemiş miktarlar sipariş düzeyine geri bildirilidir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="6c0d8-130">Seçenek **Hayır** olarak ayarlanmışsa, kalan çekilmemiş miktarlar bir açık çıkış siparişi miktarı olarak tutulur.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="6c0d8-131">Bu durumda, miktarlar ambara serbest bırakılmış kalır ve yeni bir malzeme çekme listesine **Açık çıkış emirleri** işlevinin parçası olarak eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="6c0d8-132">[![İşlevler menüsünde açık çıkış emirleri komutu](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="6c0d8-133">[![Açık çıkış emirleri sayfasındaki İşlevler menüsü](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="6c0d8-134">Miktarı azalt</span><span class="sxs-lookup"><span data-stu-id="6c0d8-134">Reduce quantity</span></span>

<span data-ttu-id="6c0d8-135">Malzeme çekme listelerini oluşturmak işleminin parçası olarak kullanabileceğiniz üçüncü parametre **Miktarı azalt** parametresidir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="6c0d8-136">Bu parametreyi ayarlamak, ambara serbest bırakmayı rezervasyon işlemini tetikleyen **Rezervasyon** ayarı ile birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="6c0d8-137">[![Miktar azaltma parametresi](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="6c0d8-138">Bir satış siparişi için çıkan işleme örnek</span><span class="sxs-lookup"><span data-stu-id="6c0d8-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="6c0d8-139">Bu örnekte, iki madde için bir satış siparişi vardır.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="6c0d8-140">Malzeme çekme listesi oluşturulmasında **Miktarı azalt** parametresini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="6c0d8-141">Bu nedenle, yalnızca eldeki stok için serbest bırakır ve çekme satırlarını oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="6c0d8-142">Çekme, malzeme çekme listeleri için bir kayıt işlemi olarak raporlanması gerekir (**Çekme rotası durumu** = **Etkinleştirildi**).</span><span class="sxs-lookup"><span data-stu-id="6c0d8-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="6c0d8-143">Malzeme çekme listesi oluşturulması sırasında halihazırda rezerve edilmemiş olan stok.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="6c0d8-144">Kullanılabilir stok satış siparişinden çıkartılabilir veya çekmek için kullanılabilir olduğunda daha sonra işlenmek üzere ambara serbest bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="6c0d8-145">[![Malzeme çekme listesini güncelleştirmek](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="6c0d8-146">Tüm çekme satırları **Çekme listesi kayıt** sayfası üzerinde çekildikten sonra, ilişkilendirilen sevkiyat tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="6c0d8-147">Daha sonra satış siparişi sevk irsaliyeleri için işlem, çekilen stoka dayalı olarak başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="6c0d8-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="6c0d8-148">[![Giden sevkiyatları güncelleştirmek](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="6c0d8-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

