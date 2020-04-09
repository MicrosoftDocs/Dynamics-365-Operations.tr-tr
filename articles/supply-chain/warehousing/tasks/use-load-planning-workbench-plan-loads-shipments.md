---
title: Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama
description: Bu konuda yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada kullanma açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a51031647e270662f37138848b0db9ed08d544e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145905"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="26bf5-103">Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama</span><span class="sxs-lookup"><span data-stu-id="26bf5-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="26bf5-104">Bu konuda yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada kullanma açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="26bf5-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="26bf5-105">Bir önkoşul olarak satış siparişi ilk oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="26bf5-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="26bf5-106">Bu yordamı ulaşım koordinatörü için günlük çalışmanın bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="26bf5-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="26bf5-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="26bf5-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="26bf5-108">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="26bf5-108">Create a sales order</span></span>
1. <span data-ttu-id="26bf5-109">**Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="26bf5-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-110">Select **New**.</span></span>
3. <span data-ttu-id="26bf5-111">**Müşteri hesabı** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="26bf5-112">**US-004** hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="26bf5-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-113">Select **OK**.</span></span>
6. <span data-ttu-id="26bf5-114">**Madde numarası** alanında, açılır menü düğmesini seçerek aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="26bf5-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="26bf5-115">**A0001** maddesini seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-115">Select item **A0001**.</span></span> <span data-ttu-id="26bf5-116">**A0001** taşıma yönetimi için etkindir.</span><span class="sxs-lookup"><span data-stu-id="26bf5-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="26bf5-117">**Tesis** alanında, açılır menü düğmesini seçerek aramayı açın, ardından bir öğe seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="26bf5-118">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="26bf5-119">**ambar** alanına bu örnek için '24' yazın.</span><span class="sxs-lookup"><span data-stu-id="26bf5-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="26bf5-120">Bu ambar taşımacılık ve gelişmiş ambar yönetimi için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="26bf5-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="26bf5-121">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-121">Select **Save**.</span></span>
12. <span data-ttu-id="26bf5-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="26bf5-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="26bf5-123">Yeni bir yük oluştur</span><span class="sxs-lookup"><span data-stu-id="26bf5-123">Create a new load</span></span>
1. <span data-ttu-id="26bf5-124">**Gezinti bölmesi > Modüller > Taşıma yönetimi > Planlama > Yük planlama çalışma ekranı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="26bf5-125">**Satış satırları** sekmesini seçin. Şimdi oluşturduğunuz satış siparişi için yük oluşturun.</span><span class="sxs-lookup"><span data-stu-id="26bf5-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="26bf5-126">Yükler satınalma siparişlerinin, transfer emirleri ve satış siparişlerinin arz ve talebine göre oluşturulabilirler</span><span class="sxs-lookup"><span data-stu-id="26bf5-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="26bf5-127">Eylem Bölmesinde **Arz ve talep**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="26bf5-128">**Yeni yüke**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-128">Select **To new load**.</span></span>
5. <span data-ttu-id="26bf5-129">**Yük şablonu kodu** alanında aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="26bf5-130">Yük şablonu, ağırlık ve hacim için tüm yükte geçerli olacak maksimum ölçümleri belirler.</span><span class="sxs-lookup"><span data-stu-id="26bf5-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="26bf5-131">Yük şablonu örneğin bir konteyner veya kamyonun boyutunu temsil edebilir.</span><span class="sxs-lookup"><span data-stu-id="26bf5-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="26bf5-132">Bir madde seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-132">Select an item.</span></span>
6. <span data-ttu-id="26bf5-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="26bf5-134">Yük için orana ve rota</span><span class="sxs-lookup"><span data-stu-id="26bf5-134">Rate and route the load</span></span>
1. <span data-ttu-id="26bf5-135">**Oran ve rota**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="26bf5-136">**Rota çalışma ekranı oranı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="26bf5-137">**Atölye oranı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="26bf5-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="26bf5-139">**Ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="26bf5-139">Select **Assign**.</span></span>
6. <span data-ttu-id="26bf5-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="26bf5-140">Close the page.</span></span>

