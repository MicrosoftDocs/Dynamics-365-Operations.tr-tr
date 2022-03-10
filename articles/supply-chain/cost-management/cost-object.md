---
title: Maliyet nesneleri
description: Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d27e2dcfd8f70c8d4b0f2ae1254f3c4fce63bb4d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572181"
---
# <a name="cost-objects"></a>Maliyet nesneleri

[!include [banner](../includes/banner.md)]

Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.  

## <a name="cost-objects"></a>Maliyet nesneleri

**Maliyet nesneleri** sayfasında, bir ürüne kayıtlı tüm maliyet nesneleri listelenir. Maliyet nesneleri aşağıdaki kaynaklardan gelen verilerle tanımlanır:

-   Ürün
-   Ürün boyut grubu
-   Depolama boyutu grubu
-   İzleme boyut grubu

**Not:** Maliyet nesnesi, yalnızca **Doğrudan malzeme** türündeki bir maliyet öğesini temsil eder. Maliyet nesnesi ve stok nesnesi arasındaki fark, maliyet nesnesinin mali stok için seçilen stok boyutlarıyla tanımlanmasıdır. Diyelim ki bir madde aşağıdaki şekilde yapılandırılmış:

-   **Tesis:** Fiziksel stok = Evet, Mali stok = Evet
-   **Ambar:** Fiziksel stok = Evet, Mali stok = Hayır
-   **Toplu İş No:** Fiziksel stok = Evet, Mali stok = Hayır

Aşağıdaki tabloda maliyet nesnesinin ve stok nesnesinin ne oldukları gösterilmektedir.

| Nesne türü      | Madde kodu | Tesis | Ambar | Bordro Numarası |
|------------------|-------------|------|-----------|-----------|
| Maliyet nesnesi      | x           | x    |           |           |
| Stok nesnesi | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Maliyetlerin ve miktarların toplamı
-   **Değer** alanındaki değer, aşağıdaki değerlerin toplamıdır:
    -   Fiziksel maliyet tutarı
    -   Mali maliyet tutarı
    -   Ayarlamalar
-   **Miktar** alanındaki değer, aşağıdaki değerlerin toplamıdır:
    -   Alınan
    -   Düşülen
    -   Deftere nakledilen miktar
-   **Ortalama birim maliyeti** alanı, hesaplanan bir alandır. Değer, **Değer** değerinin **Miktar** değerine bölünmesiyle bulunur.

**Not:** **Fiziksel değeri dahil** et parametresinin, önceki hesaplamalar üzerinde etkisi yoktur.

## <a name="additional-resources"></a>Ek kaynaklar

[Ürün boyut grubu](/dynamicsax-2012/appuser-itpro/about-product-dimensions)

[Depolama boyutu grubu](/dynamicsax-2012//storage-dimension-groups-form)

[İzleme boyutu grubu](/dynamicsax-2012//tracking-dimension-groups-form)

[Yenilikler veya değişenler](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)

[Maliyet girişleri](cost-entries.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]