---
title: Satış siparişi konumu değiştirilirse vergi bilgileri güncelleştirilmiyor
description: Bir satış siparişi başlığında tesis, ambar veya teslimat adresi değiştirilirse satırlarda duruma ait vergi bilgileri güncelleştirilmez. Bunu el ile yapmanız gerekir.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477852"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>Satış siparişi başlığındaki konum değiştirilirse vergi bilgileri güncelleştirilmiyor

## <a name="symptoms"></a>Belirtiler

Bir satış siparişi başlığında tesis, ambar veya teslimat adresi değiştirilirse satırlarda duruma ait vergi bilgileri güncelleştirilmez.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. Bu sorun; teslimat adresi, tesis ve ambar, satır düzeyinde otomatik olarak değiştirilmediğinden oluşur. Bunları el ile güncelleştirmelisiniz.
