---
title: Amortisman yöntemleri
description: Bu makalede, Microsoft Dynamics 365 Finance tarafından desteklenen amortisman kurallarına ve amortisman yöntemlerine bir genel bakış sunulmuştur.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6abf98b4c1eee3657960a1912445171acc0686a
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674538"
---
# <a name="depreciation-methods-and-conventions"></a>Amortisman yöntemleri ve kuralları

[!include [banner](../includes/banner.md)]

Bu makalede, desteklenen amortisman kurallarına ve amortisman yöntemlerine bir genel bakış sunulmuştur.

Çeşitli amortisman yöntemleri ve kuralları seçebilirsiniz. Yöntemlerin amacı, sabit kıymetin amorti edilebilir değerini mali dönemlerine tahsis etmektir. Sabit kıymetin amorti edilebilir değeri, varsa bir ıskarta değeri tarafından azaltılan alım fiyatıdır. 

Amortisman kurallarını kullanıyor ve bir kıymet için bazı amortismanları atlayan son amortisman geçerlilik tarihini değiştirirseniz, geçen yıl için amortisman beklenenden daha fazla veya daha az olabilir. Amortisman, son amortisman geçerlilik tarihinin değiştirilmesinden etkilenen amortisman dönemlerinin sayısı tarafından ayarlanır.

Örneğin, üç yıl üzerinden Yarı yıl amortisman kuralını kullanıyorsanız, amortisman normalde üç buçuk yıl üzerinden olur. Üç buçuk yıllık süre içinde son amortisman geçerlilik tarihini değiştirirseniz, amortismanın son yılı etkilenen dönem sayısın ileri atar. Tarihi üç ay ileri atarsanız, son yılda dokuz ay değerinde amortisman olur, ancak normalde altı ay değerinde amortisman olmalıdır.

Aşağıdaki amortisman kurallarından birini seçebilirsiniz:


-   Yarıyıl
-   Tam ay
-   Üç aylık dönemin ortası
-   Ayın ortası (Ayın 1'i)
-   Ayın ortası (Ayın 15'i)
-   Yarı yıl (yılın başlangıcı)
-   Yarı yıl (sonraki yıl)

Aşağıdaki amortisman yöntemlerinden birini seçebilirsiniz.
-   Straight0-line servis ömrü
-   Azalan bakiye
-   El ile
-   Faktör
-   Tüketim
-   Sabit kalan ömür
-   %200 azalan bakiye
-   %175 azalan bakiye
-   %150 azalan bakiye
-   %125 azalan bakiye





## <a name="additional-resources"></a>Ek kaynaklar

[Sabit kıymet amortismanı](fixed-asset-depreciation.md)

[Sabit servis ömrü amortismanı](Straight-line-service-life-depreciation.md)

[Azalan bakiyeli amortisman](reduce-balance-depreciation.md)

[El ile amortisman](manual-depreciation.md)

[Faktör amortisman](factor-depreciation.md)

[Tüketime göre amortisman](consumption-depreciation.md)

[Sabit kalan ömür amortismanı](straight-line-life-remaining-depreciation.md)

[Yüzde 125 azalan bakiyeli amortisman](125-percent-reducing-balance-depreciation.md)

[Yüzde 150 azalan bakiyeli amortisman](150-percent-reducing-balance-depreciation.md)

[Yüzde 175 azalan bakiyeli amortisman](175-percent-reducing-balance-depreciation.md)

[Yüzde 200 azalan bakiyeli amortisman](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
