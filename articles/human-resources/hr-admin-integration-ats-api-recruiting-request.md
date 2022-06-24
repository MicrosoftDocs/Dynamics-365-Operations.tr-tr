---
title: İşe alma isteği
description: Bu makalede, Dynamics 365 Human Resources için İşe alma isteği varlığı açıklanmaktadır.
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
ms.openlocfilehash: 58e509a819e5cda650fddab8dd0c4d55d5148db1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872282"
---
# <a name="recruiting-request"></a>İşe alma isteği


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için İşe alma isteği varlığı açıklanmaktadır.

Fiziksel ad: mshr_hcmrecruitingrequestentity

### <a name="description"></a>Tanım

Bir iş için işe alma isteğini açıklar.

### <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İşe Alma İsteği Kimliği**<br>mshr_recruitingrequestid<br>*Dize* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | HR uygulamasında görüntülenen istek için kullanıcı tarafından okunabilir benzersiz bir tanımlayıcı. Numara serisi. |
| **İşe Alma İsteği Varlık Kimliği**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | İşe alma isteğini benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |
| **Veri Alanı Kimliği**<br>mshr_dataareaid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı<br> | İşe alma isteği için tüzel kişiliği (şirketi) belirtir. |
| **Veri Alanı Kimliği Değeri**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: cdm_company varlığına ait cdm_companyid | Tüzel kişiliği (şirket) tanımlaması için işe alma isteğine yönelik sistem tarafından oluşturulan GUID değeri. |
| **İşe Alma Yöneticisi Personel Numarası**<br>mshr_hiringmanagerpersonnelnumber<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Bu işe alım isteğiyle ilişkili işe alma yöneticisinin personel numarası. |
| **İşe Alma Yöneticisi Kimlik Değeri**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmworkerbaseentity varlığına ait mshr_hcmworkerbaseentityid | İşe alma isteğiyle ilişkili yöneticiyi tanımlamak için sistem tarafından oluşturulan GUID değeri. |
| **İşe Alan Taraf Numarası**<br>mshr_recruiterpartynumber<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İstek için seçilen işe alan kişinin (taraf) numarası. |
| **İşe Alan Kişi Kimlik Değeri**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_dirpersonentity varlığına ait mshr_dirpersonentityid | İşe alma isteğiyle ilişkili işe alan kişiyi tanımlamak için sistem tarafından oluşturulan GUID değeri. |
| **Durum**<br>mshr_status<br>*RecruitingRequestStatus* seçenek kümesi | Okuma/yazma<br>Gerekli<br> | İşe alma isteğinin durumunu belirtir. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | İsteği açıklar. |
| **İşe Alma İsteği Konum Kimliği**<br>mshr_recruitingrequestlocationid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Bu istekle ilişkilendirilmiş iş konumunun kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **İşe Alım Konum Kimliği Değeri**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmrecruitingrequestlocationentity varlığına ait mshr_hcmrecruitingrequestlocationentityid | İstek için seçilen işe alma isteği konumunu tanımlamak için sistem tarafından oluşturulan GUID değeri. |
| **Yorumlar**<br>mshr_comments<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşe alım yöneticileri ve işe alan kişiler tarafından kullanılacak istek yorumları. |
| **İş Kodu**<br>mshr_jobid<br>*Dize* | Bir kez yaz<br>Gerekli |   Bu istekle ilişkilendirilmiş tüm Pozisyonlar tarafından paylaşılan kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **İş Kimlik Değeri**<br>_mshr_fk_job_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmjobentity varlığına ait mshr_hcmjobentityid | İşe alma isteğiyle ilişkili tüm Pozisyonlar tarafından paylaşılan işin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Unvan Kimliği**<br>mshr_titleid<br>*Dize* | Salt okunur<br>Gerekli | Bu istekle ilişkilendirilmiş iş unvanının kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **Unvan Kimliği Değeri**<br>_mshr_fk_title_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmtitleentity varlığına ait mshr_hcmtitleid | İşe alma isteği için seçilen iş unvanının sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **İş İşlevi Kimliği**<br>mshr_jobfunctionid<br>*Dize* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmjobfunctionentity varlığına ait mshr_jobfunctionid | Bu istekle ilişkilendirilmiş iş işlevinin kullanıcı tarafından okunabilir benzersiz tanımlayıcısı. |
| **Varsayılan Tam Zaman Eşdeğeri**<br>mshr_defaultfulltimeequivalency<br>*Çift* | Salt okunur<br>Gerekli | 1.0'ın tam zamanlı bir çalışanı temsil ettiği, iş için tam zamanlı eşdeğer değeri. |
| **Mevzuat İşi Kategorisi**<br>mshr_regulatoryjobcategory<br>*RegulatoryJobCategory* seçenek kümesi | Salt okunur<br>İsteğe bağlı | İş için seçilen iş işlevinin EEO iş kategorisi. HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory) seçenek kümesine dahil olan geçerli değerler. |
| **İş Türü Kimliği**<br>mshr_jobtypeid<br>*Dize* | Salt okunur<br>İsteğe bağlı | Pozisyonla ilişkili işin türü. İş türleri, mshr_hcmjobtypeentity varlığında bulunan kullanıcı tanımlı değerlerdir. |
| **İş Türü Kimlik Değeri**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmjobtypenentity varlığına ait mshr_hcmjobtypeentityid | İşe alma isteği için projeyle ilişkili iş türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Muafiyet durumu**<br>mshr_exemptstatus<br>*JobExemptStatus* seçenek kümesi | Salt okunur<br>İsteğe bağlı | İş türüne göre FLSA muafiyet durumu. |
| **Tahmini Başlangıç Tarihi**<br>mshr_estimatedstartdate<br>*Date* | Okuma/yazma<br>Gerekli | Bir adayın işe başlayacağı tahmini tarih. |
| **Harici Açıklama**<br>mshr_externaldescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşin/pozisyonun adaya yönelik açıklaması. | 
| **Ücret Alt Eşiği**<br>mshr_compensationlowthreshold<br>*Çift* | Okuma/yazma<br>İsteğe bağlı | Ücret düzeyi için alt sınır. |
| **Ücret Denetim Noktası**<br>mshr_compensationcontrolpoint<br>*Çift* | Okuma/yazma<br>İsteğe bağlı | Ücret düzeyi için denetim noktası. |
| **Ücret Üst Eşiği**<br>mshr_compensationhighthreshold<br>*Çift* | Okuma/yazma<br>İsteğe bağlı | Ücret düzeyi için üst sınır. |
| **Ücret Düzeyi**<br>mshr_compensationlevelid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşin maaş düzeyi. Bir iş birden çok maaş düzeyiyle ayarlanabilir. Bu öznitelik, bu istek için seçilen iş maaş düzeyini gösterir. |
| **İş Maaş Kimliği**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmjobcompensationentity varlığına ait mshr_hcmjobcompensationentityid | İşe alma isteğinin İşi ile ilişkili maaş düzeyi için sistem tarafından oluşturulan benzersiz tanımlayıcı. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
