---
title: Pozisyonlar için bordro ayrıntıları
description: Bu konu, Dynamics 365 Human Resources'taki Pozisyonlar varlığı Bordro ayrıntılarına ilişkin bilgi ve örnek bir sorgu sağlar.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056792"
---
# <a name="payroll-position"></a><span data-ttu-id="2aa18-103">Bordrolu pozisyon</span><span class="sxs-lookup"><span data-stu-id="2aa18-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2aa18-104">Bu konu, Dynamics 365 Human Resources'taki Pozisyonlar varlığı Bordro ayrıntılarına ilişkin bilgi ve örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="2aa18-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="2aa18-105">Özellikler</span><span class="sxs-lookup"><span data-stu-id="2aa18-105">Properties</span></span>

| <span data-ttu-id="2aa18-106">Özellik</span><span class="sxs-lookup"><span data-stu-id="2aa18-106">Property</span></span><br><span data-ttu-id="2aa18-107">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="2aa18-107">**Physical name**</span></span><br><span data-ttu-id="2aa18-108">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="2aa18-108">**_Type_**</span></span> | <span data-ttu-id="2aa18-109">Kullan</span><span class="sxs-lookup"><span data-stu-id="2aa18-109">Use</span></span> | <span data-ttu-id="2aa18-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="2aa18-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2aa18-111">**Yıllık mesai saatleri**</span><span class="sxs-lookup"><span data-stu-id="2aa18-111">**Annual regular hours**</span></span><br><span data-ttu-id="2aa18-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="2aa18-112">annualregularhours</span></span><br><span data-ttu-id="2aa18-113">*Ondalık*</span><span class="sxs-lookup"><span data-stu-id="2aa18-113">*Decimal*</span></span> | <span data-ttu-id="2aa18-114">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-114">Read-only</span></span><br><span data-ttu-id="2aa18-115">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-115">Required</span></span> | <span data-ttu-id="2aa18-116">Pozisyonda tanımlanan yıllık düzenli saatler.</span><span class="sxs-lookup"><span data-stu-id="2aa18-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="2aa18-117">**Bordro pozisyon ayrıntıları varlık kimliği**</span><span class="sxs-lookup"><span data-stu-id="2aa18-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="2aa18-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="2aa18-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="2aa18-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="2aa18-119">*Guid*</span></span> | <span data-ttu-id="2aa18-120">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-120">Required</span></span><br><span data-ttu-id="2aa18-121">Sistem tarafından oluşturulan.</span><span class="sxs-lookup"><span data-stu-id="2aa18-121">System generated.</span></span> | <span data-ttu-id="2aa18-122">Pozisyonu benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.</span><span class="sxs-lookup"><span data-stu-id="2aa18-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="2aa18-123">**Birincil alan**</span><span class="sxs-lookup"><span data-stu-id="2aa18-123">**Primary field**</span></span><br><span data-ttu-id="2aa18-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="2aa18-124">mshr_primaryfield</span></span><br><span data-ttu-id="2aa18-125">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2aa18-125">*String*</span></span> | <span data-ttu-id="2aa18-126">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-126">Required</span></span><br><span data-ttu-id="2aa18-127">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="2aa18-127">System generated</span></span> |  |
| <span data-ttu-id="2aa18-128">**Pozisyon iş kimliği değeri**</span><span class="sxs-lookup"><span data-stu-id="2aa18-128">**Position job ID value**</span></span><br><span data-ttu-id="2aa18-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="2aa18-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="2aa18-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2aa18-130">*GUID*</span></span> | <span data-ttu-id="2aa18-131">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-131">Read-only</span></span><br><span data-ttu-id="2aa18-132">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-132">Required</span></span><br><span data-ttu-id="2aa18-133">Yabancı anahtar: mshr_payrollpositionjobentity için mshr_PayrollPositionJobEntity</span><span class="sxs-lookup"><span data-stu-id="2aa18-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="2aa18-134">Pozisyonla ilişkili işin kimliği.</span><span class="sxs-lookup"><span data-stu-id="2aa18-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="2aa18-135">**Sabit ücret planı kimlik değeri**</span><span class="sxs-lookup"><span data-stu-id="2aa18-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="2aa18-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="2aa18-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="2aa18-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2aa18-137">*GUID*</span></span> | <span data-ttu-id="2aa18-138">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-138">Read-only</span></span><br><span data-ttu-id="2aa18-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-139">Required</span></span><br><span data-ttu-id="2aa18-140">Yabancı anahtar: mshr_payrollfixedcompensationplanentity içinmshr_FixedCompPlan_id</span><span class="sxs-lookup"><span data-stu-id="2aa18-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="2aa18-141">Pozisyonla ilişkili sabit ücret planının kimliği.</span><span class="sxs-lookup"><span data-stu-id="2aa18-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="2aa18-142">**Ödeme döngüsü kimliği**</span><span class="sxs-lookup"><span data-stu-id="2aa18-142">**Pay cycle ID**</span></span><br><span data-ttu-id="2aa18-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="2aa18-143">mshr_primaryfield</span></span><br><span data-ttu-id="2aa18-144">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2aa18-144">*String*</span></span> | <span data-ttu-id="2aa18-145">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-145">Read-only</span></span><br><span data-ttu-id="2aa18-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-146">Required</span></span> | <span data-ttu-id="2aa18-147">Pozisyonda tanımlanan ödeme döngüsü.</span><span class="sxs-lookup"><span data-stu-id="2aa18-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="2aa18-148">**Tüzel kişilik tarafından ödenen**</span><span class="sxs-lookup"><span data-stu-id="2aa18-148">**Paid by legal entity**</span></span><br><span data-ttu-id="2aa18-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="2aa18-149">paidbylegalentity</span></span><br><span data-ttu-id="2aa18-150">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2aa18-150">*String*</span></span> | <span data-ttu-id="2aa18-151">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-151">Read-only</span></span><br><span data-ttu-id="2aa18-152">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-152">Required</span></span> | <span data-ttu-id="2aa18-153">Ödemeyi yapmak için sorumlu pozisyonda tanımlanan tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="2aa18-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="2aa18-154">**Pozisyon kodu**</span><span class="sxs-lookup"><span data-stu-id="2aa18-154">**Position ID**</span></span><br><span data-ttu-id="2aa18-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="2aa18-155">mshr_positionid</span></span><br><span data-ttu-id="2aa18-156">*Dize*</span><span class="sxs-lookup"><span data-stu-id="2aa18-156">*String*</span></span> | <span data-ttu-id="2aa18-157">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-157">Read-only</span></span><br><span data-ttu-id="2aa18-158">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-158">Required</span></span> | <span data-ttu-id="2aa18-159">Pozisyonun kimliği.</span><span class="sxs-lookup"><span data-stu-id="2aa18-159">The ID of the position.</span></span> |
| <span data-ttu-id="2aa18-160">**Geçerlilik bitişi**</span><span class="sxs-lookup"><span data-stu-id="2aa18-160">**Valid to**</span></span><br><span data-ttu-id="2aa18-161">validto</span><span class="sxs-lookup"><span data-stu-id="2aa18-161">validto</span></span><br><span data-ttu-id="2aa18-162">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="2aa18-162">*Date Time Offset*</span></span> | <span data-ttu-id="2aa18-163">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-163">Read-only</span></span><br><span data-ttu-id="2aa18-164">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-164">Required</span></span> |<span data-ttu-id="2aa18-165">Pozisyon ayrıntılarının geçerlilik başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="2aa18-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="2aa18-166">**Geçerlilik başlangıcı**</span><span class="sxs-lookup"><span data-stu-id="2aa18-166">**Valid from**</span></span><br><span data-ttu-id="2aa18-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="2aa18-167">validfrom</span></span><br><span data-ttu-id="2aa18-168">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="2aa18-168">*Date Time Offset*</span></span> | <span data-ttu-id="2aa18-169">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="2aa18-169">Read-only</span></span><br><span data-ttu-id="2aa18-170">Gerekli</span><span class="sxs-lookup"><span data-stu-id="2aa18-170">Required</span></span> |<span data-ttu-id="2aa18-171">Pozisyon ayrıntılarının geçerlilik bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="2aa18-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="2aa18-172">**Sorgu**</span><span class="sxs-lookup"><span data-stu-id="2aa18-172">**Query**</span></span>

<span data-ttu-id="2aa18-173">**İstek**</span><span class="sxs-lookup"><span data-stu-id="2aa18-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="2aa18-174">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="2aa18-174">**Response**</span></span>

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
