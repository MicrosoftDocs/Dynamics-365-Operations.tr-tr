---
title: İş emrini belirli bir tarihte ve saatte zamanlama
description: Bu konu, Varlık Yönetiminde, iş emrinin belirli bir tarih ve saate nasıl planlanacağını açıklamaktadır.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439200"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>İş emrini belirli bir tarihte ve saatte zamanlama

[!include [banner](../../includes/banner.md)]

 

Bir iş emrinin belirli bir tarih *ve* saatte zamanlanması gerekiyorsa, Varlık Yönetiminde standart planlama sürecini geçersiz kılabilir ve bir iş emri için belirli bir plan oluşturabilirsiniz.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emri listesinde, **İş emri** sütunundaki İş emri koduna tıklayın.

3. **Düzenle**'yi tıklatın.

4. **İş emri başlığı** hızlı sekmesinde, **Beklenen başlangıç** ve **Beklenen bitiş** alanlarına başlangıç ve bitiş tarihlerini ve saatlerini ekleyin.

    ![Şekil 1](media/05-work-order-scheduling.png)

5. **Genel** sekmesinde, standart planlama işlemini kullanmak için **Zamanla**'ya tıklayın veya iş emrini belirli bir çalışana atamak istiyorsanız **Gönder**'e tıklayın.

6. İş emrinin beklenen dönemde zamanlandığından emin olmak amacıyla varolan herhangi bir kapasite rezervasyonunu geçersiz kılmak için **İş emrini planla** iletişim kutusu > **Sınırlı kapasite** bölümünde aşağıdaki şekilde gösterilen seçimleri yapın. Bu, iş emrinin beklenen başlangıç saatinde başlaması gerektiği için, planlama işleminin varolan kapasite rezervasyonlarını yok sayacağı anlamına gelir.

    ![Şekil 2](media/06-work-order-scheduling.png)

7. Planlamayı başlatmak için **Tamam**'a tıklayın.

8. Planlama süreci çift ayırmaya neden olursa, ekranda bir ileti görüntülenir ve ilgili iş emirlerini ayarlayabilirsiniz.

>[!NOTE]
>İş emri için bir bakım görevlisi planlamak için bu bakım görevlisinin beklenen başlangıç tarihi ve saatinde uygun olması gerekir. Çalışanın uygunluk durumu [çalışan takviminde](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md) ayarlanır. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]