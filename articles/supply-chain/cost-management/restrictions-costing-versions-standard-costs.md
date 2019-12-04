---
title: Standart maliyetler için maliyetlendirme sürümlerindeki kısıtlamalar
description: Bu konu standart maliyetler için maliyetlendirme sürümüne uygulanan kısıtlamaları açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 484471c6bbda1d7396dfcfa34c33f50d247dad98
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812684"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="c1db5-103">Standart maliyetler için maliyetlendirme sürümlerindeki kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="c1db5-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1db5-104">Bu konu standart maliyetler için maliyetlendirme sürümüne uygulanan kısıtlamaları açıklar.</span><span class="sxs-lookup"><span data-stu-id="c1db5-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="c1db5-105">Aşağıdaki kısıtlamalar, standart maliyetlendirme ilkelerine bağlı kalınmasını sağlamaya yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="c1db5-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="c1db5-106">Bir maddenin maliyetine giderler dahil edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c1db5-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="c1db5-107">Üretilen bir maddenin giderleri ürün reçetesi ve rota bilgilerinde itfa edilmiş sabit maliyetleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c1db5-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="c1db5-108">Bu nedenle, giderler birim maliyete dahil edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c1db5-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="c1db5-109">Satınalınan bir maddenin giderleri de maddenin birim maliyetine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="c1db5-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="c1db5-110">Üretilen maddelerin standart maliyetlerinin hesaplaması standart maliyetlere ilişkin bir maliyetlendirme sürümündeki maliyet kayıtlarını temel almalıdır.</span><span class="sxs-lookup"><span data-stu-id="c1db5-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="c1db5-111">Alternatif maliyet verisi kaynakları yalnızca planlanan maliyetlere (örneğin satınalınan maddeler için satınalma fiyatı ticaret anlaşmaları) ait bir maliyetlendirme sürümüyle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c1db5-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="c1db5-112">Alternatif maliyet verisi kaynakları ürün reçetesi hesaplama grubu tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="c1db5-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="c1db5-113">Ürün reçetesi hesaplamaları tek düzeyli bir açılım moduyla yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c1db5-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="c1db5-114">Standart maliyetlerin madde maliyet verileri standart veya planlanan maliyetler içeren başka bir maliyet versiyonuna kopyalanabilir.</span><span class="sxs-lookup"><span data-stu-id="c1db5-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="c1db5-115">Ancak planlanan maliyetlerin madde maliyet verileri standart maliyetler içeren başka bir maliyet versiyonuna kopyalanamaz çünkü bu bölümde daha önce listelenen kısıtlamalar planlanan maliyetler için geçerli olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="c1db5-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="c1db5-116">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="c1db5-116">Related topics</span></span>
--------

[<span data-ttu-id="c1db5-117">Maliyetlendirme sürümlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c1db5-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="c1db5-118">İmalat dışı bir ortamda standart maliyetleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c1db5-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="c1db5-119">Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma</span><span class="sxs-lookup"><span data-stu-id="c1db5-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

