---
title: İşçilik ve masraflar için standart maliyetleri yapılandırma
description: Bu konu, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı açıklar.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185417"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f68f3-103">İşçilik ve masraflar için standart maliyetleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f68f3-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f68f3-104">Bu konu, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="f68f3-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f68f3-105">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f68f3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f68f3-106">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Maliyet fiyatı (saat)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="f68f3-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-107">Select **New**.</span></span>
3. <span data-ttu-id="f68f3-108">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="f68f3-109">**Maliyet fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f68f3-110">Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya maliyet fiyatını çalışan numarası, proje numarası, kategori, tarih veya tüm diğer birleşimlere göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f68f3-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f68f3-111">Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyine sahip maliyet fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="f68f3-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f68f3-112">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-112">Select **Save**.</span></span>
6. <span data-ttu-id="f68f3-113">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Satış fiyatı (saat)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="f68f3-114">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-114">Select **New**.</span></span>
8. <span data-ttu-id="f68f3-115">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="f68f3-116">**Geçerlilik** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="f68f3-117">**Fiyatlandırma** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f68f3-118">Saat hareketleri veya bir proje kategorisi için bir standart satış fiyatı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f68f3-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f68f3-119">Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların bir birleşimine göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f68f3-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f68f3-120">Çalışan, Hizmet saatleri günlüğüne bir hareket girdiğinde uygulanan fiili satış fiyatı, en yüksek ayrıntı düzeyine sahip satış fiyatı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f68f3-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f68f3-121">Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f68f3-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="f68f3-122">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-122">Select **Save**.</span></span>
12. <span data-ttu-id="f68f3-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f68f3-123">Close the page.</span></span>
13. <span data-ttu-id="f68f3-124">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Maliyet fiyatı (gider)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="f68f3-125">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-125">Select **New**.</span></span>
15. <span data-ttu-id="f68f3-126">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="f68f3-127">**Maliyet fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f68f3-128">Birden fazla alan doldurulabilir ancak bu, kaydı kaydetmek için gereken en düşük düzeydir.</span><span class="sxs-lookup"><span data-stu-id="f68f3-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="f68f3-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-129">Select **Save**.</span></span>
18. <span data-ttu-id="f68f3-130">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Satış fiyatı (gider)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="f68f3-131">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-131">Select **New**.</span></span>
20. <span data-ttu-id="f68f3-132">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="f68f3-133">**Geçerlilik** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="f68f3-134">**Fiyatlandırma** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f68f3-135">Çalışan bir masraf günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="f68f3-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f68f3-136">Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f68f3-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="f68f3-137">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f68f3-137">Select **Save**.</span></span>

