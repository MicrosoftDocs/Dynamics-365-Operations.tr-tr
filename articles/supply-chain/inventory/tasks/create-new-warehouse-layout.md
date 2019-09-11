---
title: Yeni ambar düzeni oluşturma
description: Bu konu, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını açıklar.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 302c028a93dfdb57972e4759abbbc4fdedabbd17
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867257"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="053df-103">Yeni ambar düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="053df-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="053df-104">Bu konu, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="053df-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="053df-105">Bu, yalnızca Stok yönetim modülünde "temel depolama" kullanılarak oluşturulan depolar için geçerlidir; Ambar yönetimi modülünde oluşturulan depolara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="053df-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="053df-106">Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="053df-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="053df-107">Varsayılan konum kapasitesini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="053df-107">Set the default location capacity</span></span>
1. <span data-ttu-id="053df-108">Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok ve ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="053df-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="053df-109">**Yerleşim** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="053df-110">**Standart genişlik** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="053df-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="053df-111">**Standart derinlik** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="053df-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="053df-112">**Standart yükselik** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="053df-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="053df-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-113">Select **Save**.</span></span>
7. <span data-ttu-id="053df-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="053df-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="053df-115">Konum adı biçimini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="053df-115">Define the location name format</span></span>
1. <span data-ttu-id="053df-116">Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok dökümü > Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="053df-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="053df-117">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-117">Select **New**.</span></span>
3. <span data-ttu-id="053df-118">**Ambar** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="053df-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="053df-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="053df-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="053df-120">**Tesis** alanında, aramadan istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="053df-121">**Konum adları** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="053df-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="053df-122">Bu bölümdeki seçenekler, konum adları için varsayılan biçimi belirler.</span><span class="sxs-lookup"><span data-stu-id="053df-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="053df-123">Örneğimizde, koridor numarasını, dolap numarasını ve raf numarasını ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="053df-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="053df-124">**Koridoru dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="053df-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="053df-125">**Dolabı dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="053df-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="053df-126">**Biçim** alanına, dolap için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="053df-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="053df-127">**Raf dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="053df-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="053df-128">**Biçim** alanına, raf için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="053df-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="053df-129">Ambar konumlarını belirleyin</span><span class="sxs-lookup"><span data-stu-id="053df-129">Define warehouse locations</span></span>
1. <span data-ttu-id="053df-130">Eylem Bölmesinde, **Ambarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="053df-131">**Konum Sihirbazı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="053df-132">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-132">Select **Next**.</span></span>
4. <span data-ttu-id="053df-133">**Çıkış noktaları** seçeneğinin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="053df-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="053df-134">**Toplu konumlar** seçeneğin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="053df-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="053df-135">**Bitiş**' seçeneğine gelene kadar **Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="053df-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="053df-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="053df-136">Close the page.</span></span>
8. <span data-ttu-id="053df-137">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="053df-137">Refresh the page.</span></span>

