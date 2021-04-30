---
title: Bordrolu çalışanın adresi
description: Bu konu, Dynamics 365 Human Resources'taki Bordrolu çalışan adresi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882094"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="e7dfa-103">Bordrolu çalışanın adresi</span><span class="sxs-lookup"><span data-stu-id="e7dfa-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e7dfa-104">Bu konu, Dynamics 365 Human Resources'taki Bordrolu çalışan adresi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e7dfa-105">Özellikler</span><span class="sxs-lookup"><span data-stu-id="e7dfa-105">Properties</span></span>

| <span data-ttu-id="e7dfa-106">Özellik</span><span class="sxs-lookup"><span data-stu-id="e7dfa-106">Property</span></span><br><span data-ttu-id="e7dfa-107">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-107">**Physical name**</span></span><br><span data-ttu-id="e7dfa-108">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-108">**_Type_**</span></span> | <span data-ttu-id="e7dfa-109">Kullan</span><span class="sxs-lookup"><span data-stu-id="e7dfa-109">Use</span></span> | <span data-ttu-id="e7dfa-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7dfa-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e7dfa-111">**Şehir**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-111">**City**</span></span><br><span data-ttu-id="e7dfa-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="e7dfa-112">mshr_city</span></span><br><span data-ttu-id="e7dfa-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-113">*String*</span></span> | <span data-ttu-id="e7dfa-114">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-114">Read-only</span></span><br><span data-ttu-id="e7dfa-115">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-115">Required</span></span> | <span data-ttu-id="e7dfa-116">Adres için tanımlanan şehir.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="e7dfa-117">**Personel numarası**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-117">**Personnel number**</span></span><br><span data-ttu-id="e7dfa-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="e7dfa-118">mshr_personnelnumber</span></span><br><span data-ttu-id="e7dfa-119">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-119">*String*</span></span> | <span data-ttu-id="e7dfa-120">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-120">Read-only</span></span><br><span data-ttu-id="e7dfa-121">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-121">Required</span></span> | <span data-ttu-id="e7dfa-122">Çalışanın benzersiz personel numarası.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="e7dfa-123">**Ülke bölge**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-123">**Country region**</span></span><br><span data-ttu-id="e7dfa-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="e7dfa-124">mshr_countryregionid</span></span><br><span data-ttu-id="e7dfa-125">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-125">*String*</span></span> | <span data-ttu-id="e7dfa-126">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-126">Read-only</span></span><br><span data-ttu-id="e7dfa-127">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-127">Required</span></span> | <span data-ttu-id="e7dfa-128">Adresin için tanımlanan ülke bölge</span><span class="sxs-lookup"><span data-stu-id="e7dfa-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="e7dfa-129">**Geçerlilik başlangıcı**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-129">**Valid from**</span></span><br><span data-ttu-id="e7dfa-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="e7dfa-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="e7dfa-131">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-131">*Date Time Offset*</span></span> | <span data-ttu-id="e7dfa-132">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-132">Read-only</span></span> <br><span data-ttu-id="e7dfa-133">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-133">Required</span></span> | <span data-ttu-id="e7dfa-134">Adresin geçerlilik başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="e7dfa-135">**Çalıştığı adres**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-135">**Worked in address**</span></span><br><span data-ttu-id="e7dfa-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="e7dfa-137">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-137">Read-only</span></span><br><span data-ttu-id="e7dfa-138">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-138">Required</span></span> | <span data-ttu-id="e7dfa-139">Adresin çalışanın çalıştığı yer olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="e7dfa-140">**İlçe**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-140">**County**</span></span><br><span data-ttu-id="e7dfa-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="e7dfa-141">mshr_county</span></span><br><span data-ttu-id="e7dfa-142">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-142">*String*</span></span> | <span data-ttu-id="e7dfa-143">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-143">Read-only</span></span><br><span data-ttu-id="e7dfa-144">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-144">Required</span></span> | <span data-ttu-id="e7dfa-145">Adres için tanımlanan ilçe.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="e7dfa-146">**Bordrolu çalışan adresi kimliği**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="e7dfa-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="e7dfa-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="e7dfa-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-148">*GUID*</span></span> | <span data-ttu-id="e7dfa-149">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-149">Required</span></span><br><span data-ttu-id="e7dfa-150">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="e7dfa-150">System generated</span></span> | <span data-ttu-id="e7dfa-151">Adresi benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="e7dfa-152">**Birincil alan**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-152">**Primary field**</span></span><br><span data-ttu-id="e7dfa-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e7dfa-153">mshr_primaryfield</span></span><br><span data-ttu-id="e7dfa-154">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-154">*String*</span></span> | <span data-ttu-id="e7dfa-155">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-155">Read-only</span></span><br><span data-ttu-id="e7dfa-156">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-156">Required</span></span> |  |
| <span data-ttu-id="e7dfa-157">**Sokak**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-157">**Street**</span></span><br><span data-ttu-id="e7dfa-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="e7dfa-158">mshr_street</span></span><br><span data-ttu-id="e7dfa-159">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-159">*String*</span></span> | <span data-ttu-id="e7dfa-160">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-160">Read-only</span></span><br><span data-ttu-id="e7dfa-161">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-161">Required</span></span> | <span data-ttu-id="e7dfa-162">Adres için tanımlanan cadde.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-162">The street defined for the address.</span></span> |
| <span data-ttu-id="e7dfa-163">**Geçerlilik bitişi**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-163">**Valid to**</span></span><br><span data-ttu-id="e7dfa-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="e7dfa-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="e7dfa-165">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-165">*Date Time Offset*</span></span> | <span data-ttu-id="e7dfa-166">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-166">Read-only</span></span> <br><span data-ttu-id="e7dfa-167">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-167">Required</span></span> | <span data-ttu-id="e7dfa-168">Adresin geçerlilik bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="e7dfa-169">**Yerleşim kodu**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-169">**Location ID**</span></span><br><span data-ttu-id="e7dfa-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="e7dfa-171">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-171">Read-only</span></span> <br><span data-ttu-id="e7dfa-172">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-172">Required</span></span> | <span data-ttu-id="e7dfa-173">Adres kimliği.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-173">The ID for the address.</span></span>  |
| <span data-ttu-id="e7dfa-174">**Posta kodu**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-174">**Postal code**</span></span><br><span data-ttu-id="e7dfa-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="e7dfa-175">mshr_zipcode</span></span><br><span data-ttu-id="e7dfa-176">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-176">*String*</span></span> | <span data-ttu-id="e7dfa-177">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-177">Read-only</span></span> <br><span data-ttu-id="e7dfa-178">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-178">Required</span></span> |<span data-ttu-id="e7dfa-179">Çalışan için tanımlanan tanımlama numarası.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="e7dfa-180">**Yaşadığı adres**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-180">**Lived in address**</span></span><br><span data-ttu-id="e7dfa-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="e7dfa-182">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-182">Read-only</span></span><br><span data-ttu-id="e7dfa-183">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-183">Required</span></span> | <span data-ttu-id="e7dfa-184">Adresin çalışanın yaşadığı yer olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="e7dfa-185">**İl**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-185">**State**</span></span><br><span data-ttu-id="e7dfa-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="e7dfa-186">mshr_state</span></span><br><span data-ttu-id="e7dfa-187">*Dize*</span><span class="sxs-lookup"><span data-stu-id="e7dfa-187">*String*</span></span> | <span data-ttu-id="e7dfa-188">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="e7dfa-188">Read-only</span></span><br><span data-ttu-id="e7dfa-189">Gerekli</span><span class="sxs-lookup"><span data-stu-id="e7dfa-189">Required</span></span> | <span data-ttu-id="e7dfa-190">Adres için tanımlanan il.</span><span class="sxs-lookup"><span data-stu-id="e7dfa-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="e7dfa-191">Örnek sorgu</span><span class="sxs-lookup"><span data-stu-id="e7dfa-191">Example query</span></span>

<span data-ttu-id="e7dfa-192">**İstek**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="e7dfa-193">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="e7dfa-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
