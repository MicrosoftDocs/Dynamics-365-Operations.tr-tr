---
title: Kişi filtreleme
description: Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.
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
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798045"
---
# <a name="person-screening"></a><span data-ttu-id="361e4-103">Kişi filtreleme</span><span class="sxs-lookup"><span data-stu-id="361e4-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="361e4-104">Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="361e4-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="361e4-105">Fiziksel ad: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="361e4-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="361e4-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="361e4-106">Description</span></span>

<span data-ttu-id="361e4-107">Bu varlık, bir adayın geçtiği veya işe alım için geçmesi gereken filtrelemeleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="361e4-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="361e4-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="361e4-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="361e4-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="361e4-109">Properties</span></span>

| <span data-ttu-id="361e4-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="361e4-110">Property</span></span><br><span data-ttu-id="361e4-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="361e4-111">**Physical name**</span></span><br><span data-ttu-id="361e4-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="361e4-112">**_Type_**</span></span> | <span data-ttu-id="361e4-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="361e4-113">Use</span></span> | <span data-ttu-id="361e4-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="361e4-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="361e4-115">**Kişi Filtreleme Varlığı Kimliği**</span><span class="sxs-lookup"><span data-stu-id="361e4-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="361e4-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="361e4-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="361e4-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="361e4-117">*GUID*</span></span> | <span data-ttu-id="361e4-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="361e4-118">Read-only</span></span><br><span data-ttu-id="361e4-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="361e4-119">Required</span></span><br><span data-ttu-id="361e4-120">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="361e4-120">System-generated</span></span> | <span data-ttu-id="361e4-121">Kişi filtreleme kaydı için benzersiz birincil tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="361e4-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="361e4-122">**Taraf Numarası**</span><span class="sxs-lookup"><span data-stu-id="361e4-122">**Party Number**</span></span><br><span data-ttu-id="361e4-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="361e4-123">mshr_partynumber</span></span><br><span data-ttu-id="361e4-124">*Dize*</span><span class="sxs-lookup"><span data-stu-id="361e4-124">*String*</span></span> | <span data-ttu-id="361e4-125">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="361e4-125">Read/write</span></span><br><span data-ttu-id="361e4-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="361e4-126">Required</span></span> | <span data-ttu-id="361e4-127">Adayla ilişkili taraf (kişi) numarası.</span><span class="sxs-lookup"><span data-stu-id="361e4-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="361e4-128">**Kişi Kimliği Değeri**</span><span class="sxs-lookup"><span data-stu-id="361e4-128">**Person ID Value**</span></span><br><span data-ttu-id="361e4-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="361e4-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="361e4-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="361e4-130">*GUID*</span></span> | <span data-ttu-id="361e4-131">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="361e4-131">Read-only</span></span><br><span data-ttu-id="361e4-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="361e4-132">Required</span></span><br><span data-ttu-id="361e4-133">Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="361e4-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="361e4-134">Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="361e4-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="361e4-135">**Filtreleme Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="361e4-135">**Screening Type ID**</span></span><br><span data-ttu-id="361e4-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="361e4-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="361e4-137">*Dize*</span><span class="sxs-lookup"><span data-stu-id="361e4-137">*String*</span></span> | <span data-ttu-id="361e4-138">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="361e4-138">Read/write</span></span><br><span data-ttu-id="361e4-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="361e4-139">Required</span></span><br><span data-ttu-id="361e4-140">Yabancı anahtar: Filtreleme Türü</span><span class="sxs-lookup"><span data-stu-id="361e4-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="361e4-141">Human Resources'da tanımlanan filtreleme türünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="361e4-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="361e4-142">**Filtreleme Türü Kimlik Değeri**</span><span class="sxs-lookup"><span data-stu-id="361e4-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="361e4-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="361e4-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="361e4-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="361e4-144">*GUID*</span></span> | <span data-ttu-id="361e4-145">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="361e4-145">Read-only</span></span><br><span data-ttu-id="361e4-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="361e4-146">Required</span></span><br><span data-ttu-id="361e4-147">Yabancı anahtar: mshr_hcmscreeningtypeentity içindeki mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="361e4-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="361e4-148">İlişkili varlıktaki filtreleme türü kaydı için sistem tarafından oluşturulan tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="361e4-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="361e4-149">**Gerekli**</span><span class="sxs-lookup"><span data-stu-id="361e4-149">**Required By**</span></span><br><span data-ttu-id="361e4-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="361e4-150">mshr_requiredby</span></span><br><span data-ttu-id="361e4-151">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="361e4-151">*Datetime*</span></span> | <span data-ttu-id="361e4-152">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="361e4-152">Read/write</span></span><br><span data-ttu-id="361e4-153">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="361e4-153">Optional</span></span> | <span data-ttu-id="361e4-154">Filtrelemenin tamamlanması gereken tarih.</span><span class="sxs-lookup"><span data-stu-id="361e4-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="361e4-155">**Durum**</span><span class="sxs-lookup"><span data-stu-id="361e4-155">**Status**</span></span><br><span data-ttu-id="361e4-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="361e4-156">mshr_status</span></span><br><span data-ttu-id="361e4-157">*mshr_hcmcompletionstatus seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="361e4-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="361e4-158">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="361e4-158">Read/write</span></span><br><span data-ttu-id="361e4-159">Gerekli</span><span class="sxs-lookup"><span data-stu-id="361e4-159">Required</span></span> | <span data-ttu-id="361e4-160">Filtreleme için adayın durumunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="361e4-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="361e4-161">**Tamamlanma Tarihi**</span><span class="sxs-lookup"><span data-stu-id="361e4-161">**Completed Date**</span></span><br><span data-ttu-id="361e4-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="361e4-162">mshr_completeddate</span></span><br><span data-ttu-id="361e4-163">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="361e4-163">*Datetime*</span></span> | <span data-ttu-id="361e4-164">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="361e4-164">Read/write</span></span><br><span data-ttu-id="361e4-165">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="361e4-165">Optional</span></span> | <span data-ttu-id="361e4-166">Filtrelemenin tamamlandığı tarih.</span><span class="sxs-lookup"><span data-stu-id="361e4-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="361e4-167">**Notlar**</span><span class="sxs-lookup"><span data-stu-id="361e4-167">**Notes**</span></span><br><span data-ttu-id="361e4-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="361e4-168">mshr_note</span></span><br><span data-ttu-id="361e4-169">*Dize*</span><span class="sxs-lookup"><span data-stu-id="361e4-169">*String*</span></span> | <span data-ttu-id="361e4-170">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="361e4-170">Read/write</span></span><br><span data-ttu-id="361e4-171">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="361e4-171">Optional</span></span> | <span data-ttu-id="361e4-172">Yöneticileri ve işe alanları işe alımda kullanılacak notlar.</span><span class="sxs-lookup"><span data-stu-id="361e4-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="361e4-173">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="361e4-173">See also</span></span>

[<span data-ttu-id="361e4-174">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="361e4-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="361e4-175">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="361e4-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]