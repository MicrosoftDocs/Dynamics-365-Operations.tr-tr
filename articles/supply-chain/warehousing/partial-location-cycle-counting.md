---
title: Kısmi konum döngü sayımı
description: Döngü sayımı planları, gerçek sayım işlemlerine yol gösterir. Bir konumdaki tüm eldeki stokun sayılması yerine yalnızca belirli ürünlerin ve ürün çeşitlerinin sayılmasını talep edebilirsiniz.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd7cb8b35023ed63af191545d01c60c2c7cc8ef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "320662"
---
# <a name="partial-location-cycle-counting"></a><span data-ttu-id="27c6b-104">Kısmi konum döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="27c6b-104">Partial location cycle counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27c6b-105">Döngü sayımı planları, gerçek sayım işlemlerine yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="27c6b-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="27c6b-106">Bir konumdaki tüm eldeki stokun sayılması yerine yalnızca belirli ürünlerin ve ürün çeşitlerinin sayılmasını talep edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="27c6b-107">Döngü sayımı planlarını sayım işi oluşturmak için kullanarak, gerçek sayım işlemlerine yol gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="27c6b-108">Bir konumdaki tüm eldeki stokun sayılması yerine yalnızca belirli ürünlerin ve ürün çeşitlerinin sayılmasını talep edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="27c6b-109">Belirli ürünleri filtreleyerek, ambar yöneticisi inceleme yükünü azaltabilir, konsolidasyon hatalarının önüne geçebilir ve zaman tasarruf edebilir.</span><span class="sxs-lookup"><span data-stu-id="27c6b-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="27c6b-110">Kısmi konum döngü sayımının yapılandırılması</span><span class="sxs-lookup"><span data-stu-id="27c6b-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="27c6b-111">Sayım işlemleri için ambar iş işlemini kullanıyorsanız, her bir konum için bir iş başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27c6b-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="27c6b-112">Döngü sayım planı tanımlarsanız, **Konumları seç** sorgusunu, oluşturulan döngü sayımı işini sınırlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="27c6b-113">Döngü sayım planı için ürünler seçtiğinizde, nelerin sayıldığını belirlemek için hem ürün hem de ürün çeşidi sorgularını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="27c6b-114">Bir **iş şablonunu**, döngü sayım planının nasıl oluşturulacağını tanımlamak için bir döngü sayım planı ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="27c6b-115">Sayım işlemleri için iş şablonu, doğrudan döngü sayım planından referans alınır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="27c6b-116">İş şablonu ayrıntılarını tanımladığınızda, **İş satırı bölmeleri** seçeneğini, sayım iş satırlarının madde numarası mı yoksa ürün çeşidi numarasına mı göre gruplanacağını belirtmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="27c6b-117">Bu ayar, bir konumdaki yalnızca belirli ürünler için eldeki stoku saymak istiyorsanız gereklidir.</span><span class="sxs-lookup"><span data-stu-id="27c6b-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="27c6b-118">Oluşturulan döngü sayımı iş satırları, burada tanımladığınız bilgi düzeyine sahip olacaktır ve yönlendirmeli sayım işlemi, bu düzeye bağlı olacak ele alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="27c6b-119">Döngü sayım planlarını, iş şablonları ile **İş satır sonu** seçeneğini kullanarak ilişkilendirirseniz, **Kısmi döngü sayım** alanı, oluşturulan döngü sayımı işi seçilir ve çoklu döngü sayım iş satırları, iş şablonundaki tanıma dayalı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27c6b-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="27c6b-120">Kısmi döngü sayım işi işleme alınmadan önce, döngü sayım kurulumunun parçası olarak mobil cihaz menü öğesi için en azından **Madde numarasını görüntüle** seçeneğini işaretlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="27c6b-121">Ambar operatörü, yalnızca sayım satırları (madde numaraları ve ürün boyutları) ile ilgili sayım bilgisini kaydetmek üzere yönlendirilecektir.</span><span class="sxs-lookup"><span data-stu-id="27c6b-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="27c6b-122">Eldeki diğer tüm stoklar bu sayım işlemi için yok sayılacaktır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="27c6b-123">Kısmi döngü sayım işlemi için **Son döngü sayımı** tarihi/saati, konum için güncelleştirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="27c6b-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="27c6b-124">Örnek</span><span class="sxs-lookup"><span data-stu-id="27c6b-124">Example</span></span>
<span data-ttu-id="27c6b-125">Bu örnekte, ambar 61'de yalnızca ürün numarası A0001 sayılacaktır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="27c6b-126">Döngü sayımı için yeni bir iş şablonu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27c6b-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="27c6b-127">**Döngü satır sonları** seçeneği, sayım iş satırlarını madde numarasına göre gruplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="27c6b-128">Bu nedenle, oluşturulan döngü sayım işi, madde numarasına göre satırlara sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="27c6b-129">Satırları ayrıca ürün çeşit numarasına göre de gruplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="27c6b-130">Yeni oluşturulan iş şablonuna referans gösteren bir döngü sayım planı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27c6b-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="27c6b-131">Döngü sayım planı, ambar 61'deki (**Konum seç** sorgusu) madde numarası A0001 bulunduran tüm konumları kapsar.</span><span class="sxs-lookup"><span data-stu-id="27c6b-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="27c6b-132">Belirli ürünlerin seçimi **Döngü sayımı ürün seçimi** bölümünde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="27c6b-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="27c6b-133">**Boş yerleşimler** alanını **Boşu hariç tut** olarak ayarlayarak döngü sayımı planları için ürünler seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27c6b-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="27c6b-134">Döngü sayımı planı işlendiğinde, A0001 madde numarası için kısmi döngü sayımı işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27c6b-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="27c6b-135">Gerçek sayım işlemi, yönlendirmeli döngü sayımı için bir taşınabilir aygıt menü öğesi kullanılarak gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="27c6b-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="additional-resources"></a><span data-ttu-id="27c6b-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="27c6b-136">Additional resources</span></span>
--------

[<span data-ttu-id="27c6b-137">Döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="27c6b-137">Cycle counting</span></span>](cycle-counting.md)

