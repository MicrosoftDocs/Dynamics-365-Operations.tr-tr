---
title: Satınalma siparişindeki malların girişini kaydetme
description: Bu konu, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini açıklar.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d016df08850c75858c50b7f9a97b11b566d26cb0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022670"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="9cecf-103">Satınalma siparişindeki malların girişini kaydetme</span><span class="sxs-lookup"><span data-stu-id="9cecf-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cecf-104">Bu konu, doğrudan bir satınalma siparişi üzerinde malların girişinin nasıl kaydedileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9cecf-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="9cecf-105">Ayrıca ambarda ürün girişini kaydedip ardından satınalma siparişi üzerinde kaydetmek de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="9cecf-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="9cecf-106">Bu görev genelde bir satınalma temsilcisi veya bir borç hesapları koordinatörü tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="9cecf-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="9cecf-107">Bu kılavuzda gösterilen örnek, demo veriler şirketi USMF'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cecf-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="9cecf-108">Örnek, yordamı bir görev kılavuzu gibi kullanabilmeniz için basit bir satınalma siparişini oluşturma adımlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="9cecf-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="9cecf-109">Yordamı kendi verilerinizde kullanıyorsanız **Mal girişini kaydet** alt görevinden başlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="9cecf-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="9cecf-110">Malların girişi için yeni bir satınalma siparişi hazırlayın</span><span class="sxs-lookup"><span data-stu-id="9cecf-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="9cecf-111">**Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma siparişleri > Tüm satınalma siparişleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="9cecf-112">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-112">Select **New**.</span></span>
3. <span data-ttu-id="9cecf-113">**Satıcı hesabı** alanına `US-101` girin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="9cecf-114">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-114">Select **OK**.</span></span>
5. <span data-ttu-id="9cecf-115">**Madde numarası** alanına `M0001` girin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="9cecf-116">**Miktar** alanına `5` girin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="9cecf-117">Eylem Bölmesinde, **Satınalma** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cecf-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="9cecf-118">**Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="9cecf-119">Mal girişini kaydetme</span><span class="sxs-lookup"><span data-stu-id="9cecf-119">Record receipt of goods</span></span>
1. <span data-ttu-id="9cecf-120">Eylem Bölmesinde, **Teslim alma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="9cecf-121">**Ürün girişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-121">Select **Product receipt**.</span></span> <span data-ttu-id="9cecf-122">**Miktar** alanı almak istediğiniz miktar için farklı seçenekler seçmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="9cecf-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="9cecf-123">Örneğin, bir miktar daha önceden ambarda kaydedildiyse **Kayıtlı miktar**'ı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cecf-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="9cecf-124">Bu örnek için **Sipariş edilen miktar** değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9cecf-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="9cecf-125">**Genel bakış** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="9cecf-126">**Ürün girişi** alanına herhangi bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9cecf-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="9cecf-127">Bu alan, ürün giriş günlüğünde makbuz olarak kullanılacak bir referans girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9cecf-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="9cecf-128">**Satırlar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="9cecf-129">**Miktar**'ı '4' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9cecf-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="9cecf-130">Burada, sipariş üzerindeki her bir satır için alınan miktarı el ile belirleyebilme imkanınız bulunur.</span><span class="sxs-lookup"><span data-stu-id="9cecf-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="9cecf-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9cecf-131">Select **OK**.</span></span> <span data-ttu-id="9cecf-132">Mallar şimdi satınalma siparişinde alındı olarak kaydedilir ve bunu yansıtan belge olarak bir ürün giriş yevmiye defteri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cecf-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="9cecf-133">Satınalma siparişiyle oluşturulan günlükleri gözden geçirmek ve nelerin ve ne zaman alındığını görmek için Ürün giriş etkinliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cecf-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

