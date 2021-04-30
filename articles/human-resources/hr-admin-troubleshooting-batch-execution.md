---
title: Takılmış toplu işleri sıfırlama
description: Bu konu, takılan toplu işlerle ilgili sorunların nasıl giderileceğini açıklamaktadır.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881772"
---
# <a name="reset-stuck-batch-jobs"></a>Takılmış toplu işleri sıfırlama

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

   ![Yeni bir toplu iş durumu seç](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Ayrıca bkz.

[Toplu işleri çalışma saatleri dışına planlayarak performansını en iyi duruma getirme](hr-admin-troubleshooting-batch-jobs.md)<br>
[Otomatik temizleme görevleriyle performansı en iyi duruma getirme](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
