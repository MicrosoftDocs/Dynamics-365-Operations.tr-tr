---
title: Malzeme çekme listesi günlüğündeki ambar, bir ürün reçetesi satırında güncelleştirilmiyor.
description: Malzeme çekme listesi günlüğündeki ambar, bir ürün reçetesi (BOM) satırında güncelleştirilmiyor.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026974"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Malzeme çekme listesi günlüğündeki ambar, bir ürün reçetesi satırında güncelleştirilmiyor

KB numarası: 4614848

## <a name="symptoms"></a>Belirtiler

Malzeme çekme listesi günlüğündeki ambar, bir ürün reçetesi (BOM) satırında güncelleştirilmiyor.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Bir malzeme çekme listesi günlük satırı, ürün reçetesi satırına bir referans (lot kodu aracılığıyla) içeriyorsa, üretim malzeme çekme listesi günlük satırındaki ambar boyutu daha sonra değiştirildiğinde ürün reçetesi satırındaki ambar güncelleştirilmez.
