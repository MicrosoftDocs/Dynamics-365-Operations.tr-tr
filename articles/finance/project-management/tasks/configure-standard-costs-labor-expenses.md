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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140105"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="4038d-103">İşçilik ve masraflar için standart maliyetleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4038d-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4038d-104">Bu konu, bir projenin işgücü ve giderleri için standart maliyetleri ayarlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="4038d-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="4038d-105">Bu görev, USSI veri kümesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4038d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4038d-106">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Maliyet fiyatı (saat)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4038d-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="4038d-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-107">Select **New**.</span></span>
3. <span data-ttu-id="4038d-108">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="4038d-109">**Maliyet fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="4038d-110">Proje kategorisi için standart bir maliyet fiyatı ayarlayabilir veya maliyet fiyatını çalışan numarası, proje numarası, kategori, tarih veya tüm diğer birleşimlere göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4038d-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="4038d-111">Uygulanan maliyet fiyatı, en yüksek ayrıntı düzeyine sahip maliyet fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="4038d-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="4038d-112">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-112">Select **Save**.</span></span>
6. <span data-ttu-id="4038d-113">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Satış fiyatı (saat)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4038d-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="4038d-114">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-114">Select **New**.</span></span>
8. <span data-ttu-id="4038d-115">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="4038d-116">**Geçerlilik** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="4038d-117">**Fiyatlandırma** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="4038d-118">Saat hareketleri veya bir proje kategorisi için bir standart satış fiyatı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4038d-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="4038d-119">Ayrıca, satış fiyatlarını çalışan numarasına, proje numarasına, kategoriye, hareket tarihine veya bunların bir birleşimine göre ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4038d-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="4038d-120">Çalışan, Hizmet saatleri günlüğüne bir hareket girdiğinde uygulanan fiili satış fiyatı, en yüksek ayrıntı düzeyine sahip satış fiyatı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4038d-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4038d-121">Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4038d-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="4038d-122">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-122">Select **Save**.</span></span>
12. <span data-ttu-id="4038d-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4038d-123">Close the page.</span></span>
13. <span data-ttu-id="4038d-124">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Maliyet fiyatı (gider)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4038d-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="4038d-125">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-125">Select **New**.</span></span>
15. <span data-ttu-id="4038d-126">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="4038d-127">**Maliyet fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="4038d-128">Birden fazla alan doldurulabilir ancak bu, kaydı kaydetmek için gereken en düşük düzeydir.</span><span class="sxs-lookup"><span data-stu-id="4038d-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="4038d-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-129">Select **Save**.</span></span>
18. <span data-ttu-id="4038d-130">Gezinti bölmesinde **Modüller > Proje yönetimi muhasebe parametreleri > Ayarla > Fiyatlar > Satış fiyatı (gider)**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4038d-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="4038d-131">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-131">Select **New**.</span></span>
20. <span data-ttu-id="4038d-132">**Yürürlük tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="4038d-133">**Geçerlilik** alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="4038d-134">**Fiyatlandırma** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4038d-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="4038d-135">Çalışan bir masraf günlüğüne hareketleri girdiğinde uygulanan gerçek satış fiyatı, en yüksek ayrıntı düzeyini içeren satış fiyatıdır.</span><span class="sxs-lookup"><span data-stu-id="4038d-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4038d-136">Örneğin hem genel hem de çalışana özel bir satış fiyatı ayarlanırsa, çalışana özel satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4038d-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="4038d-137">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4038d-137">Select **Save**.</span></span>

