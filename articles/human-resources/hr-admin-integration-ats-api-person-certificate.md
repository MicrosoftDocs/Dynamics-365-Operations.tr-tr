---
title: Kişi sertifikası
description: Bu konu, Dynamics 365 Human Resources için Kişi sertifikası varlığını açıklar.
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
ms.openlocfilehash: 300bf294bb4b2fadd4c5d3e68e74674a69dd48f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067841"
---
# <a name="person-certificate"></a>Kişi sertifikası


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Kişi sertifikası varlığını açıklar.

Fiziksel ad: mshr_hcmpersoncertificateentity

## <a name="description"></a>Tanım

Bu varlık, bir adayın mesleki sertifikalarını açıklar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Sertifikası Varlık Kimliği**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Salt okunur<br>Gerekli | Kişi sertifikası varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | Adayın taraf (kişi) kimliği. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı. |
| **Sertifika Türü Kimliği**<br>mshr_certificatetypeid<br>*Dize* | Okuma/yazma<br>Gerekli |  Human Resources'da tanımlanan sertifika türünün tanımlayıcısı. |
| **Sertifika Türü Kimlik Değeri**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmcertificatetypeentity içindeki mshr_hcmcertificatetypeentityid | İlişkili varlıktaki sertifika türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Başlangıç Tarihi**<br>mshr_startdate<br>*Tarih saat* | Okuma/yazma<br>Gerekli | Sertifikanın oluşturulduğu tarih. |
| **Bitiş Tarihi**<br>mshr_enddate<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Sertifikanın süresinin dolacağı tarih. |
| **Notlar**<br>mshr_notes<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Yöneticileri ve işe alanları işe alımda kullanılacak notlar. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli |  Varlık kaydının tanımlayıcısı olarak kullanılacak alan. Taraf numarası, sertifika türü kimliği ve başlangıç tarihi birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
