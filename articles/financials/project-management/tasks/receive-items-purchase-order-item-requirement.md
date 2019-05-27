---
title: Satınalma siparişinde madde gereksiniminden maddeleri alma
description: Bu yordam, bir satınalma siparişindeki maddeleri bir madde gereksiniminden almayı gösterir.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26572a49426719fba520338a5eccd7e0af78890e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572385"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="1c60a-103">Satınalma siparişinde madde gereksiniminden maddeleri alma</span><span class="sxs-lookup"><span data-stu-id="1c60a-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c60a-104">Bu yordam, bir satınalma siparişindeki maddeleri bir madde gereksiniminden almayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c60a-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="1c60a-105">Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c60a-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="1c60a-106">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1c60a-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1c60a-107">Proje yönetimi ve muhasebe > Projeler > Tüm projeler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="1c60a-108">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="1c60a-109">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="1c60a-110">Madde gereksinimleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-110">Click Item requirements.</span></span>
5. <span data-ttu-id="1c60a-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-111">Click New.</span></span>
6. <span data-ttu-id="1c60a-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="1c60a-113">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="1c60a-114">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="1c60a-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-115">Click Save.</span></span>
10. <span data-ttu-id="1c60a-116">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="1c60a-117">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-117">Click Functions.</span></span>
12. <span data-ttu-id="1c60a-118">Satınalma siparişi oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="1c60a-119">Dahil et onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-119">Select the Include check box.</span></span>
14. <span data-ttu-id="1c60a-120">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="1c60a-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-121">Click OK.</span></span>
16. <span data-ttu-id="1c60a-122">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="1c60a-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1c60a-124">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="1c60a-125">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-125">Click Confirm.</span></span>
20. <span data-ttu-id="1c60a-126">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="1c60a-127">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-127">Click Product receipt.</span></span>
22. <span data-ttu-id="1c60a-128">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="1c60a-129">Ürün girişi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c60a-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="1c60a-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c60a-130">Click OK.</span></span>

