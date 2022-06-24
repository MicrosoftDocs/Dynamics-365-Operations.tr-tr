---
title: Bordro çalışan kazanç planı
description: Bu makalede, Dynamics 365 Human Resources'daki Bordrolu çalışan kazanç planı varlığıyla ilgili ayrıntılı bilgiler ve örnek bir sorgu sağlanmaktadır.
author: twheeloc
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef45855d9e60131ac065ae6e2769b71ae3f69537
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902299"
---
# <a name="payroll-worker-benefit-plan"></a>Bordro çalışan kazanç planı


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Dynamics 365 Human Resources için Bordrolu çalışan kazanç planı varlığı açıklanmaktadır.

Fiziksel ad: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>Tanım

Bu varlıkta, belirli bir çalışan için kazanç planı hakkında bilgiler sağlanmaktadır.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Türü_** | Kullan | Tanım |
| --- | --- | --- |
| **Personel numarası**</br>mshr_personnelnumber</br>*Dize* | Salt okunur</br>Gerekli | Çalışanın benzersiz personel numarası. |
| **Tüzel kişilik kodu**</br>mshr_legalentityID</br>*Dize* | Salt okunur | Tüzel kişiliği (şirket) belirtir. |
| **Dönem Kodu**</br>mshr_periodid</br>*Dize* | Salt okunur | Dönemin tanımlayıcısı. |
| **Plan Kodu**</br>mshr_planid</br>*Dize* | Salt okunur | Planın tanımlayıcısı. |
| **Karşılama seçeneği**</br>mshr_coverageoptionid</br>*Dize* | Salt okunur | Karşılama seçeneğinin kimliği. |
| **Kesinti başlangıç tarihi**</br>mshr_deductionstartdatetime</br>*Tarih saat sapması* | Salt okunur | Kesinti başlangıç tarihi. |
| **Kesinti bitiş tarihi**</br>mshr_deductionenddatetime</br>*Tarih saat sapması* | Salt okunur | Kesinti bitiş tarihi. |
| **Durum**</br>mshr_status</br>*[Kazanç çalışan planı durumu seçenek kümesi](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Salt okunur | Kazanç planının durumu. |
| **Geçerlilik başlangıcı**</br>mshr_validfrom</br>*Tarih Saat Sapması* | Salt okunur | Bu kaydın geçerli hale geldiği saat. |
| **Geçerlilik bitişi**</br>mshr_validto</br>*Tarih Saat Sapması* |  Salt okunur | Bu kaydın geçerliliğinin sona erdiği saat. |
| **Plan türü kimliği**</br>mshr_plantypeid</br>*Dize* | Salt okunur | Plan türünün tanımlayıcısı. |
| **Plan türü kodu**</br>mshr_plantypecode</br>*[kazanç planı türü kapsamı seçenek kümesi](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Salt okunur | Plan türünün belirtimi. |
| **Ödeme dönemi sayısı**</br>mshr_payperiod</br>*Tamsayı* | Salt okunur | Kazanç sağlayıcısının veya çalışanların ne kadar sıklıkla ödendiğini gösteren ödeme dönemlerinin sayısı. Bu tutar, çalışanın yıllık kazancının maaş tutarını hesaplamak için kullanılır. |
| **Personel tutarı**</br>mshr_amountemployee</br>*Ondalık* | Salt okunur | Çalışan tutarı veya yüzdesi. |
| **İşveren tutarı**</br>mshr_amountemployer</br>*Ondalık* | Salt okunur | İşveren tutarı veya yüzdesi. |
| **Birincil alan**</br>mshr_primaryfield</br>*Dize* | Sistem tarafından oluşturulan | Birincil alan. |
| **Çalışan kimlik değeri** </br>_mshr_fk_worker_id_value</br>*GUID* | Yabancı anahtar: mshr_hcmworkerbaseentity varlığı için mshr_hcmworkerbaseentityid. | Çalışan için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Dönem kimliği değeri**</br> _mshr_fk_period_id_value</br>*GUID* | Yabancı anahtar: mshr_benefitperiodentity varlığı için mshr_benefitperiodentityid. | Dönem için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Plan kimliği değeri**</br> _mshr_fk_plan_id_value</br>*GUID* | Yabancı anahtar: mshr_benefitplanentity varlığı için mshr_benefitplanentityid. | Plan için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Plan Türü Kimliği değeri**</br> _mshr_fk_plantype_id_value</br>*GUID* | Yabancı anahtar: mshr_benefitplantypeentity varlığı için mshr_benefitplantypeentityid. | Plan için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Kapsam seçeneği kimliği değeri**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Yabancı anahtar: mshr_benefitcoverageoptionentity varlığı için mshr_benefitcoverageoptionentityid. | Plan için sistem tarafından oluşturulan benzersiz tanımlayıcı. |
| **Bordro çalışan kazanç planı varlık kimliği değeri**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Salt okunur </br> Sistem tarafından oluşturulan | Kayıt için sistem tarafından oluşturulan benzersiz tanımlayıcı. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Bordro çalışan kazanç planı için örnek sorgu

**İstek**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Yanıt**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
