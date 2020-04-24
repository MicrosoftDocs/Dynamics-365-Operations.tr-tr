---
title: Ürün yapılandırma modeli oluşturma
description: Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9577005fb4fc016670713c36e40263ff30030caf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203783"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="6709a-103">Ürün yapılandırma modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="6709a-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6709a-104">Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6709a-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="6709a-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="6709a-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="6709a-106">Ürün modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="6709a-106">Create a product model</span></span>
1. <span data-ttu-id="6709a-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6709a-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="6709a-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6709a-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="6709a-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6709a-109">Click New.</span></span>
4. <span data-ttu-id="6709a-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6709a-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6709a-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="6709a-112">Çözüm stratejisi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="6709a-113">Çözüm stratejisi, kısıtlama tabanlı bir ürün yapılandırması modelindeki kısıtlamaların nasıl işleme koyulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="6709a-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="6709a-114">Bu seçimin ürün yapılandırma modelinin performansı üzerinde etkisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="6709a-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="6709a-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6709a-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6709a-116">Kök bileşen, ürün yapılandırması modelini temsil eder ve diğer ürün modellerinde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6709a-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="6709a-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6709a-117">Click OK.</span></span>
9. <span data-ttu-id="6709a-118">Yeniden kullanma yapılandırması alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="6709a-119">Yapılandırmaları yeniden kullanma parametresi Evet olarak ayarlanırsa, sistem her bir yapılandırma oturumunun ardından eşdeğer yapılandırmaları denetler ve tam bir eşleşme bulunursa onları yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="6709a-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="6709a-120">Öznitelikler ekle</span><span class="sxs-lookup"><span data-stu-id="6709a-120">Add attributes</span></span>
1. <span data-ttu-id="6709a-121">Öznitelikler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6709a-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="6709a-122">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6709a-122">Click Add.</span></span>
3. <span data-ttu-id="6709a-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6709a-124">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6709a-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6709a-125">Çözücü adı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="6709a-126">Çözücü adı, ürün yapılandırıcının çözücüsü tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6709a-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="6709a-127">Boşluk veya _ (alt çizgi) dışında özel karakterler içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="6709a-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="6709a-128">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6709a-129">Açıklama metni yapılandırma kullanıcısı tarafından görülür ve dolayısıyla doğru öznitelik değerinin seçilmesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="6709a-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="6709a-130">Öznitelik türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6709a-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="6709a-131">Öznitelik türü, hangi değerlerin öznitelik için kullanılabilir olduğunu belirler.</span><span class="sxs-lookup"><span data-stu-id="6709a-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="6709a-132">Yeniden kullanıma dahil et onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="6709a-133">Bu seçenek yalnızca Yapılandırmaları yeniden kullanma seçeneği belirlendiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6709a-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="6709a-134">Yeniden kullan onay kutusunda öznitelik eklenmesi, bu özniteliğin sistem tam bir eşleşme aradığında göz önüne alınacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6709a-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="6709a-135">Alt bileşenler ekleme</span><span class="sxs-lookup"><span data-stu-id="6709a-135">Add subcomponents</span></span>
1. <span data-ttu-id="6709a-136">Alt bileşenler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="6709a-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="6709a-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6709a-137">Click Add.</span></span>
3. <span data-ttu-id="6709a-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6709a-139">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="6709a-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6709a-140">Çözücü adı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="6709a-141">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="6709a-142">Bileşen alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6709a-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="6709a-143">Her alt bileşen bir bileşen tanımına başvurmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6709a-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="6709a-144">Bu tasarım, yeniden kullanılabilir bileşenleri destekler ve bir bileşenin bir kere tanımlandıktan sonra birçok ürün modelinde kullanılabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6709a-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="6709a-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6709a-145">Click Save.</span></span>
9. <span data-ttu-id="6709a-146">Ürün reçetesi satır ayrıntılarını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6709a-146">Click BOM line details.</span></span>
    * <span data-ttu-id="6709a-147">Ürün reçetesi satırı ayrıntıları, kullanıcının alt bileşen için gerekli özellikleri seçmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6709a-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="6709a-148">Her özellik sabit bir değer verebilir veya bir özniteliğine eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="6709a-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="6709a-149">Bir özniteliği eşleştirme, ürün reçetesi satır özelliğinin yapılandırma seçimine bağlı olarak farklı değerler almasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="6709a-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="6709a-150">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6709a-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6709a-151">Her alt bileşen, kısıtlama tabanlı yapılandırma teknolojisine sahip yapılandırılabilir bir ana ürünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6709a-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="6709a-152">Referans, ürün numarası üzerinden verilir.</span><span class="sxs-lookup"><span data-stu-id="6709a-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="6709a-153">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-153">Select the Set check box.</span></span>
12. <span data-ttu-id="6709a-154">Hesaplama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6709a-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="6709a-155">Hesaplama seçeneğinin ayarlanması, ürünün maliyet hesaplaması çalıştırıldığında ürünün dahil edilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6709a-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="6709a-156">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6709a-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="6709a-157">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-157">Select the Set check box.</span></span>
15. <span data-ttu-id="6709a-158">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6709a-159">Miktar alanı, bu ürünün ne kadarının yapılandırılan üründe tüketileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="6709a-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="6709a-160">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6709a-160">Select the Set check box.</span></span>
17. <span data-ttu-id="6709a-161">Seri başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="6709a-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="6709a-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6709a-162">Click OK.</span></span>

