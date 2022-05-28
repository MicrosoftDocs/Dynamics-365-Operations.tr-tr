---
title: TaxTrans kaydı oluşturulmuyor
description: Bu konu, TaxTrans kaydı oluşturulmuyorsa yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.openlocfilehash: 969d086c77b40b59495ae0d9e631579abf5e0ec6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686421"
---
# <a name="taxtrans-record-isnt-generated"></a>TaxTrans kaydı oluşturulmuyor

[!include [banner](../includes/banner.md)]

Bir hareket için **Deftere nakledilen satış vergisi**'ni seçerseniz ancak **Deftere nakledilen satış vergisi** sayfası hiçbir vergi satırı göstermiyor veya bir vergi satırı eksikse, **TaxTrans** kaydı oluşturulmamış olabilir.

[![Satır maddeleri olmayan deftere nakledilen satış vergisi sayfası.](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>Hareketi deftere nakletmeden önce satış vergisini denetleyin

1. Hareketi deftere nakletmeden önce, **Faturayı deftere nakletme** sayfasında hesaplamayı denetlemek için **Satış vergisi**'ni seçin.

    [![Fatura deftere nakli sayfasındaki satış vergisi düğmesi.](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. **Geçici satış vergisi hareketleri** sayfasında, hesaplama sonucunu gözden geçirin. Herhangi bir vergi hesaplanmamışsa bkz. [Vergi hesaplanmıyor veya vergi tutarı sıfır](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>Tüm deftere nakledilen satış vergilerinde TaxTrans kaydını bulun

1. **Vergi** \> **Sorgular ve bildirimler** \> **Satış vergisi sorguları** > **Deftere nakledilen satış vergisi**'ne gidin.
2. **TaxTrans** kaydını bulmak için **Fiş** sütunu başlığında filtre sembolünü seçin.
3. Aradığınız satış vergisi kayıtlarını bulursanız, tarihi kontrol edin. Tarih, günlük başlığındaki tarihten farklıysa, ek destek için bir Microsoft servis talebi oluşturun.

    [![Deftere nakledilen satış vergisi sayfası.](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>Ayrıntıları denetlemek için hata ayıklama

1. Hata ayıklama ve **TmpTaxWorkTrans** ve **TaxUncommitted**'ın doğru oluşturulup oluşturulmadığını tespit etmek hakkında bilgi edinmek için bkz. [TaxTrans'taki alan değeri hatalı](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).
2. **TaxTmpWorkTrans** veya **TaxUncommitted** öğesi doğru oluşturulduysa, **TaxTrans**'ın eklenmeme nedeninde hata ayıklama yapmak için **TaxPost::SaveAndPost()** ve **Tax::SaveAndPost** yönteminde kesme noktası ekleyin.

    [![Kodda eklenen kesme noktaları.](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![Eklenen kesme noktalarının sonuçları.](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>Özelleştirme olup olmadığını belirleyin

Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin. Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
