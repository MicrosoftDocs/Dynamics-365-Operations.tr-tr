---
title: "Konsinye stok yenileme siparişi oluşturma"
description: "Bu yordam bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı gösterir."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 6286e8f52b8131a8e4779f1e11d84233b8e0760e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="691c2-103">Konsinye stok yenileme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="691c2-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="691c2-104">Bu yordam bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="691c2-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="691c2-105">Ayrıca ürünlerin alımını, konsinye stoğun satıcının sahibi olduğu eldeki stok olarak kaydedilecek şekilde kaydetmeyi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="691c2-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="691c2-106">Bu yordam normalde tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="691c2-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="691c2-107">Bu kılavuzu USMF demo şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="691c2-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="691c2-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="691c2-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="691c2-109">Konsinye stok yenileme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="691c2-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="691c2-110">Tedarik ve kaynak atama > Konsinye > Konsinye stok yenileme siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="691c2-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="691c2-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-111">Click New.</span></span>
3. <span data-ttu-id="691c2-112">Satıcı hesabı alanında satıcı US-104'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="691c2-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="691c2-113">Stok sahipleri sayfasında sahip olarak kayıtlı bir satıcı seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="691c2-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="691c2-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-114">Click OK.</span></span>
5. <span data-ttu-id="691c2-115">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-115">Click Add line.</span></span>
6. <span data-ttu-id="691c2-116">Madde numarası alanına M9211CI yazın.</span><span class="sxs-lookup"><span data-stu-id="691c2-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="691c2-117">Konsinye stoğu için ayarlanmış bir madde seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="691c2-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="691c2-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="691c2-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="691c2-119">İstenen teslim tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="691c2-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="691c2-120">İstenen ve onaylanan tarihler, malların beklenen varış tarihi için MRP altyapısı tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="691c2-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="691c2-121">Teyit edilmiş teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="691c2-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="691c2-122">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="691c2-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="691c2-123">Stok boyutları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="691c2-124">Stok boyutları sahibi alanında sahibi göstermek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="691c2-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="691c2-125">Satıcı US-104 artık sahip olarak listelenir.</span><span class="sxs-lookup"><span data-stu-id="691c2-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="691c2-126">Stok hareketi durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="691c2-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="691c2-127">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="691c2-127">Click Inventory.</span></span>
2. <span data-ttu-id="691c2-128">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-128">Click Transactions.</span></span>
3. <span data-ttu-id="691c2-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="691c2-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="691c2-130">Giriş alanının Sipariş edildi olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="691c2-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="691c2-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="691c2-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="691c2-132">Maddeleri al</span><span class="sxs-lookup"><span data-stu-id="691c2-132">Receive items</span></span>
1. <span data-ttu-id="691c2-133">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-133">Click Product receipt.</span></span>
2. <span data-ttu-id="691c2-134">Harici ürün girişi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="691c2-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="691c2-135">Miktar alanına, burada gösterilenden daha küçük bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="691c2-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="691c2-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="691c2-137">Eldeki stoğu denetleme</span><span class="sxs-lookup"><span data-stu-id="691c2-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="691c2-138">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="691c2-138">Click Inventory.</span></span>
2. <span data-ttu-id="691c2-139">Eldeki öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-139">Click On-hand.</span></span>
3. <span data-ttu-id="691c2-140">Genel Bakış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-140">Click Overview.</span></span>
    * <span data-ttu-id="691c2-141">Satıcının sahip olduğu konsinye, stok olarak alınan maddelerin elde kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="691c2-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="691c2-142">Konsinye stok yenileme siparişinde kalan miktar Toplam sipariş edilen alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="691c2-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="691c2-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="691c2-143">Close the page.</span></span>
5. <span data-ttu-id="691c2-144">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="691c2-144">Click Close.</span></span>

