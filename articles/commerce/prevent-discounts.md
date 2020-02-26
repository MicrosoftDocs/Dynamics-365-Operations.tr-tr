---
title: Perakende ürünler için iskontoları engelleme seçenekleri
description: Satıcıların bazı ürünlerin ister bir promosyon isterse de POS'taki satış sırasında indirime girmesini engellemeleri için çeşitli sebepler olabilir.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 822bd39bca3a95f073bacea90a8ee58eada50ae2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024376"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Perakende ürünler için iskontoları engelleme seçenekleri

[!include [banner](includes/banner.md)]

Satıcıların bazı ürünlerin ister bir promosyon isterse de POS'taki satış sırasında indirime girmesini engellemeleri için çeşitli sebepler olabilir.

Yayımlanan ürünlerin **Commerce** sekmesinde bulunabilen aşağıdaki seçenekler, ürünün tüm veya el ile indirimlerini engellemek üzere yapılandırılabilir. Ayarlar ayrıca kategori hiyerarşisinden kategori düzeyinde de belirtilebilir.

- **Tüm indirimleri engelle** – Bu seçeneği, tüm indirimlerin bu ürüne uygulanmasını engellemek için seçin. Bu karıştırma ve eşleştirme, miktar ve eşik indirimleri dahil tüm promosyonları ve bir POS kullanıcısı tarafından uygulanan el ile satır ve hareket indirimlerini kapsar.
- **El ile indirimleri engelle** – Bu seçeneği yalnızca bir satış sırasında bir POS kullanıcısı tarafından uygulanan el ile satır ve hareket indirimlerini engellemek için kullanın. Bu seçeneğin işaretli olduğu ürünler, karıştır ve eşleştir ve miktar ve eşik indirimleri gibi promosyonlar için kullanılabilir olacaktır.

> [!NOTE]
> Bu ayarlar fiyat geçersiz kılma işlemini kısıtlamaz çünkü bu, taban fiyatı belirler ve bir indirim olarak görülmez.

[![İndirim alanlarını engelle](./media/prevent-discounts.png)](./media/prevent-discounts.png)
