---
title: Hareketler askıya alınan bir muhasebe hesabına nakledilebilir
description: Bir ürün girişi iptal edilirse ana hesaplar askıya alınmış olsa bile sistem, hareketlerin askıya alınan genel muhasebe hesaplarına nakledilmesini sağlar
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
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477896"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Hareketler askıya alınan bir muhasebe hesabına nakledilebilir

## <a name="symptoms"></a>Belirtiler

Bir ürün girişi iptal edilirse, ana hesaplar askıya alınmış olsa bile, sistem hareketlerin askıya alınan genel muhasebe hesaplarına nakledilmesini sağlar.

## <a name="reproduce-the-issue"></a>Sorunu yeniden oluşturma

Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.

1. **Borç hesapları parametreleri** sayfasındaki **Genel** sekmesinde, **Ürün girişini deftere naklet** seçeneğinin *Evet* olarak ayarlandığından emin olun.
1. Satınalma siparişi oluşturun ve *bir ürün için 1.000'lik miktarı içeren bir sipariş satırı ekleyin*.
1. Satınalma siparişini doğrulayın.
1. Ürün girişini deftere nakledin ve fişleri denetleyin.
1. *200140* ve *140200* olan ilgili ana hesapları askıya alın.
1. Deftere nakledilen ürün girişini iptal edin.
1. Hareketlerin askıya alınan muhasebe hesaplara nakledilebileceğini unutmayın.

## <a name="resolution"></a>Çözüm

Ürün girişleri iptal edildiğinde, hareketler, bu yaklaşım deftere doğru nakledilmeye olanak sağladığında, bekleyen genel muhasebe defterine nakledilebilir.
