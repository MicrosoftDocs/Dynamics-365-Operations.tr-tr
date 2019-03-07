---
title: Ürün yapılandırma modeli oluşturma
description: Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3d19c680e14fe4074314a95937d30d4ad2c7a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "315878"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="c5d74-103">Ürün yapılandırma modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5d74-103">Create a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5d74-104">Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="c5d74-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="c5d74-106">Ürün modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5d74-106">Create a product model</span></span>
1. <span data-ttu-id="c5d74-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c5d74-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="c5d74-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-109">Click New.</span></span>
4. <span data-ttu-id="c5d74-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c5d74-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c5d74-112">Çözüm stratejisi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="c5d74-113">Çözüm stratejisi, kısıtlama tabanlı bir ürün yapılandırması modelindeki kısıtlamaların nasıl işleme koyulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="c5d74-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="c5d74-114">Bu seçimin ürün yapılandırma modelinin performansı üzerinde etkisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="c5d74-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c5d74-116">Kök bileşen, ürün yapılandırması modelini temsil eder ve diğer ürün modellerinde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="c5d74-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-117">Click OK.</span></span>
9. <span data-ttu-id="c5d74-118">Yeniden kullanma yapılandırması alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="c5d74-119">Yapılandırmaları yeniden kullanma parametresi Evet olarak ayarlanırsa, sistem her bir yapılandırma oturumunun ardından eşdeğer yapılandırmaları denetler ve tam bir eşleşme bulunursa onları yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5d74-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="c5d74-120">Öznitelikler ekle</span><span class="sxs-lookup"><span data-stu-id="c5d74-120">Add attributes</span></span>
1. <span data-ttu-id="c5d74-121">Öznitelikler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="c5d74-122">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-122">Click Add.</span></span>
3. <span data-ttu-id="c5d74-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c5d74-124">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c5d74-125">Çözücü adı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="c5d74-126">Çözücü adı, ürün yapılandırıcının çözücüsü tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c5d74-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="c5d74-127">Boşluk veya _ (alt çizgi) dışında özel karakterler içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="c5d74-128">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c5d74-129">Açıklama metni yapılandırma kullanıcısı tarafından görülür ve dolayısıyla doğru öznitelik değerinin seçilmesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="c5d74-130">Öznitelik türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="c5d74-131">Öznitelik türü, hangi değerlerin öznitelik için kullanılabilir olduğunu belirler.</span><span class="sxs-lookup"><span data-stu-id="c5d74-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="c5d74-132">Yeniden kullanıma dahil et onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="c5d74-133">Bu seçenek yalnızca Yapılandırmaları yeniden kullanma seçeneği belirlendiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="c5d74-134">Yeniden kullan onay kutusunda öznitelik eklenmesi, bu özniteliğin sistem tam bir eşleşme aradığında göz önüne alınacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="c5d74-135">Alt bileşenler ekleme</span><span class="sxs-lookup"><span data-stu-id="c5d74-135">Add subcomponents</span></span>
1. <span data-ttu-id="c5d74-136">Alt bileşenler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="c5d74-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-137">Click Add.</span></span>
3. <span data-ttu-id="c5d74-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="c5d74-139">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c5d74-140">Çözücü adı alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="c5d74-141">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="c5d74-142">Bileşen alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="c5d74-143">Her alt bileşen bir bileşen tanımına başvurmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c5d74-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="c5d74-144">Bu tasarım, yeniden kullanılabilir bileşenleri destekler ve bir bileşenin bir kere tanımlandıktan sonra birçok ürün modelinde kullanılabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5d74-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="c5d74-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-145">Click Save.</span></span>
9. <span data-ttu-id="c5d74-146">Ürün reçetesi satır ayrıntılarını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-146">Click BOM line details.</span></span>
    * <span data-ttu-id="c5d74-147">Ürün reçetesi satırı ayrıntıları, kullanıcının alt bileşen için gerekli özellikleri seçmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5d74-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="c5d74-148">Her özellik sabit bir değer verebilir veya bir özniteliğine eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="c5d74-149">Bir özniteliği eşleştirme, ürün reçetesi satır özelliğinin yapılandırma seçimine bağlı olarak farklı değerler almasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="c5d74-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="c5d74-150">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c5d74-151">Her alt bileşen, kısıtlama tabanlı yapılandırma teknolojisine sahip yapılandırılabilir bir ana ürünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c5d74-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="c5d74-152">Referans, ürün numarası üzerinden verilir.</span><span class="sxs-lookup"><span data-stu-id="c5d74-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="c5d74-153">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-153">Select the Set check box.</span></span>
12. <span data-ttu-id="c5d74-154">Hesaplama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="c5d74-155">Hesaplama seçeneğinin ayarlanması, ürünün maliyet hesaplaması çalıştırıldığında ürünün dahil edilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5d74-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="c5d74-156">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="c5d74-157">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-157">Select the Set check box.</span></span>
15. <span data-ttu-id="c5d74-158">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c5d74-159">Miktar alanı, bu ürünün ne kadarının yapılandırılan üründe tüketileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="c5d74-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="c5d74-160">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-160">Select the Set check box.</span></span>
17. <span data-ttu-id="c5d74-161">Seri başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c5d74-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="c5d74-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c5d74-162">Click OK.</span></span>

