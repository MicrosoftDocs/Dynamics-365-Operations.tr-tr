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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58213d4d6e8c29ab6605eb7aa5c6cb9ca6ba4a10
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="create-production-orders"></a>Üretim emirleri oluşturma

[!include[banner](../includes/banner.md)]


Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur. Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir. Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir.

Bir üretim emri, üretim döngüsü aşamalarından geçer. Bir emir oluşturulduğunda, durumu **Oluşturulmuş** olarak atanır. Bir emir tamamlandığında, durumu **Sonlandırılmış** olarak atanır. Her aşamada bulunan bir parametre ayarı, kullanıcının tüm adımları yapılandırmasına izin verir. Bu ayar, tek bir kullanıcı veya tüm kullanıcılar için ayarlanabilir.

Üretim ürün reçetesi ve üretim rotası, üretim emrinin ana varlıklarıdır. Bunlar, üretilmek için seçilen öğeye ve miktarına dayalı olarak üretim emrine kopyalanırlar. Üretim emri başlamadan önce üretim ürün reçeteleri ve rotaları düzenlenebilir.

Üretim emri aşağıdaki senaryolarda oluşturulabilir:

-   Malzeme talebine göre ana planlama yürütme tarafından oluşturulur.
-   Bir satış siparişi satırından ya da üst düzey bir üretim emri oluşturulduğunda ve (pegged tedarik) tahmini doğrudan oluşturulabilir.
-   El ile oluşturulmuş.





