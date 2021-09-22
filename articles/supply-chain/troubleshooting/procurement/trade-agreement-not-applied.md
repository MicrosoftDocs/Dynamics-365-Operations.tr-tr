---
title: Ticari sözleşme koşulları, içeri aktarılan sipariş satırlarına uygulanamıyor
description: Ticari sözleşme fiyatları ve iskontolar, veri yönetimi aracılığıyla içeri aktarılan satış veya satınalma siparişi satırlarına uygulanmıyor
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477876"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Ticari sözleşme koşulları, içeri aktarılan sipariş satırlarına uygulanamıyor

## <a name="symptoms"></a>Belirtiler

Satış veya satınalma siparişi için uygulanan ticari sözleşmeler veri yönetimi aracılığıyla içe aktarılan satırlara uygulanmaz. Ancak, aynı ticari sözleşmeler el ile oluşturulan satış veya satınalma siparişi satırlarına uygulanır.

## <a name="cause"></a>Nedeni

Veri yönetimi aracılığıyla içe aktarılan satınalma siparişi satırları zaten fiyat bilgilerini içeriyorsa, ticaret sözleşmesi bu satırlar için yeniden değerlendirilmeyecektir. Örneğin **Satır iskontosu yüzdesi** veya fiyat ve iskonto değerlerinin herhangi biri bir satırla ilgili olarak ayarlanmışsa, ticari sözleşmeler bu satır için aranmayacaktır.

## <a name="workaround"></a>Geçici çözüm

Bu beklenen bir davranıştır ve hem satış siparişleri hem de satınalma siparişleri için benzerdir.

Geçici çözüm olarak, herhangi bir fiyat bilgisi ayarlamadan satınalma siparişi satırlarını içe aktarın. Ticari sözleşmeler daha sonra uygulanır ve satınalma siparişi satırları tanımlanan ticari sözleşmelere göre güncelleştirilir.
