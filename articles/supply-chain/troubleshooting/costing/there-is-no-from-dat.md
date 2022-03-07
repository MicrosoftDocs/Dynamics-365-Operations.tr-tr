---
title: Madde fiyatı sayfasının Etkin fiyatlar sekmesinde Başlangıç tarihi değeri yok
description: Madde fiyatı sayfasının Etkin fiyatlar sekmesinde Başlangıç tarihi değeri yok.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026998"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Madde fiyatı sayfasının Etkin fiyatlar sekmesinde Başlangıç tarihi değeri yok

KB numarası: 4613548

## <a name="symptoms"></a>Belirtiler

**Madde fiyatı** sayfasının **Etkin fiyatlar** sekmesinde **Başlangıç tarihi** değeri yok.

## <a name="resolution"></a>Çözünürlük

Bekleyen fiyata ayarlanan **Başlangıç tarihi** değeri (geçerlilik tarihi) etkin fiyata transfer edilmedi.

Bir madde maliyeti kaydı ilk olarak girildiğinde *Bekleyen* durumunda olur ve amaçlanan yürürlük tarihi vardır. Madde maliyeti kaydını etkinleştirdiğinizde, durumu *Etkin* olarak güncellenir ve yürürlük tarihini etkinleştirme tarihine güncelleştirilir. Bu nedenle, etkin fiyatın etkinleştirme tarihi her zaman etkinleştirmenin gerçek tarihidir.

Daha fazla bilgi için bkz. [Maliyetlendirme sürümlerine genel bakış](../../cost-management/costing-versions.md).
