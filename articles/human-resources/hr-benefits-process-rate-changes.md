---
title: Oran değişikliklerini işleme
description: Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasında kazanç oranı değişikliklerinin nasıl işleneceği açıklanmaktadır.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa94584749e72cab7aa3466814ed8ea9d59665da
ms.sourcegitcommit: 4f9c889e5cf72f34dd9746a322f8c0d6b983037b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/25/2021
ms.locfileid: "7417519"
---
# <a name="process-rate-changes"></a>Oran değişikliklerini işleme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, uygunluk kuralı ayarlarındaki yeni veya var olan bir kazanç planında bir değişiklik olduğunda Microsoft Dynamics 365 Human Resources uygulamasında kazanç oranı değişikliklerinin nasıl işleneceği açıklanmaktadır. Yeni bir uygunluk kuralı oluşturulup plana atanmışsa, bu durum sisteme, çalışanların şimdi yeni uygunluk seçeneklerine dayalı olarak planlama için uygun olup olmadığını denetlemek amacıyla, alt uygunluğu yeniden çalıştırması için uyarır. 

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
