---
title: Planlama işini iptal etme
description: Bu konuda, Planlamayı en iyi duruma getirme işlevini kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 18c5c7b8030fc6adbc548dab750e4f454aebc867
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076364"
---
# <a name="cancel-a-planning-job"></a>Planlama işini iptal etme

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management'ta, Planlamayı en iyi duruma getirme işlevini kullanan etkin bir planlama işini iptal edebilirsiniz. Bir Planlama en iyi duruma getirme işi doğrudan kullanıcı arabiriminden tetiklendiğinde (arka planda değil), iletişim kutusunda **İptal**'i seçerseniz bu işlem Planlama en iyi duruma getirme işini iptal etmez. "İşlem iptal edildi" gibi bir uyarı alsanız bile Planlama en iyi duruma getirme işlemi ile planlama işini iptal etmek için yine de aşağıdaki adımları kullanmanız gerekir.


Etkin bir planlama işini iptal etmek için aşağıdaki adımları izleyin. 

> [!NOTE]
> Yalnızca etkin işler iptal edilebilir.

1. **Master planlama \> Ayar \> Planlar**'a gidin.
2. Planlama çalışması için uygun bir plan seçin.
3. **Geçmiş**'i seçin.
4. İptal edilecek planlama işini seçin.
5. **İptal**'i seçin.

Planlamayı En İyi Duruma Getirme hizmeti işin iptal edilmesini onaylayana kadar iş durumu **İptal ediliyor** olur. Ardından durum **İptal Edildi** olarak değiştirilir.

> [!NOTE]
> Durum değişikliklerini görmek için **Yenile** düğmesini seçerek sayfayı yenilemeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Planlamayı En İyi Duruma Getirmeye genel bakış](planning-optimization-overview.md)

[Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama](get-started.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)
