---
title: Bordro sabit ücret planı
description: Bu konu, Dynamics 365 Human Resources'taki Bordro sabit ücret planı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
manager: tfehr
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882097"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="5944f-103">Bordro sabit ücret planı</span><span class="sxs-lookup"><span data-stu-id="5944f-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5944f-104">Bu konu, Dynamics 365 Human Resources'taki Bordro sabit ücret planı varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="5944f-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="5944f-105">Özellikler</span><span class="sxs-lookup"><span data-stu-id="5944f-105">Properties</span></span>

| <span data-ttu-id="5944f-106">Özellik</span><span class="sxs-lookup"><span data-stu-id="5944f-106">Property</span></span><br><span data-ttu-id="5944f-107">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="5944f-107">**Physical name**</span></span><br><span data-ttu-id="5944f-108">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="5944f-108">**_Type_**</span></span> | <span data-ttu-id="5944f-109">Kullan</span><span class="sxs-lookup"><span data-stu-id="5944f-109">Use</span></span> | <span data-ttu-id="5944f-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="5944f-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5944f-111">**Personel kodu**</span><span class="sxs-lookup"><span data-stu-id="5944f-111">**Employee ID**</span></span><br><span data-ttu-id="5944f-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="5944f-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="5944f-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5944f-113">*GUID*</span></span> | <span data-ttu-id="5944f-114">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-114">Read-only</span></span><br><span data-ttu-id="5944f-115">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-115">Required</span></span><br><span data-ttu-id="5944f-116">Yabancı anahtar: mshr_payrollemployeeentity entity için mshr_Employee_id</span><span class="sxs-lookup"><span data-stu-id="5944f-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="5944f-117">Personel kodu</span><span class="sxs-lookup"><span data-stu-id="5944f-117">Employee ID</span></span> |
| <span data-ttu-id="5944f-118">**Ödeme oranı**</span><span class="sxs-lookup"><span data-stu-id="5944f-118">**Pay rate**</span></span><br><span data-ttu-id="5944f-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="5944f-119">mshr_payrate</span></span><br><span data-ttu-id="5944f-120">*Ondalık*</span><span class="sxs-lookup"><span data-stu-id="5944f-120">*Decimal*</span></span> | <span data-ttu-id="5944f-121">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-121">Read-only</span></span><br><span data-ttu-id="5944f-122">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-122">Required</span></span> | <span data-ttu-id="5944f-123">Sabit ücret planında tanımlanan ödeme oranı.</span><span class="sxs-lookup"><span data-stu-id="5944f-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="5944f-124">**Plan Kodu**</span><span class="sxs-lookup"><span data-stu-id="5944f-124">**Plan ID**</span></span><br><span data-ttu-id="5944f-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="5944f-125">mshr_planid</span></span><br><span data-ttu-id="5944f-126">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5944f-126">*String*</span></span> | <span data-ttu-id="5944f-127">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-127">Read-only</span></span><br><span data-ttu-id="5944f-128">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-128">Required</span></span> |<span data-ttu-id="5944f-129">Ücret planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5944f-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="5944f-130">**Geçerlilik başlangıcı**</span><span class="sxs-lookup"><span data-stu-id="5944f-130">**Valid from**</span></span><br><span data-ttu-id="5944f-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="5944f-131">mshr_validfrom</span></span><br><span data-ttu-id="5944f-132">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="5944f-132">*Date Time Offset*</span></span> |  <span data-ttu-id="5944f-133">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-133">Read-only</span></span><br><span data-ttu-id="5944f-134">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-134">Required</span></span> |<span data-ttu-id="5944f-135">Personel sabit ücretinin geçerlilik başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="5944f-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="5944f-136">**Bordro Sabit Ücret Planı varlığı**</span><span class="sxs-lookup"><span data-stu-id="5944f-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="5944f-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="5944f-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="5944f-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5944f-138">*GUID*</span></span> | <span data-ttu-id="5944f-139">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-139">Required</span></span><br><span data-ttu-id="5944f-140">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="5944f-140">Sytem generated</span></span> | <span data-ttu-id="5944f-141">Ücret planını benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.</span><span class="sxs-lookup"><span data-stu-id="5944f-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="5944f-142">**Ödeme sıklığı**</span><span class="sxs-lookup"><span data-stu-id="5944f-142">**Pay frequency**</span></span><br><span data-ttu-id="5944f-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="5944f-143">mshr_payfrequency</span></span><br><span data-ttu-id="5944f-144">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5944f-144">*String*</span></span> | <span data-ttu-id="5944f-145">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-145">Read-only</span></span><br><span data-ttu-id="5944f-146">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-146">Required</span></span> |<span data-ttu-id="5944f-147">Çalışana ödeme yapma sıklığı.</span><span class="sxs-lookup"><span data-stu-id="5944f-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="5944f-148">**Geçerlilik bitişi**</span><span class="sxs-lookup"><span data-stu-id="5944f-148">**Valid to**</span></span><br><span data-ttu-id="5944f-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="5944f-149">mshr_validto</span></span><br><span data-ttu-id="5944f-150">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="5944f-150">*Date Time Offset*</span></span> | <span data-ttu-id="5944f-151">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-151">Read-only</span></span> <br><span data-ttu-id="5944f-152">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-152">Required</span></span> | <span data-ttu-id="5944f-153">Personel sabit ücretinin geçerlilik bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="5944f-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="5944f-154">**Pozisyon kodu**</span><span class="sxs-lookup"><span data-stu-id="5944f-154">**Position ID**</span></span><br><span data-ttu-id="5944f-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="5944f-155">mshr_positionid</span></span><br><span data-ttu-id="5944f-156">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5944f-156">*String*</span></span> | <span data-ttu-id="5944f-157">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-157">Read-only</span></span> <br><span data-ttu-id="5944f-158">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-158">Required</span></span> | <span data-ttu-id="5944f-159">Çalışan ve sabit ücret planı kaydı ile ilişkili pozisyon kimliği.</span><span class="sxs-lookup"><span data-stu-id="5944f-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="5944f-160">**Para Birimi**</span><span class="sxs-lookup"><span data-stu-id="5944f-160">**Currency**</span></span><br><span data-ttu-id="5944f-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="5944f-161">mshr_currency</span></span><br><span data-ttu-id="5944f-162">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5944f-162">*String*</span></span> | <span data-ttu-id="5944f-163">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-163">Read-only</span></span> <br><span data-ttu-id="5944f-164">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-164">Required</span></span> |<span data-ttu-id="5944f-165">Sabit ücret planı için tanımlanan para birimi</span><span class="sxs-lookup"><span data-stu-id="5944f-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="5944f-166">**Personel numarası**</span><span class="sxs-lookup"><span data-stu-id="5944f-166">**Personnel number**</span></span><br><span data-ttu-id="5944f-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="5944f-167">mshr_personnelnumber</span></span><br><span data-ttu-id="5944f-168">*Dize*</span><span class="sxs-lookup"><span data-stu-id="5944f-168">*String*</span></span> | <span data-ttu-id="5944f-169">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="5944f-169">Read-only</span></span><br><span data-ttu-id="5944f-170">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5944f-170">Required</span></span> |<span data-ttu-id="5944f-171">Çalışanın benzersiz personel numarası.</span><span class="sxs-lookup"><span data-stu-id="5944f-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="5944f-172">**Sorgu**</span><span class="sxs-lookup"><span data-stu-id="5944f-172">**Query**</span></span>

<span data-ttu-id="5944f-173">**İstek**</span><span class="sxs-lookup"><span data-stu-id="5944f-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="5944f-174">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="5944f-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
