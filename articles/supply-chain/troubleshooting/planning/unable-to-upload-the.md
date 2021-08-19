---
title: Talep tahmini kayıtlarını içe aktardığınızda, tahmin edilen birim maliyeti güncelleştiremezsiniz
description: Talep tahmin kayıtlarını içe aktarmak için veri varlıklarını kullandığınızda, mevcut kayıtların maliyet fiyatı, içe aktarılan verilerle eşleşmesi için güncelleştirilmez.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765382"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Talep tahmini kayıtlarını içe aktardığınızda, tahmin edilen birim maliyeti güncelleştiremezsiniz

KB numarası: 4614109

## <a name="symptoms"></a>Belirtiler

Talep tahmin kayıtlarını içe aktarmak için veri varlıklarını kullandığınızda, mevcut kayıtların **Tahmin edilen birim maliyeti** değeri, içe aktarılan verilerle eşleşmesi için güncelleştirilmez.

## <a name="cause"></a>Nedeni

**Tahmin edilen birim maliyet** salt okunur bir alandır. Değer, ürün birim maliyetine dayanır ve içe aktarma yoluyla doğrudan ayarlanamaz.

## <a name="resolution"></a>Çözünürlük

Alan salt okunur olduğundan, buraya değerleri aktaramazsınız. Değer, mevcut iş mantığına göre hesaplanır.
