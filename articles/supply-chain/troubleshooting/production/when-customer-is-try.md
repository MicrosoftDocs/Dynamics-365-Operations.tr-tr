---
title: Yeni bir lot kodu seçildiğinde toplu iş numarası temizlenir
description: Bir malzeme çekme listesi günlük satırını incelediğiniz zaman, Lot Kodu alanında yeni bir değer seçerseniz Toplu iş numarası alanındaki değer temizlenir.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738831"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Yeni bir lot kodu seçildiğinde toplu iş numarası temizlenir

KB numarası: 4613107

## <a name="symptoms"></a>Belirtiler

Bir malzeme çekme listesi günlük satırını incelediğiniz zaman, **Lot Kodu** alanında yeni bir değer seçerseniz **Toplu iş numarası** alanındaki değer temizlenir.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Lot kodunu değiştirirseniz, madde bağlamını değiştirirsiniz. Bu nedenle, toplu iş numarası sıfırlanır.

Toplu iş numarasını bir lot koduyla ilişkilendirmek için, önce lot kodunu ayarlamanız gerekir.
