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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026973"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Madde indirim grupları kullanıldığında müşteri indirimlerinin toplamı başarısız olur

KB numarası: 4611372

## <a name="symptoms"></a>Belirtiler

Madde indirim gruplarıyla birlikte müşteri indirim anlaşmaları (*tutar* türünden) kullandığınızda indirimler hesaplanır ancak toplama başarısız olur.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Madde grupları, yalnızca eşik koşulu aynı olan maddeleri gruplandırır. İndirim koşulu (eşik), madde grubundaki her bir maddenin tutarı için belirlenir, madde grubundaki tüm maddelerin toplam tutarı için değil.
