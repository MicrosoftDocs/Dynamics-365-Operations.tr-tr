---
title: Şirket başına Kazanç yönetimi parametrelerini yapılandırma
description: Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasında şirket başına Kazanç yönetimi için parametrelerin nasıl yapılandırılacağı açıklanmaktadır.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6b3f068c9d3198afa8cd10aaa14bbc7ec9ef3c4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065830"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Şirket başına Kazanç yönetimi parametrelerini yapılandırma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Yararlar sunan her organizasyon için, kazançlar onayı e-postaları ayarlarını konfigüre etmelisiniz.

## <a name="configure-confirmation-email-settings"></a>E-posta ayarlarını yapılandırma onayı

1. **Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Parametreleri**'ni seçin.

2. **Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin: 

   | Alan | Tanım |
   | --- | --- |
   | **Onay e-postası gönder** | Bu özellik açık olduğunda **Personel self servisi**'ndeki kazanç kaydı deneyiminden çıkış yapan çalışanlara bir onay e-postası gönderilir. |
   | **Onay e-postası şablonu** | Kayıt onayını gönderirken kullanılacak organizasyon e-posta şablonunu seçin. Şablon seçmezseniz, aşağıdaki genel e-posta gönderilir:<br><br>%EmployeeFirstName%,<br><br>Tebrikler! Sosyal haklar kaydını başarıyla tamamladınız.<br><br>Teşekkür ederiz,<br><Company/Org name> Kazançlar. |
   | **Gönderenin varsayılan e-posta adresi** | Onay e-postası gönderilirken kullanılacak e-posta adresi. |

3. **Kaydet**'i seçin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
