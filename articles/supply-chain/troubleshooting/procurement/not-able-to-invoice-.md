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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756763"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Müşteriyle tarafındaki bir satış siparişini faturalayamazsınız

KB numarası: 4611793

## <a name="symptoms"></a>Belirtiler

Bir satıcı için **Şirketlerarası** sayfasında **Faturayı otomatik olarak deftere naklet** seçeneğini etkinleştirdikten sonra, orijinal satış siparişini ve başlangıçtaki doğrudan teslim alma siparişini faturalayamazsınız.

## <a name="resolution"></a>Çözünürlük

Şirketlerarası ve doğrudan teslimat siparişi faturalarının eşitleme davranışı, [Şirketlerarası siparişi deftere nakletmek için parametreleri ayarlama](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order) bölümünde açıklanan parametreler tarafından kontrol edilir ve zorlanır.

Bu parametreleri ayarladıktan sonra, öncelikle şirketlerarası satış siparişini faturalamalısınız. Ardından orijinal satış siparişleri ve satınalma siparişleri eşitlenir.
