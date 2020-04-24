---
title: Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma
description: Bu konu üretilmiş maddeler için maliyetleri korumaya hazırlanmayla ilgili adımları açıklar.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 866da2ce58e33676c2fa4bb2d6abfde891a5d021
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214608"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="9ceb4-103">Üretilmiş maddeler için standart maliyetleri sürdürmeye hazırlanma</span><span class="sxs-lookup"><span data-stu-id="9ceb4-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ceb4-104">Bu konu üretilmiş maddeler için maliyetleri korumaya hazırlanmayla ilgili adımları açıklar.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="9ceb4-105">Üretilmiş maddelerle ilgili adımlar satın alınan maddelerle ilgili adımlardan biraz farklıdır.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="9ceb4-106">Üretilmiş maddelere atanan ilkeler, üretilmiş üst maddelere ait maliyet hesaplarını etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="9ceb4-107">Üretilmiş maddeler için standart maliyetleri korumaya hazırlanmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="9ceb4-108">Üretilmiş maddeye bir madde modeli grubu atayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="9ceb4-109">Madde modeli grubu standart maliyetlerin kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="9ceb4-110">Üretilmiş maddeye bir madde grubu atayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="9ceb4-111">Madde grubu, üretilmiş maddeye uygulanan genel muhasebe hesaplarını içerir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="9ceb4-112">Bir standart maliyet stok modeli içeren üretilmiş bir maddenin genel muhasebe hesapları çeşitli üretim farklılıkları, maliyet değişim farklılığı ve stok maliyeti yeniden değerleme içerir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="9ceb4-113">Maddeye stok ölçüm birimi atayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="9ceb4-114">Maddenin maliyetleri her zaman maddenin stok ölçüm biriminde ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="9ceb4-115">Üretilmiş maddeye, satın alınmış madde gibi ele alınmadığı sürece bir maliyet grubu atamayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="9ceb4-116">Üretilmiş maddeye bir ürün reçetesi (BOM) hesap grubu atayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="9ceb4-117">Maddenin ürün reçetesi hesaplama grubu uygulanacak uyarı durumlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="9ceb4-118">Bu şekilde, bir ürün reçetesi hesaplaması yapıldığında, olası hesaplama hatalarının kaynakları hakkında uyarı iletileri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="9ceb4-119">Örneğin, bir hata iletisi bir etkin ürün reçetesi veya rotanın olmadığı durumları belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="9ceb4-120">Ürün reçetesi hesap gurubu, üretilmiş bir maddenin ne zaman satın alınan bir madde gibi ele alınması gerektiğini gösteren açılım durdurma ilkesi içerir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="9ceb4-121">Üretilmiş maddenin sabit maliyetleri varsa üretilmiş maddeye standart bir sipariş miktarı atayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="9ceb4-122">Standart sipariş miktarı, sabit maliyetlerin itfa edilmesi için bir muhasebe lot boyutudur.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="9ceb4-123">Sabit maliyet örnekleri rota operasyonlarındaki kurulum sürelerini ve bir ürün reçetesindeki sabit bileşen miktarını içerir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="9ceb4-124">Üretilmiş madde için ürün reçetesini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="9ceb4-125">Üretilmiş madde için bir veya daha fazla ürün reçetesi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="9ceb4-126">İstediğiniz versiyonların onaylanmış ve etkin olarak işaretlendiğini ve istediğiniz geçerlilik tarihlerine sahip olduklarını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="9ceb4-127">Ürün reçetesi versiyonu şirket çağında veya tesise özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="9ceb4-128">Üretilmiş madde için rotayı tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="9ceb4-129">Üretilmiş madde için bir veya daha fazla rota tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="9ceb4-130">İstediğiniz versiyonların onaylanmış ve etkin olarak işaretlendiğini ve istediğiniz geçerlilik tarihlerine sahip olduklarını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="9ceb4-131">Rota versiyonunun tesise özel olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-131">The route version must be site-specific.</span></span>

<span data-ttu-id="9ceb4-132">Rota bilgilerini maliyetlendirme amaçlı kullanmak istemeniz durumunda ek hazırlık adımları gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="9ceb4-133">Örneğin, rota operasyonlarına atanan maliyet kategorilerinin doğru ve tam olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ceb4-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="9ceb4-134">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="9ceb4-134">Related topics</span></span>
--------

[<span data-ttu-id="9ceb4-135">Üretilen maddeler için sabit maliyetlerin itfası</span><span class="sxs-lookup"><span data-stu-id="9ceb4-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="9ceb4-136">Üretilen ya da temin edilen ürünleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="9ceb4-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

