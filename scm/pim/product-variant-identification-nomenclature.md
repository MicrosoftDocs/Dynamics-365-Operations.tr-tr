---
title: "Ürün çeşidi numaraları ve adlarının terminolojisi"
description: "Bu konu, ürün numaraları terminolojisini, sabit [Ana ürün numarası - Yapılandırma - Ebat - Renk - Stil] biçimini değiştirmek için nasıl ayarlayabileceğinizi açıklar. Yeni terminoloji, ana ürün numarası, etkin ürün boyutları ve tercihiniz olan metin ayırıcılarını içeren hedeflenmiş bir biçime sahiptir. Ürün adları için bir terminoloji de oluşturabilirsiniz. Son olarak, kısıtlama tabanlı ürün yapılandırıcısı ile oluşturulan yapılandırmaları belirlemek için bir terminoloji oluşturabilirsiniz. Bu terminolojiler istediğiniz öznitelikleri içerebilir."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="cb0ee-107">Ürün çeşidi numaraları ve adlarının terminolojisi</span><span class="sxs-lookup"><span data-stu-id="cb0ee-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="cb0ee-108">Bu konu, ürün numaraları terminolojisini, sabit [Ana ürün numarası - Yapılandırma - Ebat - Renk - Stil] biçimini değiştirmek için nasıl ayarlayabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="cb0ee-109">Yeni terminoloji, ana ürün numarası, etkin ürün boyutları ve tercihiniz olan metin ayırıcılarını içeren hedeflenmiş bir biçime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="cb0ee-110">Ürün adları için bir terminoloji de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="cb0ee-111">Son olarak, kısıtlama tabanlı ürün yapılandırıcısı ile oluşturulan yapılandırmaları belirlemek için bir terminoloji oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="cb0ee-112">Bu terminolojiler istediğiniz öznitelikleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="cb0ee-113">Ürün çeşidi numaraları ve ürün çeşit adları için yeni terminoloji, ürün çeşitleri için kimlik tanımlayıcıları içerisinde bölümler dahil etmenize de izin verir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="cb0ee-114">Bu bölümler, ana ürün numarası ve adı, ürün boyut kimlikleri ve adları, numara serileri, sabit metinler ve öznitelikleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="cb0ee-115">Bu işlev, bir satış siparişi veya bir satınalma siparişi oluşturduğunuzda belirli bir ürün çeşidini hızlı bir şekilde bulmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="cb0ee-116">**Ürün terminolojisi** sayfasını kullanarak hem ürün çeşit numaraları hem de ürün çeşit adları için terminolojiler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="cb0ee-117">Bu sayfayı açmak için **Ürün bilgi yönetimi** &gt; **Kurulum** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="cb0ee-118">Önceden tanımlanmış ürün çeşitleri terminolojisi</span><span class="sxs-lookup"><span data-stu-id="cb0ee-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="cb0ee-119">Ürün çeşitleri, ana ürünler için üç yapılandırma teknolojisinden birine göre oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="cb0ee-120">Önceden tanımlanmış çeşitler</span><span class="sxs-lookup"><span data-stu-id="cb0ee-120">Predefined variants</span></span>
-   <span data-ttu-id="cb0ee-121">Kısıtlama tabanlı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-121">Constraint-based</span></span>
-   <span data-ttu-id="cb0ee-122">Boyut tabanlı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-122">Dimension-based</span></span>

<span data-ttu-id="cb0ee-123">Her ürün çeşidinin bir numarası ve adı vardır ve ürün çeşidi kimlik saptama terminolojileri, her ürün çeşidi numarasının veya adının dahil olacağı segmentleri seçmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="cb0ee-124">**Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="cb0ee-125">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="cb0ee-125">Product master number</span></span>
-   <span data-ttu-id="cb0ee-126">Ana ürün adı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-126">Product master name</span></span>
-   <span data-ttu-id="cb0ee-127">Numara serisi değeri</span><span class="sxs-lookup"><span data-stu-id="cb0ee-127">Number sequence value</span></span>
-   <span data-ttu-id="cb0ee-128">Metin sabiti</span><span class="sxs-lookup"><span data-stu-id="cb0ee-128">Text constant</span></span>
-   <span data-ttu-id="cb0ee-129">Ürün boyutları</span><span class="sxs-lookup"><span data-stu-id="cb0ee-129">Product dimensions</span></span>
    -   <span data-ttu-id="cb0ee-130">Yapılandırma kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="cb0ee-131">Renk kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-131">Color ID or name</span></span>
    -   <span data-ttu-id="cb0ee-132">Beden kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-132">Size ID or name</span></span>
    -   <span data-ttu-id="cb0ee-133">Stil kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="cb0ee-133">Style ID or name</span></span>

<span data-ttu-id="cb0ee-134">Bir ürün çeşidi kimlik saptama numarası terminolojisini tanımladıktan sonra, bunu bir ürün boyutu grubu ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="cb0ee-135">Bu ürün boyutu grubuna başvuran tüm ana ürünlere daha sonra, terminolojiye uygun olarak bir ürün çeşidi numarası atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="cb0ee-136">Ancak, ürün çeşidi adı terminolojileri, ürün boyut grupları ile ilişkilendirilemez.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="cb0ee-137">Ayrıca bir ürün çeşidini kimlik saptama terminolojisini doğrudan ana ürüne de atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="cb0ee-138">Bu durumda, ana ürüne ait ürün çeşitlerine ürün çeşidi numaraları ve adları, terminolojilere uygun bir biçimde atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="cb0ee-139">Örnek</span><span class="sxs-lookup"><span data-stu-id="cb0ee-139">Example</span></span>

<span data-ttu-id="cb0ee-140">Bir tişört (TS1234), üç bedende (S, M, L), dört renkte (Kırmızı, Yeşil, Mavi, Sarı) ve iki stilde (Polo, V yaka) üretilmektedir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="cb0ee-141">Bu nedenle, 24 ürün çeşidi mümkündür (= 3 x 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="cb0ee-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="cb0ee-142">Aşağıdaki bölümlere sahip bir ürün çeşidi numarası terminolojisi oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-143">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="cb0ee-143">Product master number</span></span>
2.  <span data-ttu-id="cb0ee-144">Metin sabiti: "-"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="cb0ee-145">Renk</span><span class="sxs-lookup"><span data-stu-id="cb0ee-145">Color</span></span>
4.  <span data-ttu-id="cb0ee-146">Metin sabiti: "-"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="cb0ee-147">Ebat</span><span class="sxs-lookup"><span data-stu-id="cb0ee-147">Size</span></span>
6.  <span data-ttu-id="cb0ee-148">Metin sabiti: "-"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="cb0ee-149">Stil</span><span class="sxs-lookup"><span data-stu-id="cb0ee-149">Style</span></span>

<span data-ttu-id="cb0ee-150">Bu durumda, kırmızı, small bir polo tişört için ürün çeşidi numarası TS1234-Kırmızı-Small-Polo olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="cb0ee-151">Kısıtlama tabanlı yapılandırma terminolojisi</span><span class="sxs-lookup"><span data-stu-id="cb0ee-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="cb0ee-152">Kısıtlama tabanlı yapılandırmalar için yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="cb0ee-153">**Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="cb0ee-154">Numara serisi değeri</span><span class="sxs-lookup"><span data-stu-id="cb0ee-154">Number sequence value</span></span>
-   <span data-ttu-id="cb0ee-155">Metin sabiti</span><span class="sxs-lookup"><span data-stu-id="cb0ee-155">Text constant</span></span>
-   <span data-ttu-id="cb0ee-156">Öznitelik değeri</span><span class="sxs-lookup"><span data-stu-id="cb0ee-156">Attribute value</span></span>

<span data-ttu-id="cb0ee-157">Ürün yapılandırma modelindeki her bileşenin kendi yapılandırma terminolojisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="cb0ee-158">Yalnızca bileşene ait olan öznitelikler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="cb0ee-159">Alt bileşenlerden gelen öznitelikler veya kullanıcı gereksinimleri kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="cb0ee-160">Örnek</span><span class="sxs-lookup"><span data-stu-id="cb0ee-160">Example</span></span>

<span data-ttu-id="cb0ee-161">Bir ürün yapılandırma modeli, iki özniteliğe sahip bir kök bileşene sahiptir:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="cb0ee-162">Malzeme (Plastik, Ahşap, Çelik)</span><span class="sxs-lookup"><span data-stu-id="cb0ee-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="cb0ee-163">Uzunluk (10...100)</span><span class="sxs-lookup"><span data-stu-id="cb0ee-163">Length (10...100)</span></span>

<span data-ttu-id="cb0ee-164">Aşağıdaki bölümlere sahip bir yapılandırma terminolojisi oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-165">Öznitelik değeri: Malzeme</span><span class="sxs-lookup"><span data-stu-id="cb0ee-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="cb0ee-166">Metin sabiti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="cb0ee-167">Öznitelik değeri: Uzunluk</span><span class="sxs-lookup"><span data-stu-id="cb0ee-167">Attribute value: Length</span></span>

<span data-ttu-id="cb0ee-168">Bu durumda, 78 uzunluğuna sahip ahşap malzeme için yapılandırma kodu WoodAAA78 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="cb0ee-169">Boyut tabanlı yapılandırmaların terminolojisi</span><span class="sxs-lookup"><span data-stu-id="cb0ee-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="cb0ee-170">Boyut tabanlı yapılandırmalar için yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="cb0ee-171">**Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="cb0ee-172">Numara serisi değeri</span><span class="sxs-lookup"><span data-stu-id="cb0ee-172">Number sequence value</span></span>
-   <span data-ttu-id="cb0ee-173">Metin sabiti</span><span class="sxs-lookup"><span data-stu-id="cb0ee-173">Text constant</span></span>
-   <span data-ttu-id="cb0ee-174">Konfigürasyon grubu maddesi</span><span class="sxs-lookup"><span data-stu-id="cb0ee-174">Configuration group item</span></span>

<span data-ttu-id="cb0ee-175">Ürün reçetesi (BOM) için bir yapılandırma terminolojisi oluşturulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="cb0ee-176">Örnek</span><span class="sxs-lookup"><span data-stu-id="cb0ee-176">Example</span></span>

<span data-ttu-id="cb0ee-177">Bir ürün reçetesi, iki farklı yapılandırma grubuna ayrılmış dört ürün reçetesi satırına sahiptir:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="cb0ee-178">Ürün reçetesi satırı: M0007, Standart dolap</span><span class="sxs-lookup"><span data-stu-id="cb0ee-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="cb0ee-179">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="cb0ee-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="cb0ee-180">Ürün reçetesi satırı: M0008, Son teknolojili dolap</span><span class="sxs-lookup"><span data-stu-id="cb0ee-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="cb0ee-181">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="cb0ee-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="cb0ee-182">Ürün reçetesi satırı: M0021, Ön ızgara dokuması</span><span class="sxs-lookup"><span data-stu-id="cb0ee-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="cb0ee-183">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="cb0ee-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="cb0ee-184">Ürün reçetesi satırı: M0022, Ön ızgara metali</span><span class="sxs-lookup"><span data-stu-id="cb0ee-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="cb0ee-185">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="cb0ee-185">Configuration group: Front grill</span></span>

<span data-ttu-id="cb0ee-186">Aşağıdaki bölümlere sahip bir yapılandırma terminolojisi oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-187">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="cb0ee-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="cb0ee-188">Metin sabiti: "&"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="cb0ee-189">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="cb0ee-189">Configuration group: Front grill</span></span>

<span data-ttu-id="cb0ee-190">Bu durumda, ön ızgara dokumasına sahip standart bir dolap için yapılandırma kodu M0007&M0021 olur.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="cb0ee-191">Ürün çeşitlerinin ve yapılandırmalarının birleşimi için terminoloji</span><span class="sxs-lookup"><span data-stu-id="cb0ee-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="cb0ee-192">Kısıtlama tabanlı yapılandırma teknolojisi ya da boyut tabanlı yapılandırma teknolojisini, bir ana ürün için ürün çeşitlerini yapılandırmakta kullandığınızda, ürün çeşidi için ürün çeşidi numaraları, yapılandırma boyutundaki terminolojiyi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="cb0ee-193">Çeşitleri yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="cb0ee-194">**Ürün terminolojisi** sayfası üzerinde, yapılandırma boyutunu içeren bir ürün çeşidi numarası terminolojisi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="cb0ee-195">Terminolojiyi, yapılandırma boyutuna sahip bir boyut grubuna atayın.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="cb0ee-196">Ürün çeşitlerini yapılandırma amacıyla kullanılacak bileşenler veya ürün reçeteleri için bir yapılandırma terminolojisi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="cb0ee-197">Ürün çeşidi adları için terminolojiler de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="cb0ee-198">Ürün çeşidi adları, yapılandırma kodunu veya adını içermek üzere de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="cb0ee-199">Kısıtlama tabanlı yapılandırmalar için örnek</span><span class="sxs-lookup"><span data-stu-id="cb0ee-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="cb0ee-200">Bu örnek için aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-201">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="cb0ee-201">Product master number</span></span>
2.  <span data-ttu-id="cb0ee-202">Metin sabiti "\_"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="cb0ee-203">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cb0ee-203">Configuration</span></span>

<span data-ttu-id="cb0ee-204">Yapılandırma terminolojisi aşağıdaki segmentlerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-205">Öznitelik değeri: Malzeme</span><span class="sxs-lookup"><span data-stu-id="cb0ee-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="cb0ee-206">Metin sabiti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="cb0ee-207">Öznitelik değeri: Uzunluk</span><span class="sxs-lookup"><span data-stu-id="cb0ee-207">Attribute value: Length</span></span>

<span data-ttu-id="cb0ee-208">Segmentler için aşağıdaki değerleri girersiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="cb0ee-209">Ürün ana numarası = **M0099**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="cb0ee-210">Malzeme = **Plastik**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="cb0ee-211">Uzunluk = **12**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-211">Length = **12**</span></span>

<span data-ttu-id="cb0ee-212">Bu durumda, ürün çeşidi numarası M0099\_PlastikAAA12 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="cb0ee-213">Boyut tabanlı yapılandırmalar için örnek</span><span class="sxs-lookup"><span data-stu-id="cb0ee-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="cb0ee-214">Bu örnek için aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-215">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="cb0ee-215">Product master number</span></span>
2.  <span data-ttu-id="cb0ee-216">Metin sabiti "//"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-216">Text constant "//"</span></span>
3.  <span data-ttu-id="cb0ee-217">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cb0ee-217">Configuration</span></span>

<span data-ttu-id="cb0ee-218">Yapılandırma terminolojisi aşağıdaki segmentlerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="cb0ee-219">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="cb0ee-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="cb0ee-220">Metin sabiti: "&"</span><span class="sxs-lookup"><span data-stu-id="cb0ee-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="cb0ee-221">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="cb0ee-221">Configuration group: Front grill</span></span>

<span data-ttu-id="cb0ee-222">Segmentler için aşağıdaki değerleri girersiniz:</span><span class="sxs-lookup"><span data-stu-id="cb0ee-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="cb0ee-223">Ürün ana numarası = **D0123**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="cb0ee-224">Dolap = **M0008**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="cb0ee-225">Ön ızgara = **M0022**</span><span class="sxs-lookup"><span data-stu-id="cb0ee-225">Front grill = **M0022**</span></span>

<span data-ttu-id="cb0ee-226">Bu durumda, ürün çeşidi numarası D0123//M0008&M0022 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="cb0ee-227">Çakışmaları numaralandırma</span><span class="sxs-lookup"><span data-stu-id="cb0ee-227">Numbering conflicts</span></span>
<span data-ttu-id="cb0ee-228">Bazı durumlarda, ayarladığınız bir ürün çeşidi numarası terminolojisi, benzersiz ürün çeşidi numaraları oluşturmayabilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="cb0ee-229">Örneğin etkin bir ürün boyutu, önceden tanımlı çeşit yapılandırma teknolojisini kullanan bir ana ürün terminolojisine dahil edilmezse ürün çeşidi numaraları benzersiz olmaz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="cb0ee-230">Bu çakışmayı nasıl çözeceğiniz, yapılandırma teknolojisine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="cb0ee-231">Önceden tanımlanmış çeşitler</span><span class="sxs-lookup"><span data-stu-id="cb0ee-231">Predefined variants</span></span>

<span data-ttu-id="cb0ee-232">Ürün çeşitlerini el ile oluşturmaya çalıştığınızda veya otomatik ürün çeşitleri oluşturduğunuzda bir hata ortaya çıkar ve birden fazla ürün çeşidi aynı ürün çeşidi numarasına sahip olur.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="cb0ee-233">Bu durumun önüne geçmek için tüm etkin ürün boyutlarını ürün boyutu grubunda kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="cb0ee-234">Alternatif olarak, ürün çeşit numarasının benzersiz olduğunu garanti etmeye yardımcı olmak için bir numara serisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="cb0ee-235">Kısıtlama tabanlı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="cb0ee-235">Constraint-based configurations</span></span>

<span data-ttu-id="cb0ee-236">Terminolojiye bağlı olarak, sistem, yapılandırmaya benzersiz olmayan bir ürün numarası atama denemesinde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="cb0ee-237">Bu durumda, sitem yapılandırma boyutu için numara serisini ürün numarası olarak kullanır ve bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="cb0ee-238">Bu durumu engellemek için benzersiz ürün çeşidi numaralarını garanti etmeye yardımcı olmak için terminolojide yeterli sayıda öznitelik dahil etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="cb0ee-239">Ayrıca **Yeniden kullan** seçeneğinin bileşen için açık olduğundan emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="cb0ee-240">Boyut tabanlı yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="cb0ee-240">Dimension-based configurations</span></span>

<span data-ttu-id="cb0ee-241">Yapılandırma işleminin bir adımında, sistem terminolojiye göre bir yapılandırma değeri önerir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="cb0ee-242">Bu adımda, yapılandırma değerini el ile değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="cb0ee-243">Yapılandırmayı kaydettiğinizde sistem, yapılandırma değerinin benzersiz olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="cb0ee-244">Girmiş olduğunuz değer benzersiz değilse, bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="cb0ee-245">Yapılandırmayı kaydetmek için, benzersiz bir yapılandırma değeri girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="cb0ee-246">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="cb0ee-246">See also</span></span>
--------

[<span data-ttu-id="cb0ee-247">Önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb0ee-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="cb0ee-248">Yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="cb0ee-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


