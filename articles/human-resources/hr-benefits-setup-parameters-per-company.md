---
title: Şirket başına Kazanç yönetimi parametrelerini yapılandırma
description: Microsoft Dynamics 365 Human Resources'Ta sosyal haklar yönetimiyle ilgili şirket başıan parametreleri yapılandırın.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057634"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Şirket başına Kazanç yönetimi parametrelerini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Yararlar sunan her organizasyon için, kazançlar onayı e-postaları ayarlarını konfigüre etmelisiniz.

## <a name="configure-confirmation-email-settings"></a>E-posta ayarlarını yapılandırma onayı

1. **Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Parametreleri**'ni seçin.

2. **Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin: 

   | Alan | Tanım |
   | --- | --- |
   | **Onay e-postası gönder** | Bu özellik açık olduğunda, çalışan self servis 'deki sosyal haklar kayıt deneyiminden çıktığında çalışanlara bir onay e-postası gönderilir. |
   | **Onay e-postası şablonu** | Kayıt onayını gönderirken kullanılacak organizasyon e-posta şablonunu seçin. Şablon seçmezseniz, aşağıdaki genel e-posta gönderilir:<br><br>%EmployeeFirstName%,<br><br>Tebrikler! Sosyal haklar kaydını başarıyla tamamladınız.<br><br>Teşekkür ederiz,<br><Company/Org name> Kazançlar. |
   | **Gönderenin varsayılan e-posta adresi** | Onay e-postası gönderilirken kullanılacak e-posta adresi. |

3. **Kaydet**'i seçin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]