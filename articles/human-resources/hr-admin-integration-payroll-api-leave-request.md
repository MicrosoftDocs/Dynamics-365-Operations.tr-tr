---
title: İzin isteği
description: Bu makalede, Dynamics 365 Human Resources'daki izin isteği varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlanmaktadır.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899686"
---
# <a name="leave-request"></a>İzin isteği


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için izin isteği varlığı açıklanmaktadır.

### <a name="description"></a>Açıklama

Bu varlık bir izin isteği hakkında bilgi sağlar.

Fiziksel ad: mshr_essleaverequestentity.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İstek kodu**</br>mshr_requestid</br>*Dize* | Salt okunur | İstek Kodu. |
| **İzin türü kodu**</br>mshr_leavetypeid</br>*Dize* | Salt okunur | İzin türü kodu. |
| **Date**</br>mshr_leavedate</br>*Tarih Saat Sapması* | Salt okunur | İzin isteği tarihi. |
| **Tutar**</br>mshr_amount</br>*Ondalık* | Salt okunur | İzin isteği tutarı. |
| **Yarım gün türü**</br>mshr_halfdaydefinition</br>*mshr_LeaveHalfDayDefinition seçenek kümesi* | Salt okunur | Yarım gün izin türü. |
| **Yorum**</br>mshr_comment</br>*Dize* | Salt okunur | İzin için açıklama. |
| **Durum**</br>mshr_status</br>*mshr_status seçenek kümesi* | Salt okunur | İsteğin durumu. |
| **Date**</br>mshr_requestdate</br>*Tarih Saat Sapması* | Salt okunur | İstek tarihi. |
| **Personel numarası**</br>mshr_personnelnumber</br>*Dize* | Salt okunur | Çalışanın benzersiz personel numarası. |
| **Neden kodu kimliği**</br>mshr_reasoncodeid</br>*Dize* | Salt okunur | Neden kodu kimliği. |
| **Veri alanı kimliği**</br>mshr_dataareaid</br>*Dize* | Salt okunur | Tüzel kişiliği (şirket) belirtir. |
| **Birincil alan**</br>mshr_primaryfield</br>*GUID* | Salt okunur</br>Sistem tarafından oluşturulan | |
| **İzin türü varlığı**</br>mshr_essleaverequestentityid</br>*GUID* | Sistem tarafından oluşturulan | İzin isteğini benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Yanıt**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
