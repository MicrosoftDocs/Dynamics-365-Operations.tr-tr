---
title: Satınalma siparişi teslimat adresi değiştirildikten sonra teslimat adı eşitlenemiyor
description: Satınalma siparişi başlığında teslimat adresini değiştirdikten sonra teslimat adı eşitlenemiyor
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477816"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Satınalma siparişi teslimat adresi değiştirildikten sonra teslimat adı eşitlenemiyor

## <a name="symptoms"></a>Belirtiler

Bir satınalma siparişinin başlığındaki adres teslimat adresi olmayan bir adresle güncelleştirildi. Adres satınalma siparişinde güncelleştirilse de, teslimat adı güncelleştirilmiş adrese göre güncelleştirilmez.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. Seçilen adresin teslimat adresi olarak sınıflandırılması gerekir. Aksi durumda, teslimat adı seçilen adrese göre güncelleştirilmez.
