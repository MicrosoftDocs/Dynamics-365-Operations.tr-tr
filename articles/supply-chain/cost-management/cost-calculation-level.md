---
title: Maliyet hesaplama düzeyi
description: Bu konuda, maliyet hesaplama düzeyi olarak adlandırılan ürün reçetesi (BOM) düzeyi açıklanmaktadır. Bu ürün reçetesi düzeyi, üretim ve toplu iş emirlerini hesaplamalarından çıkarır.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410990"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="6d170-104">Maliyet hesaplama düzeyi</span><span class="sxs-lookup"><span data-stu-id="6d170-104">Cost calculation level</span></span>

<span data-ttu-id="6d170-105">**Maliyet hesaplama düzeyi** adlı ürün reçetesi düzeyi, üretim emirlerini ve toplu iş emirlerini hesaplamalarından çıkarır.</span><span class="sxs-lookup"><span data-stu-id="6d170-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="6d170-106">Sistem bu düzeyi, maliyetlendirme sürümlerindeki maliyet hesaplamalarını çalıştırdığında kullanır.</span><span class="sxs-lookup"><span data-stu-id="6d170-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="6d170-107">Yeniden hesaplama ve stok kapanışı gibi işlemlerde, sistem bunun yerine **maliyetlendirme düzeyi** BOM düzeyini kullanır.</span><span class="sxs-lookup"><span data-stu-id="6d170-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="6d170-108">Aşağıdaki basit senaryo, **maliyet hesaplama düzeyi** BOM düzeyi ile **Maliyetlendirme düzeyi** BOM düzeyi arasındaki farkları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d170-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="6d170-109">Üç ürününüz var: A, B ve C. Ürün C, ürün B'nin bileşenidir ve B ürünü, A ürününün bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="6d170-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="6d170-110">**Maliyetlendirme düzeyi** aşağıdaki BOM düzeylerini atar:</span><span class="sxs-lookup"><span data-stu-id="6d170-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6d170-111">**Ürün A:** 0</span><span class="sxs-lookup"><span data-stu-id="6d170-111">**Product A:** 0</span></span>
    - <span data-ttu-id="6d170-112">**Ürün B:** 1</span><span class="sxs-lookup"><span data-stu-id="6d170-112">**Product B:** 1</span></span>
    - <span data-ttu-id="6d170-113">**Ürün C:** 2</span><span class="sxs-lookup"><span data-stu-id="6d170-113">**Product C:** 2</span></span>

- <span data-ttu-id="6d170-114">**Maliyet hesaplama düzeyi** aşağıdaki BOM düzeylerini atar:</span><span class="sxs-lookup"><span data-stu-id="6d170-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6d170-115">**Ürün A:** 0</span><span class="sxs-lookup"><span data-stu-id="6d170-115">**Product A:** 0</span></span>
    - <span data-ttu-id="6d170-116">**Ürün B:** 1</span><span class="sxs-lookup"><span data-stu-id="6d170-116">**Product B:** 1</span></span>
    - <span data-ttu-id="6d170-117">**Ürün C:** 2</span><span class="sxs-lookup"><span data-stu-id="6d170-117">**Product C:** 2</span></span>

<span data-ttu-id="6d170-118">Daha sonra ürün C'nin üretim emri oluşturulur ve üretim emri ürün reçetesine bir ürün A eklenir.</span><span class="sxs-lookup"><span data-stu-id="6d170-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="6d170-119">Sipariş tahmini yapıldıktan sonra, BOM düzeyleri aşağıdaki şekilde güncelleştirilir:</span><span class="sxs-lookup"><span data-stu-id="6d170-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="6d170-120">**Maliyetlendirme düzeyi** aşağıdaki BOM düzeylerini atar:</span><span class="sxs-lookup"><span data-stu-id="6d170-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6d170-121">**Ürün B:** 1</span><span class="sxs-lookup"><span data-stu-id="6d170-121">**Product B:** 1</span></span>
    - <span data-ttu-id="6d170-122">**Ürün C:** 2</span><span class="sxs-lookup"><span data-stu-id="6d170-122">**Product C:** 2</span></span>
    - <span data-ttu-id="6d170-123">**Ürün A:** 3</span><span class="sxs-lookup"><span data-stu-id="6d170-123">**Product A:** 3</span></span>

- <span data-ttu-id="6d170-124">**Maliyet hesaplama düzeyi** aşağıdaki BOM düzeylerini atar:</span><span class="sxs-lookup"><span data-stu-id="6d170-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="6d170-125">**Ürün A:** 0</span><span class="sxs-lookup"><span data-stu-id="6d170-125">**Product A:** 0</span></span>
    - <span data-ttu-id="6d170-126">**Ürün B:** 1</span><span class="sxs-lookup"><span data-stu-id="6d170-126">**Product B:** 1</span></span>
    - <span data-ttu-id="6d170-127">**Ürün C:** 2</span><span class="sxs-lookup"><span data-stu-id="6d170-127">**Product C:** 2</span></span>

<span data-ttu-id="6d170-128">Bu davranış, üretim emri ürün reçeteleri üzerindeki değişikliklerin sonraki maliyet hesaplamalarını etkilememesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6d170-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
