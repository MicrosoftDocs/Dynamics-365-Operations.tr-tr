---
title: Otomatik temizleme görevleriyle performansı en iyi duruma getirme
description: Bu konu altında, toplu iş geçmişini temizleyerek Microsoft Dynamics 365 Human Resources ile ilgili bazı performans sorunlarının nasıl çözüleceğini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010823"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Otomatik temizleme görevleriyle performansı en iyi duruma getirme

**Çıkış**

Toplu iş geçmişi çok fazla büyürse Microsoft Dynamics 365 Human Resources performans sorunlarıyla karşılaşabilir.

**Nedeni**

Sık çalıştırılan toplu işler, toplu iş geçmişinin bozulmasına neden olabilecek büyümeye yol açabilir. Bu durum performans sorunlarına neden olabilir. 

**Çözünürlük**

Toplu iş geçmişinizi temizlemek için bir otomatik görev zamanlayın. Görevi haftalık çalışacak şekilde ayarlamanız önerilir ancak çalışma ortamınıza bağlı olarak temizleme işlemini daha çok veya daha sık çalıştırmanız gerekebilir. Aşağıdaki yordamda önerdiğimiz ayarlar vardır ancak bunları gereksinimlerinize göre değiştirebilirsiniz.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Arama** çubuğunda, **Toplu iş geçmişi temizleme**'yi girin.

   ![Toplu iş geçmişi temizlemeyi arayın](media/talent-batch-history-cleanup-search-bar.png)

3. **Geçmiş sınırı (gün)** bölümüne **30** girin.

   ![Geçmiş sınırı ayarını 30 yapın](media/talent-batch-history-cleanup-history-limit.png)

4. **Arka planda çalıştır**'ı ve sonra **Tekrar**ı seçin.

   ![Yinelemeyi ayarlayın](media/talent-batch-history-cleanup-recurrence.png)

5. **Yineleme tanımla** altında, **Başlangıç tarihini** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın ve **BİTİŞ TARİHİ YOK**'u seçin. 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın](media/talent-batch-history-cleanup-define-recurrence.png)

6. **YİNELEME DÜZENİ** altında, **Günler**'i seçin ve **BELİRTİLEN ARALIKTAN SONRA TEKRARLA** ayarını **7** yapın.

   ![Temizleme tekrarını haftalık yapın](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. **Tamam**'ı seçin.

8. **Arka planda çalıştır** altındaki diğer gerekli parametreleri değiştirin ve **Tamam**'ı seçin.
