---
title: Planlı siparişlerin güncelleştirilmesi uzun zaman alabilir
description: Planlı bir siparişte gereksinim miktarı ve/veya teslimat tarihi güncelleştirilirken güncelleştirmeyi kaydetmek için genellikle sipariş başına en az 30 saniye gerekir
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477861"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Planlı siparişlerin güncelleştirilmesi uzun zaman alabilir

## <a name="symptoms"></a>Belirtiler

Planlı bir siparişte gereksinim miktarı ve/veya teslimat tarihi güncelleştirilirken, güncelleştirmeyi kaydetmek için genellikle sipariş başına en az 30 saniye süre gerekir.

## <a name="resolution"></a>Çözüm

Bu, yerleşik master planlama altyapısında oluşan bilinen bir sorundur. Düzenleme sırasında, ürün reçetesi yapısı üzerinden, temel alınan otomatik açılımdan kaynaklanır. Bu sorun, Planlama İyileştirmesi'nde giderilmiştir ve burada bir planlayıcı ilgili siparişleri güncelleştirebilir ve onaylayabilir ve istendiğinde, temel alınan ürün reçetesi yapısı için planlı siparişleri güncelleştirmek amacıyla bir planlama çalıştırmasını tetikleyebilir.

Yerleşik master planlama altyapısıyla performansı artırmanın bir yolu aşağıdaki adımları uygulamaktır:

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Plan seçin.
1. **Gün cinsinden zaman dilimi** hızlı sekmesini genişletin.
1. **Açılım**'ı *Evet* olarak ayarlayın ve bu ayarın altındaki alanı 0 (sıfır) olarak ayarlayın.

> [!NOTE]
> Bu, bu master plan için gerçekleştirilen açılımları tek bir güne sınırlandırır.
