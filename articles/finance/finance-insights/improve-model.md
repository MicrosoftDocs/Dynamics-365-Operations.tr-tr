---
title: Tahmin modelini geliştirme (önizleme)
description: Bu konu, tahmin modellerinin performansını artırmak için kullanabileceğiniz özellikleri açıklamaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646091"
---
# <a name="improve-the-prediction-model-preview"></a><span data-ttu-id="6949b-103">Tahmin modelini geliştirme (önizleme)</span><span class="sxs-lookup"><span data-stu-id="6949b-103">Improve the prediction model (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6949b-104">Bu konu, tahmin modellerinin performansını artırmak için kullanabileceğiniz özellikleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6949b-104">This topic describes features that you can use to improve the performance of prediction models.</span></span> <span data-ttu-id="6949b-105">Modelinizi Microsoft Dynamics 365 Finance'teki **Müşteri ödeme tahminleri** çalışma alanında geliştirmeye başlarsınız.</span><span class="sxs-lookup"><span data-stu-id="6949b-105">You start to improve your model in the **Customer payment predictions** workspace in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="6949b-106">Ardından geliştirme adımları AI Builder'da tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="6949b-106">The improvement steps are then completed in AI Builder.</span></span>

## <a name="select-historical-outcomes"></a><span data-ttu-id="6949b-107">Geçmiş sonuçları seçme</span><span class="sxs-lookup"><span data-stu-id="6949b-107">Select historical outcomes</span></span>

<span data-ttu-id="6949b-108">Önce faturalar için üç olası sonucu seçersiniz: **Zamanında**, **Geç** ve **Çok geç**.</span><span class="sxs-lookup"><span data-stu-id="6949b-108">You first select one or more of the three possible outcomes for invoices: **On time**, **Late**, and **Very late**.</span></span> <span data-ttu-id="6949b-109">Üç sonuç da seçilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6949b-109">All three outcomes should be selected.</span></span> <span data-ttu-id="6949b-110">Sonuçlardan herhangi birinin seçimini kaldırırsanız eğitim faturalar eğitim işleminde filtrelenerek çıkarılır ve tahminin doğruluğu azalır.</span><span class="sxs-lookup"><span data-stu-id="6949b-110">If you clear the selection of any of the outcomes, invoices will be filtered out of the training process and the accuracy of the prediction will be reduced.</span></span>

<span data-ttu-id="6949b-111">[![Sonuçları onaylama](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span><span class="sxs-lookup"><span data-stu-id="6949b-111">[![Confirming outcomes](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)</span></span>

<span data-ttu-id="6949b-112">Kuruluşunuz yalnızca iki sonuç gerektiriyorsa **Geç** ve **Çok geç** eşiklerini 0 (sıfır) gün olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6949b-112">If your organization requires only two outcomes, change the **Late** and **Very late** thresholds to 0 (zero) days.</span></span> <span data-ttu-id="6949b-113">Bu şekilde tahmini etkili bir şekilde ikili duruma daraltabilirsiniz: **Zamanında** veya **Geç**.</span><span class="sxs-lookup"><span data-stu-id="6949b-113">In this way, you effectively collapse the prediction to a binary state of **On time** or **Late**.</span></span>

## <a name="select-fields"></a><span data-ttu-id="6949b-114">Alanları seçin</span><span class="sxs-lookup"><span data-stu-id="6949b-114">Select fields</span></span>

<span data-ttu-id="6949b-115">Modele dahil edilecek alanları seçerken, bu listenin Azure Data Lake içindeki verilerle eşlenen tüm kullanılabilir Common Data Service alanlarını içerdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="6949b-115">When you're selecting fields to include in the model, be aware that the list includes all available fields in the Common Data Service entity that is mapped to the data in the Azure data lake.</span></span> <span data-ttu-id="6949b-116">Bu alanlardan bazıları **seçilmemelidir**.</span><span class="sxs-lookup"><span data-stu-id="6949b-116">Some of these fields should **not** be selected.</span></span> <span data-ttu-id="6949b-117">Seçilmemesi gereken alanlar üç kategoriden birine girer:</span><span class="sxs-lookup"><span data-stu-id="6949b-117">The fields that should not be selected fall into one of three categories:</span></span>

- <span data-ttu-id="6949b-118">Alan, Common Data Service varlığı için gereklidir ancak veri gölünde alanla ilgili destekleyici veri yoktur.</span><span class="sxs-lookup"><span data-stu-id="6949b-118">The field is required for the Common Data Service entity, but there is no backing data for it in the data lake.</span></span>
- <span data-ttu-id="6949b-119">Alan bir kimlik olduğundan makine öğrenimi özelliği için bir anlam ifade etmez.</span><span class="sxs-lookup"><span data-stu-id="6949b-119">The field is an ID and therefore doesn't make sense for a machine learning feature.</span></span>
- <span data-ttu-id="6949b-120">Alan, tahmin sırasında kullanılamayacak bilgileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6949b-120">The field represents information that won't be available during prediction.</span></span>

<span data-ttu-id="6949b-121">Aşağıdaki bölümlerde, fatura ve müşteri varlıkları için kullanılabilir alanlar gösterilir ve eğitim için **seçilmemesi** gereken alanlar listelenir.</span><span class="sxs-lookup"><span data-stu-id="6949b-121">The following sections show the fields that are available for the invoice and customer entities, and list the fields that should **not** be selected for training.</span></span> <span data-ttu-id="6949b-122">Bu alanların her biri için belirtilen kategori, önceki listede yer alan kategorilere başvurur.</span><span class="sxs-lookup"><span data-stu-id="6949b-122">The category that is specified for each of those fields refers to the categories in the preceding list.</span></span>
 
### <a name="invoice-common-data-model-entity"></a><span data-ttu-id="6949b-123">Fatura Common Data Model varlığı</span><span class="sxs-lookup"><span data-stu-id="6949b-123">Invoice Common Data Model entity</span></span>

<span data-ttu-id="6949b-124">Aşağıdaki şekilde, fatura varlığı için kullanılabilir alanlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6949b-124">The following illustration shows the fields that are available for the invoice entity.</span></span>

<span data-ttu-id="6949b-125">[![Fatura varlığı için kullanılabilir alanlar](./media/available-fields.png)](./media/available-fields.png)</span><span class="sxs-lookup"><span data-stu-id="6949b-125">[![Available fields for the invoice entity](./media/available-fields.png)](./media/available-fields.png)</span></span>

<span data-ttu-id="6949b-126">Eğitim için aşağıdaki alanlar seçilmemelidir:</span><span class="sxs-lookup"><span data-stu-id="6949b-126">The following fields should not be selected for training:</span></span>

- <span data-ttu-id="6949b-127">**Fatura Hesabı** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6949b-127">**Invoice Account** (category 2)</span></span>
- <span data-ttu-id="6949b-128">**Kapalı** (kategori 3): Bu alan, faturaları eğitim (kapalı) ve tahmin (kapalı değil) için filtrelemek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6949b-128">**Is closed** (category 3) – This field is used to filter invoices for training (closed) and prediction (not closed).</span></span>
- <span data-ttu-id="6949b-129">**Ad** (kategori 1)</span><span class="sxs-lookup"><span data-stu-id="6949b-129">**Name** (category 1)</span></span>
- <span data-ttu-id="6949b-130">**Kaynak kimliği** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6949b-130">**Source Id** (category 2)</span></span>
- <span data-ttu-id="6949b-131">**Kaynak kaydı** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6949b-131">**Source record** (category 2)</span></span>
- <span data-ttu-id="6949b-132">**Kaynak tablosu** (kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6949b-132">**Source table** (category 2)</span></span>

### <a name="customer-common-data-model-entity"></a><span data-ttu-id="6949b-133">Müşteri Common Data Model varlığı</span><span class="sxs-lookup"><span data-stu-id="6949b-133">Customer Common Data Model entity</span></span>

<span data-ttu-id="6949b-134">Aşağıdaki şekilde, müşteri varlığı için kullanılabilir alanlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6949b-134">The following illustration shows the fields that are available for the customer entity.</span></span>

<span data-ttu-id="6949b-135">[![Müşteri varlığı için kullanılabilir alanlar](./media/related-entities.png)](./media/related-entities.png)</span><span class="sxs-lookup"><span data-stu-id="6949b-135">[![Available fields for the customer entity](./media/related-entities.png)](./media/related-entities.png)</span></span>

<span data-ttu-id="6949b-136">Eğitim için aşağıdaki alan seçilmemelidir:</span><span class="sxs-lookup"><span data-stu-id="6949b-136">The following field should not be selected for training:</span></span>

- <span data-ttu-id="6949b-137">**Satır benzersiz anahtarı** (Kategori 2)</span><span class="sxs-lookup"><span data-stu-id="6949b-137">**Row Unique Key** (category 2)</span></span>

## <a name="filters"></a><span data-ttu-id="6949b-138">Filtreler</span><span class="sxs-lookup"><span data-stu-id="6949b-138">Filters</span></span>

<span data-ttu-id="6949b-139">Filtreler, şu anda Müşteri ödeme tahmini senaryosunu desteklemez.</span><span class="sxs-lookup"><span data-stu-id="6949b-139">The filters don't currently support the Customer payment predictor scenario.</span></span> <span data-ttu-id="6949b-140">Bu nedenle, **Bu adımı atla**'yı seçin ve özet sayfasına devam edin.</span><span class="sxs-lookup"><span data-stu-id="6949b-140">Therefore, select **Skip this step**, and continue to the summary page.</span></span>

<span data-ttu-id="6949b-141">[![Filtrelerle modeli odaklama](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span><span class="sxs-lookup"><span data-stu-id="6949b-141">[![Focus model with filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="6949b-142">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="6949b-142">Privacy notice</span></span>
<span data-ttu-id="6949b-143">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="6949b-143">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
