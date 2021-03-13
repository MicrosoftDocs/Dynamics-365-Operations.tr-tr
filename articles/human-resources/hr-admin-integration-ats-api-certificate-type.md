---
title: Sertifika türü
description: Bu konu, Dynamics 365 Human Resources için Sertifika türü varlığını açıklar.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125725"
---
# <a name="certificate-type"></a><span data-ttu-id="89af5-103">Sertifika türü</span><span class="sxs-lookup"><span data-stu-id="89af5-103">Certificate type</span></span>

<span data-ttu-id="89af5-104">Bu konu, Dynamics 365 Human Resources için Sertifika türü varlığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="89af5-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="89af5-105">Fiziksel ad: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="89af5-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="89af5-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="89af5-106">Description</span></span>

<span data-ttu-id="89af5-107">Bu varlık, Human Resources'da ayarlanan profesyonel sertifika türlerinin listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="89af5-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="89af5-108">Varlık, tüzel kişiliklere (şirketler) özgü değildir.</span><span class="sxs-lookup"><span data-stu-id="89af5-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="89af5-109">JSON gösterimi</span><span class="sxs-lookup"><span data-stu-id="89af5-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="89af5-110">Özellikler</span><span class="sxs-lookup"><span data-stu-id="89af5-110">Properties</span></span>

| <span data-ttu-id="89af5-111">Özellik</span><span class="sxs-lookup"><span data-stu-id="89af5-111">Property</span></span><br><span data-ttu-id="89af5-112">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="89af5-112">**Physical name**</span></span><br><span data-ttu-id="89af5-113">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="89af5-113">**_Type_**</span></span> | <span data-ttu-id="89af5-114">Kullan</span><span class="sxs-lookup"><span data-stu-id="89af5-114">Use</span></span> | <span data-ttu-id="89af5-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="89af5-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="89af5-116">**Sertifika Türü Varlık Kimliği**</span><span class="sxs-lookup"><span data-stu-id="89af5-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="89af5-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="89af5-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="89af5-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="89af5-118">*GUID*</span></span> | <span data-ttu-id="89af5-119">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="89af5-119">Read-only</span></span><br><span data-ttu-id="89af5-120">Gerekli</span><span class="sxs-lookup"><span data-stu-id="89af5-120">Required</span></span> 
<span data-ttu-id="89af5-121">Sistem tarafından oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="89af5-121">System-generated</span></span> | <span data-ttu-id="89af5-122">Sertifika türü için benzersiz birincil tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="89af5-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="89af5-123">**Sertifika Türü**</span><span class="sxs-lookup"><span data-stu-id="89af5-123">**Certificate Type**</span></span><br><span data-ttu-id="89af5-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="89af5-124">mshr_certificatetype</span></span><br><span data-ttu-id="89af5-125">*Dize*</span><span class="sxs-lookup"><span data-stu-id="89af5-125">*String*</span></span> | <span data-ttu-id="89af5-126">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="89af5-126">Read/write</span></span><br><span data-ttu-id="89af5-127">Gerekli</span><span class="sxs-lookup"><span data-stu-id="89af5-127">Required</span></span> | <span data-ttu-id="89af5-128">Sertifika türü için benzersiz kullanıcı tarafından okunabilir tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="89af5-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="89af5-129">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="89af5-129">**Description**</span></span><br><span data-ttu-id="89af5-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="89af5-130">mshr_description</span></span><br><span data-ttu-id="89af5-131">*Dize*</span><span class="sxs-lookup"><span data-stu-id="89af5-131">*String*</span></span> | <span data-ttu-id="89af5-132">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="89af5-132">Read/write</span></span><br><span data-ttu-id="89af5-133">Gerekli</span><span class="sxs-lookup"><span data-stu-id="89af5-133">Required</span></span> | <span data-ttu-id="89af5-134">Sertifika türü açıklaması.</span><span class="sxs-lookup"><span data-stu-id="89af5-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="89af5-135">**Yenileme Gerektir**</span><span class="sxs-lookup"><span data-stu-id="89af5-135">**Require Renewal**</span></span><br><span data-ttu-id="89af5-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="89af5-136">mshr_requirerenewal</span></span><br><span data-ttu-id="89af5-137">*mshr_noyes seçenek kümesi*</span><span class="sxs-lookup"><span data-stu-id="89af5-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="89af5-138">Okuma/yazma</span><span class="sxs-lookup"><span data-stu-id="89af5-138">Read/write</span></span><br><span data-ttu-id="89af5-139">İsteğe bağlı</span><span class="sxs-lookup"><span data-stu-id="89af5-139">Optional</span></span> | <span data-ttu-id="89af5-140">Sertifika için yenileme gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="89af5-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="89af5-141">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="89af5-141">See also</span></span>

[<span data-ttu-id="89af5-142">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="89af5-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="89af5-143">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="89af5-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

