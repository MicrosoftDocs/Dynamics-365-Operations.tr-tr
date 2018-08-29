---
title: "Mağaza stok yönetimi"
description: "Bu makalede, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 72f6f5e2645240ee3ddd31657176f27cb7db404f
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="store-inventory-management"></a><span data-ttu-id="13560-103">Mağaza stok yönetimi</span><span class="sxs-lookup"><span data-stu-id="13560-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13560-104">Bu makalede, stoku yönetmek için kullanabileceğiniz belge türleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="13560-104">This article describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="13560-105">Kuruluşunuzun stoğunu yönetmek için aşağıdaki belge türlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="13560-105">You can use the following types of documents to manage your organization's inventory.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="13560-106">Satınalma siparişleri</span><span class="sxs-lookup"><span data-stu-id="13560-106">Purchase orders</span></span>
<span data-ttu-id="13560-107">Satınalma siparişleri merkez ofiste oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="13560-107">Purchase orders are created at the head office.</span></span> <span data-ttu-id="13560-108">Satınalma siparişi başlığına bir perakende ambarı dahil edilirse, sipariş, Microsoft Dynamics 365 for Retail'de Modern POS (MPOS) veya Cloud POS kullanılarak mağazadan teslim alınabilir.</span><span class="sxs-lookup"><span data-stu-id="13560-108">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="13560-109">Mağazada teslim alınan miktarlar girildikten sonra ek değişiklikler için yerel olarak kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-109">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="13560-110">Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-110">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="13560-111">Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Retail'da, satınalma siparişindeki **Şimdi al** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="13560-111">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="13560-112">Transfer emirleri</span><span class="sxs-lookup"><span data-stu-id="13560-112">Transfer orders</span></span>
<span data-ttu-id="13560-113">Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-113">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="13560-114">Bu durumda, transfer emri MPOS'ta veya Cloud POS'ta bir malzeme çekme isteği olarak mağazada görünür.</span><span class="sxs-lookup"><span data-stu-id="13560-114">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="13560-115">Talep edilen miktarlar çekildikten sonra taahhüt edilip merkez ofise gönderilir.</span><span class="sxs-lookup"><span data-stu-id="13560-115">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="13560-116">Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Retail'da, transfer emrindeki **Şimdi sevk et** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="13560-116">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="13560-117">Transfer emri belirli bir mağazanın maddelerin sevk edilebileceği bir konum olduğunu belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-117">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="13560-118">Bu durumda, transfer emri MPOS'ta veya Cloud POS'ta teslim alma isteği olarak mağazada görünür.</span><span class="sxs-lookup"><span data-stu-id="13560-118">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="13560-119">Mağazada teslim alınan miktarlar girildikten sonra ek değişiklikler için yerel olarak kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-119">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="13560-120">Alternatif olarak, miktarlar ayrılıp merkez ofise gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-120">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="13560-121">Merkez ofiste, mağazada alınan miktarlar Dynamics 365 for Retail'da, transfer siparişindeki **Şimdi al** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="13560-121">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="13560-122">Stok sayımları</span><span class="sxs-lookup"><span data-stu-id="13560-122">Stock counts</span></span>
<span data-ttu-id="13560-123">Stok sayımları zamanlanmış veya zamanlanmamış olabilir.</span><span class="sxs-lookup"><span data-stu-id="13560-123">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="13560-124">Planlı stok sayımları sayılması gereken maddeleri belirten merkez ofiste başlatılır.</span><span class="sxs-lookup"><span data-stu-id="13560-124">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="13560-125">Merkez ofis mağazada alınabilecek bir sayım belgesi oluşturur ve fiili eldeki stok miktarları burada MPOS'a veya Cloud POS'a girilir.</span><span class="sxs-lookup"><span data-stu-id="13560-125">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="13560-126">Mağazada planlanmamış stok sayımları başlatılır ve fiili eldeki stok miktarları MPOS'ta veya Cloud POS'te güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="13560-126">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="13560-127">Planlı stok sayımlarından farklı olarak, planlanmamış stok sayımlarında önceden tanımlanmış bir madde listesi yoktur.</span><span class="sxs-lookup"><span data-stu-id="13560-127">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="13560-128">Her iki türün birinden bir stok sayımı tamamlandığında, özen ve merkez ofise gönderilir.</span><span class="sxs-lookup"><span data-stu-id="13560-128">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="13560-129">Merkez ofiste sayım doğrulanır ve nakledilir.</span><span class="sxs-lookup"><span data-stu-id="13560-129">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="13560-130">Stok arama</span><span class="sxs-lookup"><span data-stu-id="13560-130">Inventory lookup</span></span>
<span data-ttu-id="13560-131">Çok sayıda mağaza ve ambar için geçerli eldeki ürün miktarı, Stok arama sayfasından görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-131">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="13560-132">Geçerli eldeki miktara ek olarak, gelecekte karşılanabilir (ATP) miktarlar, her bir mağaza için görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="13560-132">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="13560-133">Bunu yapmak için, ATP'sini görüntülemek istediğiniz mağazayı seçin ve **Mağaza kullanılabilirliğini göster** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="13560-133">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>





