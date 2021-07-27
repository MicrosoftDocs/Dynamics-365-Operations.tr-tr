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
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314514"
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
