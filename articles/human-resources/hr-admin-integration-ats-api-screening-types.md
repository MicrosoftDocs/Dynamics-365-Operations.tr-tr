---
title: Filtreleme türleri
description: Bu konu, Dynamics 365 Human Resources için Filtreleme türleri varlığını açıklar.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126182"
---
# <a name="screening-types"></a>Filtreleme türleri

Bu konu, Dynamics 365 Human Resources için Filtreleme türleri varlığını açıklar.

Fiziksel ad: mshr_hcmscreeningtypeentity

## <a name="description"></a>Tanım

Bu varlık, şirket tarafından işe alım öncesi ve devam eden personel filtreleme işlemleri için ayarlanan filtreleme türlerini açıklar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Filtreleme Türü Varlık Kimliği**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Filtreleme türü kaydı için benzersiz birincil tanımlayıcı. |
| **Filtreleme Türü Kimliği**<br>mshr_screeningtypeid<br>*Dize* | Okuma/yazma<br>Gerekli | Filtreleme türü için kullanıcı tanımlı benzersiz tanımlayıcı. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | Filtreleme türünün açıklaması. |
| **Sıklık Birimi**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit seçenek kümesi* | Okuma/yazma<br>Gerekli | Atanan kişi için filtrelemenin tamamlanacağı sıklığı açıklar. |
| **Oluşturma Kaynağı**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom seçenek kümesi* | Okuma/yazma<br>Gerekli | Sıklık değeri "Yalnızca bir seferlik" dışında bir değerse, GenerateFrom değeri bir sonraki filtreleme olayının hesaplanacağı tarihi belirler. |
| **Sıklık Aralığı**<br>mshr_frequencyinterval<br>*Tamsayı* | Okuma/yazma<br>Gerekli | Sıklık değeri "Yalnızca bir seferlik" dışında bir değerse her filtreleme olayı arasındaki zaman birimleri için bir aralık tanımlamanız gerekir. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
