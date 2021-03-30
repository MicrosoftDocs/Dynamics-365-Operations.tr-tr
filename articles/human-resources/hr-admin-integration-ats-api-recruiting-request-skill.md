---
title: İşe alma isteği becerisi
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği yetenek varlığını açıklar.
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
ms.openlocfilehash: 83a9956b9aa820e8aca9bf6b2ab920a45c1061f6
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126014"
---
# <a name="recruiting-request-skill"></a>İşe alma isteği becerisi

Bu konu, Dynamics 365 Human Resources için İşe alma isteği yetenek varlığını açıklar.

Fiziksel ad: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>Tanım

İşe Alma İsteği için yetenek gereksinimlerini açıklar.

### <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İşe Alma İsteği Yetenek Varlığı Kimliği**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Salt okunur<br>Gerekli | **İşe Alma İsteği Yetenek** kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **İşe Alma İsteği Kimliği**<br>mshr_recruitingrequestid<br>*Dize* | Bir kez yaz<br>Gerekli | İlişkili işe alma isteğinin kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **İşe Alma İsteği Kimlik Değeri**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Salt okunur<br>Gerekli<br> Yabancı anahtar: mshr_hcmrecruitingrequestentity varlığına ait mshr_hcmrecruitingrequestentityid | İlişkili işe alma isteğinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Yetenek Kimliği**<br>mshr_skillid<br>*Dize*<br> | Bir kez yaz<br>Gerekli | Gerekli yeteneğin kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **Yetenek Kimliği Değeri**<br>_mshr_fk_skill_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmskillentity varlığına ait mshr_hcmskillentityid | Gerekli yeteneğin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Değerlendirme Düzeyi Kimliği**<br>mshr_ratinglevelid<br>*Dize* | Bir kez yaz<br>İsteğe bağlı | Yeteneğe atanan değerlendirme modelini temel alarak iş için seçilen gerekli yetenek düzeyi değeri. |
| **Değerlendirme Düzeyi Kimlik Değeri**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmratinglevelentity varlığına ait mshr_hcmratinglevelentityid | Düzey için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Yetenek Açıklaması**<br>mshr_skilldescription<br>*Dize* | Salt okunur<br>Gerekli | Yetenek tanımı. |
| **Değerlendirme Düzeyi Açıklaması**<br>mshr_ratingleveldescription<br>*Dize* | Salt okunur<br>İsteğe bağlı | Seçilen yetenek düzeyinin açıklaması. |
| **Veri Alanı Kimliği**<br>mshr_dataareaid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Tüzel kişiliği (şirket) belirtir. |
| **Veri Alanı Kimliği Değeri**<br>_mshr_dataareaid_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: cdm_company varlığına ait cdm_companyid | Tüzel kişiliği (şirket) tanımlaması için sistem tarafından oluşturulan GUID değeri. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Kaydı benzersiz olarak tanımlamak için başka bir yöntem olarak İşe Alma İsteği değerinin ve Yetenek Kimliğinin birleştirilmesi. |
| **Değerlendirme Modeli Kimliği**<br>mshr_ratingmodelid<br>*Dize* | Okuma/yazma<br>Gerekli | Yeteneği derecelendirmek için kullanılan değerlendirme modeli. |
| **Değerlendirme Modeli Kimlik Değeri**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmratingmodelentity varlığına ait mshr_hcmratingmodelentityid | Yeteneği derecelendirmek için kullanılan değerlendirme modelinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]