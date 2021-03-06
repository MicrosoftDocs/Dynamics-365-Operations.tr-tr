---
title: Üretim emri yaşam döngüsüne genel bakış
description: Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur. Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir. Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df773cf13b8ccd9ee4f861955b1a4321af38a150
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811810"
---
# <a name="production-order-lifecycle-overview"></a>Üretim emri yaşam döngüsüne genel bakış

[!include [banner](../includes/banner.md)]

Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur. Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir. Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir.

Bir üretim emri, üretim döngüsü aşamalarından geçer. Bir emir oluşturulduğunda, durumu **Oluşturulmuş** olarak atanır. Bir emir tamamlandığında, durumu **Sonlandırılmış** olarak atanır. Her aşamada bulunan bir parametre ayarı, kullanıcının tüm adımları yapılandırmasına izin verir. Bu ayar, tek bir kullanıcı veya tüm kullanıcılar için ayarlanabilir.

Üretim ürün reçetesi ve üretim rotası, üretim emrinin ana varlıklarıdır. Bunlar, üretilmek için seçilen öğeye ve miktarına dayalı olarak üretim emrine kopyalanırlar. Üretim emri başlamadan önce üretim ürün reçeteleri ve rotaları düzenlenebilir.

Üretim emri aşağıdaki senaryolarda oluşturulabilir:

-   Malzeme talebine göre ana planlama yürütme tarafından oluşturulur.
-   Bir satış siparişi satırından ya da üst düzey bir üretim emri oluşturulduğunda ve (pegged tedarik) tahmini doğrudan oluşturulabilir.
-   El ile oluşturulmuş.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]