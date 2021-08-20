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
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723467"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Bir fiili ağırlık miktarı bölündüğünde, nominal miktar yerine minimum miktar kullanılıyor

KB numarası: 4612073

## <a name="symptoms"></a>Belirtiler

Fiili ağırlık miktarı toplu işlemlere bölündüğünde, **Malzeme çekme miktarı** alanı, nominal miktarı değil madde için ayarlanan minimum miktarı kullanıyor.

## <a name="resolution"></a>Çözünürlük

Sistem, beklendiği şekilde davranıyordur. Sistem, her maddenin malzeme çekme için minimum miktar ayarını kullanır.
