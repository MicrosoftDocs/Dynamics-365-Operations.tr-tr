---
title: Satış siparişi satırlarını oluştururken aynı ticari sözleşme seçildi
description: Belirli bir tarih için tanımlı birden fazla ticari sözleşme varsa satış siparişi satırlarını oluştururken her zaman en düşük fiyata sahip olan sözleşme seçilir.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a586a399fb349965b972191bec1271651bec5fcb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477853"
---
# <a name="if-two-trade-agreements-exist-for-overlapping-dates-the-same-one-is-always-selected"></a>Çakışan tarihler için iki ticari sözleşme varsa her zaman aynı sözleşme seçilir

## <a name="symptoms"></a>Belirtiler

Aynı dönem veya çakışan dönemler için iki ticari sözleşme tanımlanmışsa bu maddeleri içeren satış siparişi satırlarını oluştururken her zaman aynı ticari sözleşmenin seçildiği görülüyor.

## <a name="resolution"></a>Çözüm

Belirli bir tarihe ait birden fazla ticari sözleşme varsa, en düşük fiyata sahip olan ticari sözleşme her zaman seçilir. Daha fazla bilgi için, aşağıdaki teknik incelemeyi karşıdan yükleyin: [Microsoft Dynamics AX 2012'de ticari sözleşmeler](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).
