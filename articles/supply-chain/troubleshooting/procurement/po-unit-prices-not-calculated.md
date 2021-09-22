---
title: Satınalma siparişlerindeki birim fiyatlar birim dönüştürmesi temel alınarak hesaplanmaz
description: Satınalma siparişlerindeki birim fiyatlar birim dönüştürmesi temel alınarak hesaplanmaz
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477843"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Satınalma siparişlerindeki birim fiyatlar birim dönüştürmesi temel alınarak hesaplanmaz

## <a name="symptoms"></a>Belirtiler

Bir satınalma siparişinde bir birim değiştirildiğinde, ticari sözleşme fiyatları birim dönüştürme tanımlarına göre yeniden hesaplanmazlar.

## <a name="cause"></a>Nedeni

Fiyatlar her zaman ticari sözleşmelerden (veya satış sözleşmeleri veya malzeme fiyatları gibi sistemdeki diğer fiyat ayarlarından) elde edilir ve bunlar bir birim için ayarlanır.

Sipariş satırındaki birim değiştirilirse, sistem yeni birim için bir fiyat arar ve bu fiyatı uygular. Birim için bir fiyat bulunamazsa, sistem bir fiyat uygulamaz. Birim dönüştürme fiyatı başka bir birime yeniden hesaplamak için kullanılamaz. Teorik olarak, içerisinde on parça bulunan bir kutunun fiyatı bir tek kutunun fiyatının on katına eşit olmayabilir.

## <a name="workaround"></a>Geçici çözüm

Bu sorunu geçici olarak gidermek için kullanabileceğiniz bir yöntem de, malzemenin sipariş satırlarında kullanılmasını beklediğiniz birimler için ticari sözleşmeler olduğundan emin olmalıdır.
