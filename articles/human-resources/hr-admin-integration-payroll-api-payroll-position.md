---
title: Pozisyonlar için bordro ayrıntıları
description: Bu konu, Dynamics 365 Human Resources'taki Pozisyonlar varlığı Bordro ayrıntılarına ilişkin bilgi ve örnek bir sorgu sağlar.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019334"
---
# <a name="payroll-position"></a><span data-ttu-id="e4c57-103">Bordrolu pozisyon</span><span class="sxs-lookup"><span data-stu-id="e4c57-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e4c57-104">Bu konu, Dynamics 365 Human Resources'taki Pozisyonlar varlığı Bordro ayrıntılarına ilişkin bilgi ve örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4c57-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e4c57-105">Özellikler</span><span class="sxs-lookup"><span data-stu-id="e4c57-105">Properties</span></span>

| <span data-ttu-id="e4c57-106">Özellik</span><span class="sxs-lookup"><span data-stu-id="e4c57-106">Property</span></span><br><span data-ttu-id="e4c57-107">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="e4c57-107">**Physical name**</span></span><br><span data-ttu-id="e4c57-108">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="e4c57-108">**_Type_**</span></span> | <span data-ttu-id="e4c57-109">Kullan</span><span class="sxs-lookup"><span data-stu-id="e4c57-109">Use</span></span> | <span data-ttu-id="e4c57-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4c57-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e4c57-111">**Yıllık mesai saatleri**</span><span class="sxs-lookup"><span data-stu-id="e4c57-111">**Annual regular hours**</span></span><br><span data-ttu-id="e4c57-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="e4c57-112">annualregularhours</span></span><br><span data-ttu-id="e4c57-113">*Ondalık*</span><span class="sxs-lookup"><span data-stu-id="e4c57-113">*Decimal*</span></span> | <span data-ttu-id="e4c57-114">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-114">Read-only</span></span><br><span data-ttu-id="e4c57-115">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-115">Required</span></span> | <span data-ttu-id="e4c57-116">Pozisyonda tanımlanan yıllık düzenli saatler.</span><span class="sxs-lookup"><span data-stu-id="e4c57-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="e4c57-117">**Bordro pozisyon ayrıntıları varlık kimliği**</span><span class="sxs-lookup"><span data-stu-id="e4c57-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="e4c57-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="e4c57-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="e4c57-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="e4c57-119">*Guid*</span></span> | <span data-ttu-id="e4c57-120">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-120">Required</span></span><br><span data-ttu-id="e4c57-121">Sistem tarafından oluşturulan.</span><span class="sxs-lookup"><span data-stu-id="e4c57-121">System generated.</span></span> | <span data-ttu-id="e4c57-122">Pozisyonu benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.</span><span class="sxs-lookup"><span data-stu-id="e4c57-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="e4c57-123">**Birincil alan**</span><span class="sxs-lookup"><span data-stu-id="e4c57-123">**Primary field**</span></span><br><span data-ttu-id="e4c57-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e4c57-124">mshr_primaryfield</span></span><br><span data-ttu-id="e4c57-125">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e4c57-125">*String*</span></span> | <span data-ttu-id="e4c57-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-126">Required</span></span><br><span data-ttu-id="e4c57-127">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="e4c57-127">System generated</span></span> |  |
| <span data-ttu-id="e4c57-128">**Pozisyon iş kimliği değeri**</span><span class="sxs-lookup"><span data-stu-id="e4c57-128">**Position job ID value**</span></span><br><span data-ttu-id="e4c57-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="e4c57-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="e4c57-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4c57-130">*GUID*</span></span> | <span data-ttu-id="e4c57-131">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-131">Read-only</span></span><br><span data-ttu-id="e4c57-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-132">Required</span></span><br><span data-ttu-id="e4c57-133">Yabancı anahtar: mshr_payrollpositionjobentity için mshr_PayrollPositionJobEntity</span><span class="sxs-lookup"><span data-stu-id="e4c57-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="e4c57-134">Pozisyonla ilişkili işin kimliği.</span><span class="sxs-lookup"><span data-stu-id="e4c57-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="e4c57-135">**Sabit ücret planı kimlik değeri**</span><span class="sxs-lookup"><span data-stu-id="e4c57-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="e4c57-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="e4c57-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="e4c57-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4c57-137">*GUID*</span></span> | <span data-ttu-id="e4c57-138">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-138">Read-only</span></span><br><span data-ttu-id="e4c57-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-139">Required</span></span><br><span data-ttu-id="e4c57-140">Yabancı anahtar: mshr_payrollfixedcompensationplanentity içinmshr_FixedCompPlan_id</span><span class="sxs-lookup"><span data-stu-id="e4c57-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="e4c57-141">Pozisyonla ilişkili sabit ücret planının kimliği.</span><span class="sxs-lookup"><span data-stu-id="e4c57-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="e4c57-142">**Ödeme döngüsü kimliği**</span><span class="sxs-lookup"><span data-stu-id="e4c57-142">**Pay cycle ID**</span></span><br><span data-ttu-id="e4c57-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e4c57-143">mshr_primaryfield</span></span><br><span data-ttu-id="e4c57-144">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e4c57-144">*String*</span></span> | <span data-ttu-id="e4c57-145">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-145">Read-only</span></span><br><span data-ttu-id="e4c57-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-146">Required</span></span> | <span data-ttu-id="e4c57-147">Pozisyonda tanımlanan ödeme döngüsü.</span><span class="sxs-lookup"><span data-stu-id="e4c57-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="e4c57-148">**Tüzel kişilik tarafından ödenen**</span><span class="sxs-lookup"><span data-stu-id="e4c57-148">**Paid by legal entity**</span></span><br><span data-ttu-id="e4c57-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="e4c57-149">paidbylegalentity</span></span><br><span data-ttu-id="e4c57-150">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e4c57-150">*String*</span></span> | <span data-ttu-id="e4c57-151">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-151">Read-only</span></span><br><span data-ttu-id="e4c57-152">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-152">Required</span></span> | <span data-ttu-id="e4c57-153">Ödemeyi yapmak için sorumlu pozisyonda tanımlanan tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="e4c57-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="e4c57-154">**Pozisyon kodu**</span><span class="sxs-lookup"><span data-stu-id="e4c57-154">**Position ID**</span></span><br><span data-ttu-id="e4c57-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="e4c57-155">mshr_positionid</span></span><br><span data-ttu-id="e4c57-156">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e4c57-156">*String*</span></span> | <span data-ttu-id="e4c57-157">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-157">Read-only</span></span><br><span data-ttu-id="e4c57-158">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-158">Required</span></span> | <span data-ttu-id="e4c57-159">Pozisyonun kimliği.</span><span class="sxs-lookup"><span data-stu-id="e4c57-159">The ID of the position.</span></span> |
| <span data-ttu-id="e4c57-160">**Geçerlilik bitişi**</span><span class="sxs-lookup"><span data-stu-id="e4c57-160">**Valid to**</span></span><br><span data-ttu-id="e4c57-161">validto</span><span class="sxs-lookup"><span data-stu-id="e4c57-161">validto</span></span><br><span data-ttu-id="e4c57-162">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="e4c57-162">*Date Time Offset*</span></span> | <span data-ttu-id="e4c57-163">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-163">Read-only</span></span><br><span data-ttu-id="e4c57-164">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-164">Required</span></span> |<span data-ttu-id="e4c57-165">Pozisyon ayrıntılarının geçerlilik başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="e4c57-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="e4c57-166">**Geçerlilik başlangıcı**</span><span class="sxs-lookup"><span data-stu-id="e4c57-166">**Valid from**</span></span><br><span data-ttu-id="e4c57-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="e4c57-167">validfrom</span></span><br><span data-ttu-id="e4c57-168">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="e4c57-168">*Date Time Offset*</span></span> | <span data-ttu-id="e4c57-169">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e4c57-169">Read-only</span></span><br><span data-ttu-id="e4c57-170">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e4c57-170">Required</span></span> |<span data-ttu-id="e4c57-171">Pozisyon ayrıntılarının geçerlilik bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="e4c57-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="e4c57-172">**Sorgu**</span><span class="sxs-lookup"><span data-stu-id="e4c57-172">**Query**</span></span>

<span data-ttu-id="e4c57-173">**İstek**</span><span class="sxs-lookup"><span data-stu-id="e4c57-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="e4c57-174">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="e4c57-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
