---
title: İşe alma isteği eğitimi
description: Bu makalede, Dynamics 365 Human Resources için İşe alma isteği eğitim durumu varlığı açıklanmaktadır.
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
ms.openlocfilehash: bcdb5e2cc61ce551af21401ea34d8e85bc21fc6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893859"
---
# <a name="recruiting-request-education"></a>İşe alma isteği eğitimi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için İşe alma isteği eğitim durumu varlığı açıklanmaktadır.

Fiziksel ad: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>Tanım

İşe Alma İsteği için eğitim gereksinimlerini açıklar.

### <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İşe Alma İsteği Eğitim Varlığı Kimliği**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Salt okunur<br>Gerekli | İşe Alma İsteği Eğitim kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **İşe Alma İsteği Kimliği**<br>mshr_recruitingrequestid<br>*Dize* | Bir kez yaz<br>Gerekli | İlgili işe alma isteğinin kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **İşe Alma İsteği Kimlik Değeri**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmrecruitingrequestentity içindeki mshr_hcmrecruitingrequestentityid | İlgili işe alma isteğinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Eğitim Düzeyi Kimliği**<br>mshr_educationlevelid<br>*Dize* | Bir kez yaz<br>Gerekli | Gerekli eğitim seviyesi. |
| **Eğitim Düzeyi Kimlik Değeri**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmeducationlevelentity içindeki mshr_hcmeducationlevelentityid | Gerekli eğitim düzeyinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Eğitim Düzeyi Açıklaması**<br>mshr_educationleveldescription<br>*Dize* | Salt okunur<br>Gerekli | Beceri için gereken düzeyin açıklaması. |
| **Eğitim Alanı Kimliği**<br>mshr_educationdisciplinedescription<br>*Dize* | Bir kez yaz<br>Gerekli | Eğitim alanı alanı. |
| **Eğitim Alanı Kimlik Değeri**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmeducationdisciplineentity varlığına ait mshr_hcmeducationdisciplineentityid | Eğitim disiplini alanının sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Eğitim Alanı Açıklaması**<br>mshr_educationdisciplinedescription<br>Dize | Salt okunur<br>Gerekli | Eğitim disiplini alanının tanımı. |
| **Veri Alanı Kimliği**<br>mshr_dataareaid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Tüzel kişiliği (şirket) belirtir.|
| **Veri Alanı Kimliği Değeri**<br>_mshr_dataareaid_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: cdm_company varlığına ait cdm_companyid | Tüzel kişiliği (şirket) tanımlaması için sistem tarafından oluşturulan GUID değeri. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Kaydı benzersiz olarak tanımlamak için başka bir yöntem olarak İşe Alma İsteği değerinin, Eğitim Düzeyi Kimliğinin ve Eğitim Disiplini Kimliğinin birleştirilmesi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
