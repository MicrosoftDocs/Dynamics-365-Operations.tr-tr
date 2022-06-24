---
title: Kişi yeteneği
description: Bu makalede, Dynamics 365 Human Resources için Kişinin becerileri varlığı açıklanmaktadır.
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
ms.openlocfilehash: 713fde6d05904f96f7b17721e15805e07159cf78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891335"
---
# <a name="person-skill"></a>Kişi yeteneği


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Kişinin becerileri varlığı açıklanmaktadır.

Fiziksel ad: mshr_hcmpersonskillentity

## <a name="description"></a>Tanım

Bu varlık, bir adayın yeteneklerini açıklar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Yetenek Varlığı Kimliği**<br>mshr_hcmpersonskillentityid<br>*GUID* | Salt okunur<br>Gerekli | Varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli |   İlişkili taraf (kişi) kaydının kimliği. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı. |
| **Sertifika veren**<br>mshr_certifier<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Bu yeteneği onaylayan çalışanın personel numarası. |
| **Sertifikayı Veren Kimlik Değeri**<br>_mshr_fk_certifier_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmworkerentity varlığına ait mshr_hcmworkerentityid | Yetenek için sertifikalanan çalışan için çalışan kaydının sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Yetenek Kimliği**<br>mshr_skillid<br>*Dize* | Okuma/yazma<br>Gerekli | Human Resources'da tanımlanan yeteneğin tanımlayıcısı. |
| **Yetenek Kimliği Değeri**<br>_mshr_fk_skill_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmskillentity varlığına ait mshr_hcmskillentityid | Seçili yeteneğin sistem tarafından oluşturulan tanımlayıcısı. |
| **Deneyim Yılı Sayısı**<br>mshr_yearsofexperience<br>*Ondalık* | Okuma/yazma<br>İsteğe bağlı | Adayın bu yetenekle sahip olduğu deneyim yılı sayısı. |
| **Değerlendirme Kimliği**<br>mshr_ratingid<br>*Dize* | Okuma/yazma<br>Gerekli | Değerlendirme ölçeği türü. Bu varlk için değer **Yetenekler**'dir. |
| **Düzey Türü**<br>mshr_leveltype<br>*mshr_hrmskillleveltype seçenek kümesi* | Okuma/yazma<br>Gerekli | Yeteneğe atanan düzey için tür kategorizasyonu. |
| **Düzey Kimliği**<br>mshr_levelid<br>*Dize* | Okuma/yazma<br>Gerekli | Adayın bu yetenek için sahip olduğu Değerlendirme Düzeyinin Kimliği. |
| **Değerlendirme Düzeyi Kimlik Değeri**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmratinglevelentity varlığına ait mshr_hcmratinglevelentityid | Değerlendirme düzeyinin sistem tarafından oluşturulan tanımlayıcısı. |
| **Düzey Tarihi**<br>mshr_leveldate<br>*Tarih saat* | Okuma/yazma<br>Gerekli | Adayın yetenek için değerlendirildiği tarih. |
| **Değerlendirme Düzeyi Denetleyicisi**<br>mshr_ratinglevelexaminer<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adayı değerlendiren çalışanın personel numarası. |
| **Değerlendirme Düzeyi Denetleyicisi Değeri**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmworkerentity varlığına ait mshr_hcmworkerentityid | Adayın yetenek düzeyini inceleyen çalışanın sistem tarafından oluşturulan tanımlayıcısı. |
| **Doğrulandı**<br>mshr_verified<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | Değerlendirilen yetenek düzeyinin doğrulanıp doğrulanmadığını gösterir. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının tanımlayıcısı olarak kullanılacak alan. Taraf numarası, düzey türü, yetenek kimliği ve başlangıç tarihi birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
