---
title: Işe alma isteği için sorgu örneği
description: Bu konu, Dynamics 365 Human Resources'taki İşe alma isteği varlığı için örnek bir sorgu sağlar.
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
ms.openlocfilehash: ec8b881282d3e79f83cc7205e4742f7e6c5c3464
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466002"
---
# <a name="example-query-for-recruiting-request"></a>Işe alma isteği için sorgu örneği

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources'taki İşe alma isteği varlığı için örnek bir sorgu sağlar.

Aşağıdaki sorgu, belirli bir işe alma isteği kaydı ve belirtilen istekle ilgili tüm ilişkili pozisyonlar, gerekli yetenekler ve Eğitim gereksinimlerini almak için $expand sorgu seçeneğini bir alma işlemi içinde nasıl kullanabileceğinizi gösterir. Örnek yanıt, iki pozisyon için işe alma isteğini ve istenen pozisyonlar için gerekli becerileri ve eğitim bilgilerini gösterir.

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmrecruitingrequestentities(<recruiting request entity ID>)?$expand=mshr_FK_HcmRecruitingRequestPositionEntity_RecruitingRequest,mshr_FK_HcmRecruitingRequestSkillEntity_RecruitingRequest,mshr_FK_HcmRecruitingRequestEducationEntity_RecruitingRequest
```

**Yanıt**

```json
{
    "mshr_recruitingrequestid": "USMF-000001",
    "mshr_exemptstatus": 200000001,
    "mshr_regulatoryjobcategory": 200000000,
    "_mshr_fk_compensationlevel_id_value": "0000041c-0000-0000-ce27-fef003000000",
    "mshr_recruitingrequestlocationid": "",
    "mshr_hiringmanagerpersonnelnumber": "000662",
    "mshr_titleid": "Project Manager",
    "_mshr_fk_title_id_value": "000003a6-0000-0000-a4ff-004105000000",
    "_mshr_fk_jobtype_id_value": "000004ff-0000-0000-b127-fef003000000",
    "mshr_compensationhighthreshold": 92500,
    "mshr_comments": "",
    "mshr_description": "Project Manager",
    "mshr_estimatedstartdate": "2021-01-04T00:00:00Z",
    "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb",
    "_mshr_fk_recruiter_id_value": "00000007-0000-0000-5509-014105000000",
    "_mshr_fk_hiringmanager_id_value": "0000009e-0000-0000-2a0d-000010000000",
    "mshr_externaldescription": "A Program Manager plans and manages a program’s strategy and main objectives and assesses its impact in our organization.",
    "mshr_compensationlowthreshold": 70000,
    "mshr_hcmrecruitingrequestentityid": "00000d6b-0000-0000-0000-005001000000",
    "mshr_recruiterpartynumber": "HR000000518",
    "_mshr_fk_job_id_value": "00000ab2-0000-0000-baff-004105000000",
    "mshr_status": 200000005,
    "_mshr_fk_recruitingrequestlocation_id_value": null,
    "mshr_jobtypeid": "Managers",
    "mshr_defaultfulltimeequivalency": 1,
    "mshr_dataareaid": "usmf",
    "mshr_jobid": "Project Manager",
    "mshr_jobfunctionid": "0100",
    "mshr_compensationcontrolpoint": 80000,
    "mshr_compensationlevelid": "G05",
    "mshr_FK_HcmRecruitingRequestPositionEntity_RecruitingRequest": [
        {
            "mshr_description": "Project Manager",
            "mshr_positiontypeid": "Full-time",
            "mshr_hcmrecruitingrequestpositionentityid": "00000d6b-0000-0000-ee02-005001000000",
            "mshr_primaryfield": "USMF-000001 | 000426",
            "_mshr_fk_position_id_value": "000006b9-0000-0000-0e03-014105000000",
            "_mshr_fk_reportstoworker_id_value": "0000009e-0000-0000-ea01-014105000000",
            "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb",
            "_mshr_fk_positiontype_id_value": "000008e5-0000-0000-ab27-fef003000000",
            "_mshr_fk_recruitingrequest_id_value": "00000d78-0000-0000-0000-005001000000",
            "_mshr_fk_department_id_value": "00000b01-0000-0000-0108-014105000000",
            "mshr_reportstopositionid": "000434",
            "mshr_reportstopersonnelnumber": "000364",
            "mshr_financialdimension": "007",
            "mshr_dataareaid": "usmf",
            "_mshr_fk_reportstoposition_id_value": "000006b9-0000-0000-1603-014105000000",
            "mshr_status": 200000001,
            "mshr_departmentnumber": "028",
            "mshr_recruitingrequestid": "USMF-000001",
            "mshr_positionid": "000426"
        },
        {
            "mshr_description": "Project Manager",
            "mshr_positiontypeid": "Full-time",
            "mshr_hcmrecruitingrequestpositionentityid": "00000d6b-0000-0000-0000-005001000000",
            "mshr_primaryfield": "USMF-000001 | 000461",
            "_mshr_fk_position_id_value": "000006b9-0000-0000-3103-014105000000",
            "_mshr_fk_reportstoworker_id_value": "0000009e-0000-0000-8601-014105000000",
            "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb",
            "_mshr_fk_positiontype_id_value": "000008e5-0000-0000-ab27-fef003000000",
            "_mshr_fk_recruitingrequest_id_value": "00000d78-0000-0000-0000-005001000000",
            "_mshr_fk_department_id_value": "00000b01-0000-0000-0108-014105000000",
            "mshr_reportstopositionid": "000329",
            "mshr_reportstopersonnelnumber": "000277",
            "mshr_financialdimension": "019",
            "mshr_dataareaid": "usmf",
            "_mshr_fk_reportstoposition_id_value": "000006b9-0000-0000-1401-014105000000",
            "mshr_status": 200000000,
            "mshr_departmentnumber": "028",
            "mshr_recruitingrequestid": "USMF-000001",
            "mshr_positionid": "000461"
        }
    ],
    "mshr_FK_HcmRecruitingRequestSkillEntity_RecruitingRequest": [
        {
            "_mshr_fk_skill_id_value": "00000228-0000-0000-c3ff-004105000000",
            "mshr_skillid": "Present",
            "mshr_dataareaid": "usmf",
            "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb",
            "mshr_ratinglevelid": "4",
            "_mshr_fk_recruitingrequest_id_value": "00000d78-0000-0000-0000-005001000000",
            "mshr_skilldescription": "Organize and present ideas",
            "mshr_recruitingrequestid": "USMF-000001",
            "mshr_ratingmodelid": "Skills",
            "mshr_primaryfield": "USMF-000001 | Present",
            "_mshr_fk_ratingmodel_id_value": "0000066e-0000-0000-79ff-004105000000",
            "_mshr_fk_ratinglevel_id_value": "000000c3-0000-0000-87ff-004105000000",
            "mshr_hcmrecruitingrequestskillentityid": "00000d69-0000-0000-0000-005001000000",
            "mshr_ratingleveldescription": "Advanced"
        },
        {
            "_mshr_fk_skill_id_value": "00000228-0000-0000-d3ff-004105000000",
            "mshr_skillid": "ProjectMgmt",
            "mshr_dataareaid": "usmf",
            "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb",
            "mshr_ratinglevelid": "5",
            "_mshr_fk_recruitingrequest_id_value": "00000d78-0000-0000-0000-005001000000",
            "mshr_skilldescription": "Project management",
            "mshr_recruitingrequestid": "USMF-000001",
            "mshr_ratingmodelid": "Skills",
            "mshr_primaryfield": "USMF-000001 | ProjectMgmt",
            "_mshr_fk_ratingmodel_id_value": "0000066e-0000-0000-79ff-004105000000",
            "_mshr_fk_ratinglevel_id_value": "000000c3-0000-0000-88ff-004105000000",
            "mshr_hcmrecruitingrequestskillentityid": "00000d69-0000-0000-0300-005001000000",
            "mshr_ratingleveldescription": "Expert"
        }
    ],
    "mshr_FK_HcmRecruitingRequestEducationEntity_RecruitingRequest": [
        {
            "mshr_educationdisciplineid": "Business Admin",
            "_mshr_fk_educationdiscipline_id_value": "000009e6-0000-0000-9eff-004105000000",
            "mshr_primaryfield": "USMF-000001 | Bachelor | Business Admin",
            "_mshr_fk_educationlevel_id_value": "00000d6d-0000-0000-82ff-004105000000",
            "mshr_educationdisciplinedescription": "Business Administration",
            "_mshr_fk_recruitingrequest_id_value": "00000d78-0000-0000-0000-005001000000",
            "mshr_dataareaid": "usmf",
            "mshr_recruitingrequestid": "USMF-000001",
            "mshr_hcmrecruitingrequesteducationentityid": "00000d75-0000-0000-ef02-005001000000",
            "mshr_educationlevelid": "Bachelor",
            "mshr_educationleveldescription": "Bachelor",
            "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb"
        },
        {
            "mshr_educationdisciplineid": "Business Mgmt",
            "_mshr_fk_educationdiscipline_id_value": "000009e6-0000-0000-9dff-004105000000",
            "mshr_primaryfield": "USMF-000001 | Bachelor | Business Mgmt",
            "_mshr_fk_educationlevel_id_value": "00000d6d-0000-0000-82ff-004105000000",
            "mshr_educationdisciplinedescription": "Business Management",
            "_mshr_fk_recruitingrequest_id_value": "00000d78-0000-0000-0000-005001000000",
            "mshr_dataareaid": "usmf",
            "mshr_recruitingrequestid": "USMF-000001",
            "mshr_hcmrecruitingrequesteducationentityid": "00000d75-0000-0000-0000-005001000000",
            "mshr_educationlevelid": "Bachelor",
            "mshr_educationleveldescription": "Bachelor",
            "_mshr_dataareaid_id_value": "e13a8e22-f278-ea11-a811-000d3a17b4eb"
        }
    ]
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]