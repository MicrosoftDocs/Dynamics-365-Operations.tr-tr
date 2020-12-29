---
title: Proje satınalma siparişi oluşturma
description: Bu yordam, size bir proje satınalma siparişi oluşturmayı gösterir.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, PurchCreateOrder, PurchTable, PurchTablePart, InventItemIdLookupPurchase
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85079a843de02a8c8d5ae0ec291fa77464dd2dff
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439706"
---
# <a name="create-project-purchase-order"></a><span data-ttu-id="de4b2-103">Proje satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="de4b2-103">Create project purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de4b2-104">Bu yordam, size bir proje satınalma siparişi oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="de4b2-104">This procedure shows you how to create a project purchase order.</span></span> <span data-ttu-id="de4b2-105">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="de4b2-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="de4b2-106">Proje yönetimi ve muhasebe > Projeler > Tüm projeler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-106">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="de4b2-107">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-107">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="de4b2-108">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-108">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="de4b2-109">Madde Görevi'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-109">Click Item task.</span></span>
5. <span data-ttu-id="de4b2-110">Satın alma siparişini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-110">Click Purchase order.</span></span>
6. <span data-ttu-id="de4b2-111">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-111">In the Vendor account field, enter or select a value.</span></span>
7. <span data-ttu-id="de4b2-112">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-112">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="de4b2-113">Bu adımlar gerekli değildir ancak satınalma siparişi satırları için varsayılan bir tesis ve ambar ayarlayarak, satınalma siparişini basitleştirirler.</span><span class="sxs-lookup"><span data-stu-id="de4b2-113">These steps aren't required, but they do simplify the purchase order by setting up a default site and warehouse for the purchase order lines.</span></span>  
8. <span data-ttu-id="de4b2-114">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-114">In the Warehouse field, enter or select a value.</span></span>
9. <span data-ttu-id="de4b2-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-115">Click OK.</span></span>
10. <span data-ttu-id="de4b2-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="de4b2-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="de4b2-118">Bu, madde numarası veya tedarik kategorisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="de4b2-118">This can be the item number or a procurement category.</span></span>  
12. <span data-ttu-id="de4b2-119">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-119">Expand the Line details section.</span></span>
13. <span data-ttu-id="de4b2-120">Proje sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-120">Click the Project tab.</span></span>
    * <span data-ttu-id="de4b2-121">Satışların ve maliyet fiyatlarının kullanılabilir olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-121">Verify that the sales and cost prices are available.</span></span> <span data-ttu-id="de4b2-122">Kullanılabilir olmayıp gerekli oldukları durumda, bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="de4b2-122">If they are not available but needed, enter the information.</span></span>  
14. <span data-ttu-id="de4b2-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de4b2-123">Click Save.</span></span>

