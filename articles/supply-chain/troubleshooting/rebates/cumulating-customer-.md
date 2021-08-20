---
title: Madde indirim grupları kullanıldığında müşteri indirimlerinin toplamı başarısız olur
description: Madde indirim gruplarıyla birlikte müşteri indirim anlaşmaları kullandığınızda indirimler hesaplanır ancak toplama başarısız olur.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760382"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Madde indirim grupları kullanıldığında müşteri indirimlerinin toplamı başarısız olur

KB numarası: 4611372

## <a name="symptoms"></a>Belirtiler

Madde indirim gruplarıyla birlikte müşteri indirim anlaşmaları (*tutar* türünden) kullandığınızda indirimler hesaplanır ancak toplama başarısız olur.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Madde grupları, yalnızca eşik koşulu aynı olan maddeleri gruplandırır. İndirim koşulu (eşik), madde grubundaki her bir maddenin tutarı için belirlenir, madde grubundaki tüm maddelerin toplam tutarı için değil.
