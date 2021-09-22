---
title: Üretim emirleriyle stokta bulunanlar için planlı siparişler oluşturulur
description: Stoktaki maddeler ve bu maddeler için üretim emirleriniz olsa bile planlı siparişler oluşturulur
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
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477897"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Üretim emirleriyle stokta bulunanlar için planlı siparişler oluşturulur

## <a name="symptoms"></a>Belirtiler

Stoktaki maddeler ve bu maddeler için üretim emirleriniz olsa bile planlı siparişler oluşturulur.

## <a name="resolution"></a>Çözüm

**Kapsam grubu** sayfasında, ilgili grupların **Pozitif günler** değerlerini artırarak bu sorunu giderebilirsiniz. Bu değişiklik, sistemin talep için eldeki stoğun kullanılabileceği konusunda karar vermesine neden olur. Daha sonra, stokta bulunan maddeler için yeni bir planlı sipariş oluşturulmaz.
