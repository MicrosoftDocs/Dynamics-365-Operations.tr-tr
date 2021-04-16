---
title: Kişi kimlik numarası
description: Bu konu, Dynamics 365 Human Resources için Kişi kimlik numarası varlığını açıklar.
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
ms.openlocfilehash: a8fa924898472302e67dd4e32251ca0c94da0ea9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798093"
---
# <a name="person-identification-number"></a>Kişi kimlik numarası

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Kişi kimlik numarası varlığını açıklar.

Fiziksel ad: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>Tanım

Bu varlık, adayın kimlik numaralarını açıklar. API tüketicisinin aday kaydına Sosyal Güvenlik numaraları veya pasaport numaraları gibi kimlik numaraları yazmasını sağlar. Kimlik numaraları çalışan kaydında ortaya çıkar ancak aday kaydında kullanılmaz. Tümleştirici bir uygulama, değerleri Human Resources veritabanına yazabilir ancak adayın çalışan kaydı oluşturulana kadar numaralar Human Resources'da görünmez.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Kimlik Numarası Varlık Kimliği**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Kişi kimlik numarası kaydı için benzersiz birincil tanımlayıcı. |
| **Giriş türü**<br>mshr_entrytype<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kimlik numarası için giriş türüne başvuracak serbest değer. |
| **Açıklama**<br>mshr_description<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kimlik numarasının açıklaması. |
| **Bitiş Tarihi**<br>mshr_expirationdate<br>*Tarih saat* | Okuma/yazma<br>İsteğe bağlı | Kimlik numarasının veya ilişkili belgenin süresinin dolacağı tarih. |
| **Birincil**<br>mshr_isprimary<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kimlik numarasının, bu kimlik türü için kişinin birincil kaydı olup olmadığını tanımlar. |
| **Kimlik Numarası**<br>mshr_identificationnumber<br>*Dize* | Okuma/yazma<br>Gerekli | Kimlik numarası. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Okuma/yazma<br>Gerekli | Kimlik numarasına sahip olan tarafın (kişinin) tanımlayıcısı. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_dirpersonentity varlığına ait mshr_dirpersonentityid | Tarafın (kişi) benzersiz tanımlayıcısı. |
| **Tanımlama Türü Kimliği**<br>mshr_identificationtypeid<br>*Dize* | Okuma/yazma<br>Gerekli | Kimlik numarasının türü. |
| **Tanımlama Türü Kimlik Değeri**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_hcmidentificationtypeentity varlığına ait mshr_hcmidentificationtypeentityid | Kimlik türünün sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Veren Kurum Kimliği**<br>mshr_issuingagencyid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kimlik numarasını veren kurum veya kuruluş. |
| **Veren Kurum Kimlik Değeri**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmissuingagencyentity varlığına ait mshr_hcmissuingagencyentityid | Kimlik numarasını veren kurumun sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Birincil Alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli | Varlık kaydının tanımlayıcısı olarak kullanılacak alan. Taraf numarası, tanımlama türü kimliği ve kimlik numarası birleşimi. |
| **Düzenleme tarihi**<br>mshr_issuedate<br>*Date* | Okuma/yazma<br>İsteğe bağlı | Kimlik numarasının verildiği tarih. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]