---
title: İşe alma isteği pozisyonu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyonu varlığını açıklar.
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
ms.openlocfilehash: 01d73d390f72343c7498ccbb99838d38be45a19e
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126038"
---
# <a name="recruiting-request-position"></a>İşe alma isteği pozisyonu

Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyonu varlığını açıklar.

Fiziksel ad: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>Tanım

İşe alma isteği için doldurulacak pozisyon veya pozisyonları açıklar. İşe alma isteğine bir pozisyon eklenmesi isteğe bağlıdır. Pozisyon özellikleri, işe alma isteğinde, pozisyon master kaydında olduğundan farklı olmadığından, pozisyonun özellikleri salt okunurdur. Özelliklerin değiştirilmesi gerekiyorsa değişiklik, pozisyon işe alma isteğine eklenmeden önce pozisyon master kaydında yapılmalıdır.

### <a name="json-representation"></a>JSON gösterimi
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İşe Alma İsteği Pozisyonu Varlık Kimliği**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Salt okunur<br>Gerekli |    İşe alma pozisyonu kaydının sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **İşe Alma İsteği Kimliği**<br>mshr_recruitingrequestid<br>*Dize* | Bir kez yaz<br>Gerekli | İşe alma isteğinin kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **İşe Alma İsteği Kimlik Değeri**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmrecruitingrequestentity varlığına ait mshr_hcmrecruitingrequestentityid | Pozisyonun atandığı işe alma isteğinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Pozisyon kodu**<br>mshr_positionid<br>*Dize* | Bir kez yaz<br>Gerekli | Pozisyonun kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **Pozisyon Kimlik Değeri**<br>_mshr_fk_position_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmpositionv2entity varlığına ait mshr_hcmpositionv2entityid | Pozisyonun sistem tarafından oluşturulan tanımlayıcısı. |
| **Açıklama**<br>mshr_description<br>*Dize* | Salt okunur<br>Gerekli | Pozisyon açıklaması. |
| **Pozisyon Türü Kimliği**<br>mshr_positiontypeid<br>*Dize* | Salt okunur<br>İsteğe bağlı | Bu pozisyon için pozisyon türünün kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **Pozisyon Türü Kimlik Değeri**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmpositiontypeentity varlığına ait mshr_hcmpositiontypeentityid | Bu pozisyon için pozisyon türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Durum**<br>mshr_status<br>*RecruitingRequestPositionStatus* seçenek kümesi | Okuma/yazma<br>Gerekli | İşe alma isteği için pozisyonun durumu. |
| **Departman Numarası**<br>mshr_departmentnumber<br>*Dize* | Salt okunur<br>İsteğe bağlı<br> | Pozisyonun departman numarası. |
| **Departman Kimliği Değeri**<br>_mshr_fk_department_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_omdepartmententity varlığına ait mshr_omdepartmententityid | Pozisyonun departmanının sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Üst Pozisyon Kimliği**<br>mshr_reportstopositionid<br>*Dize* | Salt okunur<br>Gerekli | İşe alınan pozisyonun, kuruluş hiyerarşisindeki üst pozisyonunun kullanıcı tarafından okunabilen kimliği. |
| **Üst Pozisyon Kimliği Değeri**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmpositionv2entity varlığına ait mshr_hcmpositionv2entityid | İşe alınan pozisyonun üst pozisyonunun sistem tarafından oluşturulan kimliği. |
| **Üst Pozisyon Personel Numarası**<br>mshr_reportstopersonnelnumber<br>*Dize* | Salt okunur<br>Gerekli | İşe alınan adayın üst pozisyonundaki çalışanın çalışan kimliği. |
| **Üst Pozisyon Çalışan Kimliği Değeri**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmworkerbaseentity varlığına ait mshr_hcmworkerbaseentityid | İşe alınan adayın üst pozisyonundaki çalışanın sistem tarafından oluşturulan kimliği. |
| **Mali Boyut**<br>mshr_financialdimension<br>*Dize* | Salt okunur<br>İsteğe bağlı | Pozisyona atanan mali boyut (örneğin maliyet merkezi). Mali boyut, her bir geçerli varlıkta her bir pozisyon için atanır. Boyutlara göre tanımlanan maliyet merkezlerine mshr_dimattributeomcostcenterentity varlığı üzerinden erişilebilir. |
| **Veri Alanı Kimliği**<br>mshr_dataareaid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşe alma isteği pozisyonu için tüzel kişiliği (şirket) belirtir. |
| **Veri Alanı Kimliği Değeri**<br>_mshr_dataareaid_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: cdm_company varlığına ait cdm_companyid | İşe alma isteği pozisyonu için tüzel kişiliği (şirket) tanımlayan sistem tarafından oluşturulmuş GUID değeri. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Kaydı benzersiz olarak tanımlamak için başka bir yöntem olarak İşe Alma İsteği değerinin ve Pozisyon Kimliğinin birleştirilmesi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)

