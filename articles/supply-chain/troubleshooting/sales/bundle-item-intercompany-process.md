---
title: Ürün demeti maddesi şirketlerarası bir işlemde desteklenmiyor
description: Ürün demeti maddesi satın almaya uygun değil. Satış siparişi, ürün demeti maddesinin kendisi yerine yalnızca ürün demeti maddesinin bileşenlerini satın alır.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477850"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Ürün demeti maddesi şirketlerarası bir işlemde desteklenmez

## <a name="symptoms"></a>Belirtiler

Ürün demeti öğesi satınalma siparişlerinde kullanılmaz; çünkü ürün demeti öğesi için satış siparişi satırlarını incelerseniz miktarın *0* (sıfır) olduğunu ve durumun *İptal edildi* olduğunu fark edeceksiniz.

## <a name="resolution"></a>Çözüm

Bu davranış tasarımdan kaynaklanır. Satış siparişi yalnızca paket satış öğesinin bileşenlerini satın alır. Paket satış öğesinin kendisini satın almaz. Bir ürün demeti satın almanız gerekiyorsa, bunu ürün demeti öğesi olarak işaretlemenizin gerekip gerekmediğini gözden geçirin; çünkü bu işlev gelir tanıma senaryoları için tasarlanmıştır. Paket satış öğeleri hakkında daha fazla bilgi için bkz. [Paket satış öğeleri](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
