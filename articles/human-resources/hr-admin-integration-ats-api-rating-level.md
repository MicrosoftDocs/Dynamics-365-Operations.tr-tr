---
title: Değerlendirme düzeyi
description: Bu makalede, Dynamics 365 Human Resources için Değerlendirme düzeyi varlığı açıklanmaktadır.
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
ms.openlocfilehash: dcd366632456c186eca9682d79a0c8690772e8bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893888"
---
# <a name="rating-level"></a>Değerlendirme düzeyi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Değerlendirme düzeyi varlığı açıklanmaktadır.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
