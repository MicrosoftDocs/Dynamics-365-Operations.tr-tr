---
title: Bordrolu çalışanın adresi
description: Bu konu, Dynamics 365 Human Resources'taki Bordrolu çalışan adresi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020717"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="43916-103">Bordrolu çalışanın adresi</span><span class="sxs-lookup"><span data-stu-id="43916-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="43916-104">Bu konu, Dynamics 365 Human Resources'taki Bordrolu çalışan adresi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="43916-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="43916-105">Özellikler</span><span class="sxs-lookup"><span data-stu-id="43916-105">Properties</span></span>

| <span data-ttu-id="43916-106">Özellik</span><span class="sxs-lookup"><span data-stu-id="43916-106">Property</span></span><br><span data-ttu-id="43916-107">**Fiziksel ad**</span><span class="sxs-lookup"><span data-stu-id="43916-107">**Physical name**</span></span><br><span data-ttu-id="43916-108">**_Türü_**</span><span class="sxs-lookup"><span data-stu-id="43916-108">**_Type_**</span></span> | <span data-ttu-id="43916-109">Kullan</span><span class="sxs-lookup"><span data-stu-id="43916-109">Use</span></span> | <span data-ttu-id="43916-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="43916-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="43916-111">**Şehir**</span><span class="sxs-lookup"><span data-stu-id="43916-111">**City**</span></span><br><span data-ttu-id="43916-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="43916-112">mshr_city</span></span><br><span data-ttu-id="43916-113">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-113">*String*</span></span> | <span data-ttu-id="43916-114">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-114">Read-only</span></span><br><span data-ttu-id="43916-115">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-115">Required</span></span> | <span data-ttu-id="43916-116">Adres için tanımlanan şehir.</span><span class="sxs-lookup"><span data-stu-id="43916-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="43916-117">**Personel numarası**</span><span class="sxs-lookup"><span data-stu-id="43916-117">**Personnel number**</span></span><br><span data-ttu-id="43916-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="43916-118">mshr_personnelnumber</span></span><br><span data-ttu-id="43916-119">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-119">*String*</span></span> | <span data-ttu-id="43916-120">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-120">Read-only</span></span><br><span data-ttu-id="43916-121">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-121">Required</span></span> | <span data-ttu-id="43916-122">Çalışanın benzersiz personel numarası.</span><span class="sxs-lookup"><span data-stu-id="43916-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="43916-123">**Ülke bölge**</span><span class="sxs-lookup"><span data-stu-id="43916-123">**Country region**</span></span><br><span data-ttu-id="43916-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="43916-124">mshr_countryregionid</span></span><br><span data-ttu-id="43916-125">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-125">*String*</span></span> | <span data-ttu-id="43916-126">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-126">Read-only</span></span><br><span data-ttu-id="43916-127">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-127">Required</span></span> | <span data-ttu-id="43916-128">Adresin için tanımlanan ülke bölge</span><span class="sxs-lookup"><span data-stu-id="43916-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="43916-129">**Geçerlilik başlangıcı**</span><span class="sxs-lookup"><span data-stu-id="43916-129">**Valid from**</span></span><br><span data-ttu-id="43916-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="43916-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="43916-131">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="43916-131">*Date Time Offset*</span></span> | <span data-ttu-id="43916-132">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-132">Read-only</span></span> <br><span data-ttu-id="43916-133">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-133">Required</span></span> | <span data-ttu-id="43916-134">Adresin geçerlilik başlangıç tarihi.</span><span class="sxs-lookup"><span data-stu-id="43916-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="43916-135">**Çalıştığı adres**</span><span class="sxs-lookup"><span data-stu-id="43916-135">**Worked in address**</span></span><br><span data-ttu-id="43916-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="43916-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="43916-137">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-137">Read-only</span></span><br><span data-ttu-id="43916-138">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-138">Required</span></span> | <span data-ttu-id="43916-139">Adresin çalışanın çalıştığı yer olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43916-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="43916-140">**İlçe**</span><span class="sxs-lookup"><span data-stu-id="43916-140">**County**</span></span><br><span data-ttu-id="43916-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="43916-141">mshr_county</span></span><br><span data-ttu-id="43916-142">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-142">*String*</span></span> | <span data-ttu-id="43916-143">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-143">Read-only</span></span><br><span data-ttu-id="43916-144">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-144">Required</span></span> | <span data-ttu-id="43916-145">Adres için tanımlanan ilçe.</span><span class="sxs-lookup"><span data-stu-id="43916-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="43916-146">**Bordrolu çalışan adresi kimliği**</span><span class="sxs-lookup"><span data-stu-id="43916-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="43916-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="43916-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="43916-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="43916-148">*GUID*</span></span> | <span data-ttu-id="43916-149">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-149">Required</span></span><br><span data-ttu-id="43916-150">Sistem tarafından oluşturulan</span><span class="sxs-lookup"><span data-stu-id="43916-150">System generated</span></span> | <span data-ttu-id="43916-151">Adresi benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.</span><span class="sxs-lookup"><span data-stu-id="43916-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="43916-152">**Birincil alan**</span><span class="sxs-lookup"><span data-stu-id="43916-152">**Primary field**</span></span><br><span data-ttu-id="43916-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="43916-153">mshr_primaryfield</span></span><br><span data-ttu-id="43916-154">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-154">*String*</span></span> | <span data-ttu-id="43916-155">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-155">Read-only</span></span><br><span data-ttu-id="43916-156">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-156">Required</span></span> |  |
| <span data-ttu-id="43916-157">**Sokak**</span><span class="sxs-lookup"><span data-stu-id="43916-157">**Street**</span></span><br><span data-ttu-id="43916-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="43916-158">mshr_street</span></span><br><span data-ttu-id="43916-159">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-159">*String*</span></span> | <span data-ttu-id="43916-160">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-160">Read-only</span></span><br><span data-ttu-id="43916-161">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-161">Required</span></span> | <span data-ttu-id="43916-162">Adres için tanımlanan cadde.</span><span class="sxs-lookup"><span data-stu-id="43916-162">The street defined for the address.</span></span> |
| <span data-ttu-id="43916-163">**Geçerlilik bitişi**</span><span class="sxs-lookup"><span data-stu-id="43916-163">**Valid to**</span></span><br><span data-ttu-id="43916-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="43916-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="43916-165">*Tarih Saat Sapması*</span><span class="sxs-lookup"><span data-stu-id="43916-165">*Date Time Offset*</span></span> | <span data-ttu-id="43916-166">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-166">Read-only</span></span> <br><span data-ttu-id="43916-167">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-167">Required</span></span> | <span data-ttu-id="43916-168">Adresin geçerlilik bitiş tarihi.</span><span class="sxs-lookup"><span data-stu-id="43916-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="43916-169">**Yerleşim kodu**</span><span class="sxs-lookup"><span data-stu-id="43916-169">**Location ID**</span></span><br><span data-ttu-id="43916-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="43916-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="43916-171">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-171">Read-only</span></span> <br><span data-ttu-id="43916-172">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-172">Required</span></span> | <span data-ttu-id="43916-173">Adres kimliği.</span><span class="sxs-lookup"><span data-stu-id="43916-173">The ID for the address.</span></span>  |
| <span data-ttu-id="43916-174">**Posta kodu**</span><span class="sxs-lookup"><span data-stu-id="43916-174">**Postal code**</span></span><br><span data-ttu-id="43916-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="43916-175">mshr_zipcode</span></span><br><span data-ttu-id="43916-176">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-176">*String*</span></span> | <span data-ttu-id="43916-177">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-177">Read-only</span></span> <br><span data-ttu-id="43916-178">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-178">Required</span></span> |<span data-ttu-id="43916-179">Çalışan için tanımlanan tanımlama numarası.</span><span class="sxs-lookup"><span data-stu-id="43916-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="43916-180">**Yaşadığı adres**</span><span class="sxs-lookup"><span data-stu-id="43916-180">**Lived in address**</span></span><br><span data-ttu-id="43916-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="43916-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="43916-182">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-182">Read-only</span></span><br><span data-ttu-id="43916-183">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-183">Required</span></span> | <span data-ttu-id="43916-184">Adresin çalışanın yaşadığı yer olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43916-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="43916-185">**İl**</span><span class="sxs-lookup"><span data-stu-id="43916-185">**State**</span></span><br><span data-ttu-id="43916-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="43916-186">mshr_state</span></span><br><span data-ttu-id="43916-187">*Dize*</span><span class="sxs-lookup"><span data-stu-id="43916-187">*String*</span></span> | <span data-ttu-id="43916-188">Salt okunur</span><span class="sxs-lookup"><span data-stu-id="43916-188">Read-only</span></span><br><span data-ttu-id="43916-189">Gerekli</span><span class="sxs-lookup"><span data-stu-id="43916-189">Required</span></span> | <span data-ttu-id="43916-190">Adres için tanımlanan il.</span><span class="sxs-lookup"><span data-stu-id="43916-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="43916-191">Örnek sorgu</span><span class="sxs-lookup"><span data-stu-id="43916-191">Example query</span></span>

<span data-ttu-id="43916-192">**İstek**</span><span class="sxs-lookup"><span data-stu-id="43916-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="43916-193">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="43916-193">**Response**</span></span>

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
