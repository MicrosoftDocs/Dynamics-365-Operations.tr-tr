---
title: Değerlendirme düzeyi
description: Bu konu, Dynamics 365 Human Resources için Değerlendirme düzeyi varlığını açıklar.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125269"
---
# <a name="rating-level"></a>Değerlendirme düzeyi

Bu konu, Dynamics 365 Human Resources için Değerlendirme düzeyi varlığını açıklar.

Fiziksel ad: mshr_hcmratinglevelentity

## <a name="description"></a>Tanım

Bu varlık, beceriler için kullanılabilir değerlendirme düzeylerini sağlar. Değerlendirme düzeyleri tüm tüzel kişiliklerde geçerlidir.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Değerlendirme Düzeyi Varlık Kimliği**<br>mshr_hcmratinglevelentityid<br>*GUID* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Düzey için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Değerlendirme Düzeyi Kimliği**<br>mshr_ratinglevelid<br>*Dize* | Okuma/yazma<br>Gerekli | Düzey için kullanıcı tarafından okunabilir benzersiz tanımlayıcı. |
| **Değerlendirme Modeli Kimliği**<br>mshr_ratingmodelid<br>*Dize* | Okuma/yazma<br>Gerekli | Değerlendirme düzeyinin ait olduğu değerlendirme modeli. |
| **Değerlendirme Modeli Varlık Kimliği**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmratingmodelentity içindeki mshr_hcmratingmodelentityid | Değerlendirme düzeyinin ait olduğu değerlendirme modeli için sistem tarafından oluşturulan tanımlayıcı. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | Değerlendirme düzeyinin açıklaması. |
| **Faktör**<br>mshr_factor<br>*Tamsayı* | Okuma/yazma<br>Gerekli | Derecelendirme düzeyi için faktör. Öğeleri farklı sayıda değerlendirme düzeylerinde karşılaştırdığınızda, puanlar normalleştirmek için faktör kullanılır. Değer 0 ile 9 arasında bir tamsayı olmalıdır. |
| **Not**<br>mshr_note<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Değerlendirme düzeyiyle ilişkili notlar. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının tanımlayıcısı olarak kullanılacak alan. Değerlendirme düzeyi kimliği ve değerlendirme modeli kimliği birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

