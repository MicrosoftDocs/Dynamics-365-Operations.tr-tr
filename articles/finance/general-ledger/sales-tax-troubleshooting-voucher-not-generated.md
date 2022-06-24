---
title: Fiş oluşturulmuyor
description: Bu makale, oluşturulması gereken fiş oluşturulmuyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1200fe50bf9be4c6d1ca809ad9a86da2ff3e0ced
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909025"
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
