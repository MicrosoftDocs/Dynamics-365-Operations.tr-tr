---
title: "Üretim emirleri oluşturma"
description: "Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur. Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir. Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d962dbf5a5a4e3847252171d3631f78341640bc7
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="create-production-orders"></a>Üretim emirleri oluşturma

[!include [banner](../includes/banner.md)]

Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur. Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir. Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir.

Bir üretim emri, üretim döngüsü aşamalarından geçer. Bir emir oluşturulduğunda, durumu **Oluşturulmuş** olarak atanır. Bir emir tamamlandığında, durumu **Sonlandırılmış** olarak atanır. Her aşamada bulunan bir parametre ayarı, kullanıcının tüm adımları yapılandırmasına izin verir. Bu ayar, tek bir kullanıcı veya tüm kullanıcılar için ayarlanabilir.

Üretim ürün reçetesi ve üretim rotası, üretim emrinin ana varlıklarıdır. Bunlar, üretilmek için seçilen öğeye ve miktarına dayalı olarak üretim emrine kopyalanırlar. Üretim emri başlamadan önce üretim ürün reçeteleri ve rotaları düzenlenebilir.

Üretim emri aşağıdaki senaryolarda oluşturulabilir:

-   Malzeme talebine göre ana planlama yürütme tarafından oluşturulur.
-   Bir satış siparişi satırından ya da üst düzey bir üretim emri oluşturulduğunda ve (pegged tedarik) tahmini doğrudan oluşturulabilir.
-   El ile oluşturulmuş.





