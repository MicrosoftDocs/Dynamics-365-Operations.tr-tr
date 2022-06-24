---
title: Takılmış toplu işleri sıfırlama
description: Bu makalede, takılan toplu işlerle ilgili sorunların nasıl giderileceği açıklanmaktadır.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896032"
---
# <a name="reset-stuck-batch-jobs"></a>Takılmış toplu işleri sıfırlama


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Çıkış

Microsoft Dynamics 365 Human Resources, **çalıştırılıyor** veya **iptal ediliyor** durumunda takılı kalan ve tamamlanmayan toplu işlerle ilgili sorunlar yaşayabilir.

## <a name="resolution"></a>Çözünürlük

Toplu iş, **çalıştırılıyor** veya **iptal ediliyor** durumunda takılı kaldığında işin iptal edilmesini zorlayarak durumu sıfırlayabilirsiniz. Bunu iptal ettikten sonra, toplu işi **bekliyor** durumuna ayarlayarak sıfırlayabilirsiniz. Daha sonra, zamanlanan bir sonraki toplu işte yürütülmek üzere yeniden alınır.

1. **Sistem Yönetimi** çalışma alanında, **Bağlantılar** sayfasını seçin ve **toplu işler**'i seçin.

2. **Toplu iş** liste sayfasında, sıfırlanması gereken işi seçin.

3. Eylem şeridinde, **iptal etmeye zorla**'yı seçin ve eylemi onaylayın.

   > [!NOTE]
   > **İptal etmeye zorla** eylemi, yalnızca seçilen toplu işin durumu **çalıştırılıyor** veya **iptal ediliyor** olduğunda ve iş için hiçbir toplu yürütme veya iptal işlemi çalıştırılmazken kullanılabilir.

4. Eylem şeridinde **Durumu değiştir**'i seçin.

5. **Yeni durum Seç** sayfasında, **bekliyor**'u seçin ve ardından **Tamam**'ı seçin.

   ![Yeni bir toplu iş durumu seçme.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Ayrıca bkz.

[Toplu işleri çalışma saatleri dışına planlayarak performansı en iyi duruma getirme](hr-admin-troubleshooting-batch-jobs.md)<br>
[Otomatik temizleme görevleriyle performansı en iyi duruma getirme](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
