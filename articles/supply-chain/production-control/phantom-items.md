---
title: Hayali maddeler
description: Bu konu, Dynamics 365 Supply Chain Management içinde ayrıntılı olarak Hayali hat türünün bir ürün reçetesi (BOM) satırlarında ve formülünde nasıl kullanılabileceğini açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: dc69687b1dd94407b28209178e923fe5169bcdac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211342"
---
# <a name="phantom-items"></a><span data-ttu-id="a523d-103">Hayali maddeler</span><span class="sxs-lookup"><span data-stu-id="a523d-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a523d-104">Bu konu, ayrıntılı olarak Hayali hat türünün bir ürün reçetesi (BOM) satırlarında ve formülünde nasıl kullanılabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="a523d-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="a523d-105">Aşağıdaki çizimde, (a) ürün H ve parçalar F ve G için ürün reçetesidir, ve (b), ürünler H ve parça F için rota tablosudur.</span><span class="sxs-lookup"><span data-stu-id="a523d-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Ürün H ve parça F](media/product-H-part-F.png)


<span data-ttu-id="a523d-107">Bu çizim, bir ürün reçetesi yapısını iki düzeyde gösterir.</span><span class="sxs-lookup"><span data-stu-id="a523d-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="a523d-108">Tamamlanmış ürün H, bir makine montajı için bir ürünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a523d-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="a523d-109">Makine montajı iki parçadan oluşur, iki malzemeye (A ve B) sahip bir elektriksel birim (F) ve iki malzemeye sahip (C ve D) bir paketleme malzemeleri grubu (G).</span><span class="sxs-lookup"><span data-stu-id="a523d-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="a523d-110">Başka bir malzeme (E), makinenin genel montajında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a523d-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Ürün H ve parça F](media/product-H-part-B.png)

<span data-ttu-id="a523d-112">önceki şekil, ürün H için Mühendislik Ürün Reçetesini temsil etmektedir. Bu yapı, genel makine montajının parçaları ve bileşenlerine genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="a523d-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="a523d-113">Ancak, ürün tasarımcıları ürün reçetesinin bu şekilde temsil edilmesini tercih etseler de, bu yapı makinenin atölyede nasıl ortaya çıkarıldığını doğru şekilde temsil etmeyebilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="a523d-114">Örneğin, önceki örnekteki Mühendislik ürün reçetesi, elektriksel birim F'nin ayrı bir iş emrinde, ayrı bir parça olarak monte edildiğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a523d-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="a523d-115">Ancak, atölyede, elektriksel birimi ayrı bir iş emri olarak değil, genel makine montajının bir parçası olarak monte etmek daha optimal olarak değerlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="a523d-116">Mühendislik ürün reçetesi, parça G'nin ayrı bir parça olduğunu belirtmektedir.</span><span class="sxs-lookup"><span data-stu-id="a523d-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="a523d-117">Ancak, bu yapıda, parça G fiziksel bir parçayı değil, bir paketleme malzemeleri grubunu temsil etmektedir.</span><span class="sxs-lookup"><span data-stu-id="a523d-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="a523d-118">Bu nedenle, bir Mühendislik Ürün reçetesi bir ürünün tasarımı ve bu tasarımın bakımı için önemli değer sağlasa da, ürünün üretilmesi işlemini desteklemek için en mantıksal yolu sunmuyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="a523d-119">Bunun tersine, bir Üretim ürün reçetesi, bir ürünü oluşturmanın en iyi yolunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a523d-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="a523d-120">Aşağıdaki çizim, önceki Mühendislik ürün reçetesinin bir Üretim ürün reçetesine nasıl dönüştürüldüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="a523d-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="a523d-121">Bu şekilde, (a) ürün H için ürün reçetesidir ve b, ürün H için rota tablosudur.</span><span class="sxs-lookup"><span data-stu-id="a523d-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="a523d-122">Bu yapıda, parçalar F ve G kavramı yoktur ve bu parçaların oluştuğu malzemeler bir sonraki ürün reçetesi seviyesine yükseltilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a523d-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="a523d-123">İki operasyon sayfasına sahip Mühendislik ürün reçetesinin aksine, Üretim ürün reçetesi yalnızca bir operasyon sayfasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="a523d-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="a523d-124">Parça G ile bağlantılı olan paketleme operasyonu da yükseltilmiştir ve ürün H için operasyon sayfasının parçasıdır. Elektriksel birimin montajı ilk operasyondur.</span><span class="sxs-lookup"><span data-stu-id="a523d-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="a523d-125">Bu sıralama mantıklıdır, çünkü birim, makine montajı olan bir sonraki operasyonda kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a523d-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="a523d-126">Son operasyon, paketleme operasyonudur, bu da iki paketleme malzemesi tüketir (C ve D).</span><span class="sxs-lookup"><span data-stu-id="a523d-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="a523d-127">Mühendislik BOM ve Üretim BOM arasındaki geçiş, Phantom BOM satır türü ile gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="a523d-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="a523d-128">"Hayali" teriminin belirttiği gibi, parçalar F ve G iki ürün reçetesi türü arasında geçiş yapılırken ortadan kaybolmuştur.</span><span class="sxs-lookup"><span data-stu-id="a523d-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="a523d-129">Bu örnekte, Hayali satır türü parçalar F ve G için Mühendislik ürün reçetesinde ürün reçetesi satırlarına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a523d-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="a523d-130">Bir üretim veya toplu iş emri oluşturulduğunda, Mühendislik ürün reçetesi üretim veya toplu iş emrine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="a523d-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="a523d-131">Daha sonra siparişin tahmini yapıldığında, Mühendislik ürün reçetesinden Üretim ürün reçetesine geçiş, önceden belirtilen şekillerdeki gibi ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="a523d-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="a523d-132">İkinci şekildeki operasyonlar sayfasından, paketleme malzemeleri C ve D operasyon için dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="a523d-133">Çok düzeyli hayali ürün reçetesi yapıları</span><span class="sxs-lookup"><span data-stu-id="a523d-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="a523d-134">Hayali satır türü çok düzeyli ürün reçetesi yapıları için aşağıdaki şekilde gösterildiği gibi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="a523d-135">Bu şekilde, (a) ürün G için ürün reçetesidir ve (b) parçalar E ve F ve ürün G için rota tablosudur.</span><span class="sxs-lookup"><span data-stu-id="a523d-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Ürün G ve parça F rota tablolarıyla](media/product-G-route-sheet-G.png)


<span data-ttu-id="a523d-137">Aşağıdaki şekil, ortaya çıkan Üretim ürün reçetesi ve rota tablosunu, parçalar E ve F için ürün reçetesi satırları satır tipinin Hayali olarak yapılandırılması durumunda gösterir.</span><span class="sxs-lookup"><span data-stu-id="a523d-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="a523d-138">Bu şekilde, (a) ürün G için ürün reçetesidir ve (b), ürün G için rota tablosudur.</span><span class="sxs-lookup"><span data-stu-id="a523d-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Ürün G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="a523d-140">Hayali ve rota ağı</span><span class="sxs-lookup"><span data-stu-id="a523d-140">Phantom and route network</span></span>
<span data-ttu-id="a523d-141">Hayali ürün reçeteleri de bir rota ağına sahip bir ürün reçetesi için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="a523d-142">Bir rota ağında, bir veya daha fazla operasyon paralel olarak çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="a523d-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="a523d-143">Aşağıdaki şekil, çok düzeyli bir ürün reçetesinde kullanılan bir rota ağına bir örnek göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a523d-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="a523d-144">Bu şekilde, (a) ürün G ve parça F için ürün reçetesidir ve (b) bir rota ağına sahip ürün G ve parça F için bir rota tablosudur.</span><span class="sxs-lookup"><span data-stu-id="a523d-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Ürün G ve parça F](media/product-G-part-F.png)


<span data-ttu-id="a523d-146">Aşağıdaki çizimde, (a) ürün G ve parça F ve G için ürün reçetesidir, ve (b), ürün G ve parça F için rota tablosudur.</span><span class="sxs-lookup"><span data-stu-id="a523d-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Ürün G ve parça F rota tablolarıyla](media/product-G-part-F-with-route-sheet.png)
