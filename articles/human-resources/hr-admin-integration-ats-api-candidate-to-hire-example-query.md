---
title: İşe alınacak aday için sorgu örneği
description: Bu konu, Dynamics 365 Human Resources'taki İşe alınacak aday için örnek bir sorgu sağlar.
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
ms.openlocfilehash: efec8c0a8eb75f818acd4ed02632f1db96719d81
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054728"
---
# <a name="example-query-for-candidate-to-hire"></a><span data-ttu-id="1ff8a-103">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="1ff8a-103">Example query for Candidate to hire</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1ff8a-104">Bu konu, Dynamics 365 Human Resources'taki İşe alınacak aday için örnek bir sorgu sağlar.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-104">This topic provides an example query for the Candidate to hire entity in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1ff8a-105">Bu konuda, tek bir API işleminde yeni bir aday kaydının tüm ayrıntısını oluşturmak için *derin eklemeleri* nasıl kullanabileceğinizi gösteren bir örnek sağlanır.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-105">This topic provides an example demonstrating how you can use *deep inserts* to create all the detail of a new candidate record in a single API operation.</span></span> <span data-ttu-id="1ff8a-106">Derin eklemeler hakkında daha fazla bilgi için bkz. [Bir işlemde ilgili varlık kayıtlarını oluşturma](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span><span class="sxs-lookup"><span data-stu-id="1ff8a-106">For more information about deep inserts, see [Create related entity records in one operation](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).</span></span>

<span data-ttu-id="1ff8a-107">**mshr_hcmcandidatetohireentity** varlığı, **mshr_dirpersonentity** varlığıyla olan ilişkisi nedeniyle benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-107">The **mshr_hcmcandidatetohireentity** entity is unique because of its relationship to the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="1ff8a-108">**mshr_hcmcandidatetohireentity** varlığındaki birçok özellik (örneğin, **mshr_firstname**, **mshr_lastname** ve **mshr_birthdate**) **mshr_dirpersonentity** kaydından türetilir.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-108">Many of the properties on the **mshr_hcmcandidatetohireentity** (for example, **mshr_firstname**, **mshr_lastname**, and **mshr_birthdate**) are derived from the **mshr_dirpersonentity** record.</span></span> <span data-ttu-id="1ff8a-109">Derin eklemeler kullanmadan **mshr_hcmcandidatetohireentity** varlığına yeni bir aday kaydı naklederseniz, bu özellikler için değerleri doğrudan **mshr_hcmcandidatetohireentity** kaydında tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-109">If you post a new candidate record to **mshr_hcmcandidatetohireentity** without using deep inserts, you can define values for these properties directly on the **mshr_hcmcandidatetohireentity** record.</span></span> <span data-ttu-id="1ff8a-110">İlişkili **mshr_dirpersonentity** kaydı, özellikler için tanımlanan değerlerle örtülü olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-110">The associated **mshr_dirpersonentity** record is created implicitly with the defined values for the properties.</span></span> <span data-ttu-id="1ff8a-111">Daha sonra ayrı API çağrıları olarak diğer ilgili varlık kayıtlarını (yetenekler veya eğitim gibi) oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-111">You can then create any other related entity records (such as skills or education) as separate API calls.</span></span>

<span data-ttu-id="1ff8a-112">Ancak, tek bir işlemde ilgili tüm varlıkları oluşturmak için derin eklemeler kullanmak istiyorsanız **mshr_dirpersonentity** varlığına özgü özelliklerin işlemin iç içe geçmiş düzeyinde tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-112">If, however, you want to use deep inserts to create all related entities in one operation, the properties specific to the **mshr_dirpersonentity** entity must be defined on that nested level of the operation.</span></span>

<span data-ttu-id="1ff8a-113">Bu örnek, tek bir API işleminde derin eklemeler kullanarak bir aday kaydını, ilişkili kişi kaydını ve kişinin yeteneklerini ve eğitimini üç iç içe düzeyde nasıl oluşturabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-113">This example shows how you can create a candidate record, the associated person record, and the person's skills and education in three nested levels using deep inserts in a single API operation.</span></span>

> [!NOTE]
> <span data-ttu-id="1ff8a-114">Örnek, API varlıklarının her birinin tüm özelliklerini içermez.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-114">The example does not include all properties of each of the API entities.</span></span> <span data-ttu-id="1ff8a-115">Gösterim amacıyla basitleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-115">It is simplified for demonstration purposes.</span></span>

<span data-ttu-id="1ff8a-116">**İstek**</span><span class="sxs-lookup"><span data-stu-id="1ff8a-116">**Request**</span></span>

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

<span data-ttu-id="1ff8a-117">**Yanıt**</span><span class="sxs-lookup"><span data-stu-id="1ff8a-117">**Response**</span></span>

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a><span data-ttu-id="1ff8a-118">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1ff8a-118">See also</span></span>

[<span data-ttu-id="1ff8a-119">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="1ff8a-119">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]