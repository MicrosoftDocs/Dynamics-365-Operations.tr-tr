--- 
title: "Satınalma siparişinde madde gereksiniminden maddeleri alma"
description: "Bu yordam, bir satınalma siparişindeki maddeleri bir madde gereksiniminden almayı gösterir."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7c9093439c4c0c4645d96ad97ba56f31026ec334
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="a4025-103">Satınalma siparişinde madde gereksiniminden maddeleri alma</span><span class="sxs-lookup"><span data-stu-id="a4025-103">Receive items on purchase order from item requirement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4025-104">Bu yordam, bir satınalma siparişindeki maddeleri bir madde gereksiniminden almayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4025-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="a4025-105">Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4025-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="a4025-106">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a4025-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a4025-107">Proje yönetimi ve muhasebe > Projeler > Tüm projeler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a4025-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="a4025-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="a4025-109">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="a4025-110">Madde gereksinimleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-110">Click Item requirements.</span></span>
5. <span data-ttu-id="a4025-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-111">Click New.</span></span>
6. <span data-ttu-id="a4025-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a4025-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="a4025-113">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a4025-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="a4025-114">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a4025-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="a4025-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-115">Click Save.</span></span>
10. <span data-ttu-id="a4025-116">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4025-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="a4025-117">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4025-117">Click Functions.</span></span>
12. <span data-ttu-id="a4025-118">Satınalma siparişi oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="a4025-119">Dahil et onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a4025-119">Select the Include check box.</span></span>
14. <span data-ttu-id="a4025-120">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a4025-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="a4025-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-121">Click OK.</span></span>
16. <span data-ttu-id="a4025-122">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4025-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="a4025-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="a4025-124">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="a4025-125">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-125">Click Confirm.</span></span>
20. <span data-ttu-id="a4025-126">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="a4025-127">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-127">Click Product receipt.</span></span>
22. <span data-ttu-id="a4025-128">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a4025-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="a4025-129">Ürün girişi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4025-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="a4025-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4025-130">Click OK.</span></span>


