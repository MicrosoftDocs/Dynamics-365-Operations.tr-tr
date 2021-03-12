---
title: Yeni ambar düzeni oluşturma
description: Bu konu, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını açıklar.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07fee1787cc2719bafbe2bb6d54849edda14018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000046"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="eb4c7-103">Yeni ambar düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="eb4c7-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb4c7-104">Bu konu, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="eb4c7-105">Bu, yalnızca Stok yönetim modülünde "temel depolama" kullanılarak oluşturulan depolar için geçerlidir; Ambar yönetimi modülünde oluşturulan depolara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="eb4c7-106">Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="eb4c7-107">Varsayılan konum kapasitesini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="eb4c7-107">Set the default location capacity</span></span>
1. <span data-ttu-id="eb4c7-108">Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok ve ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="eb4c7-109">**Yerleşim** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="eb4c7-110">**Standart genişlik** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="eb4c7-111">**Standart derinlik** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="eb4c7-112">**Standart yükselik** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="eb4c7-113">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-113">Select **Save**.</span></span>
7. <span data-ttu-id="eb4c7-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="eb4c7-115">Konum adı biçimini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="eb4c7-115">Define the location name format</span></span>
1. <span data-ttu-id="eb4c7-116">Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Stok dökümü > Ambarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="eb4c7-117">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-117">Select **New**.</span></span>
3. <span data-ttu-id="eb4c7-118">**Ambar** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="eb4c7-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="eb4c7-120">**Tesis** alanında, aramadan istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="eb4c7-121">**Konum adları** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="eb4c7-122">Bu bölümdeki seçenekler, konum adları için varsayılan biçimi belirler.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="eb4c7-123">Örneğimizde, koridor numarasını, dolap numarasını ve raf numarasını ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="eb4c7-124">**Koridoru dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="eb4c7-125">**Dolabı dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="eb4c7-126">**Biçim** alanına, dolap için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="eb4c7-127">**Raf dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="eb4c7-128">**Biçim** alanına, raf için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="eb4c7-129">Ambar konumlarını belirleyin</span><span class="sxs-lookup"><span data-stu-id="eb4c7-129">Define warehouse locations</span></span>
1. <span data-ttu-id="eb4c7-130">Eylem Bölmesinde, **Ambarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="eb4c7-131">**Konum Sihirbazı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="eb4c7-132">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-132">Select **Next**.</span></span>
4. <span data-ttu-id="eb4c7-133">**Çıkış noktaları** seçeneğinin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="eb4c7-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="eb4c7-134">**Toplu konumlar** seçeneğin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="eb4c7-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="eb4c7-135">**Bitiş**' seçeneğine gelene kadar **Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="eb4c7-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-136">Close the page.</span></span>
8. <span data-ttu-id="eb4c7-137">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="eb4c7-137">Refresh the page.</span></span>

