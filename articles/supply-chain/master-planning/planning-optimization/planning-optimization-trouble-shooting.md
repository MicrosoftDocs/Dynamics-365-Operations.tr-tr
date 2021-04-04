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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457341"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="38630-103">Planlamayı En İyi Duruma Getirmeyle İlgili Sorunları Giderme</span><span class="sxs-lookup"><span data-stu-id="38630-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38630-104">Bu konu, Planlamayı En İyi Duruma Getirme ile çalışırken karşılaşabileceğiniz yaygın sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="38630-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="38630-105">Planlamayı En İyi Duruma Getirme eklentisinin yüklenmesi tamamlanmadı</span><span class="sxs-lookup"><span data-stu-id="38630-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="38630-106">Planlamayı En İyi Duruma Getirme; etkin bir LifeCycle Services (LCS), yüksek kullanılabilirlik ortamı, katman 2 veya üstü (OneBox ortamı olmayan), Dynamics 365 Supply Chain Management 10.0.7 veya daha yeni bir sürümünü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="38630-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="38630-107">Eklentiyi OneBox ortamına yüklemeye çalışırsanız, yükleme tamamlanmaz.</span><span class="sxs-lookup"><span data-stu-id="38630-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="38630-108">**Düzeltme**: Yüklemeyi iptal edin ve yüksek kullanılabilirlik ortamı, katman 2 veya daha yüksek bir ortam (OneBox ortamı olmayan) kullanın.</span><span class="sxs-lookup"><span data-stu-id="38630-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="38630-109">Planlamayı En İyi Duruma Getirme etkinleştirildiğinde toplu işler planlanamıyor</span><span class="sxs-lookup"><span data-stu-id="38630-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="38630-110">Planlamayı En İyi Duruma Getirme'yi etkinleştirdiğinizde, yerleşik ana planlama altyapısı otomatik olarak devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="38630-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="38630-111">Yerleşik Supply Chain Management planlama altyapısı için oluşturulan ana planlama toplu işleri, Planlamayı En İyi Duruma Getirme etkinken tetiklenirse bu işler başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="38630-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="38630-112">*Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi* gibi bir hata iletisi alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38630-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="38630-113">**Düzeltme**: Yerleşik Supply Chain Management planlama altyapısı için oluşturulan tüm ana planlama toplu işlerini iptal edin.</span><span class="sxs-lookup"><span data-stu-id="38630-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="38630-114">Planlamayı En İyi Duruma Getirme sonuçları önceki sonuçlardan farklı</span><span class="sxs-lookup"><span data-stu-id="38630-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="38630-115">Planlamayı En İyi Duruma Getirme, bazı alanlardaki yerleşik ana planlama tasarımdan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="38630-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="38630-116">Bunun nedeni beklemedeki özellikler de olabilir.</span><span class="sxs-lookup"><span data-stu-id="38630-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="38630-117">**Düzeltme**: Planlamayı En İyi Duruma Getirme uygun analizini çalıştırın ve sonra, etkisini anlamak için ilgili belgelere başvurarak sonuçları analiz edin.</span><span class="sxs-lookup"><span data-stu-id="38630-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="38630-118">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="38630-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="38630-119">Planlamayı En İyi Duruma Getirme etkinleştirilemiyor</span><span class="sxs-lookup"><span data-stu-id="38630-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="38630-120">**Planlamayı En İyi Duruma Getirmeyi Kullan** ayarını **Evet** olarak ayarlamadan önce **Bağlantı durumu** değerinin **Bağlı** olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="38630-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="38630-121">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="38630-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="38630-122">**Düzeltme**: Planlamayı En İyi Duruma Getirme eklentisinin başarıyla yüklendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="38630-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="38630-123">CTP sırasında hata iletisi gösteriliyor</span><span class="sxs-lookup"><span data-stu-id="38630-123">Error message is shown during CTP</span></span>

<span data-ttu-id="38630-124">Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, bir satış siparişinden teslim edilebilir miktarı (CTP) çalıştırmayı denerseniz şu hata iletisini alırsınız: *Bu işlem, Planlamayı En İyi Duruma Getirme etkinken desteklenmeyen ana planlamayı tetikledi*.</span><span class="sxs-lookup"><span data-stu-id="38630-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="38630-125">Bu, üretim emirleri desteğinin bir parçası olarak planlanan beklemedeki bir özellikle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="38630-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="38630-126">**Düzeltme:** CTP desteği kullanılabilir hale gelene kadar Planlamayı En İyi Hale Getirme etkinken CTP hesaplamalarından kaçının.</span><span class="sxs-lookup"><span data-stu-id="38630-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38630-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="38630-127">Additional resources</span></span>

[<span data-ttu-id="38630-128">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="38630-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="38630-129">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="38630-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]