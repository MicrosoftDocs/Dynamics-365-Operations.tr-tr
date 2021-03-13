---
title: Ürün çeşidi numaraları ve adlarının terminolojisi
description: Bu konu, ürün numaraları terminolojisini, sabit [Ana ürün numarası - Yapılandırma - Ebat - Renk - Stil] biçimini değiştirmek için nasıl ayarlayabileceğinizi açıklar.
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f17f9e1401c68c11e23f327d96028663470b3245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011334"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="12604-103">Ürün çeşidi numaraları ve adlarının terminolojisi</span><span class="sxs-lookup"><span data-stu-id="12604-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12604-104">Bu konu, ürün numaraları terminolojisini, sabit [Ana ürün numarası - Yapılandırma - Ebat - Renk - Stil] biçimini değiştirmek için nasıl ayarlayabileceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="12604-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="12604-105">Yeni terminoloji, ana ürün numarası, etkin ürün boyutları ve tercihiniz olan metin ayırıcılarını içeren hedeflenmiş bir biçime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="12604-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="12604-106">Ürün adları için bir terminoloji de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="12604-107">Son olarak, kısıtlama tabanlı ürün yapılandırıcısı ile oluşturulan yapılandırmaları belirlemek için bir terminoloji oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="12604-108">Bu terminolojiler istediğiniz öznitelikleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="12604-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="12604-109">Ürün çeşidi numaraları ve ürün çeşit adları için yeni terminoloji, ürün çeşitleri için kimlik tanımlayıcıları içerisinde bölümler dahil etmenize de izin verir.</span><span class="sxs-lookup"><span data-stu-id="12604-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="12604-110">Bu bölümler, ana ürün numarası ve adı, ürün boyut kimlikleri ve adları, numara serileri, sabit metinler ve öznitelikleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="12604-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="12604-111">Bu işlev, bir satış siparişi veya bir satınalma siparişi oluşturduğunuzda belirli bir ürün çeşidini hızlı bir şekilde bulmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="12604-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="12604-112">**Ürün terminolojisi** sayfasını kullanarak hem ürün çeşit numaraları hem de ürün çeşit adları için terminolojiler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="12604-113">Bu sayfayı açmak için **Ürün bilgi yönetimi** &gt; **Kurulum** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="12604-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="12604-114">Önceden tanımlanmış ürün çeşitleri terminolojisi</span><span class="sxs-lookup"><span data-stu-id="12604-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="12604-115">Ürün çeşitleri, ana ürünler için üç yapılandırma teknolojisinden birine göre oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="12604-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="12604-116">Önceden tanımlanmış çeşitler</span><span class="sxs-lookup"><span data-stu-id="12604-116">Predefined variants</span></span>
-   <span data-ttu-id="12604-117">Kısıtlama tabanlı</span><span class="sxs-lookup"><span data-stu-id="12604-117">Constraint-based</span></span>
-   <span data-ttu-id="12604-118">Boyut tabanlı</span><span class="sxs-lookup"><span data-stu-id="12604-118">Dimension-based</span></span>

<span data-ttu-id="12604-119">Her ürün çeşidinin bir numarası ve adı vardır ve ürün çeşidi kimlik saptama terminolojileri, her ürün çeşidi numarasının veya adının dahil olacağı segmentleri seçmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="12604-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="12604-120">**Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="12604-121">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="12604-121">Product master number</span></span>
-   <span data-ttu-id="12604-122">Ana ürün adı</span><span class="sxs-lookup"><span data-stu-id="12604-122">Product master name</span></span>
-   <span data-ttu-id="12604-123">Numara serisi değeri</span><span class="sxs-lookup"><span data-stu-id="12604-123">Number sequence value</span></span>
-   <span data-ttu-id="12604-124">Metin sabiti</span><span class="sxs-lookup"><span data-stu-id="12604-124">Text constant</span></span>
-   <span data-ttu-id="12604-125">Ürün boyutları</span><span class="sxs-lookup"><span data-stu-id="12604-125">Product dimensions</span></span>
    -   <span data-ttu-id="12604-126">Yapılandırma kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="12604-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="12604-127">Renk kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="12604-127">Color ID or name</span></span>
    -   <span data-ttu-id="12604-128">Beden kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="12604-128">Size ID or name</span></span>
    -   <span data-ttu-id="12604-129">Stil kodu veya adı</span><span class="sxs-lookup"><span data-stu-id="12604-129">Style ID or name</span></span>

<span data-ttu-id="12604-130">Bir ürün çeşidi kimlik saptama numarası terminolojisini tanımladıktan sonra, bunu bir ürün boyutu grubu ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="12604-131">Bu ürün boyutu grubuna başvuran tüm ana ürünlere daha sonra, terminolojiye uygun olarak bir ürün çeşidi numarası atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="12604-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="12604-132">Ancak, ürün çeşidi adı terminolojileri, ürün boyut grupları ile ilişkilendirilemez.</span><span class="sxs-lookup"><span data-stu-id="12604-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="12604-133">Ayrıca bir ürün çeşidini kimlik saptama terminolojisini doğrudan ana ürüne de atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="12604-134">Bu durumda, ana ürüne ait ürün çeşitlerine ürün çeşidi numaraları ve adları, terminolojilere uygun bir biçimde atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="12604-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="12604-135">Örnek</span><span class="sxs-lookup"><span data-stu-id="12604-135">Example</span></span>

<span data-ttu-id="12604-136">Bir tişört (TS1234), üç bedende (S, M, L), dört renkte (Kırmızı, Yeşil, Mavi, Sarı) ve iki stilde (Polo, V yaka) üretilmektedir.</span><span class="sxs-lookup"><span data-stu-id="12604-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="12604-137">Bu nedenle, 24 ürün çeşidi mümkündür (= 3 x 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="12604-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="12604-138">Aşağıdaki bölümlere sahip bir ürün çeşidi numarası terminolojisi oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="12604-139">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="12604-139">Product master number</span></span>
2.  <span data-ttu-id="12604-140">Metin sabiti: "-"</span><span class="sxs-lookup"><span data-stu-id="12604-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="12604-141">Renk</span><span class="sxs-lookup"><span data-stu-id="12604-141">Color</span></span>
4.  <span data-ttu-id="12604-142">Metin sabiti: "-"</span><span class="sxs-lookup"><span data-stu-id="12604-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="12604-143">Ebat</span><span class="sxs-lookup"><span data-stu-id="12604-143">Size</span></span>
6.  <span data-ttu-id="12604-144">Metin sabiti: "-"</span><span class="sxs-lookup"><span data-stu-id="12604-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="12604-145">Stil</span><span class="sxs-lookup"><span data-stu-id="12604-145">Style</span></span>

<span data-ttu-id="12604-146">Bu durumda, kırmızı, small bir polo tişört için ürün çeşidi numarası TS1234-Kırmızı-Small-Polo olacaktır.</span><span class="sxs-lookup"><span data-stu-id="12604-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="12604-147">Kısıtlama tabanlı yapılandırma terminolojisi</span><span class="sxs-lookup"><span data-stu-id="12604-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="12604-148">Kısıtlama tabanlı yapılandırmalar için yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="12604-149">**Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="12604-150">Numara serisi değeri</span><span class="sxs-lookup"><span data-stu-id="12604-150">Number sequence value</span></span>
-   <span data-ttu-id="12604-151">Metin sabiti</span><span class="sxs-lookup"><span data-stu-id="12604-151">Text constant</span></span>
-   <span data-ttu-id="12604-152">Öznitelik değeri</span><span class="sxs-lookup"><span data-stu-id="12604-152">Attribute value</span></span>

<span data-ttu-id="12604-153">Ürün yapılandırma modelindeki her bileşenin kendi yapılandırma terminolojisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="12604-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="12604-154">Yalnızca bileşene ait olan öznitelikler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="12604-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="12604-155">Alt bileşenlerden gelen öznitelikler veya kullanıcı gereksinimleri kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="12604-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="12604-156">Örnek</span><span class="sxs-lookup"><span data-stu-id="12604-156">Example</span></span>

<span data-ttu-id="12604-157">Bir ürün yapılandırma modeli, iki özniteliğe sahip bir kök bileşene sahiptir:</span><span class="sxs-lookup"><span data-stu-id="12604-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="12604-158">Malzeme (Plastik, Ahşap, Çelik)</span><span class="sxs-lookup"><span data-stu-id="12604-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="12604-159">Uzunluk (10...100)</span><span class="sxs-lookup"><span data-stu-id="12604-159">Length (10...100)</span></span>

<span data-ttu-id="12604-160">Aşağıdaki bölümlere sahip bir yapılandırma terminolojisi oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="12604-161">Öznitelik değeri: Malzeme</span><span class="sxs-lookup"><span data-stu-id="12604-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="12604-162">Metin sabiti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="12604-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="12604-163">Öznitelik değeri: Uzunluk</span><span class="sxs-lookup"><span data-stu-id="12604-163">Attribute value: Length</span></span>

<span data-ttu-id="12604-164">Bu durumda, 78 uzunluğuna sahip ahşap malzeme için yapılandırma kodu WoodAAA78 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="12604-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="12604-165">Boyut tabanlı yapılandırmaların terminolojisi</span><span class="sxs-lookup"><span data-stu-id="12604-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="12604-166">Boyut tabanlı yapılandırmalar için yapılandırma ürün boyutuna yönelik adanmış bir terminoloji oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="12604-167">**Ürün terminolojisi** sayfasında aşağıdaki segmentleri seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="12604-168">Numara serisi değeri</span><span class="sxs-lookup"><span data-stu-id="12604-168">Number sequence value</span></span>
-   <span data-ttu-id="12604-169">Metin sabiti</span><span class="sxs-lookup"><span data-stu-id="12604-169">Text constant</span></span>
-   <span data-ttu-id="12604-170">Konfigürasyon grubu maddesi</span><span class="sxs-lookup"><span data-stu-id="12604-170">Configuration group item</span></span>

<span data-ttu-id="12604-171">Ürün reçetesi (BOM) için bir yapılandırma terminolojisi oluşturulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="12604-172">Örnek</span><span class="sxs-lookup"><span data-stu-id="12604-172">Example</span></span>

<span data-ttu-id="12604-173">Bir ürün reçetesi, iki farklı yapılandırma grubuna ayrılmış dört ürün reçetesi satırına sahiptir:</span><span class="sxs-lookup"><span data-stu-id="12604-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="12604-174">Ürün reçetesi satırı: M0007, Standart dolap</span><span class="sxs-lookup"><span data-stu-id="12604-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="12604-175">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="12604-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="12604-176">Ürün reçetesi satırı: M0008, Son teknolojili dolap</span><span class="sxs-lookup"><span data-stu-id="12604-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="12604-177">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="12604-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="12604-178">Ürün reçetesi satırı: M0021, Ön ızgara dokuması</span><span class="sxs-lookup"><span data-stu-id="12604-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="12604-179">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="12604-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="12604-180">Ürün reçetesi satırı: M0022, Ön ızgara metali</span><span class="sxs-lookup"><span data-stu-id="12604-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="12604-181">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="12604-181">Configuration group: Front grill</span></span>

<span data-ttu-id="12604-182">Aşağıdaki bölümlere sahip bir yapılandırma terminolojisi oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="12604-183">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="12604-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="12604-184">Metin sabiti: "&"</span><span class="sxs-lookup"><span data-stu-id="12604-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="12604-185">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="12604-185">Configuration group: Front grill</span></span>

<span data-ttu-id="12604-186">Bu durumda, ön ızgara dokumasına sahip standart bir dolap için yapılandırma kodu M0007&M0021 olur.</span><span class="sxs-lookup"><span data-stu-id="12604-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="12604-187">Ürün çeşitlerinin ve yapılandırmalarının birleşimi için terminoloji</span><span class="sxs-lookup"><span data-stu-id="12604-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="12604-188">Kısıtlama tabanlı yapılandırma teknolojisi ya da boyut tabanlı yapılandırma teknolojisini, bir ana ürün için ürün çeşitlerini yapılandırmakta kullandığınızda, ürün çeşidi için ürün çeşidi numaraları, yapılandırma boyutundaki terminolojiyi içerebilir.</span><span class="sxs-lookup"><span data-stu-id="12604-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="12604-189">Çeşitleri yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="12604-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="12604-190">**Ürün terminolojisi** sayfası üzerinde, yapılandırma boyutunu içeren bir ürün çeşidi numarası terminolojisi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="12604-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="12604-191">Terminolojiyi, yapılandırma boyutuna sahip bir boyut grubuna atayın.</span><span class="sxs-lookup"><span data-stu-id="12604-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="12604-192">Ürün çeşitlerini yapılandırma amacıyla kullanılacak bileşenler veya ürün reçeteleri için bir yapılandırma terminolojisi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="12604-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="12604-193">Ürün çeşidi adları için terminolojiler de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="12604-194">Ürün çeşidi adları, yapılandırma kodunu veya adını içermek üzere de yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="12604-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="12604-195">Kısıtlama tabanlı yapılandırmalar için örnek</span><span class="sxs-lookup"><span data-stu-id="12604-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="12604-196">Bu örnek için aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="12604-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="12604-197">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="12604-197">Product master number</span></span>
2.  <span data-ttu-id="12604-198">Metin sabiti "\_"</span><span class="sxs-lookup"><span data-stu-id="12604-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="12604-199">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="12604-199">Configuration</span></span>

<span data-ttu-id="12604-200">Yapılandırma terminolojisi aşağıdaki segmentlerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="12604-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="12604-201">Öznitelik değeri: Malzeme</span><span class="sxs-lookup"><span data-stu-id="12604-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="12604-202">Metin sabiti: "AAA"</span><span class="sxs-lookup"><span data-stu-id="12604-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="12604-203">Öznitelik değeri: Uzunluk</span><span class="sxs-lookup"><span data-stu-id="12604-203">Attribute value: Length</span></span>

<span data-ttu-id="12604-204">Segmentler için aşağıdaki değerleri girersiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="12604-205">Ürün ana numarası = **M0099**</span><span class="sxs-lookup"><span data-stu-id="12604-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="12604-206">Malzeme = **Plastik**</span><span class="sxs-lookup"><span data-stu-id="12604-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="12604-207">Uzunluk = **12**</span><span class="sxs-lookup"><span data-stu-id="12604-207">Length = **12**</span></span>

<span data-ttu-id="12604-208">Bu durumda, ürün çeşidi numarası M0099\_PlastikAAA12 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="12604-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="12604-209">Boyut tabanlı yapılandırmalar için örnek</span><span class="sxs-lookup"><span data-stu-id="12604-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="12604-210">Bu örnek için aşağıdaki segmentlerden oluşan bir ürün çeşidi numarası terminolojisi kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="12604-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="12604-211">Ürün ana numarası</span><span class="sxs-lookup"><span data-stu-id="12604-211">Product master number</span></span>
2.  <span data-ttu-id="12604-212">Metin sabiti "//"</span><span class="sxs-lookup"><span data-stu-id="12604-212">Text constant "//"</span></span>
3.  <span data-ttu-id="12604-213">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="12604-213">Configuration</span></span>

<span data-ttu-id="12604-214">Yapılandırma terminolojisi aşağıdaki segmentlerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="12604-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="12604-215">Yapılandırma grubu: Dolap</span><span class="sxs-lookup"><span data-stu-id="12604-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="12604-216">Metin sabiti: "&"</span><span class="sxs-lookup"><span data-stu-id="12604-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="12604-217">Yapılandırma grubu: Ön ızgara</span><span class="sxs-lookup"><span data-stu-id="12604-217">Configuration group: Front grill</span></span>

<span data-ttu-id="12604-218">Segmentler için aşağıdaki değerleri girersiniz:</span><span class="sxs-lookup"><span data-stu-id="12604-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="12604-219">Ürün ana numarası = **D0123**</span><span class="sxs-lookup"><span data-stu-id="12604-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="12604-220">Dolap = **M0008**</span><span class="sxs-lookup"><span data-stu-id="12604-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="12604-221">Ön ızgara = **M0022**</span><span class="sxs-lookup"><span data-stu-id="12604-221">Front grill = **M0022**</span></span>

<span data-ttu-id="12604-222">Bu durumda, ürün çeşidi numarası D0123//M0008&M0022 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="12604-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="12604-223">Çakışmaları numaralandırma</span><span class="sxs-lookup"><span data-stu-id="12604-223">Numbering conflicts</span></span>
<span data-ttu-id="12604-224">Bazı durumlarda, ayarladığınız bir ürün çeşidi numarası terminolojisi, benzersiz ürün çeşidi numaraları oluşturmayabilir.</span><span class="sxs-lookup"><span data-stu-id="12604-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="12604-225">Örneğin etkin bir ürün boyutu, önceden tanımlı çeşit yapılandırma teknolojisini kullanan bir ana ürün terminolojisine dahil edilmezse ürün çeşidi numaraları benzersiz olmaz.</span><span class="sxs-lookup"><span data-stu-id="12604-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="12604-226">Bu çakışmayı nasıl çözeceğiniz, yapılandırma teknolojisine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="12604-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="12604-227">Önceden tanımlanmış çeşitler</span><span class="sxs-lookup"><span data-stu-id="12604-227">Predefined variants</span></span>

<span data-ttu-id="12604-228">Ürün çeşitlerini el ile oluşturmaya çalıştığınızda veya otomatik ürün çeşitleri oluşturduğunuzda bir hata ortaya çıkar ve birden fazla ürün çeşidi aynı ürün çeşidi numarasına sahip olur.</span><span class="sxs-lookup"><span data-stu-id="12604-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="12604-229">Bu durumun önüne geçmek için tüm etkin ürün boyutlarını ürün boyutu grubunda kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="12604-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="12604-230">Alternatif olarak, ürün çeşit numarasının benzersiz olduğunu garanti etmeye yardımcı olmak için bir numara serisi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="12604-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="12604-231">Kısıtlama tabanlı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="12604-231">Constraint-based configurations</span></span>

<span data-ttu-id="12604-232">Terminolojiye bağlı olarak, sistem, yapılandırmaya benzersiz olmayan bir ürün numarası atama denemesinde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="12604-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="12604-233">Bu durumda, sitem yapılandırma boyutu için numara serisini ürün numarası olarak kullanır ve bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12604-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="12604-234">Bu durumu engellemek için benzersiz ürün çeşidi numaralarını garanti etmeye yardımcı olmak için terminolojide yeterli sayıda öznitelik dahil etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="12604-235">Ayrıca **Yeniden kullan** seçeneğinin bileşen için açık olduğundan emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="12604-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="12604-236">Boyut tabanlı yapılandırmalar</span><span class="sxs-lookup"><span data-stu-id="12604-236">Dimension-based configurations</span></span>

<span data-ttu-id="12604-237">Yapılandırma işleminin bir adımında, sistem terminolojiye göre bir yapılandırma değeri önerir.</span><span class="sxs-lookup"><span data-stu-id="12604-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="12604-238">Bu adımda, yapılandırma değerini el ile değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12604-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="12604-239">Yapılandırmayı kaydettiğinizde sistem, yapılandırma değerinin benzersiz olduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="12604-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="12604-240">Girmiş olduğunuz değer benzersiz değilse, bir hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12604-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="12604-241">Yapılandırmayı kaydetmek için, benzersiz bir yapılandırma değeri girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12604-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="12604-242">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="12604-242">Additional resources</span></span>
--------

[<span data-ttu-id="12604-243">Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="12604-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="12604-244">Yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="12604-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

