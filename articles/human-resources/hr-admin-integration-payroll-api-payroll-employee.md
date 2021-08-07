---
title: Bordrolu personel
description: Bu konu, Dynamics 365 Human Resources'taki Bordrolu personelle ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
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
ms.openlocfilehash: 672db002ddf8d12aaab5b97241390c036ad7ab5c
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538866"
---
# <a name="payroll-employee"></a>Bordrolu personel

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Bordro personel varlığını açıklar.

Fiziksel ad: mshr_payrollemployeeentity.

### <a name="description"></a>Tanım

Bu varlık çalışan hakkında bilgi sağlar. Bu varlığı kullanmadan önce [Bordro tümleştirme parametrelerini](hr-admin-integration-payroll-api-parameters.md) ayarlamanız gerekir.

>[!IMPORTANT] 
>**FirstName**, **MiddleName**, **LastName**, **NameValidFrom** ve **NameValidTo** alanları artık bu varlıkta kullanılamayacak. Bu durum, **EmploymentStartDate** ve **EmploymentEndDate** alanlarıyla **HcmEmployment** olan bu varlığı destekleyen tek bir geçerlilik tarihli veri kaynağı olduğundan emin olmaya yöneliktir.

>Bu alanlar, Platform Güncelleştirmesi 43'te yayınlanan **DirPersonNameHistoricalEntity**'de kullanılabilir. **Kişi** alanında **PayrollEmployeeEntity** ile **DirPersonNameHistoricalEntity** arasında bir OData ilişkisi vardır. Alternatif olarak, **DirPersonNameHistoricalEntity** varlığı, **PersonHistoricalNames** ortak adı kullanılarak doğrudan OData aracılığıyla sorgulanabilir.


## <a name="properties"></a>Özellikler

| Özellik<br>**Fiziksel ad**<br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Personel numarası**<br>mshr_personnelnumber<br>*Dize* | Salt okunur<br>Gerekli | Çalışanın benzersiz personel numarası. |
| **Birincil alan**<br>mshr_primaryfield<br>*Dize* | Gerekli<br>Sistem tarafından oluşturulan |  |
| **Tüzel kişilik kodu**<br>mshr_legalentityID<br>*Dize* | Salt okunur<br>Gerekli | Tüzel kişiliği (şirket) belirtir. |
| **Cinsiyet**<br>mshr_gender<br>[mshr_hcmpersongender seçenek kümesi](hr-admin-integration-payroll-api-gender.md) | Salt okunur<br>Gerekli | Çalışanın cinsiyeti. |
| **Bordrolu personel varlık kodu**<br>mshr_payrollemployeeentityid<br>*GUID* | Gerekli<br>Sistem tarafından oluşturulan | Personeli benzersiz olarak tanımlamak için sistem tarafından oluşturulan GUID değeri. |
| **İstihdam başlama tarihi**<br>mshr_employmentstartdate<br>*Tarih saat sapması* | Salt okunur<br>Gerekli | Çalışanın işe başlama tarihi. |
| **Tanımlama türü kimliği**<br>mshr_identificationtypeid<br>*Dize* |Salt okunur<br>Gerekli | Çalışan için tanımlanan tanımlama türü. |
| **İş bitiş tarihi**<br>mshr_employmentenddate<br>*Tarih saat sapması* | Salt okunur<br>Gerekli |Çalışanın istihdam bitiş tarihi.  |
| **Veri alanı kimliği**<br>mshr_dataareaid_id<br>*GUID* | Gerekli <br>Sistem tarafından oluşturulan | Tüzel kişiliği (şirket) tanımlaması için sistem tarafından oluşturulan GUID değeri. |
| **Geçerlilik bitişi**<br>mshr_namevalidto<br>*Tarih Saat Sapması* |  Salt okunur<br>Gerekli | Personel bilgilerinin geçerlilik bitiş tarihi. |
| **Doğum tarihi**<br>mshr_birthdate<br>*Tarih Saat Sapması* | Salt okunur <br>Gerekli | Çalışanın doğum tarihi |
| **Kimlik numarası**<br>mshr_identificationnumber<br>*Dize* | Salt okunur <br>Gerekli |Çalışan için tanımlanan tanımlama numarası.  |

## <a name="example-query-for-payroll-employee"></a>Bordrolu personel için örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Yanıt**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
