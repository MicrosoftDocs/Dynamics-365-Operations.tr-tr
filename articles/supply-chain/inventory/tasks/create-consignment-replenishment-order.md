---
title: Konsinye stok yenileme siparişi oluşturma
description: Bu yordam bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı gösterir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845558"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="5cdcb-103">Konsinye stok yenileme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5cdcb-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5cdcb-104">Bu yordam bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="5cdcb-105">Ayrıca ürünlerin alımını, konsinye stoğun satıcının sahibi olduğu eldeki stok olarak kaydedilecek şekilde kaydetmeyi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="5cdcb-106">Bu yordam normalde tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="5cdcb-107">Bu kılavuzu USMF demo şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="5cdcb-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="5cdcb-109">Konsinye stok yenileme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5cdcb-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="5cdcb-110">Tedarik ve kaynak atama > Konsinye > Konsinye stok yenileme siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="5cdcb-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-111">Click New.</span></span>
3. <span data-ttu-id="5cdcb-112">Satıcı hesabı alanında satıcı US-104'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="5cdcb-113">Stok sahipleri sayfasında sahip olarak kayıtlı bir satıcı seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="5cdcb-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-114">Click OK.</span></span>
5. <span data-ttu-id="5cdcb-115">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-115">Click Add line.</span></span>
6. <span data-ttu-id="5cdcb-116">Madde numarası alanına M9211CI yazın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="5cdcb-117">Konsinye stoğu için ayarlanmış bir madde seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="5cdcb-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="5cdcb-119">İstenen teslim tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="5cdcb-120">İstenen ve onaylanan tarihler, malların beklenen varış tarihi için MRP altyapısı tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="5cdcb-121">Teyit edilmiş teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="5cdcb-122">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="5cdcb-123">Stok boyutları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="5cdcb-124">Stok boyutları sahibi alanında sahibi göstermek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="5cdcb-125">Satıcı US-104 artık sahip olarak listelenir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="5cdcb-126">Stok hareketi durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="5cdcb-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="5cdcb-127">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-127">Click Inventory.</span></span>
2. <span data-ttu-id="5cdcb-128">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-128">Click Transactions.</span></span>
3. <span data-ttu-id="5cdcb-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5cdcb-130">Giriş alanının Sipariş edildi olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="5cdcb-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="5cdcb-132">Maddeleri al</span><span class="sxs-lookup"><span data-stu-id="5cdcb-132">Receive items</span></span>
1. <span data-ttu-id="5cdcb-133">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-133">Click Product receipt.</span></span>
2. <span data-ttu-id="5cdcb-134">Harici ürün girişi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="5cdcb-135">Miktar alanına, burada gösterilenden daha küçük bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="5cdcb-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="5cdcb-137">Eldeki stoğu denetleme</span><span class="sxs-lookup"><span data-stu-id="5cdcb-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="5cdcb-138">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-138">Click Inventory.</span></span>
2. <span data-ttu-id="5cdcb-139">Eldeki öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-139">Click On-hand.</span></span>
3. <span data-ttu-id="5cdcb-140">Genel Bakış'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-140">Click Overview.</span></span>
    * <span data-ttu-id="5cdcb-141">Satıcının sahip olduğu konsinye, stok olarak alınan maddelerin elde kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="5cdcb-142">Konsinye stok yenileme siparişinde kalan miktar Toplam sipariş edilen alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="5cdcb-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-143">Close the page.</span></span>
5. <span data-ttu-id="5cdcb-144">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5cdcb-144">Click Close.</span></span>

