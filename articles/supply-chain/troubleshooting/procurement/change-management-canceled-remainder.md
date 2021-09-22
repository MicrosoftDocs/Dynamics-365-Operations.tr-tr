---
title: Teslimatın geri kalanı iptal edildiğinde satınalma siparişi Onaylandı durumuna geçiyor
description: Değişiklik yönetiminin açık olduğu bir satınalma siparişinde teslimatın geri kalanı iptal edilirse satınalma siparişi Onaylandı durumuna geçer
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
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477860"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Teslimatın geri kalanı iptal edildiğinde satınalma siparişi Onaylandı durumuna geçiyor

## <a name="symptoms"></a>Belirtiler

Değişiklik yönetimine bağlı bir satınalma siparişi için, istenen tek değişiklik bir veya daha fazla satırda kalan teslimatın iptali ise, onaylandığında satınalma siparişi doğrudan *Onaylandı* durumuna geçer ve hiçbir günlük oluşturulmaz.

## <a name="resolution"></a>Çözüm

Bir teslim işleminin geri kalanının iptal edilmesi onay günlüğünün içeriğini etkilemez. Bu işlev, satır kısmen alındığında kullanılmalıdır ve satınalma siparişi satıcıyla onaylandıktan sonra işlem adımında geri kalan miktarı iptal edilmelidir.

Bu, satınalma siparişi teyidini yansıtılacağından, onayın gerekli olabilmesi için satınalma siparişi satırında miktar ayarlanmalıdır. Bunun yerine, satırda hiçbir şey alınmadığında, miktar kaldırılır. Bu durumda, yeniden onay gerekir.
