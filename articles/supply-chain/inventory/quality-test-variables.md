---
title: Kalite yönetimi test değişkenleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle niteliksel testlerin kullanılabilmesi için, test değişkenlerinin nasıl oluşturulacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5102d09f5762a390d6fd3aadafcb2ed23820982
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021720"
---
# <a name="quality-management-test-variables"></a><span data-ttu-id="369eb-103">Kalite yönetimi test değişkenleri</span><span class="sxs-lookup"><span data-stu-id="369eb-103">Quality management test variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="369eb-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite emirleriyle niteliksel testlerin kullanılabilmesi için, test değişkenlerinin nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="369eb-104">This topic describes how to create test variables that can be used for qualitative tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="369eb-105">**Testler** sayfasında tanımlanan her niteliksel test için bir test değişkeni ve bu değişkenin olası çıktılarını (sonuçlar) tanımlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="369eb-105">For every qualitative test that is defined on the **Tests** page, you must define a test variable and its possible outcomes (results).</span></span> <span data-ttu-id="369eb-106">(Niteliksel testler için, **Testler** sayfası üzerinde **Tür** alanı *Seçenek* olarak ayarlanmıştır.)</span><span class="sxs-lookup"><span data-stu-id="369eb-106">(For qualitative tests, the **Type** field on the **Tests** page is set to *Option*.)</span></span>

<span data-ttu-id="369eb-107">Bir niteliksel testle ilişkili bir test değişkenine ait olası sonuçları ayarlamak, düzenlemek ve görüntülemek için **Test değişkenleri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="369eb-107">You use the **Test variables** page to set up, edit, and view the possible outcomes for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="369eb-108">Her bir sonuç için, test sonucu olarak bu sonucun seçildiği durumda testin başarılı veya başarısız olduğunu belirtmek için *Başarılı* veya *Başarısız* seçeneklerinden birini sonuç durumu olarak atarsınız.</span><span class="sxs-lookup"><span data-stu-id="369eb-108">For each outcome, you assign an outcome status of either *Pass* or *Fail* to indicate whether the test is passed or failed when that outcome is selected as a test result.</span></span> <span data-ttu-id="369eb-109">**Test grupları** sayfasını kullanarak bir test değişkenini ve test değişkeninin varsayılan sonucunu bir niteliksel teste atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="369eb-109">You use the **Test groups** page to assign a test variable and a default outcome for it to an individual qualitative test.</span></span>

<span data-ttu-id="369eb-110">Her test değişkeni için en az iki sonuç tanımlamanız önerilir: bu sonuçlardan birinin sonuç durumu *Başarılı* ve diğeri ise *Başarısız* olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="369eb-110">For every test variable, we recommend that you define at least two outcomes: one that has an outcome status of *Pass* and one that has an outcome status of *Fail*.</span></span> <span data-ttu-id="369eb-111">Tanımlanabilecek değişkenlerin veya sonuç sayısının bir limiti yoktur.</span><span class="sxs-lookup"><span data-stu-id="369eb-111">There is no limit on the total number of variables or outcomes that can be defined.</span></span> <span data-ttu-id="369eb-112">Ek olarak, birden fazla test, sonuçları kaydetmek için aynı test değişkenlerini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="369eb-112">Additionally, multiple tests can use the same test variables to record results.</span></span>

## <a name="examples-of-test-variables"></a><span data-ttu-id="369eb-113">Test değişkenlerine örnekler</span><span class="sxs-lookup"><span data-stu-id="369eb-113">Examples of test variables</span></span>

### <a name="example-1"></a><span data-ttu-id="369eb-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="369eb-114">Example 1</span></span>

<span data-ttu-id="369eb-115">Bir üretim şirketi, üretilen malzemeler üzerinde iki test yapar.</span><span class="sxs-lookup"><span data-stu-id="369eb-115">A manufacturing company performs two tests on manufactured materials.</span></span> <span data-ttu-id="369eb-116">Bir testte, pH düzeyi bir renk şeridiyle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="369eb-116">In one test, the pH level is associated with a color strip.</span></span> <span data-ttu-id="369eb-117">Kabul edilebilir pH düzeyleri daha açık renklerde ve kabul edilemez pH düzeyleri daha koyu renklerdedir.</span><span class="sxs-lookup"><span data-stu-id="369eb-117">Acceptable pH levels are in lighter colors, and unacceptable pH levels are in darker colors.</span></span> <span data-ttu-id="369eb-118">Başka bir testte, birden çok görsel inceleme gerçekleştirilir ve kalite çalışanları, görsel incelemeden geçen maddelerin hatalı olup olmadığını belirlemek için kendi yargılarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="369eb-118">In another test, multiple visual inspections are performed, and quality workers use their judgement to determine whether the item passes or fails the visual inspection.</span></span>

### <a name="example-2"></a><span data-ttu-id="369eb-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="369eb-119">Example 2</span></span>

<span data-ttu-id="369eb-120">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="369eb-120">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="369eb-121">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="369eb-121">This inspection test has several variables.</span></span> <span data-ttu-id="369eb-122">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="369eb-122">One variable is taste, and the possible outcomes for it are good and bad.</span></span> <span data-ttu-id="369eb-123">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="369eb-123">A second variable is color, and the possible outcomes for it are too dark, too light, and correct.</span></span>

## <a name="create-a-test-variable"></a><span data-ttu-id="369eb-124">Yeni bir test değişkeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="369eb-124">Create a test variable</span></span>

<span data-ttu-id="369eb-125">Test değişkeni oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="369eb-125">Follow these steps to create a test variable.</span></span>

1. <span data-ttu-id="369eb-126">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Test değişkenleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="369eb-126">Go to **Inventory management \> Setup \> Quality control \> Test variables**.</span></span>
1. <span data-ttu-id="369eb-127">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="369eb-127">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="369eb-128">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="369eb-128">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="369eb-129">**Değişken** – Değişken için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="369eb-129">**Variable** – Enter a unique ID or name for the variable.</span></span>
    - <span data-ttu-id="369eb-130">**Açıklama**: – Değişkenin detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="369eb-130">**Description** – Enter a detailed description of the variable.</span></span>

1. <span data-ttu-id="369eb-131">Yeni satır seçiliyken, Eylem Bölmesinde **Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="369eb-131">While the new row is still selected, select **Outcomes** on the Action Pane.</span></span>
1. <span data-ttu-id="369eb-132">**Test değişkeni sonuçları** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="369eb-132">On the **Test variable outcomes** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="369eb-133">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="369eb-133">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="369eb-134">**Sonuç** – Sonuç için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="369eb-134">**Outcome** – Enter a unique ID or name for the outcome.</span></span>
    - <span data-ttu-id="369eb-135">**Açıklama**: – Sonucun detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="369eb-135">**Description** – Enter a detailed description of the outcome.</span></span>
    - <span data-ttu-id="369eb-136">**Sonuç durumu** – Her bir sonuç için, test sonucu olarak sonucun seçildiği durumda testin başarılı veya başarısız olduğunu belirtmek için *Başarılı* veya *Başarısız* seçeneklerinden birini sonuç durumu olarak atarsınız.</span><span class="sxs-lookup"><span data-stu-id="369eb-136">**Outcome status** – Select either *Pass* or *Fail* to indicate whether the test is passed or failed when the outcome is selected as a test result.</span></span>

1. <span data-ttu-id="369eb-137">Her bir ek sonuç için önceki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="369eb-137">Repeat the previous step for each additional outcome.</span></span> <span data-ttu-id="369eb-138">En az bir sonucun *Başarılı* sonuç durumuna sahip olduğundan ve en azından bir sonucun *Başarısız* sonuç durumuna sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="369eb-138">Make sure that at least one outcome has an outcome status of *Pass* and at least one has an outcome status of *Fail*.</span></span>
1. <span data-ttu-id="369eb-139">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="369eb-139">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="369eb-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="369eb-140">Additional resources</span></span>

- [<span data-ttu-id="369eb-141">Kalite yönetimi test gereçleri</span><span class="sxs-lookup"><span data-stu-id="369eb-141">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="369eb-142">Kalite yönetimi testleri</span><span class="sxs-lookup"><span data-stu-id="369eb-142">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="369eb-143">Kalite yönetimi test grupları</span><span class="sxs-lookup"><span data-stu-id="369eb-143">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
