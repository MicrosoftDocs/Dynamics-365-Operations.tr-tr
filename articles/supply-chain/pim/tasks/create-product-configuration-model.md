---
title: Ürün yapılandırma modeli oluşturma
description: Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921377"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="1a1f7-103">Ürün yapılandırma modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a1f7-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a1f7-104">Bu yordam, bir ürün yapılandırma modelinin nasıl oluşturulacağını ve öznitelikler ve alt bileşenler gibi temel bilgilerin nasıl girileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="1a1f7-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="1a1f7-106">Ürün modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a1f7-106">Create a product model</span></span>

1. <span data-ttu-id="1a1f7-107">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="1a1f7-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-108">Select **New**.</span></span>
1. <span data-ttu-id="1a1f7-109">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="1a1f7-110">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="1a1f7-111">**Çözüm stratejisi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="1a1f7-112">Çözüm stratejisi, kısıtlama tabanlı bir ürün yapılandırması modelindeki kısıtlamaların nasıl işleme koyulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="1a1f7-113">Bu seçimin ürün yapılandırma modelinin performansı üzerinde etkisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="1a1f7-114">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="1a1f7-115">Kök bileşen, ürün yapılandırması modelini temsil eder ve diğer ürün modellerinde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="1a1f7-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-116">Select **OK**.</span></span>
1. <span data-ttu-id="1a1f7-117">**Yeniden kullanma yapılandırması** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="1a1f7-118">Yapılandırmaları yeniden kullanma parametresi Evet olarak ayarlanırsa, sistem her bir yapılandırma oturumunun ardından eşdeğer yapılandırmaları denetler ve tam bir eşleşme bulunursa onları yeniden kullanır.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="1a1f7-119">Öznitelikler ekle</span><span class="sxs-lookup"><span data-stu-id="1a1f7-119">Add attributes</span></span>

1. <span data-ttu-id="1a1f7-120">**Öznitelikler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="1a1f7-121">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-121">Select **Add**.</span></span>
3. <span data-ttu-id="1a1f7-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1a1f7-123">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1a1f7-124">**Çözücü adı** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="1a1f7-125">Çözücü adı, ürün yapılandırıcının çözücüsü tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="1a1f7-126">Boşluk veya _ (alt çizgi) dışında özel karakterler içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="1a1f7-127">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="1a1f7-128">Açıklama metni yapılandırma kullanıcısı tarafından görülür ve dolayısıyla doğru öznitelik değerinin seçilmesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="1a1f7-129">**Öznitelik türü** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="1a1f7-130">Öznitelik türü, hangi değerlerin öznitelik için kullanılabilir olduğunu belirler.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="1a1f7-131">**Yeniden kullanıma dahil et** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="1a1f7-132">Bu seçenek yalnızca Yapılandırmaları yeniden kullanma seçeneği belirlendiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="1a1f7-133">Yeniden kullan onay kutusunda öznitelik eklenmesi, bu özniteliğin sistem tam bir eşleşme aradığında göz önüne alınacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="1a1f7-134">Alt bileşenler ekleme</span><span class="sxs-lookup"><span data-stu-id="1a1f7-134">Add subcomponents</span></span>

1. <span data-ttu-id="1a1f7-135">**Alt bileşenler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="1a1f7-136">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-136">Select **Add**.</span></span>
3. <span data-ttu-id="1a1f7-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1a1f7-138">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1a1f7-139">**Çözücü adı** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="1a1f7-140">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="1a1f7-141">**Bileşen** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="1a1f7-142">Her alt bileşen bir bileşen tanımına başvurmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="1a1f7-143">Bu tasarım, yeniden kullanılabilir bileşenleri destekler ve bir bileşenin bir kere tanımlandıktan sonra birçok ürün modelinde kullanılabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="1a1f7-144">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-144">Select **Save**.</span></span>
9. <span data-ttu-id="1a1f7-145">**Ürün reçetesi satırı ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="1a1f7-146">Ürün reçetesi satırı ayrıntıları, kullanıcının alt bileşen için gerekli özellikleri seçmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="1a1f7-147">Her özellik sabit bir değer verebilir veya bir özniteliğine eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="1a1f7-148">Bir özniteliği eşleştirme, ürün reçetesi satır özelliğinin yapılandırma seçimine bağlı olarak farklı değerler almasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="1a1f7-149">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="1a1f7-150">Her alt bileşen, kısıtlama tabanlı yapılandırma teknolojisine sahip yapılandırılabilir bir ana ürünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="1a1f7-151">Referans, ürün numarası üzerinden verilir.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="1a1f7-152">**Ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="1a1f7-153">**Hesaplama** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="1a1f7-154">Hesaplama seçeneğinin ayarlanması, ürünün maliyet hesaplaması çalıştırıldığında ürünün dahil edilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="1a1f7-155">**Kurulum** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="1a1f7-156">**Ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="1a1f7-157">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="1a1f7-158">Miktar alanı, bu ürünün ne kadarının yapılandırılan üründe tüketileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="1a1f7-159">**Ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="1a1f7-160">**Seri başına** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="1a1f7-161">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1a1f7-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]