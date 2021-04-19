---
title: Mağazanın ürün çeşidinden olmayan ürünleri satma ve iade etme
description: Dynamics 365 Commerce ile, çeşitler dışında ürünler satabilir ve iade alabilirsiniz.
author: pdp1207
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b6bae9f0d3a236c69ee3ee47226c19c1e1dcaf42
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794055"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Mağazanın ürün çeşidinden olmayan ürünleri satma ve iade etme

[!include [banner](includes/banner.md)]

Tüm Perakendeciler için genel bir senaryo, mağazalarında belirli ürünleri bulundurmasalar bile (diğer bir deyişle, ürünler mağazadaki çeşitler arasında olmasa bile) kendi müşterilerine ürünleri satmak veya müşterilerden gelen iadeleri kabul etmektir.

Burada bazı tipik senaryolar vardır:

+ Bir perakendeci tüm ürünlerini belirli bir mağazada bulundurmaz. Kalan ürünler ambarda depolanır. Mağaza çalışanı depodaki ürünleri arayarak veya bunlara göz atarak müşteriye yardımcı olabilir, ürünleri sepete ekleyebilir ve depodan adrese teslim gibi bir teslimat yöntemi seçerek veya müşterinin ürünü geçerli mağazadan veya başka bir mağazadan çekmesini sağlayarak işlemi tamamlayabilir.
+ Perakendeci belirli ürünleri mağaza bulundurmaz veya ürünler müşterinin ziyaret ettiği mağazanın stoğunda bulunmayabilir ancak ürünler diğer mağazalarda olabilir. Mağaza çalışanı ürünleri diğer bir mağazada arayarak veya göz atarak müşterinin bunları sepete eklemesine ve bir teslimat yöntemi seçerek satınalma işlemini tamamlamaya yardımcı olabilir.
+ Perakendecinin belirli bir şehir veya bölgede birçok mağazası vardır ve müşteriyi iade edeceği ürünü satın aldığı mağazaya iade etmek konusunda zorlamak istemez. Bunun yerine, müşteri ürünleri herhangi bir mağazaya iade edebilir.

Bu ortak senaryolar Commerce kullanan perakendeciler için kullanılabilir. Commerce ile şunları yapabilirsiniz:

+ Diğer mağazalarda ürünleri aramak veya diğer mağazalardaki ürünlere göz atmak.
+ Tüm serbest bırakılan ürünleri aramak veya göz atmak.
+ peşin alış veriş hareketleri veya müşteri siparişleri oluşturmak.
+ Müşteri siparişleri için teslim seçeneklerini belirlemek.
+ Ürünleri geçerli mağazadan veya başka mağazadan seçmek.
+ Geçerli mağazadaki veya başka mağazadaki siparişi iptal etmek.
+ Bir siparişi makbuzla veya makbuz olmadan geçerli mağazaya veya başka bir mağazaya iade etmek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]