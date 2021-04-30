---
title: Bordro varlıkları oluşturma ve gözden geçirme
description: Bu konuda, bordro varlıklarının nasıl oluşturulacağı ve inceleneceği açıklanmıştır.
author: andreabichsel
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
ms.openlocfilehash: c6e043498d4e36e38575a16c6475a5edfef51fc6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882095"
---
# <a name="generate-payroll-entities"></a><span data-ttu-id="1c519-103">Bordro varlıkları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1c519-103">Generate payroll entities</span></span>

<span data-ttu-id="1c519-104">Bordro tümleştirmesi için gereken varlıkları oluşturmak üzere bu OData işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c519-104">Use this OData function to generate the entities needed for payroll integration.</span></span> <span data-ttu-id="1c519-105">Human Resources'da bu varlıklarda özel alanlar ekleme gibi değişiklikler yapılırsa, her bir varlığın meta verilerini yenilemek için bu işlev tekrar çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="1c519-105">If any changes are made to these entities in Human Resources, such as adding custom fields, this function can be called again to refresh the metadata of each entity.</span></span> <span data-ttu-id="1c519-106">Yanıt, oluşturma işleminin ne zaman tamamlandığını bilmek üzere izleyebildiğiniz bir işlem kimliği içerir.</span><span class="sxs-lookup"><span data-stu-id="1c519-106">The response contains an operation ID that you can monitor so you know when the generation process has completed.</span></span>

<span data-ttu-id="1c519-107">**İstek**</span><span class="sxs-lookup"><span data-stu-id="1c519-107">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/RefreshHumanResourcesVirtualEntities
```

<span data-ttu-id="1c519-108">**gövde**</span><span class="sxs-lookup"><span data-stu-id="1c519-108">**body**</span></span>

```json
{
    "PhysicalNames" : ["PayrollEmployeeEntity", "HcmWorkerBaseEntity", "PayrollPositionEntity", "PayrollPositionJobEntity", "PayrollWorkerAddressEntity", "HcmJobDetailEntity", "HcmCompFixedPlanTableEntity", "PayrollFixedCompensationPlanEntity", "HcmEmploymentDetailEntity"]
}
```

<span data-ttu-id="1c519-109">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="1c519-109">**Response**</span></span>

```json
{
    "AsyncOperationId": "8b98d338-f939-4c86-9a91-80b76b6ab2ea"
}
```

## <a name="review-payroll-entities"></a><span data-ttu-id="1c519-110">Bordro varlıklarını inceleme</span><span class="sxs-lookup"><span data-stu-id="1c519-110">Review payroll entities</span></span>

<span data-ttu-id="1c519-111">Başarıyla oluşturulmuş ve kullanıma hazır varlıkların listesini almak için bu API'yı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c519-111">Use this API to retrieve a list of the entities that have been successfully generated and are ready for use.</span></span>

<span data-ttu-id="1c519-112">**İstek**</span><span class="sxs-lookup"><span data-stu-id="1c519-112">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hrvirtualentitycatalogs?$filter=mshr_hasbeengenerated eq true
```

<span data-ttu-id="1c519-113">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="1c519-113">**Response**</span></span>

```json
{
      "value": [
        {
            "mshr_physicalname": "PayrollWorkerAddressEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-1c00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmJobDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6400-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmCompFixedPlanTableEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6b00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollEmployeeEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6d00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmEmploymentDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-7e00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollFixedCompensationPlanEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-9300-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmWorkerBaseEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-c000-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollPositionJobEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-e700-005001000000",
            "mshr_refresh": null
        }
    ]
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]