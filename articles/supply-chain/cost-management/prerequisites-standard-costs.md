---
title: Standart maliyetler için önkoşullar
description: Bu konu, standart maliyetleri kullanmak için temel adımları açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5a4a4e49ef1cee923011ddab24497c65f85c1e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "359095"
---
# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="d6477-103">Standart maliyetler için önkoşullar</span><span class="sxs-lookup"><span data-stu-id="d6477-103">Prerequisites for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6477-104">Bu konu, standart maliyetleri kullanmak için temel adımları açıklar.</span><span class="sxs-lookup"><span data-stu-id="d6477-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="d6477-105">Sonraki adımlar şirketin işlemlerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d6477-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="d6477-106">Örneğin, adımlar üretim yapılmayan bir ortam, rotaları kullanmayan bir üretim ortamı ve rotaları kullanan üretim ortamı için farklıdır.</span><span class="sxs-lookup"><span data-stu-id="d6477-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="d6477-107">Standart maliyetleri ayarlamak için aşağıdaki adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="d6477-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="d6477-108">**1. Standart maliyetler için bir madde modeli grubu oluşturun.**</span><span class="sxs-lookup"><span data-stu-id="d6477-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="d6477-109">Standart maliyetler için yeni bir grup oluşturmak ve **Standart maliyet** stok modeli atamak için **Madde modeli grupları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6477-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="d6477-110">Madde modeli grubu tanımlayıcısının **Std Cost** gibi anlamlı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6477-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="d6477-111">Grubun mali negatif stoka izin vermesi ve fiziksel stok ile mali stoğu nakletmesi gerektiğini belirtmek için onay kutularını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d6477-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="d6477-112">Bu standart maliyet grubu maddelere atanır.</span><span class="sxs-lookup"><span data-stu-id="d6477-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="d6477-113">**2. Standart maliyet farklarıyla ilişkili genel muhasebe hesapları tanımlayın.**</span><span class="sxs-lookup"><span data-stu-id="d6477-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="d6477-114">Standart maliyet farklarıyla ilişkili genel muhasebe hesapları tanımlamak için **Hesap planı** formunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6477-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="d6477-115">Bu genel muhasebe hesaplarının **Deftere nakil** sayfasında atanabilmeleri için önce tanımlanmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6477-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="d6477-116">Genel muhasebe hesapları madde gruplarını ve maliyet gruplarını yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="d6477-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="d6477-117">**3. Madde nakillerine, standart maliyet farklarıyla ilişkili genel muhasebe hesapları atayın.**</span><span class="sxs-lookup"><span data-stu-id="d6477-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="d6477-118">Standart maliyet farklarıyla ilişkili genel muhasebe hesapları atamak için **Deftere nakil** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6477-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="d6477-119">Bir farklılığın genel muhasebe hesabını maddeye (veya madde grubuna) göre belirtme veya genel muhasebe hesabının tüm madde ve maliyet gruplarına uygulanacağını belirtme seçeneklerinden birini tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6477-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="d6477-120">Bu seçenekler tablolar, gruplar ve tümü için maliyet ilişkilerine karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="d6477-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="d6477-121">Madde deftere nakil kuralları tanımlamadan önce maliyet ilişkilerini (tablolar, gruplar ve tümü için) etkinleştirmek için **Hareket birleşimleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6477-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="d6477-122">**4. Standart maliyetlerle ilişkili stok parametreleri tanımlayın.**</span><span class="sxs-lookup"><span data-stu-id="d6477-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="d6477-123">Standart maliyetlerle ilişkili iki maliyet denetimi parametresi tanımlamak için **Stok muhasebesi politikaları kurulumu > Parametreler** sayfasındaki **Stok muhasebesi** sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6477-123">Use the **Inventory accounting** tab on the **Inventory accounting policies setup > Parameters** page to define two cost control parameters that are related to standard costs.</span></span>

    -  <span data-ttu-id="d6477-124">**Maliyet dökümü** alanında **Hiçbiri** veya **Yardımcı muhasebe**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6477-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="d6477-125">**Yardımcı defter**'i seçmeniz durumunda, maliyet dökümü *etkin* bir maliyet dökümü olur.</span><span class="sxs-lookup"><span data-stu-id="d6477-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="d6477-126">Etkin maliyet dökümü, standart maliyet maddeleri için çok düzeyli bir ürün yapısı üzerinde maliyet grubu segmentasyonunun hesaplanması, sürdürülmesi ve görüntülenmesi için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="d6477-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="d6477-127">Maliyet dökümü etkin olduğunda, tek düzeyli, çok düzeyli veya toplam biçiminde her maliyet grubu için stok, süren iş ve satılan malların maliyet tutarını rapor edebilir ve analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6477-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="d6477-128">Maliyet dökümü etkin olduğunda, üretilen bir öğenin maliyetini etkinleştirmeniz halinde, maliyet grubu segmentleri maddenin maliyet kaydında saklanır.</span><span class="sxs-lookup"><span data-stu-id="d6477-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="d6477-129">**Hiçbiri** öğesini seçerseniz, maliyet grubu segmentleri standart maliyet maddeleri için tutulmaz.</span><span class="sxs-lookup"><span data-stu-id="d6477-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="d6477-130">Başka bir deyişle, üretilmiş bir maddenin standart maliyeti hesaplanır ve maliyet grubu segmentleri olmadan tek bir tutar olarak tutulur.</span><span class="sxs-lookup"><span data-stu-id="d6477-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="d6477-131">Üretilmiş bileşenlerin maliyet katkıları tek bir tutarda toplanır.</span><span class="sxs-lookup"><span data-stu-id="d6477-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="d6477-132">**Standarttan farkılıklar** alanında **Özetlenmiş** veya **Maliyet grubu başına** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d6477-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="d6477-133">**Maliyet grubu başına** seçeneğini belirlerseniz, satınalma fiyatı farklarını ve üretim farklarını maliyet grubuna göre tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6477-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="d6477-134">Ayrıca dört tip üretim farkı tanımlayabilirsiniz: lot boyutu, miktar, fiyat ve değer değiştirme farkları.</span><span class="sxs-lookup"><span data-stu-id="d6477-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="d6477-135">**Özetlenmiş** öğesini seçerseniz, farkları maliyet grubuna göre belirleyemez ve dört üretim farkı tipini belirleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6477-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="d6477-136">Yalnızca özetlenmiş bir üretim farkı görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6477-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="d6477-137">Standarttan fark ilkesi, maliyet dökümü ilkesinden bağımsız çalışır.</span><span class="sxs-lookup"><span data-stu-id="d6477-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="d6477-138">Başka bir deyişle, maliyet grubuna göre üretim farklarının yakalanmaya devam edilebilmesi için maliyet dökümü ilkesi olarak **Hiçbiri** seçeneğini seçebilir ve maliyet grubu başına farkları belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6477-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="d6477-139">**5. Standart maliyetler için maliyetlendirme sürümleri oluşturun.**</span><span class="sxs-lookup"><span data-stu-id="d6477-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="d6477-140">Standart maliyetler için bir veya daha fazla maliyetlendirme sürümü oluşturmak için **Maliyet sürümü kurulumu** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6477-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="d6477-141">Her maliyetlendirme sürümünün **Standart maliyetler** maliyetlendirme türü ile atanması ve içeriğin maliyet verilerini dahil etmesine izin vermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6477-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="d6477-142">**6. Standart maliyetleri kullanmak için varolan bir müşteri hazırlayın.**</span><span class="sxs-lookup"><span data-stu-id="d6477-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="d6477-143">Varolan maddelerini standart bir maliyet stok modeline değiştirmek isteyen müşterilerin **Standart maliyet dönüştürmeleri** sayfasını kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6477-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="d6477-144">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="d6477-144">Related topics</span></span>
--------

[<span data-ttu-id="d6477-145">Standart maliyet dönüştürmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="d6477-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)

### <a name="blogs"></a><span data-ttu-id="d6477-146">Bloglar</span><span class="sxs-lookup"><span data-stu-id="d6477-146">Blogs</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="d6477-147">Topluluk blogları</span><span class="sxs-lookup"><span data-stu-id="d6477-147">Community blogs</span></span>

- [<span data-ttu-id="d6477-148">Dynamics 365 for Finance and Operations içindeki doğrudan malzemeler için standart maliyetleri ayarlamak</span><span class="sxs-lookup"><span data-stu-id="d6477-148">How to set up standard costs for direct materials in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [<span data-ttu-id="d6477-149">Dynamics 365 for Finance and Operations içinde standart işgücü maliyetleri</span><span class="sxs-lookup"><span data-stu-id="d6477-149">Standard direct labor costs in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)
