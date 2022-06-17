---
title: Birden çok müşteri siparişi ve fatura arasında iade kalemleri
description: Bu makalede, Dynamics 365 Commerce'te birden çok müşteri siparişi ve faturası arasında iadeleri etkinleştirme işlevi açıklanmaktadır.
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
ms.openlocfilehash: 65ef700db5a81c49a962fd388af54e7811c088d2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890335"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Birden çok müşteri siparişi ve fatura arasında iade kalemleri

[!include [banner](includes/banner.md)]


İadeler, birden fazla sipariş ve fatura arasında yapılabilir. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Birden fazla müşteri siparişi ve faturası arasındaki iadeleri desteklemek için Commerce'i yapılandırma

1. **Commerce parametreleri \> Müşteri siparişleri**'ne gidin.
1. **Birden fazla sipariş için iadeleri etkinleştirme** parametresini açın. 

## <a name="process-returns"></a>İadeleri işleme

Parametre açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.

Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir. Daha sonra kasiyer, iade edilecek ürünleri seçebilir. Seçilen tüm ürünler için tek bir iade emri oluşturulur.
