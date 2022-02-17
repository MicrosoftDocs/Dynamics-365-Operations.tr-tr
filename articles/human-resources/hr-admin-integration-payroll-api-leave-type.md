---
title: İzin türü
description: Bu konu, Dynamics 365 Human Resources'taki izin türü varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
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
ms.openlocfilehash: dced58e6e9f6c20578e4582e4cf39162622713e7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069919"
---
# <a name="leave-type"></a>İzin türü


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için izin türü varlığını açıklar.

### <a name="description"></a>Tanım

Bu varlık belirtilen izin türü hakkında bilgi sağlar.

Fiziksel ad: mshr_essleavetypeentity.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İzin türü kodu**</br>mshr_leavetypeid</br>*Dize* | Salt okunur | İzin türü kodu. |
| **Açıklama**</br>mshr_description</br>*Dize* | Salt okunur | İzin türünün açıklaması. |
| **Kategori**</br>mshr_category</br>*mshr_LeaveTypeCategory seçenek kümesi* | Salt okunur | İzin türü kategorisi. |
| **Neden kodu gereklidir**</br>mshr_isreasoncoderequired</br>*mshr_NoYes seçenek kümesi* | Salt okunur | İzin türü için neden kodu gerekli olup olmadığını tanımlar. |
| **İzin birimi**</br>mshr_leaveamountunit</br>*mshr_LeaveAmountUnit seçenek kümesi* | Salt okunur | Bu izin türünün birimi. |
| **Yarım günü etkinleştir**</br>mshr_enablehalfdaydefinition</br>*mshr_NoYes seçenek kümesi* | İzin türü için yarım günün etkin olup olmadığı tanımlar. |
| **Veri alanı kimliği**</br>mshr_dataareaid_id</br>*Dize* | Salt okunur | Tüzel kişiliği (şirket) belirtir. |
| **İzin türü varlığı**</br>mshr_essleavetypeentityid</br>*GUID* | Sistem tarafından oluşturulan | İzin türünü benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Yanıt**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
