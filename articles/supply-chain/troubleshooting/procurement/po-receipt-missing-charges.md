---
title: Satınalma siparişi girişi tüm giderleri içermiyor
description: Satınalma siparişi girişi tüm giderleri içermiyor
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477806"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Satınalma siparişi girişi tüm giderleri içermiyor

## <a name="symptoms"></a>Belirtiler

Satınalma siparişi aldığınızda tüm giderler girişe dahil edilmez.

### <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. **Satın alma ve kaynak hizmeti parametreleri** sayfasındaki **Teslimat** sekmesinde, **Ürün girişinde masraf oluştur** seçeneğinin *Evet* olarak ayarlandığından emin olun.
1. Masrafları içeren bir satınalma siparişi oluşturun.
1. Satınalma siparişini doğrulayın.
1. Satınalma siparişini teslim alın.
1. Makbuz toplamına bakın ve beklenen toplamla karşılaştırın.
1. Tüm giderlerin satınalma siparişi girişine dahil edilmediğinden emin olun.

## <a name="resolution"></a>Çözüm

Çözüm, sair giderlerin ayarlandığı yönteme bağlıdır. Gereksinimlerinizi karşılamak amacıyla sair giderlerin nasıl ayarlanacağı hakkında bilgi için aşağıdaki blog yazısına bakın: [Ürün makbuzu oluşturulurken sair giderleri deftere nakletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
