---
title: "Amortisman yöntemleri"
description: "Bu makalede, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tarafından desteklenen amortisman dönüştürmelerine ve amortisman yöntemlerine bir genel bakış sunulmuştur."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 69e0decd3ffbdf1f64fa4fbfe070927990f880ad
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="depreciation-methods-and-conventions"></a>Amortisman yöntemleri

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tarafından desteklenen amortisman dönüştürmelerine ve amortisman yöntemlerine bir genel bakış sunulmuştur.

Çeşitli amortisman yöntemleri ve kuralları seçebilirsiniz. Yöntemlerin amacı, sabit kıymetin amorti edilebilir değerini mali dönemlerine tahsis etmektir. Sabit kıymetin amorti edilebilir değeri, varsa bir ıskarta değeri tarafından azaltılan alım fiyatıdır. 

Amortisman kurallarını kullanıyor ve bir kıymet için bazı amortismanları atlayan son amortisman geçerlilik tarihini değiştirirseniz, geçen yıl için amortisman beklenenden daha fazla veya daha az olabilir. Amortisman, son amortisman geçerlilik tarihinin değiştirilmesinden etkilenen amortisman dönemlerinin sayısı tarafından ayarlanır.

Örneğin, üç yıl üzerinden Yarı yıl amortisman kuralını kullanıyorsanız, amortisman normalde 3 1/2 yıl üzerinden olur. 3 1/2 yıllık süre içinde son amortisman geçerlilik tarihini değiştirirseniz, amortismanın son yılı etkilenen dönem sayısın ileri atar. Tarihi üç ay ileri atarsanız, son yılda dokuz ay değerinde amortisman olur, ancak normalde altı ay değerinde amortisman olmalıdır.

Aşağıdaki amortisman kurallarından birini seçebilirsiniz:


-   Yarıyıl
-   Tam ay
-   Üç aylık dönemin ortası
-   Ayın ortası (Ayın 1'i)
-   Ayın ortası (Ayın 15'i)
-   Yarı yıl (yılın başlangıcı)
-   Yarı yıl (sonraki yıl)

Aşağıdaki amortisman yöntemlerinden birini seçebilirsiniz.
-   Sabit servis ömrü
-   Azalan bakiye
-   El ile
-   Faktör
-   Tüketim
-   Sabit kalan ömür
-   %200 azalan bakiye
-   %175 azalan bakiye
-   %150 azalan bakiye
-   %125 azalan bakiye

 



<a name="see-also"></a>Ayrıca bkz.
--------

[Sabit kıymet amortismanı](fixed-asset-depreciation.md)

[Sabit servis ömrü amortismanı](Straight-line-service-life-depreciation.md)

[Azalan bakiyeli amortisman](reduce-balance-depreciation.md)

[El ile amortisman](manual-depreciation.md)

[Faktör amortisman](factor-depreciation.md)

[Tüketim esasına göre amortisman](consumption-depreciation.md)

[Sabit kalan ömür amortismanı](straight-line-life-remaining-depreciation.md)

[Yüzde 125 azalan bakiyeli amortisman](125-percent-reducing-balance-depreciation.md)

[Yüzde 150 azalan bakiyeli amortisman](150-percent-reducing-balance-depreciation.md)

[Yüzde 175 azalan bakiyeli amortisman](175-percent-reducing-balance-depreciation.md)

[%200 azalan bakiyeli amortisman](200-percent-reducing-balance-depreciation.md)




