---
title: Sertifika türü
description: Bu konu, Dynamics 365 Human Resources için Sertifika türü varlığını açıklar.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125725"
---
# <a name="certificate-type"></a>Sertifika türü

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