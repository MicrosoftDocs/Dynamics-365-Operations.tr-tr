---
title: Bordrolu personel
description: Bu konu, Dynamics 365 Human Resources'taki Bordrolu personelle ilgili ayrıntılı bilgi ve örnek bir sorgu sağlar.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 7f43476cd044a9cc2e11412aac4af1cff2f9e511
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559545"
---
# <a name="payroll-employee"></a>Bordrolu personel

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konu, Dynamics 365 Human Resources için Bordro personel varlığını açıklar.

Fiziksel ad: mshr_payrollemployeeentity.

### <a name="description"></a>Tanım

Bu varlık çalışan hakkında bilgi sağlar. Bu varlığı kullanmadan önce [Bordro tümleştirme parametrelerini](hr-admin-integration-payroll-api-parameters.md) ayarlamanız gerekir.

>[!IMPORTANT] 
>**FirstName**, **MiddleName**, **LastName**, **NameValidFrom** ve **NameValidTo** alanları artık bu varlıkta kullanılamayacak. Bu, bu varlığı yedekleyen yalnızca bir yürürlük tarihli veri kaynağı olmasını sağlar.
>Bu alanlar, Platform Güncelleştirmesi 43'te yayınlanan **DirPersonNameHistoricalEntity**'de kullanılabilir. Burada, **PayrollEmployeeEntity** ile **DirPersonNameHistoricalEntity** arasında bir OData ilişkisi vardır. 

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Tüzel kişilik kodu**</br>mshr_legalentityid</br>*Dize* | Salt okunur | Tüzel kişiliği (şirket) belirtir. |
| **Personel numarası**</br>mshr_personnelnumber</br>*Dize* | Salt okunur | Çalışanın benzersiz personel numarası. |
| **İstihdam başlangıç tarihi**</br>mshr_employmentstartdate</br>*Tarih saat sapması* | Salt okunur | Çalışanın işe başlama tarihi. |
| **İş bitiş tarihi**</br>mshr_employmentenddate</br>*Tarih saat sapması* | Salt okunur |Çalışanın istihdam bitiş tarihi.  |
| **Doğum tarihi**</br>mshr_birthdate</br>*Tarih Saat Sapması* | Salt okunur | Çalışanın doğum tarihi. |
| **Cinsiyet**</br>mshr_gender</br>[mshr_hcmpersongender seçenek kümesi](hr-admin-integration-payroll-api-gender.md) | Salt okunur | Çalışanın cinsiyeti. |
| **İstihdam türü**</br>mshr_employmenttype</br>[mshr_hcmemploymenttype seçenek kümesi](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Salt okunur | İstihdam türü. |
| **Tanımlama türü kimliği**</br>mshr_identificationtypeid</br>*Dize* |Salt okunur | Çalışan için tanımlanan tanımlama türü. |
| **Kimlik numarası**</br>mshr_identificationnumber</br>*Dize* | Salt okunur |Çalışan için tanımlanan tanımlama numarası. |
| **Ödemeye hazır**</br>mshr_readytopay</br>[mshr_noyes seçenek kümesi](hr-admin-integration-payroll-api-no-yes.md) | Salt okunur | Çalışanın ödeme için hazır olarak işaretlenip işaretlenmediğini gösterir. |
| **Bordrolu personel varlık kodu**</br>mshr_payrollemployeeentityid</br>*GUID* | Sistem tarafından oluşturulan | Personeli benzersiz bir şekilde tanımlamak için sistem tarafından oluşturulan genel benzersiz tanımlayıcı (GUID) değeri. |

## <a name="relations"></a>İlişkiler

|Özellik değeri | İlgili varlık | Gezinti özelliği | Tahsilat türü |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Bordrolu personel için örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
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
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
