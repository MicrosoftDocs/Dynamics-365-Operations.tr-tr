---
title: Bordro tümleştirme parametreleri
description: Bu konuda, Dynamics 365 Human Resources Bordro tümleştirme parametreleri açıklanmaktadır.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37d4dc52e7fe5ddd95f43d98267db819a275bd92
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069869"
---
# <a name="payroll-integration-parameters"></a>Bordro tümleştirme parametreleri


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources Bordro tümleştirmesini kullanmadan önce, bu konuda açıklanan parametreleri ayarlamanız gerekir.

## <a name="enable-payroll-address"></a>Bordrolu adresini etkinleştirme

Bordro adresini kullanabilmeniz için, bunu Bordro tümleştirme sekmesindeki [Paylaşılan Parametreler formundan](hr-setup-shared-parameters.md) etkinleştirmelisiniz.

## <a name="define-the-identification-type"></a>Kimlik türünü tanımlama

Kimlik türü kodunu [Bordro çalışan varlığında](hr-admin-integration-payroll-api-payroll-employee.md) göstermek için her şirkete yönelik [insan kaynakları parametrelerini yapılandırmalısınız](hr-setup-shared-parameters.md).

1. **Ücret yönetimi** çalışma alanında, bağlantılar altında **İnsan Kaynakları Parametreleri**'ni seçin. 
2. **Bordro tümleştirme** sekmesinde, aşağıdaki alanların değerini belirtin.

| Alan | Tanım |
| --- | --- |
| Bordro işlemede kimlik türlerini kullan | Bu seçenek belirlendiğinde, seçilen tür kodu Bordro çalışan varlığı içinde görüntülenir. |
| Kimlik türü | [Bordro çalışan varlığının](hr-admin-integration-payroll-api-payroll-employee.md) **mshr_payrollemployeeentityid** alanıdan gösterilen kimlik türü. |

## <a name="see-also"></a>Ayrıca bkz.

[Bordro tümleştirme API'sına giriş](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
