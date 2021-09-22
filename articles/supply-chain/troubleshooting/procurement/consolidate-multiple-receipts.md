---
title: Çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremezsiniz
description: Farklı ürün giriş satırları farklı muhasebe tarihlerine sahipse, çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremezsiniz.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 485306279281ceb55a140526f4216af35574af42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477817"
---
# <a name="you-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremezsiniz

## <a name="symptoms"></a>Belirtiler

Farklı ürün giriş satırları farklı muhasebe tarihlerine sahipse, çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremezsiniz.

## <a name="resolution"></a>Çözüm

Dynamics 365 Supply Chain Management uygulamasının önceki sürümlerinde, bu durumda birleştirmeye izin veriliyordu. Ancak, uygulama hataya açıktır. Oluşturulan satınalma siparişi satırlarındaki hesap tarihi, bu satınalma siparişi satırlarının oluşturulduğu ürün giriş satırlarındaki hesap tarihinden farklı olmamalıdır. (Satınalma siparişi satırlarındaki muhasebe tarihi, satınalma siparişi başlığındaki hesap tarihiyle eşleşir.) Bu nedenle, çoklu ürün girişinin tek bir satınalma siparişinde birleştirilmesine artık izin verilmez.

Muhasebe tarihi, örneğin bütçe rezervasyonları ve tutarlılık için kullanılır. Bu nedenle, ürün girişinden satınalma siparişine geçiş sırasında tutulmalıdır.
