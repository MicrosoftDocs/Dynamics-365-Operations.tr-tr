---
title: İşçilik ve masraflar için standart maliyetleri yapılandırma
description: Bu yordam, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı gösterir.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "339407"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="9e757-103">İşçilik ve masraflar için standart maliyetleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9e757-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e757-104">Bu yordam, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e757-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="9e757-105">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9e757-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9e757-106">Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (saat) öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9e757-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="9e757-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-107">Click New.</span></span>
3. <span data-ttu-id="9e757-108">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="9e757-109">Maliyet fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="9e757-110">Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya maliyet fiyatını çalışan numarası, proje numarası, kategori, tarih veya tüm diğer birleşimlere göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e757-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="9e757-111">Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyine sahip maliyet fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="9e757-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="9e757-112">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-112">Click Save.</span></span>
6. <span data-ttu-id="9e757-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9e757-113">Close the page.</span></span>
7. <span data-ttu-id="9e757-114">Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (saat) öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9e757-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="9e757-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-115">Click New.</span></span>
9. <span data-ttu-id="9e757-116">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="9e757-117">Geçerlilik alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="9e757-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="9e757-118">Fiyatlandırma alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="9e757-119">Saat hareketleri veya bir proje kategorisi için bir standart satış fiyatı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e757-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="9e757-120">Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların bir birleşimine göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e757-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="9e757-121">Çalışan, Hizmet saatleri günlüğüne bir hareket girdiğinde uygulanan fiili satış fiyatı, en yüksek ayrıntı düzeyine sahip satış fiyatı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9e757-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9e757-122">Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9e757-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="9e757-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-123">Click Save.</span></span>
13. <span data-ttu-id="9e757-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9e757-124">Close the page.</span></span>
14. <span data-ttu-id="9e757-125">Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Maliyet fiyatı (gider) öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9e757-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="9e757-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-126">Click New.</span></span>
16. <span data-ttu-id="9e757-127">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="9e757-128">Maliyet fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="9e757-129">Birden fazla alan doldurulabilir ancak bu, kaydı kaydetmek için gereken en düşük düzeydir.</span><span class="sxs-lookup"><span data-stu-id="9e757-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="9e757-130">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-130">Click Save.</span></span>
19. <span data-ttu-id="9e757-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9e757-131">Close the page.</span></span>
20. <span data-ttu-id="9e757-132">Proje yönetimi ve muhasebe > Kurulum > Fiyatlar > Satış fiyatı (gider) öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9e757-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="9e757-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-133">Click New.</span></span>
22. <span data-ttu-id="9e757-134">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="9e757-135">Geçerlilik alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="9e757-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="9e757-136">Fiyatlandırma alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e757-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="9e757-137">Çalışan bir masraf günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="9e757-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9e757-138">Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9e757-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="9e757-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e757-139">Click Save.</span></span>

