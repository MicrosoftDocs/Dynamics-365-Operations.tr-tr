---
title: Kişi profesyonel deneyimi
description: Bu makalede, Dynamics 365 Human Resources için Kişinin profesyonel deneyimi varlığı açıklanmaktadır.
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
ms.openlocfilehash: d306213e4c647ecd4be98598cba92376aba0d5bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856439"
---
# <a name="person-professional-experience"></a>Kişi profesyonel deneyimi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Kişinin profesyonel deneyimi varlığı açıklanmaktadır.

Fiziksel ad: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>Tanım

Bu varlık, bir adayın professional deneyimini veya iş geçmişini açıklar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişinin Profesyonel Deneyimi Varlık Kimliği**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Salt okunur<br>Gerekli | Varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | Aday için kişi kaydının benzersiz tanıtıcısı. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Kişi varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **İşveren Pozisyonu**<br>mshr_employerposition<br>*Dize* | Okuma/yazma<br>Gerekli | Adayın çalıştığı sıradaki pozisyonun unvanı. |
| **İşveren Adı**<br>mshr_employername<br>*Dize* | Okuma/yazma<br>Gerekli | İşverenin adı. |
| **İşveren Konumu**<br>mshr_employerlocation<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşverenin konumu. Maks. uzunluk: 60. Tanımlanmış veya gerekli belirli bir biçim yok. |
| **Telefon**<br>mshr_phone<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşverenin telefon numarası. |
| **URL**<br>mshr_url<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşverenin web sitesinin URL'si. |
| **Başlangıç Tarihi**<br>mshr_startdate<br>*Tarih saat* | Okuma/yazma<br>Gerekli | Adayın işe başlama tarihi. |
| **Bitiş Tarihi**<br>mshr_enddate<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Adayın işten çıkış tarihi veya aday hala burada çalışıyorsa null. |
| **İlgili Kişi İşverenine İzin Ver**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Adayın önceki işverenle iletişime geçmesine izin verip vermediğini gösterir. |
| **Notlar**<br>mshr_note<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İşe alan veya işe alma yöneticisinin kullanımına yönelik notlar. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının birincil tanımlayıcısı olarak kullanılan alan. Taraf numarası, başlangıç tarihi, işveren pozisyonu ve işveren adının birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
