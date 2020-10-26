---
title: Maliyet nesnesi boyutları
description: Maliyetleri analiz ettiğinizde maliyetlerin nereye aktığını belirlemek için maliyet öğesi boyutlarını kullanın. Maliyetleri nereye atamanız gerektiğini belirlemek için maliyet nesnesi boyutlarını kullanın. Bu konu, maliyet nesnesi boyutları hakkında bilgiler sağlar.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a090ecae2aadf1d0e08dd6127f831abdbf4a6b0a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976439"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="b088b-105">Maliyet nesnesi boyutları</span><span class="sxs-lookup"><span data-stu-id="b088b-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b088b-106">Maliyetleri analiz ettiğinizde maliyetlerin nereye aktığını belirlemek için maliyet öğesi boyutlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="b088b-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="b088b-107">Maliyetleri nereye atamanız gerektiğini belirlemek için maliyet nesnesi boyutlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="b088b-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="b088b-108">Bu konu, maliyet nesnesi boyutları hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="b088b-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="b088b-109">Maliyet nesnesi tahmin etmek, maliyetleri tahsis etmek veya doğrudan ölçmek istediğiniz herhangi bir tür nesne olabilir.</span><span class="sxs-lookup"><span data-stu-id="b088b-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="b088b-110">Maliyet nesneleri genellikle ürünleri, projeleri, kaynakları, departmanları, maliyet merkezlerini ve coğrafi bölgeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="b088b-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="b088b-111">Yönetim, maliyetlerini sayısallaştırmak ve ayrıca karlılık analizini sürdürmek için maliyet nesnelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b088b-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="b088b-112">Maliyet nesnesi boyutları ve maliyet nesnesi boyut üyeleri</span><span class="sxs-lookup"><span data-stu-id="b088b-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="b088b-113">Maliyet nesneleri *maliyet nesnesi boyutları* olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="b088b-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="b088b-114">Maliyet nesnesi boyutunun hangi varlığa başvuracağına karar vermenizden sonra tek tek boyut değerlerini belirlemeniz veya diğer kaynak sistemlerden Maliyet muhasebesine aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b088b-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="b088b-115">Bu tek tek boyut değerleri *maliyet nesnesi boyut üyeleri* olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="b088b-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="b088b-116">Örneğin, maliyet nesnesi boyutu olarak Maliyet merkezi adlandırılan mali boyutu kullanmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b088b-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="b088b-117">Maliyetlerin tek tek maliyet merkezlerine nasıl dağıldığını görmek için maliyet nesnesi boyut üyelerini içe aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b088b-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="b088b-118">Bu durumda maliyet nesnesi boyut üyeleri Satış, Üretim, Yönetim ve Coğrafi konumlar gibi fiili maliyet merkezleridir.</span><span class="sxs-lookup"><span data-stu-id="b088b-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="b088b-119">Aşağıdaki ekran görüntüsü, maliyet nesnesi boyutu olarak Maliyet Merkezlerini maliyet nesnesi boyut üyesi olarak fiili maliyet hesaplarıyla gösterir.</span><span class="sxs-lookup"><span data-stu-id="b088b-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="b088b-120">[![Maliyet nesnesi boyutu olarak Maliyet Merkezlerini gösteren ekran görüntüsü](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="b088b-120">[![Screenshot showing Cost Centers as cost object dimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="b088b-121">Veri bağlayıcıları üzerinden maliyet nesnesi boyut üyelerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="b088b-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="b088b-122">Maliyet nesnesi boyut üyelerini içe aktarmayı daha kolay hale getirmek için maliyet nesne boyutu olarak kullanmak istediğiniz varlıklardan değerleri almak için veri bağlayıcıları kullanın.</span><span class="sxs-lookup"><span data-stu-id="b088b-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="b088b-123">Önceden oluşturulmuş veri bağlayıcılarını veya oluşturduğunuz özel veri bağlayıcıları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b088b-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



