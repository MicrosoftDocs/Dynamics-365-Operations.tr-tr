---
title: Bölmeden sonra azalan bakiyeli amortisman
description: Bu makale, Sabit varlıklarda bir varlık bölündükten sonra amortismanı hesaplamak için azalan bakiye yönteminin kullanılmasını açıklamaktadır.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 539967a9a73da91f6b49c1bb89f404267ae0a804
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883314"
---
# <a name="reduce-balance-depreciation-after-a-split"></a>Bölmeden sonra azalan bakiyeli amortisman

[!include [banner](../includes/banner.md)]

Bu makale, Sabit varlıklarda varlık başka bir varlığa bölündükten sonra amortismanı hesaplamak için azalan bakiye yönteminin kullanılmasını açıklamaktadır. Varlık defterinde yapılandırılan amortisman yılı mali yıldır. Daha fazla bilgi için bkz. [Azalan bakiyeli amortisman](reduce-balance-depreciation.md) ve [Sabit varlığı bölme](tasks/split-fixed-asset.md).

Sabit bir varlığı, varlığın elde edildiği dönemden sonraki mali dönemde bölerseniz, varlığın önceki yıl için net defter değeri (NDD) azalan bakiyeli amortisman ile hesaplanır. Ayrıca, varlığı bölecek hareketten oluşturulan alım ve amortisman düzeltme hareketlerini de hesaplar. Bu davranış, varlığın bir mali yılda edinildiği ve sonraki bir mali yılda bölündüğü varsayılır. Bölünmeden sonra özgün varlık için amorti edilmesi gereken tutar, varlık bölünmeden önce varlığın NDD'sini ve bölünme için deftere nakledilen alım ve amortisman düzeltme hareketini yansıtır.

Örneğin, aşağıdaki durumlar geçerli olacaktır:

- Mali dönem 30 Haziran ile 1 Temmuz arasındadır.
- Azalan bakiye oranı yüzde 18'dir ve bir varlık Haziran 2019'da 10.000 ABD doları alım fiyatına alınmıştır.
- İlk mali yılın amortismanı 18.000 ABD dolarına eşittir, aylık amortisman 150 ABD dolarına eşittir ve varlık Kasım 2019'a kadar 738,75 ABD doları tutarında amorti edilmiştir.
- Kasım 2019'da varlığın yüzde 80'i başka bir sabit varlığa bölünmüştür.

[![Bölmeden sonra azalan bakiyeli amortisman.](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Orijinal varlık için amortisman tutarı 1.822,25 ABD dolarıdır. Bu tutar, bölünme hareketi deftere nakledilmeden önceki NDD (9.111,25 ABD doları), artı bölünme hareketinin deftere nakli sırasında oluşan alım düzeltme (-8.000 ABD doları), artı bölünme hareketi sırasında oluşan amortisman düzeltme (711 ABD doları) sonucuna eşittir. Bu nedenle, ikinci yılın amortismanı (1.822,25 × yüzde 18) ÷ 12 = 27,33 ABD dolarıdır.

İlk yılda yeni sabit varlığın amortisman tutarı (8.000 × yüzde 18) ÷ 12 = 120 ABD dolarıdır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
