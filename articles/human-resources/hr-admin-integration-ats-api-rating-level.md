---
title: Değerlendirme düzeyi
description: Bu konu, Dynamics 365 Human Resources için Değerlendirme düzeyi varlığını açıklar.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800345"
---
# <a name="rating-level"></a><span data-ttu-id="3354d-103">Değerlendirme düzeyi</span><span class="sxs-lookup"><span data-stu-id="3354d-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3354d-104">Bu konu, Dynamics 365 Human Resources için Değerlendirme düzeyi varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="3354d-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3354d-105">Fiziksel ad: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="3354d-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="3354d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="3354d-106">Description</span></span>

<span data-ttu-id="3354d-107">Bu varlık, beceriler için kullanılabilir değerlendirme düzeylerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="3354d-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="3354d-108">Değerlendirme düzeyleri tüm tüzel kişiliklerde geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3354d-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3354d-109">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="3354d-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="3354d-110">Özellikler</span><span class="sxs-lookup"><span data-stu-id="3354d-110">Properties</span></span>

| <span data-ttu-id="3354d-111">Özellik</span><span class="sxs-lookup"><span data-stu-id="3354d-111">Property</span></span><br><span data-ttu-id="3354d-112">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="3354d-112">**Physical name**</span></span><br><span data-ttu-id="3354d-113">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="3354d-113">**_Type_**</span></span> | <span data-ttu-id="3354d-114">Kullan</span><span class="sxs-lookup"><span data-stu-id="3354d-114">Use</span></span> | <span data-ttu-id="3354d-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="3354d-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3354d-116">**Değerlendirme Düzeyi Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="3354d-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="3354d-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="3354d-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="3354d-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3354d-118">*GUID*</span></span> | <span data-ttu-id="3354d-119">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="3354d-119">Read-only</span></span><br><span data-ttu-id="3354d-120">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-120">Required</span></span><br><span data-ttu-id="3354d-121">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="3354d-121">System-generated</span></span> | <span data-ttu-id="3354d-122">Düzey için sistem tarafından oluşturulan benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3354d-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="3354d-123">**Değerlendirme Düzeyi Kimliği**</span><span class="sxs-lookup"><span data-stu-id="3354d-123">**Rating Level ID**</span></span><br><span data-ttu-id="3354d-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="3354d-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="3354d-125">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3354d-125">*String*</span></span> | <span data-ttu-id="3354d-126">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="3354d-126">Read/write</span></span><br><span data-ttu-id="3354d-127">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-127">Required</span></span> | <span data-ttu-id="3354d-128">Düzey için kullanıcı tarafından okunabilir benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3354d-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="3354d-129">**Değerlendirme Modeli Kimliği**</span><span class="sxs-lookup"><span data-stu-id="3354d-129">**Rating Model ID**</span></span><br><span data-ttu-id="3354d-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="3354d-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="3354d-131">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3354d-131">*String*</span></span> | <span data-ttu-id="3354d-132">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="3354d-132">Read/write</span></span><br><span data-ttu-id="3354d-133">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-133">Required</span></span> | <span data-ttu-id="3354d-134">Değerlendirme düzeyinin ait olduğu değerlendirme modeli.</span><span class="sxs-lookup"><span data-stu-id="3354d-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3354d-135">**Değerlendirme Modeli Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="3354d-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="3354d-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="3354d-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="3354d-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3354d-137">*GUID*</span></span> | <span data-ttu-id="3354d-138">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="3354d-138">Read-only</span></span><br><span data-ttu-id="3354d-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-139">Required</span></span><br><span data-ttu-id="3354d-140">Yabancı anahtar: mshr_hcmratingmodelentity içindeki mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="3354d-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="3354d-141">Değerlendirme düzeyinin ait olduğu değerlendirme modeli için sistem tarafından oluşturulan tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="3354d-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3354d-142">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="3354d-142">**Description**</span></span><br><span data-ttu-id="3354d-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3354d-143">mshr_description</span></span><br><span data-ttu-id="3354d-144">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3354d-144">*String*</span></span> | <span data-ttu-id="3354d-145">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="3354d-145">Read/write</span></span><br><span data-ttu-id="3354d-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-146">Required</span></span> | <span data-ttu-id="3354d-147">Değerlendirme düzeyinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="3354d-147">The description of the rating level.</span></span> |
| <span data-ttu-id="3354d-148">**Faktör**</span><span class="sxs-lookup"><span data-stu-id="3354d-148">**Factor**</span></span><br><span data-ttu-id="3354d-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="3354d-149">mshr_factor</span></span><br><span data-ttu-id="3354d-150">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="3354d-150">*Integer*</span></span> | <span data-ttu-id="3354d-151">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="3354d-151">Read/write</span></span><br><span data-ttu-id="3354d-152">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-152">Required</span></span> | <span data-ttu-id="3354d-153">Derecelendirme düzeyi için faktör.</span><span class="sxs-lookup"><span data-stu-id="3354d-153">The factor for the rating level.</span></span> <span data-ttu-id="3354d-154">Öğeleri farklı sayıda değerlendirme düzeylerinde karşılaştırdığınızda, puanlar normalleştirmek için faktör kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3354d-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="3354d-155">Değer 0 ile 9 arasında bir tamsayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3354d-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="3354d-156">**Not**</span><span class="sxs-lookup"><span data-stu-id="3354d-156">**Note**</span></span><br><span data-ttu-id="3354d-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="3354d-157">mshr_note</span></span><br><span data-ttu-id="3354d-158">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3354d-158">*String*</span></span> | <span data-ttu-id="3354d-159">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="3354d-159">Read/write</span></span><br><span data-ttu-id="3354d-160">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="3354d-160">Optional</span></span> | <span data-ttu-id="3354d-161">Değerlendirme düzeyiyle ilişkili notlar.</span><span class="sxs-lookup"><span data-stu-id="3354d-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="3354d-162">**Birincil Alan**</span><span class="sxs-lookup"><span data-stu-id="3354d-162">**Primary Field**</span></span><br><span data-ttu-id="3354d-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3354d-163">mshr_primaryfield</span></span><br><span data-ttu-id="3354d-164">*Dize*</span><span class="sxs-lookup"><span data-stu-id="3354d-164">*String*</span></span> | <span data-ttu-id="3354d-165">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="3354d-165">Read-only</span></span><br><span data-ttu-id="3354d-166">Gerekli</span><span class="sxs-lookup"><span data-stu-id="3354d-166">Required</span></span> | <span data-ttu-id="3354d-167">Varlık kaydının tanımlayıcısı olarak kullanılacak alan.</span><span class="sxs-lookup"><span data-stu-id="3354d-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="3354d-168">Değerlendirme düzeyi kimliği ve değerlendirme modeli kimliği birleşimi.</span><span class="sxs-lookup"><span data-stu-id="3354d-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3354d-169">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="3354d-169">See also</span></span>

[<span data-ttu-id="3354d-170">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="3354d-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3354d-171">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="3354d-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]