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
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796909"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Birden fazla müşteri siparişi ve faturasındaki maddeleri iade etme

[!include [banner](includes/banner.md)]


Bu makalede, müşteri siparişi iadelerini birden fazla fatura üzerinden en iyi duruma getiren iki özellik açıklanmaktadır. 

## <a name="enable-refunds-over-multiple-captures"></a>Birden fazla yakalama üzerinden geri ödemeleri etkinleştir

Bu özellik aynı müşteri siparişine karşı çoklu bağlantılı geri ödemeleri etkinleştirir. 

1. **Özellik yönetimi** çalışma alanına gidin ve **Çoklu yakalamalar üzerinde geri ödemeleri etkinleştir**'i arayın.
2. **Çoklu siparişler üzerinde geri ödemeleri etkinleştir**'i seçin ve **Etkinleştir**'e tıklayın. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Kısmi miktarlı iadeler için doğru vergi hesaplamasını etkinleştirme

Bu özellik, bir sipariş birden çok fatura kullanılarak iade edildiğinde, vergilerin sonunda uygulanan vergi tutarına eşit olmasını sağlar. 

1. **Özellik yönetimi** çalışma alanına gidin ve **Kısmi miktarlı iadeler için uygun vergi hesaplamasını etkinleştir**'i arayın.
2. **Kısmi miktarlı iadelerle ilgili doğru vergi hesaplamasını etkinleştir**'ı seçin ve ardından **Etkinleştir**'e tıklayın. 


## <a name="process-returns"></a>İadeleri işleme

Bu özellikler açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.

Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir. Daha sonra kasiyer, iade edilecek ürünleri seçebilir. Seçilen tüm ürünler için tek bir iade emri oluşturulur.

Sipariş tam olarak iade edilirse müşteriye iade edilen vergilerin tutarı başlangıçta uygulanan vergi tutarına eşit olur.



[!INCLUDE[footer-include](../includes/footer-banner.md)]