---
title: Bordrolu çalışanın adresi
description: Bu konu, Dynamics 365 Human Resources'taki Bordrolu çalışan adresi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882094"
---
# <a name="payroll-worker-address"></a>Bordrolu çalışanın adresi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources'taki Bordrolu çalışan adresi varlığıyla ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.

## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Şehir**<br>mshr_city<br>*Dize* | Salt okunur<br>Gerekli | Adres için tanımlanan şehir.   |
| **Personel numarası**<br>mshr_personnelnumber<br>*Dize* | Salt okunur<br>Gerekli | Çalışanın benzersiz personel numarası.  |
| **Ülke bölge**<br>mshr_countryregionid<br>*Dize* | Salt okunur<br>Gerekli | Adresin için tanımlanan ülke bölge  |
| **Geçerlilik başlangıcı**<br>mshr_postaladdressvalidfrom<br>*Tarih Saat Sapması* | Salt okunur <br>Gerekli | Adresin geçerlilik başlangıç tarihi. |
| **Çalıştığı adres**<br>mshr_isworkedinaddressbr>*Int32* | Salt okunur<br>Gerekli | Adresin çalışanın çalıştığı yer olup olmadığını gösterir. |
| **İlçe**<br>mshr_county<br>*Dize* | Salt okunur<br>Gerekli | Adres için tanımlanan ilçe.  |
| **Bordrolu çalışan adresi kimliği**<br>mshr_payrollworkeraddressentityid<br>*GUID* | Gerekli<br>Sistem tarafından oluşturulan | Adresi benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri.  |
| **Birincil alan**<br>mshr_primaryfield<br>*Dize* | Salt okunur<br>Gerekli |  |
| **Sokak**<br>mshr_street<br>*Dize* | Salt okunur<br>Gerekli | Adres için tanımlanan cadde. |
| **Geçerlilik bitişi**<br>mshr_postaladdressvalidto<br>*Tarih Saat Sapması* | Salt okunur <br>Gerekli | Adresin geçerlilik bitiş tarihi.  |
| **Yerleşim kodu**<br>mshr_locationidbr>*String* | Salt okunur <br>Gerekli | Adres kimliği.  |
| **Posta kodu**<br>mshr_zipcode<br>*Dize* | Salt okunur <br>Gerekli |Çalışan için tanımlanan tanımlama numarası.  |
| **Yaşadığı adres**<br>mshr_islivedinaddressbr>*String* | Salt okunur<br>Gerekli | Adresin çalışanın yaşadığı yer olup olmadığını gösterir. |
| **İl**<br>mshr_state<br>*Dize* | Salt okunur<br>Gerekli | Adres için tanımlanan il.  |

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
