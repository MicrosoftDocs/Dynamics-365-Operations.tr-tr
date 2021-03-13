---
title: İşe alınacak aday
description: Bu konu, Dynamics 365 Human Resources için İşe alınacak aday varlığını açıklar.
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
ms.openlocfilehash: eb16f9f46e3f5c58854ec06c3b89ec72dd7bae00
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125749"
---
# <a name="candidate-to-hire"></a>İşe alınacak aday

Bu konu, Dynamics 365 Human Resources için İşe alınacak aday varlığını açıklar.

Fiziksel ad: mshr_hcmcandidatetohireentity

## <a name="description"></a>Tanım

Bu varlık, Dynamics 365 Human Resources'da bir çalışan oluşturmak için kullanılan aday ayrıntılarını sağlar. Tüm aday kayıtlarını okumak ve yeni aday için kişisel bilgiler oluşturmanıza olanak sağlayan iç ve dış aday kayıtları oluşturmak için kullanılır.

Sistemde yeni bir kişi kaydı olacak bir dış aday kaydı oluşturduğunuzda, yeni bir aday kaydı nakledeceğiniz bir taraf (kişi) numarası tanımlamamalısınız. Yeni kişi varlık kaydı, yeni aday kaydıyla oluşturulur.

Bir dahili aday kaydı (şirkette zaten çalışan kaydı olan, pozisyon için bir aday) oluşturduğunuzda, yeni bir kişi kaydı oluşturmak için kullanılacak kişisel bilgileri (ad, cinsiyet veya doğum tarihi gibi) tanımlamak yerine, aday kaydındaki mshr_partynumber özelliği için kişide zaten var olan kaydın taraf (kişi) numarasını tanımlayın.

## <a name="json-representation"></a>JSON gösterimi

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **İşe Alınacak Aday Varlık Kimliği**<br>mshr_hcmcandidatetohireentityid<br>GUID | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Aday Kodu**<br>mshr_candidateid<br>Dize | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Ürün varlığının benzersiz tanımlayıcısı. |
| **Taraf Numarası**<br>mshr_partynumber<br>Dize | Salt okunur<br>Gerekli | Adayın kişi kaydının taraf (kişi) numarası. |
| **Kişi Kimliği Değeri**<br>_mshr_fk_person_id_value<br>GUID | Salt okunur<br>Gerekli<br>Yabancı anahtar: mshr_direpersonentity varlığına ait mshr_dirpersonentityid | Adayın taraf (kişi) kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Türü**<br>mshr_partytype<br>mshr_dirpartytype seçenek kümesi | Salt okunur<br>Gerekli | mshr_dirpartytype seçenek kümesinde tanımlandığı gibi kaydın taraf türü. Bu varlık için tür her zaman "Kişi" olacaktır. |
| **İşe Alma İsteği Kimliği**<br>mshr_recruitingrequestid<br>Dize | Bir kez yaz<br>İsteğe bağlı | Bu adayın yerine getirdiği İşe Alım İsteği referansları. |
| **İşe Alma İsteği Kimlik Değeri**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Okuma/yazma<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmrecruitingrequestentity içindeki mshr_hcmrecruitingrequestentityid | Adayın yerine getirdiği işe alım isteğinin sistem tarafından oluşturulan benzersiz tanımlayıcısı. |
| **Pozisyon kodu**<br>mshr_positionid<br>Dize | Okuma/yazma<br>İsteğe bağlı | Adayın değerlendirilmekte olduğu pozisyonun kimliği. |
| **Pozisyon Kimlik Değeri**<br>_mshr_fk_position_if_value<br>GUID | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmpositionv2entity varlığına ait mshr_hcmpositionv2entityid | Adayın pozisyonunun sistem tarafından oluşturulan tanımlayıcısı dikkate alınmaktadır. |
| **Ad**<br>mshr_firstname<br>Dize | Okuma/yazma<br>Gerekli | Adayın adı. |
| **İkinci Ad**<br>mshr_middlename<br>Dize | Okuma/yazma<br>İsteğe bağlı | Adayın ikinci adı. |
| **Soyadı Öneki**<br>mshr_lastnameprefix<br>Dize | Okuma/yazma<br>İsteğe bağlı | Adayın soyadı öneki. |
| **Soyadı**<br>mshr_lastname<br>Dize | Okuma/yazma<br>İsteğe bağlı | Adayın soyadı. |
| **Cinsiyet**<br>mshr_gender<br>mshr_hcmpersongender seçenek kümesi | Okuma/yazma<br>İsteğe bağlı | Adayın cinsiyeti. |
| **Doğum Tarihi**<br>mshr_birthdate<br>Datetime | Okuma/yazma<br>İsteğe bağlı | Adayın doğum tarihi. |
| **Vatandaşlık Ülke Kodu**<br>mshr_citizenshipcountrycode<br>Dize | Okuma/yazma<br>İsteğe bağlı | Adayın vatandaşı olduğu ülke/bölgeyi belirtir. Geçerli ülke/bölge kodları mshr_logisticaddresscountryregionentity varlığında bulunur. |
| **Gazilik Durumu Kimliği**<br>mshr_veteranstatusid<br>Dize | Okuma/yazma<br>İsteğe bağlı | Adayın geçerli gazilik durumunu belirtir. |
| **Gazilik Durumu Kimlik Değeri**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmveteranstatusentity varlığına ait mshr_hcmveteranstatusentityid | Gazilik durumu varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Askerlik hizmeti başlangıç tarihi**<br>mshr_militaryservicestartdate<br>Datetime | Okuma/yazma<br>İsteğe bağlı | Adayın askerlik görevine başlama tarihi. |
| **Askerlik hizmeti bitiş tarihi**<br>mshr_militaryserviceenddate<br>Datetime | Okuma/yazma<br>İsteğe bağlı | Adayın askerlik görevinin bitiş tarihi. |
| **Engelli Gazi**<br>mshr_isdisabledveteran<br>mshr_noyes seçenek kümesi | Okuma/yazma<br>İsteğe bağlı | Adayın gazilik durumunu devre dışı bırakıp bırakmadığını gösterir. |
| **Müsaitlik Tarihi**<br>mshr_availabilitydate<br>Datetime | Okuma/yazma<br>İsteğe bağlı | Adayın çalışmaya başlayabileceği en erken tarih. |
| **Yer Değiştirmeye İstekli**<br>mshr_iswillingtorelocate<br>mshr_noyes seçenek kümesi | Okuma/yazma<br>İsteğe bağlı | Adayın pozisyon için yer değiştirmek isteyip istemediğini belirtir. |
| **Yorumlar**<br>mshr_comments<br>Dize | Okuma/yazma<br>İsteğe bağlı | İşe alan veya işe alım yöneticisi tarafından kullanılacak yorumlar. |
| **Başvuru Tümleştirme Sonucu**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult seçenek kümesi | Okuma/yazma<br>Gerekli | Tümleştirme ile ilgili işe alım sürecinde adayın durumu. |
| **İşe Almama Neden Kodu Kimliği**<br>mshr_donothirereasoncodeid<br>Dize | Okuma/yazma<br>İsteğe bağlı | Durum (başvuru tümleştirme sonucu) "İşe alınmadı" olarak ayarlandığında isteğe bağlı olarak sağlanan bir neden kodu. |
| **Neden Kodu Kimliği Değeri**<br>_mshr_fk_reasoncode_id_value<br>GUID | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: mshr_hcmreasoncodeentity varlığına ait mshr_hcmreasoncodeentityid | **İşe Almama** neden kodu için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Veri Alanı Kimliği**<br>mshr_dataareaid<br>Dize | Okuma/yazma<br>İsteğe bağlı |  Tüzel kişiliği (şirket) belirtir. |
| **Veri Alanı Kimliği Değeri**<br>_mshr_dataareaid_id_value<br>GUID | Salt okunur<br>İsteğe bağlı<br>Yabancı anahtar: cdm_company varlığına ait cdm_companyid | Tüzel kişiliği (şirket) tanımlaması için sistem tarafından oluşturulan GUID değeri. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
