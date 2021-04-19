---
title: Anlık stok yenileme
description: Bu konu, bir yerleşim yönergesi stok tahsis etmek için başarısız olduğunda stok yenileme için anlık stok yenilemeyi nasıl kullanabileceğinizi açıklar.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 006160a3f7eada95ebdcdbf6694ee54be439f349
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835666"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="00490-103">Anlık stok yenileme</span><span class="sxs-lookup"><span data-stu-id="00490-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00490-104">Anlık stok yenileme bir yerleşim yönergesi satırı stok tahsis etmek için başarısız olduktan hemen sonra stoğu yenilemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="00490-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="00490-105">Stok yenileme yerleşim yönergesi kurulumundaki tek bir satırı temel alır.</span><span class="sxs-lookup"><span data-stu-id="00490-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="00490-106">Stok bu satır tarafından belirtilen ölçü biriminde elde yoksa, bu ölçü birimi için stok yenileme anında gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="00490-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="00490-107">Anlık stok yenileme, stok tahsisatının yerleşim yönergesinde birçok satırı temel aldığı ve talebin tahsisat sonunda toplanıp yerleşim yönergesinin son satırı tarafından belirtilen ölçüm biriminde yenilendiği yönteme bir alternatif sağlar.</span><span class="sxs-lookup"><span data-stu-id="00490-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="00490-108">Anlık stok yenileme kullanmanın avantajları stok yenilemenin belirli birimlere göre sınırlandırılabilmesi be miktarın belirli yerleşimlere yönlendirilebilmesidir.</span><span class="sxs-lookup"><span data-stu-id="00490-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="00490-109">İş senaryosu</span><span class="sxs-lookup"><span data-stu-id="00490-109">Business scenario</span></span>

<span data-ttu-id="00490-110">Örneğin, "kutu" ve "her" ölçüm birimi için ayrı malzeme çekme alanlarına sahip bir ambarınız bulunuyor olsun.</span><span class="sxs-lookup"><span data-stu-id="00490-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="00490-111">Mümkün olduğu kadar çok kutu çekerek malzeme çekme sürecini en iyi duruma getirmek ve bir kutudan az olan kalan miktarı "her" alanından çekmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="00490-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="00490-112">Bu durumda, anında stok yenileme kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00490-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="00490-113">Yerleşim yönergesinde, kutular için anlık stok yenileme ayarlayarak talep stok yenilemesinin talep miktarı için çekilebilecek kutular eksik olduğunda kullanılmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00490-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="00490-114">Bu şekilde, malzeme çekme işlemini en iyi duruma getirerek çekme işleminin mümkün olduğunca çok kutuyu içermesini sağlarsınız.</span><span class="sxs-lookup"><span data-stu-id="00490-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="00490-115">Anlık stok yenileme kutular için stok yenileme oluşturur ve talep geçilmez, böylece miktarlar "her" ölçü biriminde çekilir.</span><span class="sxs-lookup"><span data-stu-id="00490-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="00490-116">Başka bir deyişle, "her" ölçü birimiyle (diğer bir deyişle, bir kutudan az olan miktarlar) çekilmesi gereken miktarlar "her" alanından çekilir.</span><span class="sxs-lookup"><span data-stu-id="00490-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="00490-117">"Kutu" alanında bir yetersizlik oluşursa, toplam talep dışında olabildiğince çok kutu çekebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00490-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="00490-118">Kalan miktarlar daha sonra "her" alanından çekilir.</span><span class="sxs-lookup"><span data-stu-id="00490-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="00490-119">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="00490-119">Where it applies</span></span>

<span data-ttu-id="00490-120">Anında stok yenileme, stok yenileme şablonunun ayarlandığı bir yerleşim yönergesi satırı için tahsisatın başarısız olması durumunda dalga yürütme sırasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00490-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="00490-121">Anlık stok yenileme ayarlama</span><span class="sxs-lookup"><span data-stu-id="00490-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="00490-122">**Ambar yönetimi** \> **Kurulum** \> **Yerleşim yönergeleri**'ne gidin ve **Satırlar** sekmesinde **Anlık stok yenileme şablonu** listesinde dalga talebi için bir stok yenileme şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="00490-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="00490-123">Stok yenileme şablonu, yerleşim yönergesi satırı özel bir ölçüm birimi tahsis etmede başarısız olursa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00490-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="00490-124">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="00490-124">Troubleshooting</span></span>

<span data-ttu-id="00490-125">Bir yerleşim yönergesi satırı için anlık stok yenileme seçilir ancak bu yerleşim yönergesi satırı için talep stok yenileme şablonları kullandığınızda stok yenileme işi oluşturulmazsa, iki ana nedenin araştırılması gerekir:</span><span class="sxs-lookup"><span data-stu-id="00490-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="00490-126">Uygulanan talep stok yenileme şablonunun doğru yerleşim şablonlarıyla ve **Stok yenileme** türünde iş şablonları ile kullanılmak üzere ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="00490-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="00490-127">Talep stok yenileme şablonunun stok yenileme için eldeki stoğu aradığı yerleşimlerde yeterli eldeki stok bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="00490-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]