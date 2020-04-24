---
title: Konsinye stok yenileme siparişi oluşturma
description: Bu konu bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı açıklar.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 66611e2d8a88269fe727c46ef4aa6aa809cc7836
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214056"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="e845e-103">Konsinye stok yenileme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e845e-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e845e-104">Bu konu bir satıcıdan beklenen teslimatı konsinye stoğunuzda izleyebildiğiniz bir konsinye stok yenileme siparişi oluşturmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="e845e-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="e845e-105">Ayrıca ürünlerin alımını, konsinye stoğun satıcının sahibi olduğu eldeki stok olarak kaydedilecek şekilde kaydetmeyi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="e845e-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="e845e-106">Bu yordam normalde tedarik profesyoneli tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e845e-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="e845e-107">Bu kılavuzu USMF demo şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e845e-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="e845e-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="e845e-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="e845e-109">Konsinye stok yenileme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e845e-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="e845e-110">Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Konsinye > Konsinye stok yenileme siparişleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e845e-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="e845e-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-111">Select **New**.</span></span>
3. <span data-ttu-id="e845e-112">**Satıcı hesabı** alanında, satıcı **USD-104**'ü seçin (**stok sahipleri** sayfasında sahip olarak kayıtlı bir satıcıyı seçmeniz gerekir).</span><span class="sxs-lookup"><span data-stu-id="e845e-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="e845e-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-113">Select **OK**.</span></span>
5. <span data-ttu-id="e845e-114">**Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-114">Select **Add line**.</span></span>
6. <span data-ttu-id="e845e-115">**Madde numarası** alanına, `M9211CI` yazın (konsinye stok için ayarlanmış bir maddeyi seçmeniz gerekir).</span><span class="sxs-lookup"><span data-stu-id="e845e-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="e845e-116">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e845e-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="e845e-117">**İstenen teslim tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="e845e-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="e845e-118">İstenen ve onaylanan tarihler, malların beklenen varış tarihi için MRP altyapısı tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e845e-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="e845e-119">**Teyit edilmiş teslimat tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="e845e-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="e845e-120">**Satır ayrıntıları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e845e-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="e845e-121">**Stok boyutları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="e845e-122">**Stok boyutları sahibi** alanında sahibi göstermek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="e845e-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="e845e-123">Satıcı US-104 artık sahip olarak listelenir.</span><span class="sxs-lookup"><span data-stu-id="e845e-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="e845e-124">Stok hareketi durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="e845e-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="e845e-125">**Stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="e845e-126">**Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="e845e-127">İstenen satırda **Giriş** alanının **Sipariş edildi** olarak ayarlandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e845e-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="e845e-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e845e-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="e845e-129">Maddeleri al</span><span class="sxs-lookup"><span data-stu-id="e845e-129">Receive items</span></span>
1. <span data-ttu-id="e845e-130">**Ürün girişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="e845e-131">**Harici ürün girişi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e845e-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="e845e-132">**Miktar** alanına, burada gösterilenden daha küçük bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e845e-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="e845e-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="e845e-134">Eldeki stoğu denetleme</span><span class="sxs-lookup"><span data-stu-id="e845e-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="e845e-135">**Stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="e845e-136">**Eldeki** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="e845e-137">**Genel bakış**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e845e-137">Select **Overview**.</span></span> <span data-ttu-id="e845e-138">Satıcının sahip olduğu konsinye, stok olarak alınan maddelerin elde kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="e845e-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="e845e-139">Konsinye stok yenileme siparişinde kalan miktar **Toplam sipariş edilen** alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e845e-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="e845e-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e845e-140">Close the page.</span></span>

