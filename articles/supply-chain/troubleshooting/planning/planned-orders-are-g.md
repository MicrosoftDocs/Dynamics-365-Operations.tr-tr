---
title: Master planlama, hayali ürünler için planlı siparişler oluşturuyor
description: Bir master planlama çalıştırıldıktan sonra hayali ürünler için planlı siparişler oluşturuluyor.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026990"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Master planlama, hayali ürünler için planlı siparişler oluşturuyor

KB numarası: 4614729

## <a name="symptoms"></a>Belirtiler

Bir master planlama çalıştırıldıktan sonra hayali ürünler için planlı siparişler oluşturuluyor.

## <a name="resolution"></a>Çözünürlük

Serbest bırakılan ürünlerin **Hayali** seçeneğinin ayarı, ürün reçetesindeki (BOM) varsayılan satır türünü belirler. **Hayali** seçeneği *Evet* olarak ayarlandığında, sistem madde için planlanan siparişler oluşturur, ancak her planlı sipariş için **Doğrudan türetilmiş gereksinim** seçeneği *Evet* olarak ayarlanır. Bu nedenle, planlı üretim emri kendi başına kesinleştirilemez. Bunun yerine, üst üretim emri kesinleştirildiğinde her zaman otomatik olarak dahil edilir. Ayrıca, planlı hayali siparişin ürün reçetesi satırları üst üretim emrinin ürün reçetesine dahil edilir.
