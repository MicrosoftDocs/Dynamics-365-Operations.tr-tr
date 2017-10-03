---
title: "Perakende ürünler için indirimleri engelle"
description: "Satıcıların bazı ürünlerin ister bir promosyon isterse de POS'taki satış sırasında indirime girmesini engellemeleri için çeşitli sebepler olabilir."
author: jeffbl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c124ecf104bdb3de786c9dd98c2b07a4c9c04041
ms.openlocfilehash: 0debfe984a83295dde145fe4b8c2deb836345cd6
ms.contentlocale: tr-tr
ms.lasthandoff: 07/31/2017

---

# <a name="prevent-discounts-for-retail-products"></a>Perakende ürünler için indirimleri engelle

[!include[banner](includes/banner.md)]

Satıcıların bazı ürünlerin ister bir promosyon isterse de POS'taki satış sırasında indirime girmesini engellemeleri için çeşitli sebepler olabilir.

Yayımlanan ürünlerin **Perakende** sekmesinde bulunabilen aşağıdaki seçenekler, ürünün tüm veya el ile indirimlerini engellemek üzere yapılandırılabilir. Ayarlar ayrıca kategori hiyerarşisinden kategori düzeyinde de belirtilebilir.

**Tüm indirimleri engelle**: Bu seçeneği, tüm indirimlerin bu ürüne uygulanmasını engellemek için seçin. Bu karıştırma ve eşleştirme, miktar ve eşik indirimleri dahil tüm promosyonları ve bir POS kullanıcısı tarafından uygulanan el ile satır ve hareket indirimlerini kapsar.

**El ile indirimleri engelle**: Bu seçeneği yalnızca bir satış sırasında bir POS kullanıcısı tarafından uygulanan el ile satır ve hareket indirimlerini engellemek için kullanın. Bu seçeneğin işaretli olduğu ürünler, karıştır ve eşleştir ve miktar ve eşik indirimleri gibi promosyonlar için kullanılabilir olacaktır.

**Not**: Bu ayarlar fiyat geçersiz kılma işlemini kısıtlamaz çünkü bu, taban fiyatı belirler ve bir indirim olarak görülmez.  

![indirim alanlarını engelle](/media/prevent-discounts.png)

