---
title: "Maliyet öğesi boyutları"
description: "Maliyet muhasebesinin temel direklerinden biri olarak maliyet öğesi boyutları maliyetlerin akış gerçekleştirdiği alanları sınıflandırmak ve izlemek için kullanılır."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 28595178111bc13fa6bbcb3b7d543c4675ecd805
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="38f4f-103">Maliyet öğesi boyutları</span><span class="sxs-lookup"><span data-stu-id="38f4f-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38f4f-104">Maliyet muhasebesinin temel direklerinden biri olarak maliyet öğesi boyutları maliyetlerin akış gerçekleştirdiği alanları sınıflandırmak ve izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="38f4f-105">Maliyet öğesi hesap planında maliyetle ilgili bir öğeye karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="38f4f-106">Temel olarak, maliyetlerin akış sağlayabileceği bir işletmenin en alt düzeyindeki herhangi bir öğe türü olabilir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="38f4f-107">Genel muhasebe hesaplarından maliyetle ilgili tüm kaynaklara bir kavram aralığı olarak maliyet öğeleri.</span><span class="sxs-lookup"><span data-stu-id="38f4f-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="38f4f-108">Şu anda, Maliyet muhasebesi genel muhasebe hesaplarını desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="38f4f-109">İki maliyet öğesi türü</span><span class="sxs-lookup"><span data-stu-id="38f4f-109">Two types of cost elements</span></span>
<span data-ttu-id="38f4f-110">Birincil maliyet öğeleri ve ikincil maliyet öğeleri olmak üzere iki tür maliyet öğesi vardır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="38f4f-111">Aşağıdaki tabloda iki tür arasındaki fark açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="38f4f-112"><strong>Birincil maliyet öğeleri</strong></span><span class="sxs-lookup"><span data-stu-id="38f4f-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="38f4f-113"><strong>İkincil maliyet öğeleri</strong></span><span class="sxs-lookup"><span data-stu-id="38f4f-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="38f4f-114">Birincil maliyet öğeleri, mali muhasebeden maliyet muhasebesine maliyetlerin akışını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="38f4f-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="38f4f-115">Maliyet öğesi yapısı, maliyet öğesinin bir ana hesaba karşılık gelebileceği, genel muhasebe defterindeki kar ve zarar hesabı yapısına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="38f4f-116">Tüm ana hesaplar, iş ihtiyaçlarına göre maliyet öğeleri olarak temsil edilmek zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="38f4f-117">Birincil maliyet öğeleri örnekleri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="38f4f-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="38f4f-118">Satılan malların maliyeti (SMM)</span><span class="sxs-lookup"><span data-stu-id="38f4f-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="38f4f-119">Dolaylı malzeme maliyetleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="38f4f-120">Personel maliyetleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-120">Personnel costs</span></span></li>
<li><span data-ttu-id="38f4f-121">Enerji maliyetleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="38f4f-122">İkincil maliyet öğeleri, maliyetlerin dahili akışını temsil eder çünkü bu maliyetler yalnızca Maliyet muhasebesinde oluşturulur ve kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="38f4f-123">Bunlar, maliyetlerin kaynağının izlenebilmesini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="38f4f-124">Bu maliyet öğeleri, maliyet tahsisatları ve genel gider hesaplamalarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="38f4f-125">İkincil maliyet öğeleri örnekleri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="38f4f-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="38f4f-126">Üretim maliyetleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-126">Production costs</span></span></li>
<li><span data-ttu-id="38f4f-127">Üretim, malzeme ve pazarlama genel giderleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="38f4f-128">Maliyet öğesi boyutları ve maliyet öğesi boyut üyeleri</span><span class="sxs-lookup"><span data-stu-id="38f4f-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="38f4f-129">Maliyet öğeleri, *maliyet öğesi boyutları* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="38f4f-130">Tek tek boyut değerleri *maliyet öğesi boyut üyeleri* olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="38f4f-131">Örneğin, yasal raporlamanızın temeli olan bir ABD hesap planı yapınız (COA) olsun.</span><span class="sxs-lookup"><span data-stu-id="38f4f-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="38f4f-132">Bu COA maliyet öğesi boyutu olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="38f4f-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="38f4f-133">Birincil maliyet öğesi olan hesaplar Maliyet muhasebesinde maliyet öğesi boyut üyeleri olarak temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="38f4f-134">Aşağıdaki ekran görüntüsünde fiili ana hesapları maliyet öğesi boyut üyesi olarak, Ana Hesapların maliyet öğesi boyutu olduğu bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="38f4f-135">[![maliyet-ogeleri-boyutlari](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="38f4f-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="38f4f-136">Veri bağlayıcıları üzerinden maliyet öğesi boyut üyelerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="38f4f-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="38f4f-137">Maliyet muhasebesinde maliyet öğesi boyut üyelerinin kurulumunu kolaylaştırmak için bir veya daha fazla kaynak sistemden birincil maliyet öğelerini almak üzere önceden inşa edilmiş veya sizin özel olarak inşa ettiğiniz veri bağlayıcılarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38f4f-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="38f4f-138">Uygulama ile ilgili hususlar</span><span class="sxs-lookup"><span data-stu-id="38f4f-138">Implementation considerations</span></span>
<span data-ttu-id="38f4f-139">Maliyet öğeleri, maliyet ayrıntılarınızın en düşük düzeyini temsil ettiğinden, maliyet öğesi yapısını uygularken yönetim raporlaması yapmak için gerekli tüm maliyet öğelerinin dahil edildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="38f4f-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="38f4f-140">Maliyet denetimi için uygun sayıda maliyet öğesi bulmak zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="38f4f-141">Binlerce maliyet öğesi bulundurmak her maliyet öğesini denetlemeyi zorlaştırabilir.</span><span class="sxs-lookup"><span data-stu-id="38f4f-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="38f4f-142">Alternatif olarak, maliyet öğelerini gruplandırabilir ve maliyet denetimini toplu düzeyde yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38f4f-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




