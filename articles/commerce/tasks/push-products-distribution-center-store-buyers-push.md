---
title: " Merkezi alım kullanarak ürünleri dağıtım merkezinden mağazaya gönderme"
description: Bu yordam, ürünleri bir konumundan bir veya daha fazla mağazaya dağıtmak için Merkezi Alım oluşturma ve işleme konusunda kılavuzluk sağlar.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3720945823cf127f776a9ea6a6ad75a72ceec00c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012353"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a> Merkezi alım kullanarak ürünleri dağıtım merkezinden mağazaya gönderme

[!include [banner](../includes/banner.md)]

Bu yordam, ürünleri bir konumundan bir veya daha fazla mağazaya dağıtmak için Merkezi Alım oluşturma ve işleme konusunda kılavuzluk sağlar. Kullanıcı birden çok yapılandırmalar tanımlayabilir ve ürünlerin nasıl dağıtılacağını sistemin önermesini isteyebilir ya da ürünlerin nereye dağıtılacağını ve her mağazaya ne kadar dağıtım yapılacağını el ile girebilir. Bu yordam Merkezi Alımda kullanılabilecek stok yenileme kuralları, kuruluş hiyerarşileri ve mağaza ağırlıkları gibi verilerin ayarlanmasını kapsamaz. Bu yordam, USRT demo şirketini kullanır.

1. Merkezi alım'a gidin.
2. Yeni'ye tıklayın.
3. Açıklama alanına bir değer girin.
4. Tesis alanına bir değer girin veya buradan bir değer seçin.
5. Ambar alanında, eldeki miktarları içeren ürünlerin bulunduğu bir mağaza girin veya seçin.
6. Ekle öğesini tıklatın.
7. Listede, seçili satırı işaretleyin.
8. Madde numarası alanına bir ürün girin veya bir ürün seçin.
9. Ekle öğesini tıklatın.
10. Listede, seçili satırı işaretleyin.
11. Madde numarası alanına bir varyant ürün girin veya seçin.
    * Bir varyant ürün girerken, her varyant için satırlar oluşturulur.  
12. Listede, bir satırı işaretleyin.
13. Verilen miktar alanına, seçilen ürün için dağıtmak istediğiniz miktarı girin.
14. Verilecek ek miktar alanına, dağıtmak için kullanılabilir miktarı bulunan ürünlerin miktarını girin.
15. Dağıtım alanına 'Yerleşim ağırlığı' girin.
    * Dağıtım için diğer kuralları kullanmak üzere diğer türleri seçebilirsiniz.  
16. Atok yenileme hiyerarşisi alanında bir değer seçin.
17. Ürün çeşitlerini dikkate al alanında Evet'i seçin.
18. Miktarları hesapla'yı tıklayın ve Ambar bölümündeki satırlara eklenen miktarları gözden geçirin.
19. Sipariş oluştur'u tıklayın.
20. Evet'i tıklatın.

