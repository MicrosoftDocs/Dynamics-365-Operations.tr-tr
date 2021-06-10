---
title: Kişi sertifikası
description: Bu konu, Dynamics 365 Human Resources için Kişi sertifikası varlığını açıklar.
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055208"
---
# <a name="person-certificate"></a><span data-ttu-id="75be8-103">Kişi sertifikası</span><span class="sxs-lookup"><span data-stu-id="75be8-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="75be8-104">Bu konu, Dynamics 365 Human Resources için Kişi sertifikası varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="75be8-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="75be8-105">Fiziksel ad: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="75be8-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="75be8-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="75be8-106">Description</span></span>

<span data-ttu-id="75be8-107">Bu varlık, bir adayın mesleki sertifikalarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="75be8-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="75be8-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="75be8-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="75be8-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="75be8-109">Properties</span></span>

| <span data-ttu-id="75be8-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="75be8-110">Property</span></span><br><span data-ttu-id="75be8-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="75be8-111">**Physical name**</span></span><br><span data-ttu-id="75be8-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="75be8-112">**_Type_**</span></span> | <span data-ttu-id="75be8-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="75be8-113">Use</span></span> | <span data-ttu-id="75be8-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="75be8-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="75be8-115">**Kişi Sertifikası Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="75be8-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="75be8-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="75be8-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="75be8-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75be8-117">*GUID*</span></span> | <span data-ttu-id="75be8-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="75be8-118">Read-only</span></span><br><span data-ttu-id="75be8-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-119">Required</span></span> | <span data-ttu-id="75be8-120">Kişi sertifikası varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="75be8-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="75be8-121">**Taraf Numarası**</span><span class="sxs-lookup"><span data-stu-id="75be8-121">**Party Number**</span></span><br><span data-ttu-id="75be8-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="75be8-122">mshr_partynumber</span></span><br><span data-ttu-id="75be8-123">*Dize*</span><span class="sxs-lookup"><span data-stu-id="75be8-123">*String*</span></span> | <span data-ttu-id="75be8-124">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="75be8-124">Read/write</span></span><br><span data-ttu-id="75be8-125">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-125">Required</span></span> | <span data-ttu-id="75be8-126">Adayın taraf (kişi) kimliği.</span><span class="sxs-lookup"><span data-stu-id="75be8-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="75be8-127">**Kişi Kimliği Değeri**</span><span class="sxs-lookup"><span data-stu-id="75be8-127">**Person ID Value**</span></span><br><span data-ttu-id="75be8-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="75be8-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="75be8-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75be8-129">*GUID*</span></span> | <span data-ttu-id="75be8-130">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="75be8-130">Read-only</span></span><br><span data-ttu-id="75be8-131">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-131">Required</span></span><br><span data-ttu-id="75be8-132">Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="75be8-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="75be8-133">Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="75be8-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="75be8-134">**Sertifika Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="75be8-134">**Certificate Type ID**</span></span><br><span data-ttu-id="75be8-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="75be8-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="75be8-136">*Dize*</span><span class="sxs-lookup"><span data-stu-id="75be8-136">*String*</span></span> | <span data-ttu-id="75be8-137">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="75be8-137">Read/write</span></span><br><span data-ttu-id="75be8-138">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-138">Required</span></span> |  <span data-ttu-id="75be8-139">Human Resources'da tanımlanan sertifika türünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="75be8-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="75be8-140">**Sertifika Türü Kimlik Değeri**</span><span class="sxs-lookup"><span data-stu-id="75be8-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="75be8-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="75be8-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="75be8-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="75be8-142">*GUID*</span></span> | <span data-ttu-id="75be8-143">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="75be8-143">Read-only</span></span><br><span data-ttu-id="75be8-144">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-144">Required</span></span><br><span data-ttu-id="75be8-145">Yabancı anahtar: mshr_hcmcertificatetypeentity içindeki mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="75be8-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="75be8-146">İlişkili varlıktaki sertifika türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="75be8-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="75be8-147">**Başlangıç Tarihi**</span><span class="sxs-lookup"><span data-stu-id="75be8-147">**Start Date**</span></span><br><span data-ttu-id="75be8-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="75be8-148">mshr_startdate</span></span><br><span data-ttu-id="75be8-149">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="75be8-149">*Datetime*</span></span> | <span data-ttu-id="75be8-150">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="75be8-150">Read/write</span></span><br><span data-ttu-id="75be8-151">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-151">Required</span></span> | <span data-ttu-id="75be8-152">Sertifikanın oluşturulduğu tarih.</span><span class="sxs-lookup"><span data-stu-id="75be8-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="75be8-153">**Bitiş Tarihi**</span><span class="sxs-lookup"><span data-stu-id="75be8-153">**End Date**</span></span><br><span data-ttu-id="75be8-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="75be8-154">mshr_enddate</span></span><br><span data-ttu-id="75be8-155">*Tarih saat*</span><span class="sxs-lookup"><span data-stu-id="75be8-155">*Datetime*</span></span> | <span data-ttu-id="75be8-156">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="75be8-156">Read/write</span></span><br><span data-ttu-id="75be8-157">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="75be8-157">Optional</span></span> | <span data-ttu-id="75be8-158">Sertifikanın süresinin dolacağı tarih.</span><span class="sxs-lookup"><span data-stu-id="75be8-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="75be8-159">**Notlar**</span><span class="sxs-lookup"><span data-stu-id="75be8-159">**Notes**</span></span><br><span data-ttu-id="75be8-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="75be8-160">mshr_notes</span></span><br><span data-ttu-id="75be8-161">*Dize*</span><span class="sxs-lookup"><span data-stu-id="75be8-161">*String*</span></span> | <span data-ttu-id="75be8-162">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="75be8-162">Read/write</span></span><br><span data-ttu-id="75be8-163">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="75be8-163">Optional</span></span> | <span data-ttu-id="75be8-164">Yöneticileri ve işe alanları işe alımda kullanılacak notlar.</span><span class="sxs-lookup"><span data-stu-id="75be8-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="75be8-165">**Birincil Alan**</span><span class="sxs-lookup"><span data-stu-id="75be8-165">**Primary Field**</span></span><br><span data-ttu-id="75be8-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="75be8-166">mshr_primaryfield</span></span><br><span data-ttu-id="75be8-167">*Dize*</span><span class="sxs-lookup"><span data-stu-id="75be8-167">*String*</span></span> | <span data-ttu-id="75be8-168">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="75be8-168">Read-only</span></span><br><span data-ttu-id="75be8-169">Gerekli</span><span class="sxs-lookup"><span data-stu-id="75be8-169">Required</span></span> |  <span data-ttu-id="75be8-170">Varlık kaydının tanımlayıcısı olarak kullanılacak alan.</span><span class="sxs-lookup"><span data-stu-id="75be8-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="75be8-171">Taraf numarası, sertifika türü kimliği ve başlangıç tarihi birleşimi.</span><span class="sxs-lookup"><span data-stu-id="75be8-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="75be8-172">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="75be8-172">See also</span></span>

[<span data-ttu-id="75be8-173">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="75be8-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="75be8-174">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="75be8-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]