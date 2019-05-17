---
title: Birden fazla müşteri siparişi ve faturası arasında iade kalemleri
description: Bu konuda Microsoft Dynamics 365 for Retail'daki birden fazla müşteri siparişi ve faturası arasında iadeleri etkinleştirme işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517190"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Birden fazla müşteri siparişi ve faturası arasında iade kalemleri

[!include [banner](includes/banner.md)]


Dynamics 365 for Finance and Operations sürüm 10.0'da birden fazla sipariş ve fatura arasında iade yapılabilir ancak 10.0'dan önceki sürümlerde iadeler, yalnızca tek seferde tek bir fatura ile işlenebilmektedir. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Birden fazla müşteri siparişi ve faturası arasındaki iadeleri desteklemek için Retail'ı yapılandırma

1. **Retail parametreleri \> Müşteri siparişleri**'ne gidin.
1. **Birden fazla sipariş için iadeleri etkinleştirme** parametresini açın. 

## <a name="process-returns"></a>İadeleri işleme

Parametre açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.

Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir. Daha sonra kasiyer, iade edilecek ürünleri seçebilir. Seçilen tüm ürünler için tek bir iade emri oluşturulur.
