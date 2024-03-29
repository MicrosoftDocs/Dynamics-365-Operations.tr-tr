---
title: Kişi eğitimi
description: Bu makalede, Dynamics 365 Human Resources için Kişi eğitimi varlığı açıklanmaktadır.
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
ms.openlocfilehash: 0fbbb467852d2aeb070c7732c9aa3108fd504de0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893917"
---
# <a name="person-education"></a>Kişi eğitimi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Kişi eğitimi varlığı açıklanmaktadır.

Fiziksel ad: mshr_hcmpersoneducationentity

## <a name="description"></a>Tanım

Bu varlık, aday olan kişinin eğitim geçmişini içerir. Eğitim, aday kaydına ek olarak, ilgili kişi için oluşturulmuş diğer rollerle (çalışan, yüklenici vb.) ilişkilendirilmesini sağlayan kişi kaydıyla bağlantılıdır.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Eğitim Varlığı Kimliği**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Salt okunur<br>Gerekli | Kişi eğitim varlığı kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | Taraf (kişi) için kişi kaydının benzersiz tanımlayıcısı. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Adayın kişi kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Alacak Temeli**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Eğitim derecesindeki kredi temeli. |
| **Tamamlanan Kredi Sayısı**<br>mshr_creditscompleted<br>*Ondalık* | Okuma/yazma<br>İsteğe bağlı | Eğitim için tamamlanan kredi sayısı. |
| **Kazanılan Krediler**<br>mshr_creditsearned<br>*Ondalık* | Okuma/yazma<br>İsteğe bağlı | Devam eden bir dereceyle ilgili eğitim kaydı için kazanılan krediler. |
| **Gereken Krediler**<br>mshr_creditsneeded<br>*Ondalık* | Okuma/yazma<br>İsteğe bağlı | Devam eden bir derece için gereken kredi sayısı. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adayın derecesinin açıklaması. |
| **Eğitim Düzeyi Kimliği**<br>mshr_educationlevelid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Eğitim düzeyinin kimliği. | 
| **Eğitim Düzeyi Kimlik Değeri**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmeducationdegreeentity varlığına ait mshr_hcmeducationdegreeentityid | Eğitim derecesi kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. Bu tanımlayıcı, kuruluş için tanımlanan dereceleri ve eğitim düzeylerini sağlar. |
| **Eğitim Alanı Kimliği**<br>mshr_educationdisciplineid<br>*Dize* | Okuma/yazma<br>Gerekli<br>Yabancı anahtar: EducationDiscipline | Eğitim alanının kimliği. |
| **Eğitim Alanı Kimlik Değeri**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmeducationdisciplineentity varlığına ait mshr_hcmeducationdisciplineentityid | Eğitim kaydına ait eğitim alanının sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **İkincil Vurgu**<br>mshr_secondaryemphasis<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kazanılan dereceyle ilgili ikincil vurgu. |
| **Eğitim Kurumu Kimliği**<br>mshr_educationinstitutionid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Katılınan eğitim kurumunun kimliği. |
| **Eğitim Kurumu Kimlik Değeri**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmeducationinstitutionentity varlığına ait mshr_hcmeducationinstitutionentityid | Eğitim kurumunun sistem tarafından oluşturulan tanımlayıcısı. |
| **Başlangıç Tarihi**<br>mshr_startdate<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Kazanılan derece için eğitim başlangıç tarihi. |
| **Bitiş Tarihi**<br>mshr_enddate<br>*Tarih saat* | Okuma/yazma<br>Gerekli | Kimlik bilgisinin verildiği tarih. |
| **Süre**<br>mshr_duration<br>*Ondalık* | Okuma/yazma<br>İsteğe bağlı | Eğitim kaydının süresi. |
| **Zaman Birimi**<br>mshr_durationunit<br>*mshr_periodunit option set* | Okuma/yazma<br>İsteğe bağlı | Eğitim kaydının süresiyle ilişkilendirilmiş zaman birimi. |
| **Not Puan Ortalaması**<br>mshr_gradepointaverage<br>*Ondalık* | Okuma/yazma<br>İsteğe bağlı | Derece için kazanılan not puanı. |
| **Not Ölçeği**<br>mshr_gradescale<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Not puanı ortalaması için kullanılan ölçek. |
| **Notlar**<br>mshr_notes<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşe alan veya işe alma yöneticisinin kullanımına yönelik notlar. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının başka bir birincil tanımlayıcısı olarak kullanılan alan. Taraf numarası, eğitim alanı kimliği, eğitim kurumu kimliği ve eğitim düzeyi kimliği birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
