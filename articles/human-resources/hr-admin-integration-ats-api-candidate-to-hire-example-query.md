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
ms.openlocfilehash: 5e4239b0760228699c6623ee825e08c64da5f3bb27a3b27ac8a7705e65c16b81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716604"
---
# <a name="example-query-for-candidate-to-hire"></a>İşe alınacak aday için sorgu örneği

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources'taki İşe alınacak aday için örnek bir sorgu sağlar.

Bu konuda, tek bir API işleminde yeni bir aday kaydının tüm ayrıntısını oluşturmak için *derin eklemeleri* nasıl kullanabileceğinizi gösteren bir örnek sağlanır. Derin eklemeler hakkında daha fazla bilgi için bkz. [Bir işlemde ilgili varlık kayıtlarını oluşturma](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

**mshr_hcmcandidatetohireentity** varlığı, **mshr_dirpersonentity** varlığıyla olan ilişkisi nedeniyle benzersizdir. **mshr_hcmcandidatetohireentity** varlığındaki birçok özellik (örneğin, **mshr_firstname**, **mshr_lastname** ve **mshr_birthdate**) **mshr_dirpersonentity** kaydından türetilir. Derin eklemeler kullanmadan **mshr_hcmcandidatetohireentity** varlığına yeni bir aday kaydı naklederseniz, bu özellikler için değerleri doğrudan **mshr_hcmcandidatetohireentity** kaydında tanımlayabilirsiniz. İlişkili **mshr_dirpersonentity** kaydı, özellikler için tanımlanan değerlerle örtülü olarak oluşturulur. Daha sonra ayrı API çağrıları olarak diğer ilgili varlık kayıtlarını (yetenekler veya eğitim gibi) oluşturabilirsiniz.

Ancak, tek bir işlemde ilgili tüm varlıkları oluşturmak için derin eklemeler kullanmak istiyorsanız **mshr_dirpersonentity** varlığına özgü özelliklerin işlemin iç içe geçmiş düzeyinde tanımlanması gerekir.

Bu örnek, tek bir API işleminde derin eklemeler kullanarak bir aday kaydını, ilişkili kişi kaydını ve kişinin yeteneklerini ve eğitimini üç iç içe düzeyde nasıl oluşturabileceğinizi gösterir.

> [!NOTE]
> Örnek, API varlıklarının her birinin tüm özelliklerini içermez. Gösterim amacıyla basitleştirilmiştir.

**İstek**

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

**Yanıt**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]