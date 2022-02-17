---
title: Maaş ödeme sıklığı
description: Bu konuda, Dynamics 365 Human Resources uygulamasındaki Ücret ödeme sıklığı varlığı için ayrıntılar ve örnek bir sorgu açıklanmaktadır.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066155"
---
# <a name="compensation-pay-frequency"></a>Maaş ödeme sıklığı


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources uygulamasındaki Ücret ödeme sıklığı varlığı açıklanmaktadır.

Fiziksel ad: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Tanım

Bu varlık, belirli bir ücret ödeme sıklığı için ödeme oranı dönüşümü hakkında bilgi sağlar.

## <a name="properties"></a>Özellikler

| Özellik</br>**Fiziksel ad**</br>**_Tür_** | Kullan | Tanım |
| --- | --- | --- |
| **Yıllık ödeme oranı dönüşümü**</br>mshr_annualconversionfactor</br>*Ondalık* | Salt okunur | Ödeme sıklığında, yıllık dönüştürme faktörü. |
| **Açıklama**</br>mshr_description</br>*Dize* | Salt okunur | Dönüşüm oranının açıklaması. |
| **Saatlik ödeme oranı dönüşümü**</br>mshr_hourlyconversionfactor</br>*Ondalık* | Salt okunur | Ödeme sıklığında, saatlik dönüştürme faktörü. |
| **Aylık ödeme oranı dönüşümü**</br>mshr_monthlyconversionfactor</br>*Ondalık* | Salt okunur | Ödeme sıklığında, aylık dönüştürme faktörü. |
| **Ödeme oranı dönüştürme**</br>mshr_payrateconversion</br>*Dize* | Salt okunur | Dönüştürme oranını tanımlayan benzersiz bir dize. |
| **Dönem**</br>mshr_period</br>*dönem seçenek kümesi* | Salt okunur | Verilen ödeme oranı dönüşümü için ana dönem. |
| **Haftalık ödeme oranı dönüşümü**</br>mshr_weeklyconversionfactor</br>*Ondalık* | Salt okunur | Ödeme sıklığında, haftalık dönüştürme faktörü. |
| **Veri alanı kimliği**</br>mshr_dataareaid</br>*Dize* | Salt okunur | Tüzel kişilik (şirket). |
| **Ücret ödeme sıklığı varlık kimliği**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Sistem tarafından oluşturulan | Kaydı benzersiz bir şekilde tanımlamak için sistem tarafından oluşturulan genel benzersiz tanımlayıcı (GUID) değeri. |

## <a name="example-query-for-payroll-employee"></a>Bordrolu personel için örnek sorgu

**İstek**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Yanıt**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
