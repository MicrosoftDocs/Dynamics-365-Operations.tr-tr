---
title: Kişi filtreleme
description: Bu konu, Dynamics 365 Human Resources için Kişi filtreleme varlığını açıklar.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798045"
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