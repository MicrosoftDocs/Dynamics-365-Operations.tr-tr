---
title: Bir fiili ağırlık miktarı bölündüğünde, nominal miktar yerine minimum miktar kullanılıyor
description: Fiili ağırlık miktarı toplu işlemlere bölündüğünde, Malzeme çekme miktarı alanı, nominal miktarı değil madde için ayarlanan minimum miktarı kullanıyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026992"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Bir fiili ağırlık miktarı bölündüğünde, nominal miktar yerine minimum miktar kullanılıyor

KB numarası: 4612073

## <a name="symptoms"></a>Belirtiler

Fiili ağırlık miktarı toplu işlemlere bölündüğünde, **Malzeme çekme miktarı** alanı, nominal miktarı değil madde için ayarlanan minimum miktarı kullanıyor.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Sistem, her maddenin malzeme çekme için minimum miktar ayarını kullanır.
