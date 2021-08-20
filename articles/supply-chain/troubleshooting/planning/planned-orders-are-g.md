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
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742016"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Master planlama, hayali ürünler için planlı siparişler oluşturuyor

KB numarası: 4614729

## <a name="symptoms"></a>Belirtiler

Bir master planlama çalıştırıldıktan sonra hayali ürünler için planlı siparişler oluşturuluyor.

## <a name="resolution"></a>Çözünürlük

Serbest bırakılan ürünlerin **Hayali** seçeneğinin ayarı, ürün reçetesindeki (BOM) varsayılan satır türünü belirler. **Hayali** seçeneği *Evet* olarak ayarlandığında, sistem madde için planlanan siparişler oluşturur, ancak her planlı sipariş için **Doğrudan türetilmiş gereksinim** seçeneği *Evet* olarak ayarlanır. Bu nedenle, planlı üretim emri kendi başına kesinleştirilemez. Bunun yerine, üst üretim emri kesinleştirildiğinde her zaman otomatik olarak dahil edilir. Ayrıca, planlı hayali siparişin ürün reçetesi satırları üst üretim emrinin ürün reçetesine dahil edilir.
