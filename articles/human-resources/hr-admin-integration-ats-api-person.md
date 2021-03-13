---
title: Kişi
description: Bu konu, Dynamics 365 Human Resources için Kişi varlığını açıklar.
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
ms.openlocfilehash: e61b768c5194b52178853d48c50dbf072eebbdcd
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125461"
---
# <a name="person"></a>Kişi

Bu konu, Dynamics 365 Human Resources için Kişi varlığını açıklar.

Fiziksel ad: mshr_dirpersonentity

### <a name="description"></a>Tanım

Bu varlık, aday olan kişi için kişisel bilgileri sağlar.

## <a name="json-representation"></a>JSON gösterimi

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Kişi Varlığı Kimliği**<br>mshr_dirpersonentityid<br>*GUID* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Varlık kaydı için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Taraf Numarası**<br>mshr_partynumber<br>*Dize* | Salt okunur<br>Gerekli<br>Sistem tarafından oluşturulan | Kişi için sistem tarafından oluşturulan, kullanıcı tarafından okunabilir benzersiz tanımlayıcı.  |
| **Kuruluş adı**<br>mshr_name<br>*Dize* | Salt okunur<br>Gerekli | Alan değeri, **Ad Sırasını Farklı Görüntüle** alanında tanımlanan sırayla Ad, İkinci Ad, Soyadı Öneki ve Soyadı'nın birleştirilmesidir. |
| **Ad Diğer Adı**<br>mshr_namealias<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişi için sağlanan bir ad diğer adı. |
| **Bilinen Hali**<br>mshr_knownas<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Genellikle başka bir ad olarak biliniyorsa, kişi için kullanılabilecek ad. |
| **Dil kodu**<br>mshr_languageid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | ISO 639-1 formatında tanımlandığı şekilde, kişinin birincil dilinin dil kodu. |
| **Adres defterleri**<br>mshr_addressbooks<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin atanabileceği adres defteri. Kuruluş için ayarlanan adres defterleri mshr_diraddressbooksentity varlığında listelenir. |
| **Yıldönümü Günü**<br>mshr_anniversaryday<br>*Int* | Okuma/yazma<br>İsteğe bağlı | Kişinin yıldönümü tarihinin günü. |
| **Yıldönümü Ayı**<br>mshr_anniversarymonth<br>*mshr_monthsofyear seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin yıldönümü tarihinin ayı. |
| **Yıldönümü Yılı**<br>mshr_anniversaryyear<br>*Int* | Okuma/yazma<br>İsteğe bağlı | Kişinin yıldönümü tarihinin yılı. |
| **Doğum Günü**<br>mshr_birthday<br>*Int* | Okuma/yazma<br>İsteğe bağlı | Kişinin doğum tarihinin günü. |
| **Doğum Ayı**<br>mshr_birthmonth<br>*mshr_monthsofyear seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin doğum tarihinin ayı. |
| **Doğum Yılı**<br>mshr_birthyear<br>*Int* | Okuma/yazma<br>İsteğe bağlı | Kişinin doğum tarihinin yılı. |
| **Çocuklarının Adları**<br>mshr_childrennames<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin çocuklarının adları için dize. Gerekli ayırma yoktur. |
| **Cinsiyet**<br>mshr_gender<br>*mshr_hcmpersongender seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin cinsiyeti. |
| **Hobiler**<br>mshr_hobbies<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin hobileri. |
| **Baş harfler**<br>mshr_initials<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin adının baş harfleri. |
| **Medeni Durum**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin medeni durumu. |
| **Fonetik Ad**<br>mshr_phoneticfirstname<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin adının fonetik söylenişi. |
| **Fonetik Soyadı**<br>mshr_phoneticlastname<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin soyadının fonetik söylenişi. |
| **Fonetik İkinci Ad**<br>mshr_phoneticmiddlename<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin soyadının fonetik söylenişi. |
| **Kişisel Sonek**<br>mshr_personalsuffix<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin kişisel son eki. mshr_type değerinin Sonek (200000001) olduğu mshr_dirnameaffixentity varlığındaki geçerli değerler. |
| **Kişisel Unvan**<br>mshr_personaltitle<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin kişisel unvanı. mshr_type değerinin Unvan (200000000) olduğu mshr_dirnameaffixentity varlığındaki geçerli değerler.
| **Profesyonel Sonek**<br>mshr_professionalsuffix<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Profesyonel sonek. |
| **Profesyonel Unvan**<br>mshr_professionaltitle<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Profesyonel unvan. |
| **Birincil Tam Adres**<br>mshr_fullprimaryaddress<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil adres alanlarının birleşimi olan kişinin tam birincil adresi. |
| **Adres Şehir**<br>mshr_addresscity<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin şehri. mshr_logisticsaddresscityentity varlığında ayarlanır. |
| **Adres Ülke Bölge**<br>mshr_addresscountryregionid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin ülke/bölgesi. Geçerli değerler mshr_logisticsaddresscountryregionentity varlığında bulunur. |
| **Adres Ülke Bölge ISO Kodu**<br>mshr_addresscountryregionisocode<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin ülke/bölge ISO kodu. |
| **Adres İlçe**<br>mshr_addresscounty<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin ilçesi. mshr_logisticsaddresscountyentity varlığında ayarlanır. |
| **Adres Mahalle Adı**<br>mshr_addressdistrictname<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin mahallesi. mshr_logisticsaddressdistrictentity varlığında ayarlanır. |
| **Adres Enlemi**<br>mshr_addresslatitude<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin enlemi. |
| **Adres Konum Kimliği**<br>mshr_addresslocationid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin konumuyla ilgili benzersiz tanımlayıcı. Geçerli değerler mshr_logisticspostaladdresslocationcdsentity varlığında bulunur. |
| **Adres Konumu Rolleri**<br>mshr_addresslocationroles<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin konum rolü. mshr_logisticslocationrolecdsentity varlığında ayarlanır. |
| **Adres Boylamı**<br>mshr_addresslongitude<br>*Dize* |  Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin boylamı. |
| **Adres Eyaleti**<br>mshr_addressstate<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin eyaleti. mshr_logisticsaddressstateentity varlığında ayarlanır. |
| **Adres sokak**<br>mshr_addressstreet<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin açık adresi. |
| **Adresin Geçerlilik Başlangıç Tarihi**<br>mshr_addressvalidfrom<br>*Date* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin geçerlilik başlangıç tarihi. |
| **Adresin Geçerlilik Bitiş Tarihi**<br>mshr_addressvalidto<br>*Date* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin geçerlilik bitiş tarihi. |
| **Adres Posta Kodu**<br>mshr_addresszipcode<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin posta kodu. mshr_logisticsaddresspostalcodeentity varlığında ayarlanır. |
| **Adres Özel**<br>mshr_addressisprivate<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin kuruluştaki diğer kişilerle paylaşılıp paylaşılmayacağını belirler. |
| **Adres Açıklaması**<br>mshr_addressdescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin açıklaması. |
| **Birincil İletişim E-postası**<br>mshr_primarycontactemail<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil e-posta adresi. |
| **Birincil İletişim E-postası Açıklaması**<br>mshr_primarycontactemaildescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil e-posta adresi için sağlanan açıklama. |
| **Birincil İletişim E-postası IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Birincil e-posta adresinin anlık iletilerde kullanılabilir olup olmadığını belirler. |
| **Birincil İletişim E-postası Amacı**<br>mshr_primarycontactemailpurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil e-posta adresinin amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Birincil İletişim Faks Numarası**<br>mshr_primarycontactfax<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil faks numarası. |
| **Birincil İletişim Faks Numarası Açıklaması**<br>mshr_primarycontactfaxdescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil faks numarası için sağlanan açıklama. |
| **Birincil İletişim Faks Dahili Numarası**<br>mshr_primarycontactfaxextension<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil faks dahili numarası. |
| **Birincil İletişim Faks Numarası Amacı**<br>mshr_primarycontactfaxpurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil faks numarasının amacı. mshr_logisticslocationroleentity varlığında ayarlanır.
| **Birincil İletişim Telefon Numarası**<br>mshr_primarycontactphone<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil telefon numarası. |
| **Birincil İletişim Telefon Numarası Açıklaması**<br>mshr_primarycontactphonedescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil telefon numarası için sağlanan açıklama. |
| **Birincil İletişim Telefon Dahili Numarası**<br>mshr_primarycontactphoneextension<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil dahili telefon numarası. |
| **Birincil İletişim Telefon Numarası Cep Telefonu**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Birincil telefon numarasının cep telefonu olup olmadığını belirler. |
| **Birincil İletişim Telefon Numarası Amacı**<br>mshr_primarycontactphonepurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil telefon numarasının amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Birincil İletişim Teleks**<br>mshr_primarycontacttelex<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil teleks numarası. |
| **Birincil İletişim Teleks Numarası Açıklaması**<br>mshr_primarycontacttelexdescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil teleks numarası için sağlanan açıklama. |
| **Birincil İletişim Teleks Numarası Amacı**<br>mshr_primarycontacttelexpurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil teleks numarasının amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Birincil İletişim URL'si**<br>mshr_primarycontacturl<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil URL. |
| **Birincil İletişim URL Açıklaması**<br>mshr_primarycontacturldescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil URL'si için sağlanan açıklama. |
| **Birincil İletişim URL'si Amacı**<br>mshr_primarycontacturldescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil URL'sinin amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Birincil İletişim Facebook Hesabı**<br>mshr_primarycontactfacebook<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil Facebook hesabı. Kullanıcı Kimliği ile tanımlanır. |
| **Birincil İletişim Facebook Açıklaması**<br>mshr_primarycontactfacebookdescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil Facebook hesabı için sağlanan açıklama. |
| **Birincil İletişim Facebook Özel**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Birincil Facebook hesabın diğer kullanıcılar tarafından görülüp görülmediğini belirler. |
| **Birincil İletişim Facebook Hesabının Amacı**<br>mshr_primarycontactfacebookpurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil Facebook hesabının amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Birincil İletişim LinkedIn**<br>mshr_primarycontactlinkedin<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Birincil LinkedIn hesabı. Kullanıcı adı ile tanımlanır. |
| **Birincil İletişim LinkedIn Açıklaması**<br>mshr_primarycontactlinkedindescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil LinkedIn hesabı için sağlanan açıklama. |
| **Birincil İletişim LinkedIn Özel**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil LinkedIn hesabı bilgilerinin diğer kullanıcılarla paylaşılıp paylaşılmayacağını belirler. |
| **Birincil İletişim LinkedIn Hesabı Amacı**<br>mshr_primarycontactlinkedinpurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil LinkedIn hesabının amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Birincil İletişim Twitter Hesabı**<br>mshr_primarycontacttwitter<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil Twitter hesabı. @kullanıcı adı ile tanımlanır. |
| **Birincil İletişim Twitter Hesabı Açıklaması**<br>mshr_primarycontacttwitterdescription<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil Twitter hesabı için sağlanan açıklama. |
| **Birincil İletişim Twitter Hesabı Özel**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes seçenek kümesi* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil Twitter hesabı bilgilerinin diğer kullanıcılarla paylaşılıp paylaşılmayacağını belirler. |
| **Birincil İletişim Twitter Hesabı Amacı**<br>mshr_primarycontacttwitterpurpose<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil Twitter hesabının amacı. mshr_logisticslocationroleentity varlığında ayarlanır. |
| **Taraf Türü**<br>mshr_partytype<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin taraf türü. Adaylar için daima **Kişi**'dir. |
| **Ad Sırası Farklı Görüntüle**<br>mshr_namesequencedisplayas<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin ad özelliklerinin Ad (mshr_name) özellik değerini oluşturacak şekilde birleştiği sıra. |
| **Ad**<br>mshr_firstname<br>*Dize* | Okuma/yazma<br>Gerekli | Kişinin adı. |
| **İkinci Ad**<br>mshr_middlename<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin ikinci adı. |
| **Soyadı Öneki**<br>mshr_lastnameprefix<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin soyadı ön eki. |
| **Soyadı**<br>mshr_lastname<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin soyadı. |
| **Elektronik Konum Kodu**<br>mshr_electroniclocationid<br>*Dize* | Okuma/yazma<br>İsteğe bağlı | Kişinin elektronik konum kodu. |
| **Adres Saat Dilimi**<br>mshr_addresstimezone<br>*Int* | Okuma/yazma<br>İsteğe bağlı | Kişinin birincil adresinin saat dilimi. |

## <a name="see-also"></a>Ayrıca bkz.

[Başvuran İzleme Sistemi tümleştirme API'si tanıtımı](hr-admin-integration-ats-api-introduction.md)<br>
[İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

