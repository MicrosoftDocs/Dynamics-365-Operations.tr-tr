---
title: Mağazanın ürün çeşidinden olmayan ürünleri satma ve iade etme
description: Dynamics 365 Retail ile, çeşitler dışında ürünler satabilir ve iade alabilirsiniz.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ae6bac983ddb4d4a217fe83c8f68c5a87ccd6a47
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024965"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Mağazanın ürün çeşidinden olmayan ürünleri satma ve iade etme

[!include [banner](includes/banner.md)]

Tüm Perakendeciler için genel bir senaryo, mağazalarında belirli ürünleri bulundurmasalar bile (diğer bir deyişle, ürünler mağazadaki çeşitler arasında olmasa bile) kendi müşterilerine ürünleri satmak veya müşterilerden gelen iadeleri kabul etmektir.

Burada bazı tipik senaryolar vardır:

+ Bir perakendeci tüm ürünlerini belirli bir mağazada bulundurmaz. Kalan ürünler ambarda depolanır. Mağaza çalışanı depodaki ürünleri arayarak veya bunlara göz atarak müşteriye yardımcı olabilir, ürünleri sepete ekleyebilir ve depodan adrese teslim gibi bir teslimat yöntemi seçerek veya müşterinin ürünü geçerli mağazadan veya başka bir mağazadan çekmesini sağlayarak işlemi tamamlayabilir.
+ Perakendeci belirli ürünleri mağaza bulundurmaz veya ürünler müşterinin ziyaret ettiği mağazanın stoğunda bulunmayabilir ancak ürünler diğer mağazalarda olabilir. Mağaza çalışanı ürünleri diğer bir mağazada arayarak veya göz atarak müşterinin bunları sepete eklemesine ve bir teslimat yöntemi seçerek satınalma işlemini tamamlamaya yardımcı olabilir.
+ Perakendecinin belirli bir şehir veya bölgede birçok mağazası vardır ve müşteriyi iade edeceği ürünü satın aldığı mağazaya iade etmek konusunda zorlamak istemez. Bunun yerine, müşteri ürünleri herhangi bir mağazaya iade edebilir.

Bu ortak senaryolar Retail kullanan perakendeciler için kullanılabilir. Retail ile şunları yapabilirsiniz:

+ Diğer mağazalarda ürünleri aramak veya diğer mağazalardaki ürünlere göz atmak.
+ Tüm serbest bırakılan ürünleri aramak veya göz atmak.
+ peşin alış veriş hareketleri veya müşteri siparişleri oluşturmak.
+ Müşteri siparişleri için teslim seçeneklerini belirlemek.
+ Ürünleri geçerli mağazadan veya başka mağazadan seçmek.
+ Geçerli mağazadaki veya başka mağazadaki siparişi iptal etmek.
+ Bir siparişi makbuzla veya makbuz olmadan geçerli mağazaya veya başka bir mağazaya iade etmek.
