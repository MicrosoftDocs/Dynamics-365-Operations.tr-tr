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
ms.openlocfilehash: 0c489b99d5d05ddac46d222e701512288aeb10583a5e829212e0e1c924622f16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712085"
---
# <a name="payroll-integration-parameters"></a>Bordro tümleştirme parametreleri

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
