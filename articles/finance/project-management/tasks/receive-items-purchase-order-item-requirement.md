---
title: Satınalma siparişinde madde gereksiniminden maddeleri alma
description: Bu konu, bir satınalma siparişindeki maddeleri bir madde gereksiniminden almayı açıklar.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174432"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="8788c-103">Satınalma siparişinde madde gereksiniminden maddeleri alma</span><span class="sxs-lookup"><span data-stu-id="8788c-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8788c-104">Bu konu, bir satınalma siparişindeki maddeleri bir madde gereksiniminden almayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="8788c-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="8788c-105">Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8788c-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="8788c-106">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8788c-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8788c-107">Gezinti bölmesi'nde **Modüller > Proje yönetimi muhasebe parametreleri > Projeeri > Tüm projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="8788c-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="8788c-108">Listede, istenen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="8788c-109">Eylem Bölmesinde, **Plan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="8788c-110">**Madde gereksinimleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="8788c-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-111">Select **New**.</span></span>
6. <span data-ttu-id="8788c-112">Yeni satırda **Madde numarası** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="8788c-113">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8788c-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="8788c-114">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-114">Select **Save**.</span></span>
9. <span data-ttu-id="8788c-115">Eylem Bölmesinde, **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="8788c-116">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-116">Select **Functions**.</span></span>
11. <span data-ttu-id="8788c-117">**Satınalma siparişi oluşturma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="8788c-118">**Tümünü dahil et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="8788c-119">**Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="8788c-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-120">Select **OK**.</span></span>
15. <span data-ttu-id="8788c-121">Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Tüm satın alma siparişleri** öpesine gidin.</span><span class="sxs-lookup"><span data-stu-id="8788c-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="8788c-122">Listede, istenen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="8788c-123">Eylem Bölmesinde, **Satınalma** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8788c-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="8788c-124">**Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="8788c-125">Eylem Bölmesinde, **Teslim alma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="8788c-126">**Ürün girişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="8788c-127">**Ürün girişi** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8788c-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="8788c-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8788c-128">Select **OK**.</span></span>

