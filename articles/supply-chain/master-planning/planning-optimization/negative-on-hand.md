---
title: Eldeki eksi miktarları planlama
description: Bu konu, planlama en iyileştirmesi kullanılırken eldeki eksi stokun nasıl işlendiğini açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323520"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="8fd1d-103">Eldeki eksi miktarları planlama</span><span class="sxs-lookup"><span data-stu-id="8fd1d-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fd1d-104">Sistem negatif toplu eldeki miktarı gösteriyorsa, planlama altyapısı miktardan fazla tedarik oluşmasını önlemeye yardımcı olmak için miktarı 0 (sıfır) olarak değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="8fd1d-105">Bu işlevsellik şu şekilde çalışır:</span><span class="sxs-lookup"><span data-stu-id="8fd1d-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="8fd1d-106">Planlama en iyileştirme özelliği, eldeki miktarları en düşük kapsam boyutları düzeyinde toplar.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="8fd1d-107">(Örneğin, *yerleşim* bir karşılama boyutu değilse, planlama en iyileştirme *ambar* düzeyinde eldeki miktarları toplar.)</span><span class="sxs-lookup"><span data-stu-id="8fd1d-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="8fd1d-108">En düşük karşılama boyutlarının eldeki toplam miktarı negatifse, sistem eldeki miktarın gerçekten 0 (sıfır) olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fd1d-109">Planlama sistemi yalnızca giriş verileri kadar kesin olabilir.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="8fd1d-110">Giriş verileri doğru değilse, eksi eldeki kayıtlar, Microsoft Dynamics 365 Supply Chain Management'ın stok bilgilerinin gerçek dünya ile eşitlenmemiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="8fd1d-111">Bu nedenle, planlama sonucu düzden olacaktır.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="8fd1d-112">Doğru planlama sonucu elde etmek için, eksi eldeki bir miktarı gösteren kayıt sayısını en aza indirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="8fd1d-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8fd1d-113">Example 1</span></span>

<span data-ttu-id="8fd1d-114">Ambar 13, aşağıdaki şekilde yapılandırılır:</span><span class="sxs-lookup"><span data-stu-id="8fd1d-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="8fd1d-115">**Kapsam kodu:** Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="8fd1d-116">**Minimum:** 15 parça (adet)</span><span class="sxs-lookup"><span data-stu-id="8fd1d-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="8fd1d-117">**En fazla** : 25 adet.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="8fd1d-118">Kapsam boyutlarının en düşük düzeyi *ambar*, aşağıdaki eldeki miktarlar *yerleşim* düzeyinde kaydedilir:</span><span class="sxs-lookup"><span data-stu-id="8fd1d-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="8fd1d-119">**Site 1, ambar 13, konum 1:** 20 adet.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="8fd1d-120">**Site 1 ambar 13, konum 2:** &minus;8 adet.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="8fd1d-121">Bu nedenle, ambar 13'ün eldeki toplama miktarı 12 adet olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="8fd1d-122">(= 20 adet</span><span class="sxs-lookup"><span data-stu-id="8fd1d-122">(= 20 pcs.</span></span> <span data-ttu-id="8fd1d-123">&minus; 8 adet.).</span><span class="sxs-lookup"><span data-stu-id="8fd1d-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="8fd1d-124">Bu durumda, planlama alt yapısı 12 adette toplam eldeki miktarı kullanır.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="8fd1d-125">ambar 13 için.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-125">for warehouse 13.</span></span>

<span data-ttu-id="8fd1d-126">Sonuç 13 adete ait planlı bir sipariş.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="8fd1d-127">(= 25 adet</span><span class="sxs-lookup"><span data-stu-id="8fd1d-127">(= 25 pcs.</span></span> <span data-ttu-id="8fd1d-128">&minus; 12 adet) 13 numaralı ambarı 12 adetten</span><span class="sxs-lookup"><span data-stu-id="8fd1d-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="8fd1d-129">25 adede kadar doldurmak için.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="8fd1d-130">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8fd1d-130">Example 2</span></span>

<span data-ttu-id="8fd1d-131">Ambar 13, aşağıdaki şekilde yapılandırılır:</span><span class="sxs-lookup"><span data-stu-id="8fd1d-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="8fd1d-132">**Kapsam kodu:** Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="8fd1d-133">**En düşük:** 15 adet</span><span class="sxs-lookup"><span data-stu-id="8fd1d-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="8fd1d-134">**En fazla** : 25 adet.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="8fd1d-135">Kapsam boyutlarının en düşük düzeyi *ambar*, aşağıdaki eldeki miktarlar *yerleşim* düzeyinde kaydedilir:</span><span class="sxs-lookup"><span data-stu-id="8fd1d-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="8fd1d-136">**Site 1, ambar 13, konum 1:** 4 adet.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="8fd1d-137">**Site 1 ambar 13, konum 2:** &minus;8 adet.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="8fd1d-138">Bu nedenle, ambar 13'ün eldeki toplama miktarı &minus;4 adet olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="8fd1d-139">(= 4 adet</span><span class="sxs-lookup"><span data-stu-id="8fd1d-139">(= 4 pcs.</span></span> <span data-ttu-id="8fd1d-140">&minus; 8 adet.).</span><span class="sxs-lookup"><span data-stu-id="8fd1d-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="8fd1d-141">Diğer bir deyişle, 0'dan (sıfır) azdır.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="8fd1d-142">Bu durumda, planlama alt yapısı, 13 ambar için eldeki miktarın 0 PC olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="8fd1d-143">&minus;4 adet yerine.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="8fd1d-144">Sonuç 25 adete ait planlı bir sipariş.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="8fd1d-145">(= 25 adet</span><span class="sxs-lookup"><span data-stu-id="8fd1d-145">(= 25 pcs.</span></span> <span data-ttu-id="8fd1d-146">&minus; 0 adet) 13 numaralı ambarı 0 adetten</span><span class="sxs-lookup"><span data-stu-id="8fd1d-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="8fd1d-147">25 adede kadar doldurmak için.</span><span class="sxs-lookup"><span data-stu-id="8fd1d-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="8fd1d-148">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8fd1d-148">Related resources</span></span>

[<span data-ttu-id="8fd1d-149">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="8fd1d-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="8fd1d-150">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="8fd1d-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="8fd1d-151">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="8fd1d-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="8fd1d-152">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8fd1d-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="8fd1d-153">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="8fd1d-153">Cancel a planning job</span></span>](cancel-planning-job.md)
