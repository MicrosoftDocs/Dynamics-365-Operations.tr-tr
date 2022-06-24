---
title: Oran değişikliklerini işleme
description: Bu makalede, Microsoft Dynamics 365 Human Resources'da kazanç oranı değişikliklerinin nasıl işleneceği açıklanmaktadır.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 09714c70cb00b1a1b5dbd4613bbd70ff11d35cb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882967"
---
# <a name="process-rate-changes"></a>Oran değişikliklerini işleme


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, yeni veya mevcut bir kazanç planının uygunluk kuralı ayarlarında bir değişiklik olduğunda Microsoft Dynamics 365 Human Resources'da kazanç oranı değişikliklerinin nasıl işleneceği açıklanmaktadır. Yeni bir uygunluk kuralı oluşturulup plana atanmışsa, bu durum sisteme, çalışanların şimdi yeni uygunluk seçeneklerine dayalı olarak planlama için uygun olup olmadığını denetlemek amacıyla, alt uygunluğu yeniden çalıştırması için uyarır. 

1. **Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Oran değişimi güncelleme işlemini** seçin.

2. **Kazanç kaydı oran güncelleme çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kayıt dönemi** | Oran değişiklikleri işleyecek kayıt dönemi. |

3. İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:

   1. İşlem bilgilerini girin.

   2. Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.

   3. İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.

   4. **Tamam**'ı seçin. İşlem, ayarladığınız parametrelerle çalışacaktır.

4. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
