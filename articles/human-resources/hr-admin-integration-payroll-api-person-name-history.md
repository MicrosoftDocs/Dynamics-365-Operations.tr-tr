---
title: Kişi adı geçmişi
description: Bu konuda, Dynamics 365 Human Resources uygulamasındaki Kişi ad geçmişi varlığıyla ilgili ayrıntılı bilgiler ve örnek bir sorgu sağlanmaktadır.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db22a602c782cef15b6e5769b9c0726dff158160
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533612"
---
# <a name="person-name-history"></a>Kişi adı geçmişi


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources uygulamasındaki Kişi ad geçmişi varlığı açıklanmaktadır.

Fiziksel ad: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Tanım

Bu varlık, belirli bir kişi için ad geçmişi hakkında bilgi sağlar.

> [!IMPORTANT] 
> **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** ve **NameValidTo** alanları artık Bordrolu personel varlığında kullanılamayacak. Bu alanlar, yalnızca bir adet geçerlilik tarihi veri kaynağının bu varlığı desteklediğinden emin olmak için kaldırılmıştır.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Tür_** | Kullan | Tanım |
| --- | --- | --- |
| **Ad**</br>mshr_firstname</br>*Dize* | Salt okunur | Ad. |
| **Soyadı öneki**</br>mshr_lastnameprefix</br>*Dize*) | Salt okunur | Soyadı öneki. |
| **Soyadı**</br>mshr_lastname</br>*Dize*) | Salt okunur | Soyadı. |
| **İkinci ad**</br>mshr_middlename</br>*Dize*) | Salt okunur | İkinci ad. |
| **Geçerlilik bitişi**</br>mshr_validto</br>*Dize*) | Salt okunur | Adın geçerlilik bitiş tarihi. |
| **Parti numarası**</br>mshr_partynumber</br>*Dize* | Salt okunur | Kişi için sistem tarafından oluşturulan, kullanıcı tarafından okunabilir benzersiz tanımlayıcı. |
| **Birincil alan**</br>mshr_primaryfield</br>*Dize* | Salt okunur | Kaydın benzersiz tanımlayıcısı. |
| **Kişi ad geçmişi varlık kimliği**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Sistem tarafından oluşturulan | Kaydı benzersiz bir şekilde tanımlamak için sistem tarafından oluşturulan genel benzersiz tanımlayıcı (GUID) değeri. |

## <a name="relations"></a>İlişkiler

| Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| Geçerli değil | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Geçerli değil | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Bordrolu personel için örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Yanıt**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
