---
title: Tahmin modelini geliştirme (önizleme)
description: Bu konu, tahmin modellerinin performansını artırmak için kullanabileceğiniz özellikleri açıklamaktadır.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186654"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="4d5a7-103">Tahmin modelini geliştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="4d5a7-104">Bu konu, tahmin modellerinin performansını artırmak için kullanabileceğiniz özellikleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="4d5a7-105">Modelinizi Microsoft Dynamics 365 Finance'teki **Müşteri ödeme tahminleri** çalışma alanında geliştirmeye başlarsınız.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="4d5a7-106">Ardından geliştirme adımları AI Builder'da tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="4d5a7-107">Geçmiş sonuçları seçme</span><span class="sxs-lookup"><span data-stu-id="4d5a7-107">Select historical outcomes</span></span>

<span data-ttu-id="4d5a7-108">Önce faturalar için üç olası sonucu seçersiniz: **Zamanında**, **Geç** ve **Çok geç**.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="4d5a7-109">Üç sonuç da seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-109">All three outcomes should be selected.</span></span> <span data-ttu-id="4d5a7-110">Sonuçlardan herhangi birinin seçimini kaldırırsanız eğitim faturalar eğitim işleminde filtrelenerek çıkarılır ve tahminin doğruluğu azalır.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="4d5a7-111">[![Sonuçları onaylama](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="4d5a7-112">Kuruluşunuz yalnızca iki sonuç gerektiriyorsa **Geç** ve **Çok geç** eşiklerini 0 (sıfır) gün olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="4d5a7-113">Bu şekilde tahmini etkili bir şekilde ikili duruma daraltabilirsiniz: **Zamanında** veya **Geç**.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="4d5a7-114">Alanları seçin</span><span class="sxs-lookup"><span data-stu-id="4d5a7-114">Select fields</span></span>

<span data-ttu-id="4d5a7-115">Modele dahil edilecek alanları seçerken, bu listenin Azure Data Lake içindeki verilerle eşlenen Microsoft Dataverse tablosundaki tüm kullanılabilir alanlarını içerdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Microsoft Dataverse table that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="4d5a7-116">Bu alanlardan bazıları **seçilmemelidir**.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="4d5a7-117">Seçilmemesi gereken alanlar üç kategoriden birine girer:</span><span class="sxs-lookup"><span data-stu-id="4d5a7-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="4d5a7-118">Alan, Dataverse tablosu için gereklidir ancak veri gölünde alanla ilgili destekleyici veri yoktur.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-118">The field is required for the Dataverse table, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="4d5a7-119">Alan bir kimlik olduğundan makine öğrenimi özelliği için bir anlam ifade etmez.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="4d5a7-120">Alan, tahmin sırasında kullanılamayacak bilgileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="4d5a7-121">Aşağıdaki bölümlerde, fatura ve müşteri varlıkları için kullanılabilir alanlar gösterilir ve eğitim için **seçilmemesi** gereken alanlar listelenir.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="4d5a7-122">Bu alanların her biri için belirtilen kategori, önceki listede yer alan kategorilere başvurur.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-dataverse-table"></a><span data-ttu-id="4d5a7-123">Fatura Dataverse tablosu</span><span class="sxs-lookup"><span data-stu-id="4d5a7-123">Invoice Dataverse table</span></span>

<span data-ttu-id="4d5a7-124">Aşağıdaki şekilde, fatura tablosu için kullanılabilir alanlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-124">The following illustration shows the fields that are available for the invoice table.</span></span>

<span data-ttu-id="4d5a7-125">[![Fatura tablosu için kullanılabilir alanlar](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-125">[![Available fields for the invoice table](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="4d5a7-126">Eğitim için aşağıdaki alanlar seçilmemelidir:</span><span class="sxs-lookup"><span data-stu-id="4d5a7-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="4d5a7-127">**Fatura Hesabı** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="4d5a7-128">**Kapalı** (kategori 3): Bu alan, faturaları eğitim (kapalı) ve tahmin (kapalı değil) için filtrelemek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="4d5a7-129">**Ad** (kategori 1)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-129">**Name** (category 1)</span></span>
- <span data-ttu-id="4d5a7-130">**Kaynak kimliği** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="4d5a7-131">**Kaynak kaydı** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="4d5a7-132">**Kaynak tablosu** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-132">**Source table** (category 2)</span></span>

### <a name="customer-dataverse-table"></a><span data-ttu-id="4d5a7-133">Müşteri Dataverse tablosu</span><span class="sxs-lookup"><span data-stu-id="4d5a7-133">Customer Dataverse table</span></span>

<span data-ttu-id="4d5a7-134">Aşağıdaki şekilde, müşteri tablosu için kullanılabilir alanlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-134">The following illustration shows the fields that are available for the customer table.</span></span>

<span data-ttu-id="4d5a7-135">[![Müşteri tablosu için kullanılabilir alanlar](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-135">[![Available fields for the customer table](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="4d5a7-136">Eğitim için aşağıdaki alan seçilmemelidir:</span><span class="sxs-lookup"><span data-stu-id="4d5a7-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="4d5a7-137">**Satır benzersiz anahtarı** (Kategori 2)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="4d5a7-138">Filtreler</span><span class="sxs-lookup"><span data-stu-id="4d5a7-138">Filters</span></span>

<span data-ttu-id="4d5a7-139">Filtreler, şu anda Müşteri ödeme tahmini senaryosunu desteklemez.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="4d5a7-140">Bu nedenle, **Bu adımı atla**'yı seçin ve özet sayfasına devam edin.</span><span class="sxs-lookup"><span data-stu-id="4d5a7-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="4d5a7-141">[![Filtrelerle modeli odaklama](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="4d5a7-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
