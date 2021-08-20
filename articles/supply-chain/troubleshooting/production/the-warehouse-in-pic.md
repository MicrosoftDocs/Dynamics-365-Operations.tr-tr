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
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740563"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Malzeme çekme listesi günlüğündeki ambar, bir ürün reçetesi satırında güncelleştirilmiyor

KB numarası: 4614848

## <a name="symptoms"></a>Belirtiler

Malzeme çekme listesi günlüğündeki ambar, bir ürün reçetesi (BOM) satırında güncelleştirilmiyor.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Bir malzeme çekme listesi günlük satırı, ürün reçetesi satırına bir referans (lot kodu aracılığıyla) içeriyorsa, üretim malzeme çekme listesi günlük satırındaki ambar boyutu daha sonra değiştirildiğinde ürün reçetesi satırındaki ambar güncelleştirilmez.
