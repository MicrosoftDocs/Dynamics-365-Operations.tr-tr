---
title: Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme
description: Bu konu altında, saatler sonra uzun süre çalışan toplu işler planlayarak Microsoft Dynamics 365 Human Resources ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: twheeloc
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 29521643314144c9d447ac8287fa4ee85343d624
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533922"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Toplu işleri, saatler sonra çizelgelemek için performansı en iyi duruma getirme


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Çıkış

Microsoft Dynamics 365 Human Resources, uzun süren toplu işler tipik iş saatlerinde çalışıyorsa, performans sorunlarıyla karşılaşabilir.

## <a name="resolution"></a>Çözünürlük

Aşağıdaki toplu işleri kapalı saatlerde zamanlar. Ayrıca, sık çalışan toplu işlerin sıklığını gözden geçirmeyi öneririz. Mümkünse, toplu işin tekrarlanma şeklini azaltın. Birçok durumda, varsayılan sıklık yeterlidir.

Aşağıdaki toplu işler gece veya saat tarihinden sonra çalışmalıdır. Bu yinelenen toplu işlerin saat dilimini kontrol edin. Bazı toplu işler Pasifik Standart Saati (PST) kullanabilir.

| Toplu iş | Varsayılan oluşum |
| --- | --- |
| Toplu iş geçmişi temizleme | Ayda 1 saat |
| Dışa aktarma hazırlığını temizleme | Günde 1 saat |
| Common Data Service tümleştirmesi, istek eşitlemesini atladı | Günde 1 saat |
| Saatler dışında düzenli olarak çalıştırılması gereken veritabanı sıkıştırma sistemi işi | Günde 1 saat |
| Saatler dışında düzenli olarak çalıştırılması gereken veritabanı dizin yeniden oluşturma sistem işi | Günde 1 saat |

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Arama** çubuğunda, yukarıdaki toplu işlerden birini arayın.

3. **Arka planda çalıştır**'ı ve sonra **Tekrar** ı seçin.

   ![Yinelemeyi ayarlayın.](media/talent-batch-history-cleanup-recurrence.png)

4. **Yineleme tanımla** altında, **Başlangıç tarihi** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın. **Bitiş tarihi yok**'u seçin. 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın.](media/talent-batch-history-cleanup-define-recurrence.png)

5. **Tamam**'ı seçin.

6. Gerekirse **Arka planda çalıştır** altındaki diğer parametreleri değiştirin ve **Tamam**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Otomatik temizleme görevleriyle performansı en iyi duruma getirme](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
