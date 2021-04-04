---
title: Kişi filtreleme
description: Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.
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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467253"
---
# <a name="person-screening"></a>Kişi filtreleme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.

Fiziksel ad: mshr_hcmpersonscreeningentity

## <a name="description"></a>Tanım

Bu varlık, bir adayın geçtiği veya işe alım için geçmesi gereken filtrelemeleri açıklar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Filtreleme Varlığı Kimliği**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Kişi filtreleme kaydı için benzersiz birincil tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | Adayla ilişkili taraf (kişi) numarası. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı. |
| **Filtreleme Türü Kimliği**<br>mshr_screeningtypeid<br>*Dize* | Okuma/yazma<br>Gerekli<br>Yabancı anahtar: Filtreleme Türü | Human Resources'da tanımlanan filtreleme türünün tanımlayıcısı. |
| **Filtreleme Türü Kimlik Değeri**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmscreeningtypeentity içindeki mshr_hcmscreeningtypeentityid | İlişkili varlıktaki filtreleme türü kaydı için sistem tarafından oluşturulan tanımlayıcı. |
| **Gerekli**<br>mshr_requiredby<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Filtrelemenin tamamlanması gereken tarih. |
| **Durum**<br>mshr_status<br>*mshr_hcmcompletionstatus seçenek kümesi*<br>Okuma/yazma<br>Gerekli | Filtreleme için adayın durumunu sağlar. |
| **Tamamlanma Tarihi**<br>mshr_completeddate<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Filtrelemenin tamamlandığı tarih. |
| **Notlar**<br>mshr_note<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Yöneticileri ve işe alanları işe alımda kullanılacak notlar. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]