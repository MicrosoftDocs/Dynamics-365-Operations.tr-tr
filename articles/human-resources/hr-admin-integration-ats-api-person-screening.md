---
title: Kişi filtreleme
description: Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059292"
---
# <a name="person-screening"></a><span data-ttu-id="8e9a7-103">Kişi filtreleme</span><span class="sxs-lookup"><span data-stu-id="8e9a7-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8e9a7-104">Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8e9a7-105">Fiziksel ad: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="8e9a7-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="8e9a7-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e9a7-106">Description</span></span>

<span data-ttu-id="8e9a7-107">Bu varlık, bir adayın geçtiği veya işe alım için geçmesi gereken filtrelemeleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8e9a7-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="8e9a7-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="8e9a7-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="8e9a7-109">Properties</span></span>

| <span data-ttu-id="8e9a7-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="8e9a7-110">Property</span></span><br><span data-ttu-id="8e9a7-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-111">**Physical name**</span></span><br><span data-ttu-id="8e9a7-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-112">**_Type_**</span></span> | <span data-ttu-id="8e9a7-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="8e9a7-113">Use</span></span> | <span data-ttu-id="8e9a7-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e9a7-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8e9a7-115">**Kişi Filtreleme Varlığı Kimliği**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="8e9a7-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="8e9a7-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="8e9a7-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-117">*GUID*</span></span> | <span data-ttu-id="8e9a7-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="8e9a7-118">Read-only</span></span><br><span data-ttu-id="8e9a7-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8e9a7-119">Required</span></span><br><span data-ttu-id="8e9a7-120">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="8e9a7-120">System-generated</span></span> | <span data-ttu-id="8e9a7-121">Kişi filtreleme kaydı için benzersiz birincil tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="8e9a7-122">**Taraf Numarası**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-122">**Party Number**</span></span><br><span data-ttu-id="8e9a7-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="8e9a7-123">mshr_partynumber</span></span><br><span data-ttu-id="8e9a7-124">*Dize*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-124">*String*</span></span> | <span data-ttu-id="8e9a7-125">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="8e9a7-125">Read/write</span></span><br><span data-ttu-id="8e9a7-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8e9a7-126">Required</span></span> | <span data-ttu-id="8e9a7-127">Adayla ilişkili taraf (kişi) numarası.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="8e9a7-128">**Kişi Kimliği Değeri**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-128">**Person ID Value**</span></span><br><span data-ttu-id="8e9a7-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="8e9a7-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="8e9a7-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-130">*GUID*</span></span> | <span data-ttu-id="8e9a7-131">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="8e9a7-131">Read-only</span></span><br><span data-ttu-id="8e9a7-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8e9a7-132">Required</span></span><br><span data-ttu-id="8e9a7-133">Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="8e9a7-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="8e9a7-134">Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="8e9a7-135">**Filtreleme Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-135">**Screening Type ID**</span></span><br><span data-ttu-id="8e9a7-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="8e9a7-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="8e9a7-137">*Dize*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-137">*String*</span></span> | <span data-ttu-id="8e9a7-138">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="8e9a7-138">Read/write</span></span><br><span data-ttu-id="8e9a7-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8e9a7-139">Required</span></span><br><span data-ttu-id="8e9a7-140">Yabancı anahtar: Filtreleme Türü</span><span class="sxs-lookup"><span data-stu-id="8e9a7-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="8e9a7-141">Human Resources'da tanımlanan filtreleme türünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="8e9a7-142">**Filtreleme Türü Kimlik Değeri**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="8e9a7-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="8e9a7-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="8e9a7-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-144">*GUID*</span></span> | <span data-ttu-id="8e9a7-145">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="8e9a7-145">Read-only</span></span><br><span data-ttu-id="8e9a7-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8e9a7-146">Required</span></span><br><span data-ttu-id="8e9a7-147">Yabancı anahtar: mshr_hcmscreeningtypeentity içindeki mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="8e9a7-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="8e9a7-148">İlişkili varlıktaki filtreleme türü kaydı için sistem tarafından oluşturulan tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="8e9a7-149">**Gerekli**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-149">**Required By**</span></span><br><span data-ttu-id="8e9a7-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="8e9a7-150">mshr_requiredby</span></span><br><span data-ttu-id="8e9a7-151">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-151">*Datetime*</span></span> | <span data-ttu-id="8e9a7-152">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="8e9a7-152">Read/write</span></span><br><span data-ttu-id="8e9a7-153">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="8e9a7-153">Optional</span></span> | <span data-ttu-id="8e9a7-154">Filtrelemenin tamamlanması gereken tarih.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="8e9a7-155">**Durum**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-155">**Status**</span></span><br><span data-ttu-id="8e9a7-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="8e9a7-156">mshr_status</span></span><br><span data-ttu-id="8e9a7-157">*mshr_hcmcompletionstatus seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="8e9a7-158">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="8e9a7-158">Read/write</span></span><br><span data-ttu-id="8e9a7-159">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8e9a7-159">Required</span></span> | <span data-ttu-id="8e9a7-160">Filtreleme için adayın durumunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="8e9a7-161">**Tamamlanma Tarihi**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-161">**Completed Date**</span></span><br><span data-ttu-id="8e9a7-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="8e9a7-162">mshr_completeddate</span></span><br><span data-ttu-id="8e9a7-163">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-163">*Datetime*</span></span> | <span data-ttu-id="8e9a7-164">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="8e9a7-164">Read/write</span></span><br><span data-ttu-id="8e9a7-165">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="8e9a7-165">Optional</span></span> | <span data-ttu-id="8e9a7-166">Filtrelemenin tamamlandığı tarih.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="8e9a7-167">**Notlar**</span><span class="sxs-lookup"><span data-stu-id="8e9a7-167">**Notes**</span></span><br><span data-ttu-id="8e9a7-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="8e9a7-168">mshr_note</span></span><br><span data-ttu-id="8e9a7-169">*Dize*</span><span class="sxs-lookup"><span data-stu-id="8e9a7-169">*String*</span></span> | <span data-ttu-id="8e9a7-170">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="8e9a7-170">Read/write</span></span><br><span data-ttu-id="8e9a7-171">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="8e9a7-171">Optional</span></span> | <span data-ttu-id="8e9a7-172">Yöneticileri ve işe alanları işe alımda kullanılacak notlar.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8e9a7-173">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="8e9a7-173">See also</span></span>

[<span data-ttu-id="8e9a7-174">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="8e9a7-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8e9a7-175">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="8e9a7-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]