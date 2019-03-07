---
title: Yeni ambar düzeni oluşturma
description: Bu yordam, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını gösterir.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "360544"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="aca16-103">Yeni ambar düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="aca16-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aca16-104">Bu yordam, ambardaki konumlarla ilgili bilgilerin nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aca16-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="aca16-105">Bu, yalnızca Stok yönetim modülünde "temel depolama" kullanılarak oluşturulan depolar için geçerlidir; Ambar yönetimi modülünde oluşturulan depolara uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="aca16-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="aca16-106">Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aca16-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="aca16-107">Varsayılan konum kapasitesini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="aca16-107">Set the default location capacity</span></span>
1. <span data-ttu-id="aca16-108">Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="aca16-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="aca16-109">Konumlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="aca16-110">Standart genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aca16-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="aca16-111">Standart derinlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aca16-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="aca16-112">Standart yükselik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aca16-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="aca16-113">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-113">Click Save.</span></span>
7. <span data-ttu-id="aca16-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="aca16-115">Konum adı biçimini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="aca16-115">Define the location name format</span></span>
1. <span data-ttu-id="aca16-116">Stok yönetimi > Kurulum > Stok dökümü > Ambarlar öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="aca16-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="aca16-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-117">Click New.</span></span>
3. <span data-ttu-id="aca16-118">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="aca16-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="aca16-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="aca16-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="aca16-120">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="aca16-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="aca16-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="aca16-122">Konum adları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="aca16-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="aca16-123">Bu bölümdeki seçenekler, konum adları için varsayılan biçimi belirler.</span><span class="sxs-lookup"><span data-stu-id="aca16-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="aca16-124">Örneğimizde, koridor numarasını, dolap numarasını ve raf numarasını ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="aca16-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="aca16-125">Koridoru dahil et seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="aca16-126">Dolabı dahil et seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="aca16-127">Biçin alanına, dolap için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aca16-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="aca16-128">Örneğin: -##</span><span class="sxs-lookup"><span data-stu-id="aca16-128">For example: -##</span></span>  
11. <span data-ttu-id="aca16-129">Raf dahil et seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="aca16-130">Biçin alanına, raf için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aca16-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="aca16-131">Örneğin: -##</span><span class="sxs-lookup"><span data-stu-id="aca16-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="aca16-132">Ambar konumlarını belirleyin</span><span class="sxs-lookup"><span data-stu-id="aca16-132">Define warehouse locations</span></span>
1. <span data-ttu-id="aca16-133">Eylem Bölmesinde, Ambar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="aca16-134">Konum Sihirbazı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aca16-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="aca16-135">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-135">Click Next.</span></span>
4. <span data-ttu-id="aca16-136">Çıkış noktaları seçeneğinin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="aca16-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="aca16-137">Toplu konumlar seçeneğin seçimini kaldırın</span><span class="sxs-lookup"><span data-stu-id="aca16-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="aca16-138">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-138">Click Next.</span></span>
7. <span data-ttu-id="aca16-139">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-139">Click Next.</span></span>
8. <span data-ttu-id="aca16-140">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-140">Click Next.</span></span>
9. <span data-ttu-id="aca16-141">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-141">Click Next.</span></span>
10. <span data-ttu-id="aca16-142">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-142">Click Next.</span></span>
11. <span data-ttu-id="aca16-143">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-143">Click Next.</span></span>
12. <span data-ttu-id="aca16-144">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-144">Click Next.</span></span>
    * <span data-ttu-id="aca16-145">Bu sayfada gösterilen fiziksel boyutlar, bu yordamın başlangıcında belirlediğiniz boyutlardır.</span><span class="sxs-lookup"><span data-stu-id="aca16-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="aca16-146">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-146">Click Next.</span></span>
14. <span data-ttu-id="aca16-147">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-147">Click Finish.</span></span>
15. <span data-ttu-id="aca16-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aca16-148">Close the page.</span></span>
16. <span data-ttu-id="aca16-149">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="aca16-149">Refresh the page.</span></span>

