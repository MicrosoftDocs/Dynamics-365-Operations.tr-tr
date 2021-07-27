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
ms.openlocfilehash: a99d53805efd7ee2001217ea3154d46b5d5e66cd
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314511"
---
# <a name="leave-type"></a>İzin türü

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
