---
title: Otomatik temizleme görevleriyle performansı en iyi duruma getirme
description: Bu makalede, toplu iş geçmişini temizleyerek Microsoft Dynamics 365 Human Resources'da performansın nasıl iyileştirileceği açıklanmaktadır.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 10d535e54f71e7bb90c7385e09926270a446df7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902212"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Otomatik temizleme görevleriyle performansı en iyi duruma getirme


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Çıkış**

Toplu iş geçmişi çok fazla büyürse Microsoft Dynamics 365 Human Resources performans sorunlarıyla karşılaşabilir.

**Nedeni**

Sık çalıştırılan toplu işler, toplu iş geçmişinin bozulmasına neden olabilecek büyümeye yol açabilir. Bu durum performans sorunlarına neden olabilir. 

**Çözünürlük**

Toplu iş geçmişinizi temizlemek için bir otomatik görev zamanlayın. Görevi haftalık çalışacak şekilde ayarlamanız önerilir ancak çalışma ortamınıza bağlı olarak temizleme işlemini daha çok veya daha sık çalıştırmanız gerekebilir. Aşağıdaki yordamda önerdiğimiz ayarlar vardır ancak bunları gereksinimlerinize göre değiştirebilirsiniz.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Arama** çubuğunda, **Toplu iş geçmişi temizleme**'yi girin.

   ![Toplu iş geçmişi temizlemeyi arayın.](media/talent-batch-history-cleanup-search-bar.png)

3. **Geçmiş sınırı (gün)** bölümüne **30** girin.

   ![Geçmiş sınırı ayarını 30 yapın.](media/talent-batch-history-cleanup-history-limit.png)

4. **Arka planda çalıştır**'ı ve sonra **Tekrar** ı seçin.

   ![Yinelemeyi ayarlayın.](media/talent-batch-history-cleanup-recurrence.png)

5. **Yineleme tanımla** altında, **Başlangıç tarihini** ve **Başlangıç saatini** mesai saatlerin dışında veya hafta sonu sırasında oluşacak şekilde ayarlayın ve **BİTİŞ TARİHİ YOK**'u seçin. 

   ![Yineleme başlangıç tarihini ve saatini tanımlayın.](media/talent-batch-history-cleanup-define-recurrence.png)

6. **YİNELEME DÜZENİ** altında, **Günler**'i seçin ve **BELİRTİLEN ARALIKTAN SONRA TEKRARLA** ayarını **7** yapın.

   ![Temizleme tekrarını haftalık yapın.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. **Tamam**'ı seçin.

8. **Arka planda çalıştır** altındaki diğer gerekli parametreleri değiştirin ve **Tamam**'ı seçin.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
