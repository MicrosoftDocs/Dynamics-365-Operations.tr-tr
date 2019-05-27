---
title: Satınalma siparişindeki malların girişini kaydetme
description: Bu yordam, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini gösterir.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551918"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="8c699-103">Satınalma siparişindeki malların girişini kaydetme</span><span class="sxs-lookup"><span data-stu-id="8c699-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c699-104">Bu yordam, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c699-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="8c699-105">Ayrıca ambarda ürün girişini kaydedip ardından satınalma siparişi üzerinde kaydetmek de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="8c699-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="8c699-106">Bu görev genelde bir satınalma temsilcisi veya bir borç hesapları koordinatörü tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="8c699-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="8c699-107">Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8c699-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="8c699-108">Örnek, yordamı bir görev kılavuzu gibi kullanabilmeniz için basit bir satınalma siparişini oluşturma adımlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="8c699-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="8c699-109">Yordamı kendi verilerinizde kullanıyorsanız Mal girişini kaydet alt görevinden başlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="8c699-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="8c699-110">Malların girişi için yeni bir satınalma siparişi hazırlayın</span><span class="sxs-lookup"><span data-stu-id="8c699-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="8c699-111">Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="8c699-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8c699-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-112">Click New.</span></span>
3. <span data-ttu-id="8c699-113">Satıcı hesabı alanına, US-101 girin.</span><span class="sxs-lookup"><span data-stu-id="8c699-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="8c699-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-114">Click OK.</span></span>
5. <span data-ttu-id="8c699-115">Madde numarası alanına M0001 girin.</span><span class="sxs-lookup"><span data-stu-id="8c699-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="8c699-116">Miktar alanına 5 girin.</span><span class="sxs-lookup"><span data-stu-id="8c699-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="8c699-117">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="8c699-118">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="8c699-119">Mal girişini kaydetme</span><span class="sxs-lookup"><span data-stu-id="8c699-119">Record receipt of goods</span></span>
1. <span data-ttu-id="8c699-120">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="8c699-121">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-121">Click Product receipt.</span></span>
    * <span data-ttu-id="8c699-122">Miktar alanı almak istediğiniz miktar için farklı seçenekler seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="8c699-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="8c699-123">Örneğin, bir miktar daha önceden ambarda kaydedildiyse Kayıtlı miktarı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c699-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="8c699-124">Bu örnek için Sipariş edilen miktar değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8c699-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="8c699-125">Ürün girişi alanına herhangi bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8c699-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="8c699-126">Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8c699-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="8c699-127">Satırlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8c699-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="8c699-128">Miktarı '4' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="8c699-129">Burada, sipariş üzerindeki her bir satır için alınan miktarı el ile belirleyebilme imkanınız bulunur.</span><span class="sxs-lookup"><span data-stu-id="8c699-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="8c699-130">Satırlar bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="8c699-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="8c699-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c699-131">Click OK.</span></span>
    * <span data-ttu-id="8c699-132">Mallar şimdi satınalma siparişinde alındı olarak kaydedilir ve bunu yansıtan belge olarak bir ürün giriş yevmiye defteri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8c699-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="8c699-133">Satınalma siparişiyle oluşturulan günlükleri gözden geçirmek ve nelerin ve ne zaman alındığını görmek için Ürün giriş etkinliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c699-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

