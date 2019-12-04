---
title: Master planlama ve birden çok tesis işlevine genel bakış
description: Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0b715e0c17263519a9bb1b3780170812271d93d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813765"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="ae921-103">Master planlama ve birden çok tesis işlevine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ae921-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae921-104">Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="ae921-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="ae921-105">Tesis boyutu zorunludur ve ambar boyutunu da zorunlu olacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae921-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="ae921-106">Bir boyut zorunlu olduğunda tüm boyut hareketlerine bir boyut değeri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ae921-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="ae921-107">Böylece master planlama sırasında, başlangıç talebi için tesis ve ambar bilinir.</span><span class="sxs-lookup"><span data-stu-id="ae921-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="ae921-108">Ayrıca tesis boyutu, daha alt düzey taleplerin açılımı sırasında tesisin değeri değişmeyecek şekilde tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="ae921-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="ae921-109">Ambar zorunlu olarak ayarlanmadığında başlangıç talebinden bilinemez.</span><span class="sxs-lookup"><span data-stu-id="ae921-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="ae921-110">Planlama altyapısı, kullanılacak ambarı madde ve ayrı ambar için tanımlanan ayarlara ve sipariş satırının ayrıntılarına göre belirlemelidir.</span><span class="sxs-lookup"><span data-stu-id="ae921-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="ae921-111">Aşağıdaki konularda, farklı ayarlar tanımlandığında planlama altyapısının kullanılacak ambarı belirlemek için nasıl çalıştığını açıklanır.</span><span class="sxs-lookup"><span data-stu-id="ae921-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="ae921-112">Tesis ve ambar kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="ae921-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ae921-113">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="ae921-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ae921-114">Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="ae921-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ae921-115">Tesis kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="ae921-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ae921-116">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="ae921-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



