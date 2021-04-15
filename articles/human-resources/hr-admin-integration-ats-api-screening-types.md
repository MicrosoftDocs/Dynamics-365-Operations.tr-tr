---
title: Filtreleme türleri
description: Bu konu, Dynamics 365 Human Resources için Filtreleme türleri varlığını açıklar.
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
ms.openlocfilehash: 361f8c866abb9d34eb3e2be7ea42626e98e34779
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805142"
---
# <a name="screening-types"></a><span data-ttu-id="d654e-103">Filtreleme türleri</span><span class="sxs-lookup"><span data-stu-id="d654e-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d654e-104">Bu konu, Dynamics 365 Human Resources için Filtreleme türleri varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="d654e-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d654e-105">Fiziksel ad: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="d654e-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="d654e-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d654e-106">Description</span></span>

<span data-ttu-id="d654e-107">Bu varlık, şirket tarafından işe alım öncesi ve devam eden personel filtreleme işlemleri için ayarlanan filtreleme türlerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="d654e-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d654e-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="d654e-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="d654e-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="d654e-109">Properties</span></span>

| <span data-ttu-id="d654e-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="d654e-110">Property</span></span><br><span data-ttu-id="d654e-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="d654e-111">**Physical name**</span></span><br><span data-ttu-id="d654e-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="d654e-112">**_Type_**</span></span> | <span data-ttu-id="d654e-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="d654e-113">Use</span></span> | <span data-ttu-id="d654e-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="d654e-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d654e-115">**Filtreleme Türü Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="d654e-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="d654e-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="d654e-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="d654e-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="d654e-117">*GUID*</span></span> | <span data-ttu-id="d654e-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="d654e-118">Read-only</span></span><br><span data-ttu-id="d654e-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="d654e-119">Required</span></span><br><span data-ttu-id="d654e-120">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="d654e-120">System-generated</span></span> | <span data-ttu-id="d654e-121">Filtreleme türü kaydı için benzersiz birincil tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="d654e-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="d654e-122">**Filtreleme Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="d654e-122">**Screening Type ID**</span></span><br><span data-ttu-id="d654e-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="d654e-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="d654e-124">*Dize*</span><span class="sxs-lookup"><span data-stu-id="d654e-124">*String*</span></span> | <span data-ttu-id="d654e-125">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="d654e-125">Read/write</span></span><br><span data-ttu-id="d654e-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="d654e-126">Required</span></span> | <span data-ttu-id="d654e-127">Filtreleme türü için kullanıcı tanımlı benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="d654e-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="d654e-128">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="d654e-128">**Description**</span></span><br><span data-ttu-id="d654e-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="d654e-129">mshr_description</span></span><br><span data-ttu-id="d654e-130">*Dize*</span><span class="sxs-lookup"><span data-stu-id="d654e-130">*String*</span></span> | <span data-ttu-id="d654e-131">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="d654e-131">Read/write</span></span><br><span data-ttu-id="d654e-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="d654e-132">Required</span></span> | <span data-ttu-id="d654e-133">Filtreleme türünün açıklaması.</span><span class="sxs-lookup"><span data-stu-id="d654e-133">The description of the screening type.</span></span> |
| <span data-ttu-id="d654e-134">**Sıklık Birimi**</span><span class="sxs-lookup"><span data-stu-id="d654e-134">**Frequency Unit**</span></span><br><span data-ttu-id="d654e-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="d654e-135">mshr_frequencyunit</span></span><br><span data-ttu-id="d654e-136">*mshr_hcmfrequencyunit seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="d654e-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="d654e-137">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="d654e-137">Read/write</span></span><br><span data-ttu-id="d654e-138">Gerekli</span><span class="sxs-lookup"><span data-stu-id="d654e-138">Required</span></span> | <span data-ttu-id="d654e-139">Atanan kişi için filtrelemenin tamamlanacağı sıklığı açıklar.</span><span class="sxs-lookup"><span data-stu-id="d654e-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="d654e-140">**Oluşturma Kaynağı**</span><span class="sxs-lookup"><span data-stu-id="d654e-140">**Generate From**</span></span><br><span data-ttu-id="d654e-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="d654e-141">mshr_generatefrom</span></span><br><span data-ttu-id="d654e-142">*mshr_hcmfrequencygeneratefrom seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="d654e-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="d654e-143">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="d654e-143">Read-write</span></span><br><span data-ttu-id="d654e-144">Gerekli</span><span class="sxs-lookup"><span data-stu-id="d654e-144">Required</span></span> | <span data-ttu-id="d654e-145">Sıklık değeri "Yalnızca bir seferlik" dışında bir değerse, GenerateFrom değeri bir sonraki filtreleme olayının hesaplanacağı tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="d654e-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="d654e-146">**Sıklık Aralığı**</span><span class="sxs-lookup"><span data-stu-id="d654e-146">**Frequency Interval**</span></span><br><span data-ttu-id="d654e-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="d654e-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="d654e-148">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="d654e-148">*Integer*</span></span> | <span data-ttu-id="d654e-149">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="d654e-149">Read-write</span></span><br><span data-ttu-id="d654e-150">Gerekli</span><span class="sxs-lookup"><span data-stu-id="d654e-150">Required</span></span> | <span data-ttu-id="d654e-151">Sıklık değeri "Yalnızca bir seferlik" dışında bir değerse her filtreleme olayı arasındaki zaman birimleri için bir aralık tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d654e-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d654e-152">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d654e-152">See also</span></span>

[<span data-ttu-id="d654e-153">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="d654e-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d654e-154">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="d654e-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]