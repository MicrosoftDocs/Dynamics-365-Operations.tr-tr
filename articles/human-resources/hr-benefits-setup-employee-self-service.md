---
title: Employee Self-Service'i yapılandırma
description: Microsoft Dynamics 365 Human Resources'ta, kutucukları çalışan self serviste üst düzey gezinti için yapılandırabilirsiniz.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7ddb1f1ea74a16265dac701151b2c25a4f9d4dc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687177"
---
# <a name="configure-employee-self-service"></a>Personel self servisini yapılandırma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources uygulamasında, **Personel self servisi**'nde üst düzey gezinme için kutucukları yapılandırabilirsiniz. Kazanç planı kutucukları kullanıcıları uygun oldukları kazanç planlarına yönlendirir.

## <a name="set-up-a-benefit-plans-tile"></a>Kazanç planları kutucuğu ayarlama

1. **Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.

2. **Kazanç planları kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin.

   | Alan | Tanım |
   | --- | --- |
   | **Plan türü kodu** | Bu kutucuk **Yan haklar self servisi**'nde seçildiğinde görüntülenen plan türü. |
   | **Kutucuk kodu** | Kutucuk için benzersiz tanımlayıcı. |
   | **Kutucuk etiketi metni** | **Yan haklar self servisinde** kutucuk için görüntülenecek metin. |
   | **Tanım** | Kutucuğun bir açıklaması. |
   | **Kutucuk arka plan görüntüsü** | Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı). |
   | **Açık kaydı izleme** | Bu plan türü için açık kayıt ilerlemesini izlemek üzere bu seçeneği belirleyin. Örneğin, **Plan türü = Diğer** şeklinde oluşturulmuş planlar olabilir. Bunlar, kayıt ilerleme durumunu izlemek istemediğiniz isteğe bağlı planlar olabilir. Bu plan türünü seçmezseniz **Açık kayıt** sekmesinde kayıt ilerleme durumu veya kayıt tamamlaması izlendiğinde bu tür bir plan yoksayılır. Bu ayar, tüm dönemler ve tüzel kişilikler için seçilen plan türü için geçerlidir. |

4. **Kaydet**'i seçin.

## <a name="set-up-a-flex-credit-plan-tile"></a>Esnek kredi planı kutucuğu ayarla

1. **Sosyal haklar yönetimi** çalışma alanında, **kurulum** altında **çalışan Self Servis parametreleri**'ni seçin.

2. **Esnek kredi planı kutucuk kurulumu** sekmesini seçin ve sonra **yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin.

   | Alan | Tanım |
   | --- | --- |
   | **Kazanç kredisi kodu** | Bu kutucuk **Yan haklar self servisi**'nde seçildiğinde görüntülenecek esnek kredi programı planları. |
   | **Kutucuk kodu** | Kutucuk için benzersiz tanımlayıcı. |
   | **Kutucuk etiketi metni** | **Yan haklar self servisinde** kutucuk için görüntülenecek metin. |
   | **Tanım** | Kutucuğun bir açıklaması. |
   | **Kutucuk arka plan görüntüsü** | Kutucuk için kullanılacak görüntünün URL'si (isteğe bağlı). |
   | **Açık kaydı izleme** | Bu plan türü için açık kayıt ilerlemesini izlemek üzere bu seçeneği belirleyin. Örneğin, **Plan türü = Diğer** şeklinde oluşturulmuş planlar olabilir. Bunlar, kayıt ilerleme durumunu izlemek istemediğiniz isteğe bağlı planlar olabilir. Bu plan türünü seçmezseniz **Açık kayıt** sekmesinde kayıt ilerleme durumu veya kayıt tamamlaması izlendiğinde bu tür bir plan yoksayılır. Bu ayar, tüm dönemler ve tüzel kişilikler için seçilen plan türü için geçerlidir. |

4. **Kaydet**'i seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
