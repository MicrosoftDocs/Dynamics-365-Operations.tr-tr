---
title: Geçersiz stok boyutları nedeniyle yük satırı oluşturulamıyor
description: Ambara bir iade satış siparişini serbest bırakmaya çalışırken geçersiz stok boyutları ile ilgili bir hata alabilirsiniz. Bunları sipariş satırından kaldırın.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119224"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Geçersiz stok boyutları nedeniyle iade satış siparişi için yük satırı oluşturulamıyor

## <a name="symptoms"></a>Belirtiler

Ambara bir iade satış siparişini serbest bırakmaya çalışırken aşağıdaki hata iletisini alabilirsiniz:

> Sipariş satırı, geçersiz stok boyutları içerdiğinden bu sipariş için yükleme satırı oluşturamazsınız. Rezervasyon hiyerarşisinde konum boyutunun altında bulunan stok boyutlarına referans veremezsiniz. Sipariş satırından geçersiz boyutları kaldırın.

## <a name="resolution"></a>Çözüm

Ne yazık ki, ürün bir satış iade işlemi için yük işlemeyi desteklemiyor. Bu nedenle, iade satış siparişini ambara serbest bırakamazsınız.

Satış siparişi hareketlerinde, rezervasyon hiyerarşisinde **Konum** boyutunun altında bulunan stok boyutlarına referans veremezsiniz. Çözüm, sipariş satırından geçersiz boyutları kaldırmaktadır.
