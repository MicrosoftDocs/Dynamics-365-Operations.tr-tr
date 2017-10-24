--- 
title: "Ambar iş ilkelerini ayarlama "
description: "Ambar işlemi her zaman ambar çalışmasını içermezler."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7d579ca7e2b9ca8cbead74b2c2ababfd142f171
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="21f13-103">Ambar iş ilkelerini ayarlama </span><span class="sxs-lookup"><span data-stu-id="21f13-103">Set up warehouse work policies</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21f13-104">Ambar işlemi her zaman ambar çalışmasını içermezler.</span><span class="sxs-lookup"><span data-stu-id="21f13-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="21f13-105">Bir çalışma ilkesi tanımlayarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21f13-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="21f13-106">USMF demo veri şirketi bu kaydı oluşturmak için kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="21f13-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="21f13-107">Bu görev kılavuzu Dynamics AX uygulama 7.0.1 veya sonrasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="21f13-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="21f13-108">Ambar yönetimi > Kurulum > İş > İş ilkeleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="21f13-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="21f13-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21f13-109">Click New.</span></span>
3. <span data-ttu-id="21f13-110">Çalışma ilkesi ad alanına 'Hiçbir yerine koyma çalışma' yazın.</span><span class="sxs-lookup"><span data-stu-id="21f13-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="21f13-111">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21f13-111">Click Save.</span></span>
5. <span data-ttu-id="21f13-112">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="21f13-112">Click Add.</span></span>
6. <span data-ttu-id="21f13-113">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="21f13-114">İş siparişi türü alanına, 'Mamul mallar yerine koyma' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="21f13-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="21f13-115">Click Add.</span></span>
9. <span data-ttu-id="21f13-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="21f13-117">İş emri türü alanında, "Ortak ürün ve yan ürün yerine koyma" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="21f13-118">Stok konumları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="21f13-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="21f13-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="21f13-119">Click Add.</span></span>
13. <span data-ttu-id="21f13-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="21f13-121">Ambar listesinde '51' girin.</span><span class="sxs-lookup"><span data-stu-id="21f13-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="21f13-122">Konum alanına bir '001' girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="21f13-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="21f13-123">Ürünler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="21f13-123">Expand the Products section.</span></span>
17. <span data-ttu-id="21f13-124">Ürün seçimi alanında, 'Seçili'yi işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="21f13-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="21f13-125">Click Add.</span></span>
19. <span data-ttu-id="21f13-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="21f13-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="21f13-127">Madde numarası alanında 'L0101' girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="21f13-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="21f13-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21f13-128">Click Save.</span></span>


