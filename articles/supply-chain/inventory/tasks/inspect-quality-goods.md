---
title: Malların kalitesini denetleme
description: Bu konu, kalite emirlerinin nasıl işleneceğini açıklar.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956146"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="e7b4a-103">Malların kalitesini denetleme</span><span class="sxs-lookup"><span data-stu-id="e7b4a-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7b4a-104">Bu konu, kalite emirlerinin nasıl işleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="e7b4a-105">Kalite incelemeleri genellikle bir kalite memuru tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="e7b4a-106">Standart demo verileri yüklüyse, bu konudaki prosedürleri tamamlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="e7b4a-107">Demo verilerini kullanmak için, başlamadan önce *USMF* tüzel kişiliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="e7b4a-108">Daha sonra satınalma siparişi *000016*'yı onaylamanız ve bir ürün girişini deftere nakletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="e7b4a-109">Bir kalite emri otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="e7b4a-110">1. Adım: Bir kalite emri seçin</span><span class="sxs-lookup"><span data-stu-id="e7b4a-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="e7b4a-111">Bir kalite emri seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="e7b4a-112">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="e7b4a-113">Bu yordamı başlatmadan önce oluşturulan kalite emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="e7b4a-114">2. Adım: Test sonuçlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="e7b4a-114">Step 2: Record test results</span></span>

<span data-ttu-id="e7b4a-115">Test sonuçlarını kaydetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="e7b4a-116">**Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-116">Select **Results**.</span></span>
1. <span data-ttu-id="e7b4a-117">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-117">Select **Edit**.</span></span>
1. <span data-ttu-id="e7b4a-118">**Sonuç miktarı** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="e7b4a-119">**Sonuç** alanında, istenilen kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="e7b4a-120">Bu örnekte sonuç, önceden tanımlanmış bir sonuca bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="e7b4a-121">Genellikle, bir ebat veya başka bir boyut gibi, daha belirli bir test sonucu kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="e7b4a-122">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-122">Select **Save**.</span></span>
1. <span data-ttu-id="e7b4a-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="e7b4a-124">3. Adım: Kalite emrini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="e7b4a-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="e7b4a-125">Bir kalite emrini doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="e7b4a-126">**Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-126">Select **Validate**.</span></span>
1. <span data-ttu-id="e7b4a-127">**Doğrulayan kişi** alanında, denetimi yapan kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="e7b4a-128">**Seç** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-128">Select **Select**.</span></span>
1. <span data-ttu-id="e7b4a-129">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-129">Select **OK**.</span></span>
1. <span data-ttu-id="e7b4a-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e7b4a-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
