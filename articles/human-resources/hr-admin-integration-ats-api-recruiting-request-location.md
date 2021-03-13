---
title: İşe alma isteği konumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği konum varlığını açıklar.
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
ms.openlocfilehash: fa153b1cfcbb70294ed6da3618c83396df04f8db
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125245"
---
# <a name="recruiting-request-location"></a>İşe alma isteği konumu

Bu konu, Dynamics 365 Human Resources için İşe alma isteği konum varlığını açıklar.

Fiziksel ad: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>Tanım

İşe alınan personelin işe alındıktan sonra çalışacakları yerler olarak tanımlanan konumların listesi. Bunlar tüzel kişilikler genelinde oluşturulan konumlardır.

### <a name="json-representation"></a>JSON gösterimi

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Yerleşim kodu**<br>mshr_locationid<br>*Dize* | Bir kez yaz<br>Gerekli | İşe alma konumu için sistem tarafından oluşturulan, kullanıcı tarafından okunabilir tanımlayıcı. |
| **İşe Alma İsteği Konumu**<br>mshr_recruitingrequestlocationid<br>*Dize* | Bir kez yaz<br>Gerekli | İşe alma konumu için kullanıcı tarafından tanımlanan benzersiz tanımlayıcı. |
| **İşe Alma İsteği Konumu Varlık Kimliği**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Salt okunur<br>Gerekli | İşe alma isteği konum kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>Gerekli | Yerleşimin açıklaması. |
| **Ülke/Bölge Kimliği**<br>mshr_countryregionid<br>*Dize* | Salt okunur<br>İsteğe bağlı | Adayın vatandaşı olduğu ülkeyi veya bölgeyi belirtir. |
| **Ülke/Bölge Kimlik Değeri**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_logisticsaddresscountryregionentity içindeki mshr_logisticaddresscountryregionentityid | Adresin ülkesinin/bölgesinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Posta Kodu**<br>mshr_zipcode<br>*Dize* | Salt okunur<br>İsteğe bağlı | Posta kodu. |
| **Sokak**<br>mshr_street<br>*Dize* | Salt okunur<br>İsteğe bağlı | Açık adres. |
| **Şehir**<br>mshr_city<br>*Dize* | Salt okunur<br>İsteğe bağlı | Şehir. |
| **İl**<br>mshr_state<br>*Dize* | Salt okunur<br>İsteğe bağlı | Eyalet veya il. |
| **İlçe**<br>mshr_county<br>*Dize* | Salt okunur<br>İsteğe bağlı | İlçe. |
| **Telefon**<br>mshr_telephone<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Konumun telefon numarası. |
| **E-posta**<br>mshr_email<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | E-posta adresi. |
| **İnternet Adresi**<br>mshr_internetaddress<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Konum web sitesinin URL'si. |
| **Veri Alanı Kimliği**<br>mshr_dataareaid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Tüzel kişiliği (şirket) belirtir. |
| **Veri Alanı Kimliği Değeri**<br>_mshr_dataareaid_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: cdm_company varlığına ait cdm_companyid | Tüzel kişiliği (şirket) tanımlaması için sistem tarafından oluşturulan GUID değeri. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)

