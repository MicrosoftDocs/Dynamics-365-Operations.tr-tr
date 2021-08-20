---
title: Fiş oluşturulmuyor
description: Bu konu, oluşturulması gereken fiş oluşturulmuyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1fbd5b5bb4a1d2a0c498b2abac82bd6f5ff3f1d2ed9960885eb8f44cbb17884d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759884"
---
# <a name="voucher-isnt-generated"></a>Fiş oluşturulmuyor

[!include [banner](../includes/banner.md)]

Bir fiş oluşturulması gerekirken **Fiş hareketleri** sayfasında herhangi bir fiş görüntülenmiyorsa bu sorunu gidermek için aşağıdaki bölümlerdeki adımları izleyin.

[![Fiş görüntülenmeyen fiş hareketleri sayfası.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Vergi uygulanabilirliğini kontrol edin

1. **Vergi** \> **Periyodik görevler** \> **Henüz transfer edilmemiş alt muhasebe günlük girişleri**'ne gidin.
2. Defter kaydı varsa bunu seçin ve **Şimdi transfer et**'i seçin.

    [![Henüz transfer edilmemiş alt genel muhasebe günlük girişleri sayfasındaki Şimdi transfer et düğmesi.](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Fişin oluşturulup oluşturulmadığını görmek için **Fiş hareketleri** sayfasını yeniden açın.

## <a name="determine-whether-customization-exists"></a>Özelleştirme olup olmadığını belirleyin

Önceki bölümdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin. Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
