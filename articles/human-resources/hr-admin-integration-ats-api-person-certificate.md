---
title: Kişi sertifikası
description: Bu makalede, Dynamics 365 Human Resources için Kişi sertifikası varlığı açıklanmaktadır.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887330"
---
# <a name="person-certificate"></a>Kişi sertifikası


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Kişi sertifikası varlığı açıklanmaktadır.

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

| Özellik<br>**Fiziksel ad**<br>**_Tür_** | Kullan | Açıklama |
| --- | --- | --- |
| **Sertifika Türü Kimliği**<br>mshr_certificatetypeid<br>*Dize* | Okuma/yazma<br>Gerekli |  Human Resources'da tanımlanan sertifika türünün tanımlayıcısı. |
| **Başlangıç Tarihi**<br>mshr_startdate<br>*Tarih saat* | Okuma/yazma<br>Gerekli | Sertifikanın oluşturulduğu tarih. |
| **Bitiş Tarihi**<br>mshr_enddate<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Sertifikanın süresinin dolacağı tarih. |
| **Notlar**<br>mshr_notes<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Yöneticileri ve işe alanları işe alımda kullanılacak notlar. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | Adayın taraf (kişi) kimliği. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt Okunur<br>Gerekli |  Varlık kaydının tanımlayıcısı olarak kullanılacak alan. Taraf numarası, sertifika türü kimliği ve başlangıç tarihi birleşimi. |
| **Sertifika Türü Kimlik Değeri**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmcertificatetypeentity içindeki mshr_hcmcertificatetypeentityid | İlişkili varlıktaki sertifika türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt Okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı. |
| **Kişi Sertifikası Varlık Kimliği**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Salt okunur<br>Gerekli | Kişi sertifikası varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |




## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
