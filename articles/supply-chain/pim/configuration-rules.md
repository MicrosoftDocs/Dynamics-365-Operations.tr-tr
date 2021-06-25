---
title: Konfigürasyon kuralları
description: Bu makalede, yapılandırma kuralları hakkında genel bilgiler sağlanmıştır. Yapılandırma kuralları, boyut tabanlı yapılandırma teknolojisini kullanan ürünler için ürün reçetesindeki (BOM) maddeler arasındaki ilişkileri tanımlar.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70aff927dfea602ee6c4ad5c195274248f831bcb
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190196"
---
# <a name="configuration-rules"></a><span data-ttu-id="7354e-104">Konfigürasyon kuralları</span><span class="sxs-lookup"><span data-stu-id="7354e-104">Configuration rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7354e-105">Bu makalede, yapılandırma kuralları hakkında genel bilgiler sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7354e-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="7354e-106">Yapılandırma kuralları, boyut tabanlı yapılandırma teknolojisini kullanan ürünler için ürün reçetesindeki (BOM) maddeler arasındaki ilişkileri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7354e-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="7354e-107">Boyut bazlı yapılandırma modelleri tanımladığınızda yapılandırma kuralları kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7354e-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="7354e-108">Yapılandırma kuralları ürün reçetesindeki belirli madde kombinasyonlarını zorunlu kılmak veya yasaklamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7354e-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="7354e-109">Bir ürün reçetesi oluşturulduktan ve ilgili maddeler kendi ilgili yapılandırma gruplarına atandıktan sonra, bir veya daha fazla yapılandırma kuralı tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7354e-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="7354e-110">İki madde birbirine aitse, dahil etmeyi sağlamak **Seç** işleci kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7354e-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="7354e-111">İki madde karşılıklı olarak birbirini dışlıyorsa, **Seçimi Kaldır** işleci dışlama sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7354e-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="7354e-112">**Not:** Bu bilgiler, yalnızca boyut bazlı yapılandırma teknolojisi kullanan ana ürünler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7354e-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="7354e-113">Yapılandırma kurallarında sonradan yapılan değişiklikler mevcut yapılandırmaları etkilemez.</span><span class="sxs-lookup"><span data-stu-id="7354e-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="7354e-114">Ancak, yeni bir yapılandırma tanımlamadan önce kuralları belirlemek veya kuralların değiştirildiğini düşündüğünüzde bunları kontrol etmek önemlidir.</span><span class="sxs-lookup"><span data-stu-id="7354e-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="7354e-115">**Not:** **Seç** yöntemi için, türetilen yapılandırma grubu, madde numarası ve yapılandırma otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="7354e-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="7354e-116">**Seçimi Kaldır** yöntemi için, türetilen yapılandırma grubu, madde numarası ve yapılandırma seçilemez.</span><span class="sxs-lookup"><span data-stu-id="7354e-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7354e-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7354e-117">Additional resources</span></span>

[<span data-ttu-id="7354e-118">Boyut tabanlı ürün yapılandırmasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="7354e-118">Dimension-based product configuration overview</span></span>](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]