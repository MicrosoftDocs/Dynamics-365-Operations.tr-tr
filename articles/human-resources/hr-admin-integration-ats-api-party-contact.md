---
title: Taraf ilgili kişisi
description: Bu konu, Dynamics 365 Human Resources için Taraf ilgili kişisi varlığını açıklar.
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
ms.openlocfilehash: b37910f10c0d89e2659aa0bfbdc601c3592f896c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053815"
---
# <a name="party-contact"></a>Taraf ilgili kişisi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Taraf ilgili kişisi varlığını açıklar.

Fiziksel ad: mshr_dirpartycontactentities

## <a name="description"></a>Tanım

Bu varlık; telefon, e-posta ve sosyal medya hesapları gibi adayın iletişim bilgilerini açıklar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Taraf İlgili Kişi Varlık Kimliği**<br>mshr_dirpartycontactentityid<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | İlişkili taraf (kişi) kaydının kimliği. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı. |
| **Yerleşim kodu**<br>mshr_locationid<br>*Dize* | Okuma/yazma<br>Gerekli | Adres kaydının konum kimliği. mshr_logisticspostaladdresslocationcdsentity varlığında ayarlayın. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | İlgili kişi ayrıntılarının açıklaması. |
| **Türü**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype seçenek kümesi* | Okuma/yazma<br>Gerekli | İlgili kişi ayrıntısı türü. |
| **Ülke/Bölge Kodu**<br>mshr_countryregioncode<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adresin bulunduğu ülke veya bölge. |
| **Bulucu**<br>mshr_locator<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İletişim bilgileri. Örneğin, tür **E-posta adresi** ise, bu alan adayın e-posta adresini içerir. |
| **Bulucu Uzantısı**<br>mshr_locatorextension<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Konum belirleyici uzantısı. Örneğin, tür **Telefon** ise bu özellik telefon numarası uzantısını içerir. |
| **Cep Telefonu**<br>mshr_ismobile<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | Telefonun cep telefonu numarası olup olmadığını belirtir. |
| **Anlık İleti**<br>mshr_isinstantmessage<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | Telefonun anlık ileti için etkinleştirilip etkinleştirilmediğini belirtir. |
| **Birincil**<br>mshr_isprimary<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | İlgili kişi türünün birincil kişisini belirler. İlgili kişi türü başına yalnızca bir birincil kayıt olmalıdır. |
| **Özel**<br>mshr_isprivate<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | Bu adresin kişi için özel adres olup olmadığını tanımlar. |
| **Amaç**<br>mshr_purpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | İletişim bilgilerinin amacı/rolü. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının birincil tanımlayıcısı olarak kullanılan alan. Taraf numarası, türü, açıklaması ve konum bulucu birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]