---
title: Boyut tabanlı ürün yapılandırmasına genel bakış
description: Boyut tabanlı ürün yapılandırması, tek bir ana üründen ve o ürün reçetelerinden çok sayıda ürün çeşidi oluşturmak için basit bir çözümü temsil eder.
author: cvocph
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca7e5555a242c10d2268182ed440e686a1dc46ad
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865364"
---
# <a name="dimension-based-product-configuration-overview"></a><span data-ttu-id="aa422-103">Boyut tabanlı ürün yapılandırmasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="aa422-103">Dimension-based product configuration overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa422-104">Boyut tabanlı ürün yapılandırması, tek bir ana üründen ve o ürün reçetelerinden çok sayıda ürün çeşidi oluşturmak için basit bir çözümü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="aa422-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="aa422-105">Boyuta dayalı ürün yapılandırma, üç yerleşik ürün yapılandırma teknolojisinden biridir.</span><span class="sxs-lookup"><span data-stu-id="aa422-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="aa422-106">Diğer iki teknoloji ön tanımlı farklara dayalı ve kısıtlamaya dayalı yapılandırmalardır.</span><span class="sxs-lookup"><span data-stu-id="aa422-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="aa422-107">Üç teknolojinin her biri başlangıç noktası olarak bir ürün master planı kullanır ve kullanıcının bir ürün master planından çok sayıda ürün çeşidi üretmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="aa422-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="aa422-108">Kilit kavramlar</span><span class="sxs-lookup"><span data-stu-id="aa422-108">Key concepts</span></span>
<span data-ttu-id="aa422-109">Boyuta dayalı ürün yapılandırma şu anahtar kavramlara dayanır:</span><span class="sxs-lookup"><span data-stu-id="aa422-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="aa422-110">Ana ürünler</span><span class="sxs-lookup"><span data-stu-id="aa422-110">Product masters</span></span>
-   <span data-ttu-id="aa422-111">Ürün boyutu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="aa422-111">Configuration product dimension</span></span>
-   <span data-ttu-id="aa422-112">Konfigürasyon grupları</span><span class="sxs-lookup"><span data-stu-id="aa422-112">Configuration groups</span></span>
-   <span data-ttu-id="aa422-113">Ürün reçetesi (BOM)</span><span class="sxs-lookup"><span data-stu-id="aa422-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="aa422-114">Konfigürasyon rotası</span><span class="sxs-lookup"><span data-stu-id="aa422-114">Configuration route</span></span>
-   <span data-ttu-id="aa422-115">Konfigürasyon kuralları</span><span class="sxs-lookup"><span data-stu-id="aa422-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="aa422-116">Ana ürünler</span><span class="sxs-lookup"><span data-stu-id="aa422-116">Product masters</span></span>

<span data-ttu-id="aa422-117">Bir ürün master planı, ürün yapılandırma sürecinin başlangıç noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="aa422-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="aa422-118">Boyuta dayalı ürün yapılandırma için bu belirli yapılandırma teknolojine ve yapılandırma ürün boyutunu içeren bir ürün boyut grubuna sahip bir ürün master planına ihtiyacınız vardır.</span><span class="sxs-lookup"><span data-stu-id="aa422-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="aa422-119">Ürün boyutu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="aa422-119">Configuration product dimension</span></span>

<span data-ttu-id="aa422-120">Yapılandırma ürün boyutu, boyuta dayalı yapılandırma teknolojisine sahip bir ürün master planı için ürün çeşitlerinin tanımlanması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa422-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="aa422-121">Yapılandırma boyut değeri, kullanıcı tarafından girilir ve ayrı ürün çeşitlerinin tanımlanmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="aa422-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="aa422-122">Konfigürasyon grupları</span><span class="sxs-lookup"><span data-stu-id="aa422-122">Configuration groups</span></span>

<span data-ttu-id="aa422-123">Yapılandırma grupları bir merkezi depoda tanımlanır ve tüm boyuta dayalı ürün yapılandırma modelleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="aa422-124">Yapılandırma grupları ayrı BOM satırlarıyla ilişkilendirilir ve ortak olarak özel olan bir grup satırla birlikte tutulur.</span><span class="sxs-lookup"><span data-stu-id="aa422-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="aa422-125">Bu da tek bir ürün çeşidi için bir gruptaki sadece bir satırın seçilebileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="aa422-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="aa422-126">Ürün reçetesi (BOM)</span><span class="sxs-lookup"><span data-stu-id="aa422-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="aa422-127">BOM, boyuta dayalı ürün yapılandırması için yapı taşlarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="aa422-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="aa422-128">Herhangi bir ürün çeşidinde kullanılabilecek tüm farklı ürünleri içermelidir.</span><span class="sxs-lookup"><span data-stu-id="aa422-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="aa422-129">BOM'daki her bir satır bir yapılandırma grubunu referans alabilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="aa422-130">Bir satır bir yapılandırma grubunu referans almıyorsa tüm ürün çeşitlerine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="aa422-131">Konfigürasyon rotası</span><span class="sxs-lookup"><span data-stu-id="aa422-131">Configuration route</span></span>

<span data-ttu-id="aa422-132">Yapılandırma yolu, yapılandırma gruplarının sırasını belirler ve bunlar ürün yapılandırma süreci sırasında kullanıcıya bu sırada görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="aa422-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="aa422-133">Konfigürasyon kuralları</span><span class="sxs-lookup"><span data-stu-id="aa422-133">Configuration rules</span></span>

<span data-ttu-id="aa422-134">Yapılandırma kuralları, bir BOM'da bir yapılandırma grubuna dahil edilen bir ürünün aynı BOM'daki farklı bir yapılandırma grubundaki bir ürünü dahil etmesini veya hariç tutmasını sağlayan bir mekanizmadır.</span><span class="sxs-lookup"><span data-stu-id="aa422-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="aa422-135">Ürün modelleme süreci</span><span class="sxs-lookup"><span data-stu-id="aa422-135">Product modeling process</span></span>
<span data-ttu-id="aa422-136">Boyuta dayalı bir ürün için ürün modelinin oluşturulması için doğal süreç ilgili yapılandırma gruplarının tanımlanmasıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="aa422-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="aa422-137">BOM'da kullanılacak tüm ürünlerin, ürün modelinin oluşturulduğu şirket için serbest bırakılmasının sağlanması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="aa422-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="aa422-138">Bu yapı taşları yerindeyken, kullanıcılar ürün reçetesini oluşturabilir ve yapılandırma gruplarını tüm ürün reçetesi satırlarına atayabilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="aa422-139">Bir ürün reçetesi tamamlandığında, bir yapılandırma rotası, yapılandırma gruplarını doğru sıralamada sipariş etmek için tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="aa422-140">[![Boyuta dayanan ürün modelleme işlemi](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Farklı yapılandırma gruplarından, birlikte kullanılması veya kullanılmaması gereken çeşitli ürünler mevcutsa, bu ürün ilişkilerini zorunlu kılacak yapılandırma kurallarını oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa422-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="aa422-141">BOM bir BOM sürümü üzerinden boyuta dayalı bir ürün master planıyla ilişkilendirildikten ve her ikisi onaylandıktan ve etkinleştirildikten sonra ürün yapılandırmaları oluşturabilir ve her bir yapılandırma için bir ad girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa422-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="aa422-142">Yapılandırmalar, herhangi bir hareket oluşturulmadan önce tanımlanabilir veya bu tanımlama işlemi belirli bir yapılandırma gerçekleştiğinde yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="aa422-143">Önerilen kullanım</span><span class="sxs-lookup"><span data-stu-id="aa422-143">Suggested use</span></span>

<span data-ttu-id="aa422-144">Boyuta dayalı yapılandırma teknolojisi en iyi, sınırlı ürün çeşitlerine ve standart ürün boyutları, boyları, renkleri, stillerinin kombinasyonuna sahip ürünler için kullanılır ve yapılandırma belirli bir ürün çeşidinin tanımlanması için uygun değildir.</span><span class="sxs-lookup"><span data-stu-id="aa422-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="aa422-145">Kasa yüksekliği, tekerlek boyutu, fren türleri ve dişli mekanizmaları farklı bir bisiklet örnek olarak gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="aa422-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="aa422-146">Sonraki adım</span><span class="sxs-lookup"><span data-stu-id="aa422-146">Next step</span></span> 

<span data-ttu-id="aa422-147">Aşağıdaki sekiz görev kılavuzu, tamamlamanız gereken sırada listelenmişlerdir.</span><span class="sxs-lookup"><span data-stu-id="aa422-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="aa422-148">Boyut tabanlı ana ürün oluşturma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="aa422-149">Boyut tabanlı ana ürünü serbest bırakma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="aa422-150">Serbest bırakılan ana ürünün temel kurulumunu tamamlama (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="aa422-151">Yapılandırma grupları tanımlama (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="aa422-152">Boyut tabanlı ana ürün için ürün reçetesi oluşturma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="aa422-153">Yapılandırma rotaları tanımlama (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="aa422-154">Yapılandırma kuralları oluşturma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="aa422-155">Boyut tabanlı yapılandırmalar oluşturma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="aa422-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)

