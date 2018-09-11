--- 
title: "Yeni ambar düzeni oluşturma"
description: "Bu yordam, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını gösterir."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 7db15eb5d80291641f0d0398d236b5e883cafcaf
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="ad391-103">Yeni ambar düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="ad391-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad391-104">Bu yordam, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad391-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="ad391-105">Bu, yalnızca Stok yönetim modülünde "temel depolama" kullanılarak oluşturulan depolar için geçerlidir; Ambar yönetimi modülünde oluşturulan depolara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="ad391-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="ad391-106">Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad391-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="ad391-107">Varsayılan konum kapasitesini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="ad391-107">Set the default location capacity</span></span>
1. <span data-ttu-id="ad391-108">Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ad391-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="ad391-109">Konumlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="ad391-110">Standart genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ad391-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="ad391-111">Standart derinlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ad391-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="ad391-112">Standart yükselik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ad391-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="ad391-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-113">Click Save.</span></span>
7. <span data-ttu-id="ad391-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="ad391-115">Konum adı biçimini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ad391-115">Define the location name format</span></span>
1. <span data-ttu-id="ad391-116">Stok yönetimi > Kurulum > Stok dökümü > Ambarlar öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="ad391-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="ad391-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-117">Click New.</span></span>
3. <span data-ttu-id="ad391-118">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ad391-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="ad391-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ad391-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ad391-120">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ad391-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ad391-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ad391-122">Konum adları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="ad391-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="ad391-123">Bu bölümdeki seçenekler, konum adları için varsayılan biçimi belirler.</span><span class="sxs-lookup"><span data-stu-id="ad391-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="ad391-124">Örneğimizde, koridor numarasını, dolap numarasını ve raf numarasını ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="ad391-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="ad391-125">Koridoru dahil et seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="ad391-126">Dolabı dahil et seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="ad391-127">Biçin alanına, dolap için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad391-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="ad391-128">Örneğin: -##</span><span class="sxs-lookup"><span data-stu-id="ad391-128">For example: -##</span></span>  
11. <span data-ttu-id="ad391-129">Raf dahil et seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="ad391-130">Biçin alanına, raf için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad391-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="ad391-131">Örneğin: -##</span><span class="sxs-lookup"><span data-stu-id="ad391-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="ad391-132">Ambar konumlarını belirleyin</span><span class="sxs-lookup"><span data-stu-id="ad391-132">Define warehouse locations</span></span>
1. <span data-ttu-id="ad391-133">Eylem Bölmesinde, Ambar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="ad391-134">Konum Sihirbazı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad391-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="ad391-135">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-135">Click Next.</span></span>
4. <span data-ttu-id="ad391-136">Çıkış noktaları seçeneğinin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="ad391-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="ad391-137">Toplu konumlar seçeneğin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="ad391-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="ad391-138">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-138">Click Next.</span></span>
7. <span data-ttu-id="ad391-139">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-139">Click Next.</span></span>
8. <span data-ttu-id="ad391-140">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-140">Click Next.</span></span>
9. <span data-ttu-id="ad391-141">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-141">Click Next.</span></span>
10. <span data-ttu-id="ad391-142">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-142">Click Next.</span></span>
11. <span data-ttu-id="ad391-143">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-143">Click Next.</span></span>
12. <span data-ttu-id="ad391-144">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-144">Click Next.</span></span>
    * <span data-ttu-id="ad391-145">Bu sayfada gösterilen fiziksel boyutlar, bu yordamın başlangıcında belirlediğiniz boyutlardır.</span><span class="sxs-lookup"><span data-stu-id="ad391-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="ad391-146">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-146">Click Next.</span></span>
14. <span data-ttu-id="ad391-147">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-147">Click Finish.</span></span>
15. <span data-ttu-id="ad391-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad391-148">Close the page.</span></span>
16. <span data-ttu-id="ad391-149">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="ad391-149">Refresh the page.</span></span>


