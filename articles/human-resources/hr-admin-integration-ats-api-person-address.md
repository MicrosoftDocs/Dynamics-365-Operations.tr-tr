---
title: Kişi adresi
description: Bu konu, Dynamics 365 Human Resources için Kişi adresi varlığını açıklar.
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
ms.openlocfilehash: 14db209e420770234583add93fa72d086f1b5ea6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053791"
---
# <a name="person-address"></a>Kişi adresi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Kişi adresi varlığını açıklar.

Fiziksel ad: mshr_hcmpersonaddressentities

## <a name="description"></a>Tanım

Bu varlık, aday kayıtları için posta adreslerinin listesini içerir.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Adresi Varlık Kimliği**<br>mshr_hcmpersonaddressentityid<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | İlişkili taraf (kişi) kaydının kimliği. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity içindeki mshr_dirpersonentityid | Taraf (kişi) varlık kaydının sistem tarafından oluşturulan tanımlayıcısı. |
| **Yerleşim kodu**<br>mshr_locationid<br>*Dize* | Okuma/yazma<br>Gerekli | Adres kaydının konum kimliği. mshr_logisticspostaladdresslocationcdsentity varlığında ayarlayın. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | Adayın adresinin açıklaması. |
| **Roller**<br>mshr_roles<br>*Dize* | Okuma/yazma<br>Gerekli | Bu adres için atanan roller. Birden fazla rol atanabilir. Her rol noktalı virgülle ayrılmalıdır. mshr_logisticslocationroleentity varlığında bulunan geçerli değerler. |
| **Sokak**<br>mshr_street<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Sokak numarası. |
| **Şehir**<br>mshr_city<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adresin bulunduğu şehir. mshr_logisticsaddresscityentity varlığında ayarlanır. |
| **İl**<br>mshr_state<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adresin bulunduğu il. mshr_logisticsaddressstateentity varlığında ayarlanır. |
| **İlçe**<br>mshr_county<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adresin bulunduğu ilçe. mshr_logisticsaddresscountyentity varlığında ayarlanır. |
| **Posta Kodu**<br>mshr_zipcode<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adresin posta kodu. mshr_logisticsaddresspostalcodeentity varlığında ayarlanır. |
| **Ülke/Bölge Kodu**<br>mshr_countryregionid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Adresin bulunduğu ülke veya bölge. |
| **Ülke/Bölge Kimlik Değeri**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_logisticsaddresscountryregionentity içindeki mshr_logisticaddresscountryregionentityid | Adresin ülkesinin/bölgesinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Birincil**<br>mshr_isprimary<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | Bu adresin tanımlanan rolün kişisi için birincil adres olup olmadığını tanımlar. |
| **Özel**<br>mshr_isprivate<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>Gerekli | Bu adresin kişi için özel adres olup olmadığını tanımlar. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının birincil tanımlayıcısı olarak kullanılan alan. Taraf numarası ve konum kimliği birleşimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]