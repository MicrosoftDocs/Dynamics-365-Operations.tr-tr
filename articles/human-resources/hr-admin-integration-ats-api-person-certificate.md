---
title: Kişi sertifikası
description: Bu konu, Dynamics 365 Human Resources için Kişi sertifikası varlığını açıklar.
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
ms.openlocfilehash: fa4582dc00341a647f1ea43ed16d9dce8bfcf688
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125365"
---
# <a name="person-certificate"></a><span data-ttu-id="1bce6-103">Kişi sertifikası</span><span class="sxs-lookup"><span data-stu-id="1bce6-103">Person certificate</span></span>

<span data-ttu-id="1bce6-104">Bu konu, Dynamics 365 Human Resources için Kişi sertifikası varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="1bce6-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1bce6-105">Fiziksel ad: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="1bce6-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="1bce6-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bce6-106">Description</span></span>

<span data-ttu-id="1bce6-107">Bu varlık, bir adayın mesleki sertifikalarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="1bce6-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="1bce6-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="1bce6-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="1bce6-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="1bce6-109">Properties</span></span>

| <span data-ttu-id="1bce6-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="1bce6-110">Property</span></span><br><span data-ttu-id="1bce6-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="1bce6-111">**Physical name**</span></span><br><span data-ttu-id="1bce6-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="1bce6-112">**_Type_**</span></span> | <span data-ttu-id="1bce6-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="1bce6-113">Use</span></span> | <span data-ttu-id="1bce6-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bce6-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1bce6-115">**Kişi Sertifikası Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="1bce6-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="1bce6-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="1bce6-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="1bce6-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1bce6-117">*GUID*</span></span> | <span data-ttu-id="1bce6-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="1bce6-118">Read-only</span></span><br><span data-ttu-id="1bce6-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-119">Required</span></span> | <span data-ttu-id="1bce6-120">Kişi sertifikası varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="1bce6-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="1bce6-121">**Taraf Numarası**</span><span class="sxs-lookup"><span data-stu-id="1bce6-121">**Party Number**</span></span><br><span data-ttu-id="1bce6-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="1bce6-122">mshr_partynumber</span></span><br><span data-ttu-id="1bce6-123">*Dize*</span><span class="sxs-lookup"><span data-stu-id="1bce6-123">*String*</span></span> | <span data-ttu-id="1bce6-124">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="1bce6-124">Read/write</span></span><br><span data-ttu-id="1bce6-125">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-125">Required</span></span> | <span data-ttu-id="1bce6-126">Adayın taraf (kişi) kimliği.</span><span class="sxs-lookup"><span data-stu-id="1bce6-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="1bce6-127">**Kişi Kimliği Değeri**</span><span class="sxs-lookup"><span data-stu-id="1bce6-127">**Person ID Value**</span></span><br><span data-ttu-id="1bce6-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="1bce6-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="1bce6-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1bce6-129">*GUID*</span></span> | <span data-ttu-id="1bce6-130">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="1bce6-130">Read-only</span></span><br><span data-ttu-id="1bce6-131">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-131">Required</span></span><br><span data-ttu-id="1bce6-132">Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="1bce6-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="1bce6-133">Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1bce6-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="1bce6-134">**Sertifika Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="1bce6-134">**Certificate Type ID**</span></span><br><span data-ttu-id="1bce6-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="1bce6-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="1bce6-136">*Dize*</span><span class="sxs-lookup"><span data-stu-id="1bce6-136">*String*</span></span> | <span data-ttu-id="1bce6-137">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="1bce6-137">Read/write</span></span><br><span data-ttu-id="1bce6-138">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-138">Required</span></span> |  <span data-ttu-id="1bce6-139">Human Resources'da tanımlanan sertifika türünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1bce6-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="1bce6-140">**Sertifika Türü Kimlik Değeri**</span><span class="sxs-lookup"><span data-stu-id="1bce6-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="1bce6-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="1bce6-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="1bce6-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1bce6-142">*GUID*</span></span> | <span data-ttu-id="1bce6-143">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="1bce6-143">Read-only</span></span><br><span data-ttu-id="1bce6-144">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-144">Required</span></span><br><span data-ttu-id="1bce6-145">Yabancı anahtar: mshr_hcmcertificatetypeentity içindeki mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="1bce6-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="1bce6-146">İlişkili varlıktaki sertifika türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1bce6-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="1bce6-147">**Başlangıç Tarihi**</span><span class="sxs-lookup"><span data-stu-id="1bce6-147">**Start Date**</span></span><br><span data-ttu-id="1bce6-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="1bce6-148">mshr_startdate</span></span><br><span data-ttu-id="1bce6-149">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="1bce6-149">*Datetime*</span></span> | <span data-ttu-id="1bce6-150">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="1bce6-150">Read/write</span></span><br><span data-ttu-id="1bce6-151">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-151">Required</span></span> | <span data-ttu-id="1bce6-152">Sertifikanın oluşturulduğu tarih.</span><span class="sxs-lookup"><span data-stu-id="1bce6-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="1bce6-153">**Bitiş Tarihi**</span><span class="sxs-lookup"><span data-stu-id="1bce6-153">**End Date**</span></span><br><span data-ttu-id="1bce6-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="1bce6-154">mshr_enddate</span></span><br><span data-ttu-id="1bce6-155">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="1bce6-155">*Datetime*</span></span> | <span data-ttu-id="1bce6-156">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="1bce6-156">Read/write</span></span><br><span data-ttu-id="1bce6-157">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="1bce6-157">Optional</span></span> | <span data-ttu-id="1bce6-158">Sertifikanın süresinin dolacağı tarih.</span><span class="sxs-lookup"><span data-stu-id="1bce6-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="1bce6-159">**Notlar**</span><span class="sxs-lookup"><span data-stu-id="1bce6-159">**Notes**</span></span><br><span data-ttu-id="1bce6-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="1bce6-160">mshr_notes</span></span><br><span data-ttu-id="1bce6-161">*Dize*</span><span class="sxs-lookup"><span data-stu-id="1bce6-161">*String*</span></span> | <span data-ttu-id="1bce6-162">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="1bce6-162">Read/write</span></span><br><span data-ttu-id="1bce6-163">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="1bce6-163">Optional</span></span> | <span data-ttu-id="1bce6-164">Yöneticileri ve işe alanları işe alımda kullanılacak notlar.</span><span class="sxs-lookup"><span data-stu-id="1bce6-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="1bce6-165">**Birincil Alan**</span><span class="sxs-lookup"><span data-stu-id="1bce6-165">**Primary Field**</span></span><br><span data-ttu-id="1bce6-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="1bce6-166">mshr_primaryfield</span></span><br><span data-ttu-id="1bce6-167">*Dize*</span><span class="sxs-lookup"><span data-stu-id="1bce6-167">*String*</span></span> | <span data-ttu-id="1bce6-168">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="1bce6-168">Read-only</span></span><br><span data-ttu-id="1bce6-169">Gerekli</span><span class="sxs-lookup"><span data-stu-id="1bce6-169">Required</span></span> |  <span data-ttu-id="1bce6-170">Varlık kaydının tanımlayıcısı olarak kullanılacak alan.</span><span class="sxs-lookup"><span data-stu-id="1bce6-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="1bce6-171">Taraf numarası, sertifika türü kimliği ve başlangıç tarihi birleşimi.</span><span class="sxs-lookup"><span data-stu-id="1bce6-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1bce6-172">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1bce6-172">See also</span></span>

[<span data-ttu-id="1bce6-173">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="1bce6-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="1bce6-174">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="1bce6-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

