---
title: Müşteriyle tarafındaki bir satış siparişini faturalayamazsınız
description: Faturayı otomatik olarak deftere naklet seçeneğini etkinleştirdikten sonra, orijinal satış siparişini ve başlangıçtaki doğrudan teslim alma siparişini faturalayamazsınız.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026979"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Müşteriyle tarafındaki bir satış siparişini faturalayamazsınız

KB numarası: 4611793

## <a name="symptoms"></a>Belirtiler

Bir satıcı için **Şirketlerarası** sayfasında **Faturayı otomatik olarak deftere naklet** seçeneğini etkinleştirdikten sonra, orijinal satış siparişini ve başlangıçtaki doğrudan teslim alma siparişini faturalayamazsınız.

## <a name="resolution"></a>Çözünürlük

Şirketlerarası ve doğrudan teslimat siparişi faturalarının eşitleme davranışı, [Şirketlerarası siparişi deftere nakletmek için parametreleri ayarlama](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) bölümünde açıklanan parametreler tarafından kontrol edilir ve zorlanır.

Bu parametreleri ayarladıktan sonra, öncelikle şirketlerarası satış siparişini faturalamalısınız. Ardından orijinal satış siparişleri ve satınalma siparişleri eşitlenir.
