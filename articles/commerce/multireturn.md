---
title: Birden fazla müşteri siparişi ve faturasındaki maddeleri iade etme
description: Bu konuda, Dynamics 365 Commerce'teki birden fazla müşteri siparişi ve faturası arasında iadeleri etkinleştirme işlevi açıklanmaktadır.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 410a78dca29f1d723a5b5ef43836d07ec5502a567ec81098241fafeb6354373b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770993"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Birden fazla müşteri siparişi ve faturası arasında iade kalemleri

[!include [banner](includes/banner.md)]


İadeler, birden fazla sipariş ve fatura arasında yapılabilir. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Birden fazla müşteri siparişi ve faturası arasındaki iadeleri desteklemek için Commerce'i yapılandırma

1. **Commerce parametreleri \> Müşteri siparişleri**'ne gidin.
1. **Birden fazla sipariş için iadeleri etkinleştirme** parametresini açın. 

## <a name="process-returns"></a>İadeleri işleme

Parametre açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.

Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir. Daha sonra kasiyer, iade edilecek ürünleri seçebilir. Seçilen tüm ürünler için tek bir iade emri oluşturulur.
