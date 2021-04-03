---
title: Filtreleme türleri
description: Bu konu, Dynamics 365 Human Resources için Filtreleme türleri varlığını açıklar.
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465930"
---
# <a name="screening-types"></a><span data-ttu-id="6a902-103">Filtreleme türleri</span><span class="sxs-lookup"><span data-stu-id="6a902-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6a902-104">Bu konu, Dynamics 365 Human Resources için Filtreleme türleri varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="6a902-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6a902-105">Fiziksel ad: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="6a902-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="6a902-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a902-106">Description</span></span>

<span data-ttu-id="6a902-107">Bu varlık, şirket tarafından işe alım öncesi ve devam eden personel filtreleme işlemleri için ayarlanan filtreleme türlerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6a902-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6a902-108">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="6a902-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="6a902-109">Özellikler</span><span class="sxs-lookup"><span data-stu-id="6a902-109">Properties</span></span>

| <span data-ttu-id="6a902-110">Özellik</span><span class="sxs-lookup"><span data-stu-id="6a902-110">Property</span></span><br><span data-ttu-id="6a902-111">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="6a902-111">**Physical name**</span></span><br><span data-ttu-id="6a902-112">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="6a902-112">**_Type_**</span></span> | <span data-ttu-id="6a902-113">Kullan</span><span class="sxs-lookup"><span data-stu-id="6a902-113">Use</span></span> | <span data-ttu-id="6a902-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a902-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6a902-115">**Filtreleme Türü Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="6a902-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="6a902-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="6a902-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="6a902-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6a902-117">*GUID*</span></span> | <span data-ttu-id="6a902-118">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="6a902-118">Read-only</span></span><br><span data-ttu-id="6a902-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="6a902-119">Required</span></span><br><span data-ttu-id="6a902-120">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="6a902-120">System-generated</span></span> | <span data-ttu-id="6a902-121">Filtreleme türü kaydı için benzersiz birincil tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="6a902-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="6a902-122">**Filtreleme Türü Kimliği**</span><span class="sxs-lookup"><span data-stu-id="6a902-122">**Screening Type ID**</span></span><br><span data-ttu-id="6a902-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="6a902-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="6a902-124">*Dize*</span><span class="sxs-lookup"><span data-stu-id="6a902-124">*String*</span></span> | <span data-ttu-id="6a902-125">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="6a902-125">Read/write</span></span><br><span data-ttu-id="6a902-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="6a902-126">Required</span></span> | <span data-ttu-id="6a902-127">Filtreleme türü için kullanıcı tanımlı benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="6a902-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="6a902-128">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="6a902-128">**Description**</span></span><br><span data-ttu-id="6a902-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="6a902-129">mshr_description</span></span><br><span data-ttu-id="6a902-130">*Dize*</span><span class="sxs-lookup"><span data-stu-id="6a902-130">*String*</span></span> | <span data-ttu-id="6a902-131">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="6a902-131">Read/write</span></span><br><span data-ttu-id="6a902-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="6a902-132">Required</span></span> | <span data-ttu-id="6a902-133">Filtreleme türünün açıklaması.</span><span class="sxs-lookup"><span data-stu-id="6a902-133">The description of the screening type.</span></span> |
| <span data-ttu-id="6a902-134">**Sıklık Birimi**</span><span class="sxs-lookup"><span data-stu-id="6a902-134">**Frequency Unit**</span></span><br><span data-ttu-id="6a902-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="6a902-135">mshr_frequencyunit</span></span><br><span data-ttu-id="6a902-136">*mshr_hcmfrequencyunit seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="6a902-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="6a902-137">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="6a902-137">Read/write</span></span><br><span data-ttu-id="6a902-138">Gerekli</span><span class="sxs-lookup"><span data-stu-id="6a902-138">Required</span></span> | <span data-ttu-id="6a902-139">Atanan kişi için filtrelemenin tamamlanacağı sıklığı açıklar.</span><span class="sxs-lookup"><span data-stu-id="6a902-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="6a902-140">**Oluşturma Kaynağı**</span><span class="sxs-lookup"><span data-stu-id="6a902-140">**Generate From**</span></span><br><span data-ttu-id="6a902-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="6a902-141">mshr_generatefrom</span></span><br><span data-ttu-id="6a902-142">*mshr_hcmfrequencygeneratefrom seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="6a902-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="6a902-143">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="6a902-143">Read-write</span></span><br><span data-ttu-id="6a902-144">Gerekli</span><span class="sxs-lookup"><span data-stu-id="6a902-144">Required</span></span> | <span data-ttu-id="6a902-145">Sıklık değeri "Yalnızca bir seferlik" dışında bir değerse, GenerateFrom değeri bir sonraki filtreleme olayının hesaplanacağı tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="6a902-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="6a902-146">**Sıklık Aralığı**</span><span class="sxs-lookup"><span data-stu-id="6a902-146">**Frequency Interval**</span></span><br><span data-ttu-id="6a902-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="6a902-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="6a902-148">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="6a902-148">*Integer*</span></span> | <span data-ttu-id="6a902-149">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="6a902-149">Read-write</span></span><br><span data-ttu-id="6a902-150">Gerekli</span><span class="sxs-lookup"><span data-stu-id="6a902-150">Required</span></span> | <span data-ttu-id="6a902-151">Sıklık değeri "Yalnızca bir seferlik" dışında bir değerse her filtreleme olayı arasındaki zaman birimleri için bir aralık tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a902-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6a902-152">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="6a902-152">See also</span></span>

[<span data-ttu-id="6a902-153">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="6a902-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="6a902-154">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="6a902-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]