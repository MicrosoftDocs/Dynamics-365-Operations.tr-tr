---
title: Sertifika türü
description: Bu konu, Dynamics 365 Human Resources için Sertifika türü varlığını açıklar.
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798405"
---
# <a name="certificate-type"></a>Sertifika türü

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