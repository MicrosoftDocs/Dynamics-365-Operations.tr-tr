---
title: Kişi filtreleme
description: Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467253"
---
# <a name="person-screening"></a><span data-ttu-id="5bfb5-103">Kişi filtreleme</span><span class="sxs-lookup"><span data-stu-id="5bfb5-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5bfb5-104">Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5bfb5-105">Fiziksel ad: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="5bfb5-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="5bfb5-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bfb5-106">Description</span></span>

<span data-ttu-id="5bfb5-107">Bu varlık, bir adayın geçtiği veya işe alım için geçmesi gereken filtrelemeleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5bfb5-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="5bfb5-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="5bfb5-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="5bfb5-109">Properties</span></span>

| <span data-ttu-id="5bfb5-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="5bfb5-110">Property</span></span><br><span data-ttu-id="5bfb5-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-111">**Physical name**</span></span><br><span data-ttu-id="5bfb5-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-112">**_Type_**</span></span> | <span data-ttu-id="5bfb5-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="5bfb5-113">Use</span></span> | <span data-ttu-id="5bfb5-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bfb5-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5bfb5-115">**Kişi Filtreleme Varlığı Kimliği**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="5bfb5-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="5bfb5-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="5bfb5-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-117">*GUID*</span></span> | <span data-ttu-id="5bfb5-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5bfb5-118">Read-only</span></span><br><span data-ttu-id="5bfb5-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5bfb5-119">Required</span></span><br><span data-ttu-id="5bfb5-120">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="5bfb5-120">System-generated</span></span> | <span data-ttu-id="5bfb5-121">Kişi filtreleme kaydı için benzersiz birincil tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="5bfb5-122">**Taraf Numarası**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-122">**Party Number**</span></span><br><span data-ttu-id="5bfb5-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="5bfb5-123">mshr_partynumber</span></span><br><span data-ttu-id="5bfb5-124">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-124">*String*</span></span> | <span data-ttu-id="5bfb5-125">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="5bfb5-125">Read/write</span></span><br><span data-ttu-id="5bfb5-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5bfb5-126">Required</span></span> | <span data-ttu-id="5bfb5-127">Adayla ilişkili taraf (kişi) numarası.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="5bfb5-128">**Kişi Kimliği Değeri**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-128">**Person ID Value**</span></span><br><span data-ttu-id="5bfb5-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="5bfb5-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="5bfb5-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-130">*GUID*</span></span> | <span data-ttu-id="5bfb5-131">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5bfb5-131">Read-only</span></span><br><span data-ttu-id="5bfb5-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5bfb5-132">Required</span></span><br><span data-ttu-id="5bfb5-133">Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="5bfb5-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="5bfb5-134">Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="5bfb5-135">**Filtreleme Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-135">**Screening Type ID**</span></span><br><span data-ttu-id="5bfb5-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="5bfb5-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="5bfb5-137">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-137">*String*</span></span> | <span data-ttu-id="5bfb5-138">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="5bfb5-138">Read/write</span></span><br><span data-ttu-id="5bfb5-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5bfb5-139">Required</span></span><br><span data-ttu-id="5bfb5-140">Yabancı anahtar: Filtreleme Türü</span><span class="sxs-lookup"><span data-stu-id="5bfb5-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="5bfb5-141">Human Resources'da tanımlanan filtreleme türünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="5bfb5-142">**Filtreleme Türü Kimlik Değeri**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="5bfb5-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="5bfb5-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="5bfb5-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-144">*GUID*</span></span> | <span data-ttu-id="5bfb5-145">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5bfb5-145">Read-only</span></span><br><span data-ttu-id="5bfb5-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5bfb5-146">Required</span></span><br><span data-ttu-id="5bfb5-147">Yabancı anahtar: mshr_hcmscreeningtypeentity içindeki mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="5bfb5-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="5bfb5-148">İlişkili varlıktaki filtreleme türü kaydı için sistem tarafından oluşturulan tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="5bfb5-149">**Gerekli**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-149">**Required By**</span></span><br><span data-ttu-id="5bfb5-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="5bfb5-150">mshr_requiredby</span></span><br><span data-ttu-id="5bfb5-151">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-151">*Datetime*</span></span> | <span data-ttu-id="5bfb5-152">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="5bfb5-152">Read/write</span></span><br><span data-ttu-id="5bfb5-153">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="5bfb5-153">Optional</span></span> | <span data-ttu-id="5bfb5-154">Filtrelemenin tamamlanması gereken tarih.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="5bfb5-155">**Durum**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-155">**Status**</span></span><br><span data-ttu-id="5bfb5-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="5bfb5-156">mshr_status</span></span><br><span data-ttu-id="5bfb5-157">*mshr_hcmcompletionstatus seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="5bfb5-158">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="5bfb5-158">Read/write</span></span><br><span data-ttu-id="5bfb5-159">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5bfb5-159">Required</span></span> | <span data-ttu-id="5bfb5-160">Filtreleme için adayın durumunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="5bfb5-161">**Tamamlanma Tarihi**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-161">**Completed Date**</span></span><br><span data-ttu-id="5bfb5-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="5bfb5-162">mshr_completeddate</span></span><br><span data-ttu-id="5bfb5-163">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-163">*Datetime*</span></span> | <span data-ttu-id="5bfb5-164">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="5bfb5-164">Read/write</span></span><br><span data-ttu-id="5bfb5-165">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="5bfb5-165">Optional</span></span> | <span data-ttu-id="5bfb5-166">Filtrelemenin tamamlandığı tarih.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="5bfb5-167">**Notlar**</span><span class="sxs-lookup"><span data-stu-id="5bfb5-167">**Notes**</span></span><br><span data-ttu-id="5bfb5-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="5bfb5-168">mshr_note</span></span><br><span data-ttu-id="5bfb5-169">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-169">*String*</span></span> | <span data-ttu-id="5bfb5-170">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="5bfb5-170">Read/write</span></span><br><span data-ttu-id="5bfb5-171">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="5bfb5-171">Optional</span></span> | <span data-ttu-id="5bfb5-172">Yöneticileri ve işe alanları işe alımda kullanılacak notlar.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5bfb5-173">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-173">See also</span></span>

[<span data-ttu-id="5bfb5-174">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="5bfb5-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5bfb5-175">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="5bfb5-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]