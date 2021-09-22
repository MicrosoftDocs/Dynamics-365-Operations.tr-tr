---
title: Fiş oluşturulmasa da bir ürün girişi fiş numarası kullanılıyor
description: Ürün girişi sırasında hiçbir mali fiş oluşturulmasa da bir ürün girişi fiş numarası kullanılıyor
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
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477842"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Fiş oluşturulmasa da bir ürün girişi fiş numarası kullanılıyor

## <a name="symptoms"></a>Belirtiler

Ürün girişi sırasında hiçbir mali fiş oluşturulmasa da, bir ürün girişi fiş numarası kullanılır.

## <a name="resolution"></a>Çözüm

Malzeme modeli grubu için **Ürün girişindeki tahakkuk borcu** seçeneği *Hayır* olarak ayarlanmışsa, genel muhasebeye nakil yapılmaz. Ancak, bir alt genel muhasebede muhasebe amacıyla fiziksel bir olay kaydedilir ve bu olay bir fiş numarası gerektirir. Bu fiş numarası stok hareketlerinde referans alınan fiş numarasıdır.

Aşağıdaki Web günlüğünde açıklandığı gibi, **Ürün girişindeki tahakkuk borcu** seçeneğini *Evet* olarak ayarlamanız önerilir: [Ürün makbuzu oluşturulurken sair giderleri deftere nakletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
