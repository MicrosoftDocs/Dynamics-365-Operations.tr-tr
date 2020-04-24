---
title: Ambar iş ilkelerini ayarla (Uygulama, Mayıs 2016)
description: Ambar işlemi her zaman ambar çalışmasını içermezler.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62fbf2f44216c300af5e092f5dbd05ef2239321b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216793"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="bea76-103">Ambar iş ilkelerini ayarla (Uygulama, Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="bea76-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bea76-104">Ambar işlemi her zaman ambar çalışmasını içermezler.</span><span class="sxs-lookup"><span data-stu-id="bea76-104">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="bea76-105">Bir çalışma ilkesi tanımlayarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea76-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="bea76-106">USMF demo veri şirketi bu kaydı oluşturmak için kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="bea76-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="bea76-107">Bu görev kılavuzu Dynamics AX uygulama 7.0.1 veya sonrasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="bea76-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="bea76-108">Ambar yönetimi > Kurulum > İş > İş ilkeleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="bea76-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="bea76-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea76-109">Click New.</span></span>
3. <span data-ttu-id="bea76-110">Çalışma ilkesi ad alanına 'Hiçbir yerine koyma çalışma' yazın.</span><span class="sxs-lookup"><span data-stu-id="bea76-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="bea76-111">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea76-111">Click Save.</span></span>
5. <span data-ttu-id="bea76-112">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bea76-112">Click Add.</span></span>
6. <span data-ttu-id="bea76-113">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="bea76-114">İş siparişi türü alanına, 'Mamul mallar yerine koyma' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="bea76-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bea76-115">Click Add.</span></span>
9. <span data-ttu-id="bea76-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="bea76-117">İş emri türü alanında, "Ortak ürün ve yan ürün yerine koyma" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="bea76-118">Stok konumları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="bea76-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="bea76-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bea76-119">Click Add.</span></span>
13. <span data-ttu-id="bea76-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="bea76-121">Ambar listesinde '51' girin.</span><span class="sxs-lookup"><span data-stu-id="bea76-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="bea76-122">Konum alanına bir '001' girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bea76-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="bea76-123">Ürünler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="bea76-123">Expand the Products section.</span></span>
17. <span data-ttu-id="bea76-124">Ürün seçimi alanında, 'Seçili'yi işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="bea76-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bea76-125">Click Add.</span></span>
19. <span data-ttu-id="bea76-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea76-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="bea76-127">Madde numarası alanında 'L0101' girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bea76-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="bea76-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea76-128">Click Save.</span></span>

