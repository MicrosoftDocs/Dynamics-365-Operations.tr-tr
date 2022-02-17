---
title: Sertifika türü
description: Bu konu, Dynamics 365 Human Resources için Sertifika türü varlığını açıklar.
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
ms.openlocfilehash: 3d01c7f01657af1501aed14f63dfb2cfbc133f8b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067213"
---
# <a name="certificate-type"></a>Sertifika türü


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Sertifika türü varlığını açıklar.

Fiziksel ad: mshr_hcmcertificatetypeentity

## <a name="description"></a>Tanım

Bu varlık, Human Resources'da ayarlanan profesyonel sertifika türlerinin listesini tanımlar. Varlık, tüzel kişiliklere (şirketler) özgü değildir.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Sertifika Türü Varlık Kimliği**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Salt okunur<br>Gerekli 
Sistem tarafından oluşturuldu | Sertifika türü için benzersiz birincil tanımlayıcı. |
| **Sertifika Türü**<br>mshr_certificatetype<br>*Dize* | Okuma/yazma<br>Gerekli | Sertifika türü için benzersiz kullanıcı tarafından okunabilir tanımlayıcı. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | Sertifika türü açıklaması. |
| **Yenileme Gerektir**<br>mshr_requirerenewal<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Sertifika için yenileme gerekip gerekmediğini gösterir. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
