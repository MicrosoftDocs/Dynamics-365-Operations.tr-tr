---
title: "Ürünleri bir çeşit dışında satma ve iade etme"
description: "Dynamics 365 for Retail ile, ürünleri çeşitler dışında satabilir ve iade edebilirsiniz."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fd00da1242964dddda5c19d46e61da33997e6d02
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a>Ürünleri bir çeşit dışında satma ve iade etme
Tüm Perakendeciler için genel bir senaryo, mağazalarında belirli ürünleri bulundurmasalar bile (diğer bir deyişle, ürünler mağazadaki çeşitler arasında olmasa bile) kendi müşterilerine ürünleri satmak veya müşterilerden gelen iadeleri kabul etmektir.
Burada bazı tipik senaryolar vardır:

+ Bir perakendeci tüm ürünlerini belirli bir mağazada bulundurmaz. Kalan ürünler ambarda depolanır. Mağaza çalışanı depodaki ürünleri arayarak veya bunlara göz atarak müşteriye yardımcı olabilir, ürünleri sepete ekleyebilir ve depodan adrese teslim gibi bir teslimat yöntemi seçerek veya müşterinin ürünü geçerli mağazadan veya başka bir mağazadan çekmesini sağlayarak işlemi tamamlayabilir.
+ Perakendeci belirli ürünleri mağaza bulundurmaz veya ürünler müşterinin ziyaret ettiği mağazanın stoğunda bulunmayabilir ancak ürünler diğer mağazalarda olabilir. Mağaza çalışanı ürünleri diğer bir mağazada arayarak veya göz atarak müşterinin bunları sepete eklemesine ve bir teslimat yöntemi seçerek satınalma işlemini tamamlamaya yardımcı olabilir.
+ Perakendecinin belirli bir şehir veya bölgede birçok mağazası vardır ve müşteriyi iade edeceği ürünü satın aldığı mağazaya iade etmek konusunda zorlamak istemez. Bunun yerine, müşteri ürünleri herhangi bir mağazaya iade edebilir.


Bu ortak senaryolar Dynamics 365 for Retail kullanan perakendeciler için kullanılabilir. Retail ile şunları yapabilirsiniz:
+ Diğer mağazalarda ürünleri aramak veya diğer mağazalardaki ürünlere göz atmak.
+ Tüm serbest bırakılan ürünleri aramak veya göz atmak.
+ peşin alış veriş hareketleri veya müşteri siparişleri oluşturmak.
+ Müşteri siparişleri için teslim seçeneklerini belirlemek.
+ Ürünleri geçerli mağazadan veya başka mağazadan seçmek.
+ Geçerli mağazadaki veya başka mağazadaki siparişi iptal etmek.
+ Bir siparişi makbuzla veya makbuz olmadan geçerli mağazaya veya başka bir mağazaya iade etmek.

