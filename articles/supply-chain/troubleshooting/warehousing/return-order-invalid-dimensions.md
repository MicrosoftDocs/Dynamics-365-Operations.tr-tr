---
title: Geçersiz stok boyutları nedeniyle yük satırı oluşturulamıyor
description: Ambara bir iade satış siparişini serbest bırakmaya çalışırken geçersiz stok boyutları ile ilgili bir hata alabilirsiniz. Bunları sipariş satırından kaldırın.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477864"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Geçersiz stok boyutları nedeniyle iade satış siparişi için yük satırı oluşturulamıyor

## <a name="symptoms"></a>Belirtiler

Ambara bir iade satış siparişini serbest bırakmaya çalışırken aşağıdaki hata iletisini alabilirsiniz:

> Sipariş satırı, geçersiz stok boyutları içerdiğinden bu sipariş için yükleme satırı oluşturamazsınız. Rezervasyon hiyerarşisinde konum boyutunun altında bulunan stok boyutlarına referans veremezsiniz. Sipariş satırından geçersiz boyutları kaldırın.

## <a name="resolution"></a>Çözüm

Ne yazık ki, ürün bir satış iade işlemi için yük işlemeyi desteklemiyor. Bu nedenle, iade satış siparişini ambara serbest bırakamazsınız.

Satış siparişi hareketlerinde, rezervasyon hiyerarşisinde **Konum** boyutunun altında bulunan stok boyutlarına referans veremezsiniz. Çözüm, sipariş satırından geçersiz boyutları kaldırmaktadır.
