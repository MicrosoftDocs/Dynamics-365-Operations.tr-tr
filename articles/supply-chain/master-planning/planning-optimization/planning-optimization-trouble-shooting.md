---
title: Planlamayı En İyi Duruma Getirmeyle İlgili Sorunları Giderme
description: Bu konu, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
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
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439078"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="c7de6-103">Planlamayı En İyi Duruma Getirmeyle İlgili Sorunları Giderme</span><span class="sxs-lookup"><span data-stu-id="c7de6-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7de6-104">Bu konu, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz yaygın sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7de6-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="c7de6-105">Planlamayı En İyi Duruma Getirme eklentisinin yüklenmesi tamamlanmadı</span><span class="sxs-lookup"><span data-stu-id="c7de6-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="c7de6-106">Planlamayı En İyi Duruma Getirme; etkin bir LifeCycle Services (LCS), yüksek kullanılabilirlik ortamı, katman 2 veya üstü (OneBox ortamı olmayan), Dynamics 365 Supply Chain Management 10.0.7 veya daha yeni bir sürümünü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c7de6-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="c7de6-107">Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz.</span><span class="sxs-lookup"><span data-stu-id="c7de6-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="c7de6-108">**Düzeltme**: Yüklemeyi iptal edin ve yüksek kullanılabilirlik ortamı, katman 2 veya daha yüksek bir ortam (OneBox ortamı olmayan) kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7de6-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="c7de6-109">Planlamayı En İyi Duruma Getirme etkinleştirildiğinde toplu işler planlanamıyor</span><span class="sxs-lookup"><span data-stu-id="c7de6-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="c7de6-110">Planlamayı En İyi Duruma Getirme'yi etkinleştirdiğinizde, yerleşik ana planlama altyapısı otomatik olarak devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="c7de6-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="c7de6-111">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan ana planlama toplu işleri, Planlamayı En İyi Duruma Getirme etkinken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="c7de6-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="c7de6-112">*Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi* gibi bir hata iletisi alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7de6-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="c7de6-113">**Düzeltme**: Yerleşik Supply Chain Management planlama altyapısı için oluşturulan tüm ana planlama toplu işlerini iptal edin.</span><span class="sxs-lookup"><span data-stu-id="c7de6-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="c7de6-114">Planlamayı En İyi Duruma Getirme sonuçları önceki sonuçlardan farklı</span><span class="sxs-lookup"><span data-stu-id="c7de6-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="c7de6-115">Planlamayı En İyi Duruma Getirme, bazı alanlardaki yerleşik ana planlama tasarımdan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="c7de6-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="c7de6-116">Bunun nedeni beklemedeki özellikler de olabilir.</span><span class="sxs-lookup"><span data-stu-id="c7de6-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="c7de6-117">**Düzeltme**: Planlamayı En İyi Duruma Getirme uygun analizini çalıştırın ve sonra, etkisini anlamak için ilgili belgelere başvurarak sonuçları analiz edin.</span><span class="sxs-lookup"><span data-stu-id="c7de6-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="c7de6-118">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c7de6-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="c7de6-119">Ana planlama, kapsam zaman dilimine uymuyor</span><span class="sxs-lookup"><span data-stu-id="c7de6-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="c7de6-120">Bunun nedeni, Planlamayı En İyi Duruma Getirme için bekleyen bir özelliktir.</span><span class="sxs-lookup"><span data-stu-id="c7de6-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="c7de6-121">**Düzeltme**: Beklemedeki özellik kullanılabilir hale gelinceye kadar, kapsam zaman diliminin dışındaki tedarik önerilerini kaldırmak için planlanmış siparişleri filtreleyin veya silin.</span><span class="sxs-lookup"><span data-stu-id="c7de6-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="c7de6-122">Planlamayı En İyi Duruma Getirme etkinleştirilemiyor</span><span class="sxs-lookup"><span data-stu-id="c7de6-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="c7de6-123">**Planlamayı En İyi Duruma Getirmeyi Kullan** ayarını **Evet** olarak ayarlamadan önce **Bağlantı durumu** değerinin **Bağlı** olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c7de6-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="c7de6-124">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="c7de6-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="c7de6-125">**Düzeltme**: Planlamayı En İyi Duruma Getirme eklentisinin başarıyla yüklendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="c7de6-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="c7de6-126">CTP sırasında hata iletisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="c7de6-126">Error message is shown during CTP</span></span>

<span data-ttu-id="c7de6-127">Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, bir satış siparişinden teslim edilebilir miktarı (CTP) çalıştırmayı denerseniz şu hata iletisini alırsınız: *Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi*.</span><span class="sxs-lookup"><span data-stu-id="c7de6-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="c7de6-128">Bu, üretim emirleri desteğinin bir parçası olarak planlanan beklemedeki bir özellikle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="c7de6-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="c7de6-129">**Düzeltme:** CTP desteği kullanılabilir hale gelene kadar Planlamayı En İyi Hale Getirme etkinken CTP hesaplamalarından kaçının.</span><span class="sxs-lookup"><span data-stu-id="c7de6-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7de6-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c7de6-130">Additional resources</span></span>

[<span data-ttu-id="c7de6-131">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="c7de6-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c7de6-132">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="c7de6-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
