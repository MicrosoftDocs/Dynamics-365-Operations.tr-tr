---
title: "Boyut oluşturma ve boyut üyelerini içe aktarma"
description: "Maliyet muhasebesi diğer modüllerden alınan ana verilere ihtiyaç duyan bağımsız modüldür."
author: YuyuScheller
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0fb276e7d62e2f7c02934e74741c8cf74778fc12
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="0b51a-103">Boyut oluşturma ve boyut üyelerini içe aktarma</span><span class="sxs-lookup"><span data-stu-id="0b51a-103">Create dimensions and import dimension members</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0b51a-104">Maliyet muhasebesi diğer modüllerden alınan verilere ihtiyaç duyan bağımsız modüldür.</span><span class="sxs-lookup"><span data-stu-id="0b51a-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="0b51a-105">Bu veri aşağıdaki şekilde sınıflandırılır:</span><span class="sxs-lookup"><span data-stu-id="0b51a-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="0b51a-106">Maliyet öğeleri</span><span class="sxs-lookup"><span data-stu-id="0b51a-106">Cost elements</span></span>
-  <span data-ttu-id="0b51a-107">Maliyet nesneleri</span><span class="sxs-lookup"><span data-stu-id="0b51a-107">Cost objects</span></span>
-  <span data-ttu-id="0b51a-108">İstatistiksel boyutlar</span><span class="sxs-lookup"><span data-stu-id="0b51a-108">Statistical dimensions</span></span>

<span data-ttu-id="0b51a-109">**Maliyet öğesi** hesap planında maliyetle ilgili bir öğeye karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="0b51a-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="0b51a-110">Bir **Maliyet nesnesi**, ürünler, maliyet merkezleri ve projeler gibi maliyetleri tahmin etmek, tahsis etmek ve doğrudan ölçmek istediğiniz herhangi bir türdeki mali boyuta karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="0b51a-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="0b51a-111">Bir **İstatistiksel boyut** ve üyeleri, parasal olmayan girişleri kaydetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b51a-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="0b51a-112">İstatistiksel boyut üyelerini tahsisat maliyet dağılımı ve maliyet tahsisatı gibi tahsisat temeli olarak kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="0b51a-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="0b51a-113">Aşağıdaki diyagram, Maliyet muhasebesinde kullanılan boyutları gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b51a-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="0b51a-114">[![Maliyet muhasebesi boyutları](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="0b51a-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="0b51a-115">Verinin tamamı Maliye muhasebesine aktarıldıktan sonra, kuruluşun tüm seviyesindeki yöneticilere bilgi sağlayacak perspektifler oluşturmak üzere bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b51a-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="0b51a-116">Aşağıdaki konular, boyutlar oluşturma ve boyut üyelerini içe aktarma konusunda bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b51a-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="0b51a-117">Maliyet öğesi boyutları</span><span class="sxs-lookup"><span data-stu-id="0b51a-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="0b51a-118">Maliyet öğeleri oluşturma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="0b51a-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="0b51a-119">Maliyet nesnesi boyutları</span><span class="sxs-lookup"><span data-stu-id="0b51a-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="0b51a-120">Maliyet öğeleri oluşturma (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="0b51a-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="0b51a-121">Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesine eşleme</span><span class="sxs-lookup"><span data-stu-id="0b51a-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="0b51a-122">Maliyet öğesi boyutunu eşleştirme (Görev kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="0b51a-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="0b51a-123">İstatistiksel boyut üyeleri ve istatistiksel ölçü sağlayıcısı şablonları</span><span class="sxs-lookup"><span data-stu-id="0b51a-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)







