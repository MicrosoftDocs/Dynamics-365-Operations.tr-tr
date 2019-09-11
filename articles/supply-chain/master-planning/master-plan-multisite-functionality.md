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
ms.openlocfilehash: 4f05e3efd1716a27a659ae40145f37bb0b3d977f
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865428"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="46582-103">Master planlama ve birden çok tesis işlevine genel bakış</span><span class="sxs-lookup"><span data-stu-id="46582-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46582-104">Master planlama, tesis ve ambar stok boyutlarının ayarlarını dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="46582-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="46582-105">Tesis boyutu zorunludur ve ambar boyutunu da zorunlu olacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46582-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="46582-106">Bir boyut zorunlu olduğunda tüm boyut hareketlerine bir boyut değeri girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="46582-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="46582-107">Böylece master planlama sırasında, başlangıç talebi için tesis ve ambar bilinir.</span><span class="sxs-lookup"><span data-stu-id="46582-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="46582-108">Ayrıca tesis boyutu, daha alt düzey taleplerin açılımı sırasında tesisin değeri değişmeyecek şekilde tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="46582-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="46582-109">Ambar zorunlu olarak ayarlanmadığında başlangıç talebinden bilinemez.</span><span class="sxs-lookup"><span data-stu-id="46582-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="46582-110">Planlama altyapısı, kullanılacak ambarı madde ve ayrı ambar için tanımlanan ayarlara ve sipariş satırının ayrıntılarına göre belirlemelidir.</span><span class="sxs-lookup"><span data-stu-id="46582-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="46582-111">Aşağıdaki konularda, farklı ayarlar tanımlandığında planlama altyapısının kullanılacak ambarı belirlemek için nasıl çalıştığını açıklanır.</span><span class="sxs-lookup"><span data-stu-id="46582-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="46582-112">Master planlama - tesis ve ambar kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="46582-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="46582-113">Master planlama - tesis kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="46582-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="46582-114">Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="46582-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="46582-115">Master planlama - tesis kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="46582-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="46582-116">Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği</span><span class="sxs-lookup"><span data-stu-id="46582-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



