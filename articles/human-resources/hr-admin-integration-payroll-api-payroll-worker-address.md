---
title: Bordrolu çalışanın adresi
description: Bu makalede, Dynamics 365 Human Resources'daki Bordrolu çalışanın adresi varlığıyla ilgili ayrıntılı bilgiler ve örnek bir sorgu sağlanmaktadır.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 683994b24113b8c2017f1bb3c1055e7e0f0eb75e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901132"
---
# <a name="payroll-worker-address"></a>Bordrolu çalışanın adresi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Bordrolu çalışanın adresi varlığı açıklanmaktadır.

Fiziksel ad: mshr_payrollworkeraddressentity.

### <a name="description"></a>Tanım

Bu varlık, belirli bir çalışan için bordro yerleşimi konumunu ve bordro çalışma konumunu sağlar.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Tür_** | Kullan | Tanım |
| --- | --- | --- |
| **Personel numarası**</br>mshr_personnelnumber</br>*Dize* | Salt okunur | Çalışanın benzersiz personel numarası. |
| **Yerleşim kodu**</br>mshr_locationidbr>*String* | Salt okunur | Adres kimliği. |
| **Yaşadığı adres**</br>mshr_islivedinaddressbr </br> *[mshr_NoYes seçenek kümesi](hr-admin-integration-payroll-api-no-yes.md)* | Salt okunur | Adresin, personelin yaşadığı yer olup olmadığını gösteren bir değer. |
| **Çalıştığı adres** </br> mshr_isworkedinaddressbr </br>*[mshr_NoYes seçenek kümesi](hr-admin-integration-payroll-api-no-yes.md)* | Salt okunur | Adresin, personelin çalıştığı yer olup olmadığını gösteren bir değer. |
| **Ülke bölge**</br>mshr_countryregionid</br>*Dize* | Salt okunur</br>Gerekli | Adres için tanımlanan ülke veya bölge. |
| **Posta kodu**</br>mshr_zipcode<br>*Dize* | Salt okunur | Personel için tanımlanan kimlik numarası. |
| **Cadde**</br>mshr_street</br>*Dize* | Salt okunur | Adres için tanımlanan cadde. |
| **Şehir**</br>mshr_city</br>*Dize* | Salt okunur | Adres için tanımlanan şehir. |
| **İl**</br>mshr_state</br>*Dize* | Salt okunur | Adres için tanımlanan eyalet veya il. |
| **İlçe**</br>mshr_county</br>*Dize* | Salt okunur | Adres için tanımlanan ülke/bölge. |
| **Geçerlilik başlangıcı**</br>mshr_postaladdressvalidfrom</br>*Tarih Saat Sapması* | Salt okunur | Adresin geçerlilik başlangıç tarihi. |
| **Geçerlilik bitişi**</br>mshr_postaladdressvalidto</br>*Tarih Saat Sapması* | Salt okunur | Adresin geçerlilik bitiş tarihi. |
| **Birincil alan**</br>mshr_primaryfield</br>*Dize* | Salt okunur | Birincil alan. |
| **Bordrolu çalışan adresi kimliği**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Sistem tarafından oluşturulan | Adresi benzersiz bir şekilde tanımlamak için sistem tarafından oluşturulan genel benzersiz tanımlayıcı (GUID) değeri. |

## <a name="relations"></a>İlişkiler

| Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Yanıt**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
