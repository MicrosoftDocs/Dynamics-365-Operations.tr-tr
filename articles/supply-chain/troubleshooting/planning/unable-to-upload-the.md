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
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026987"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Talep tahmini kayıtlarını içe aktardığınızda, tahmin edilen birim maliyeti güncelleştiremezsiniz

KB numarası: 4614109

## <a name="symptoms"></a>Belirtiler

Talep tahmin kayıtlarını içe aktarmak için veri varlıklarını kullandığınızda, mevcut kayıtların **Tahmin edilen birim maliyeti** değeri, içe aktarılan verilerle eşleşmesi için güncelleştirilmez.

## <a name="cause"></a>Nedeni

**Tahmin edilen birim maliyet** salt okunur bir alandır. Değer, ürün birim maliyetine dayanır ve içe aktarma yoluyla doğrudan ayarlanamaz.

## <a name="resolution"></a>Çözünürlük

Alan salt okunur olduğundan, buraya değerleri aktaramazsınız. Değer, mevcut iş mantığına göre hesaplanır.
