---
title: "Üretim emri maliyet tahmini"
description: "Bu makalede, üretim maliyet tahmini hakkında bilgiler verilmektedir. Üretim maliyeti tahmini, bir maddeyi planlanan üretim emri miktarında üretmek için gereken tahmini malzeme ve kapasite tüketim maliyetlerini sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9ae0bbb641d7517d33ad087faec231cb0bda3f78
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017

---

# <a name="production-order-cost-estimation"></a>Üretim emri maliyet tahmini

[!include[banner](../includes/banner.md)]


Bu makalede, üretim maliyet tahmini hakkında bilgiler verilmektedir. Üretim maliyeti tahmini, bir maddeyi planlanan üretim emri miktarında üretmek için gereken tahmini malzeme ve kapasite tüketim maliyetlerini sağlar. 

Bir üretim emri oluşturduktan sonra üretim maliyetlerini tahmin etmeniz gerekir. Bu tahminler sonraki planlama ve üretim süreçlerinde baz olarak kullanıldığı için, amaç, üretim süreci için madde ve rota tüketimini tahmin etmektir.

## <a name="production-cost-estimation"></a>Üretim maliyet tahmini
Üretim maliyeti tahminlerinde aşağıdaki bilgiler temel alınır:

-   Üretim emrindeki miktar
-   Üretim ürün reçetelerindeki (BOM) bileşenler
-   Üretim rotasındaki rota operasyonları
-   Bileşenlere ve işlemlere uygulanan dolaylı maliyetler
-   Hesaplama tarihi itibarıyla etkin maliyet verileri

Üretim ürün reçetelerinde bir hayali satır maddesi varsa, hesaplamalar hayali maddenin bileşenlerini ve rota operasyonlarını yansıtır. Tahmini maliyetleri, güncelleştirilen bilgileri yansıtacak şekilde yeniden hesaplamak için Tahmin görevini kullanabilirsiniz. Güncelleştirilen bilgiler, örneğin, üretim emri miktarı, üretim ürün reçetelerindeki bileşenler ve üretim rotasındaki rota operasyonları, bu bileşen ve faaliyetler için geçerli dolaylı maliyetler veya yeniden hesaplama tarihindeki etkin maliyet verilerindeki değişiklikler olabilir. Tahmini maliyet hesaplamaları, üretim maddesi için maliyet-artı-kar marjı yaklaşımına dayanan bir satış fiyatı önerir. Tahmini maliyet hesaplamaları, isteğe bağlı olarak üretim emrine bağlı diğer üretim emirlerini yansıtan referans siparişlerine uygulanabilir.

## <a name="view-the-estimated-costs"></a>Tahmin maliyetleri görüntüleyin
Tahmini çalıştırdıktan sonra sonuçları **Fiyat hesaplaması** sayfasında görüntüleyebilirsiniz. Tahmin, aşağıdaki değerleri hesaplar:

-   **Üretim maliyeti** – Üretim maliyeti, tahminin üst satırıdır. Üretim emrini çalıştırmanın toplam maliyetini ve üretim için toplam satış fiyatını gösterir. Tahmindeki tüm maliyet satırlarının toplamıdır.
-   **Rota veya kaynak maliyetleri** – Rota veya kaynak maliyetleri, üretim operasyonlarının maliyetleridir. Bunlar, kurulum süresi, çalıştırma süresi ve genel gider gibi öğelerin maliyetlerini içerir.
-   **Malzeme maliyetleri** – Maddeyi üretmek için gereken ürün reçetesi bileşenlerinin maliyetleri ve fiyatlarıdır. Bu maliyetler önceden belirlenmiş ve sisteme girilmiştir.

## <a name="other-uses-of-cost-estimation"></a>Maliyet tahmininin diğer kullanımları
Maliyet tahmini, aşağıdaki bilgileri de sağlar:

-   Anlamlı fiyat teklifleri
-   Emrin karlılık tahminleri
-   Hammadde kullanım tahminleri
-   Önceki üretimlerin maliyet bilgilerinin karşılaştırılması
-   Bütçe ve tahmin bilgileri
-   Belirli bir maliyeti korumak için gereken üretim boyutu tahminleri





