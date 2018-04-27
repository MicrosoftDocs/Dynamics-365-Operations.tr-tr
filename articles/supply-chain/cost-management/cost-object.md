---
title: Maliyet nesneleri
description: "Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1a1c964a890c0c59a01700a6987bfbdfe5a17ccb
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="cost-objects"></a>Maliyet nesneleri

[!INCLUDE [banner](../includes/banner.md)]

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

**Not:** **Fiziksel değeri dahil ** et parametresinin, önceki hesaplamalar üzerinde etkisi yoktur.

<a name="see-also"></a>Ayrıca bkz.
--------

[Ürün boyut grubu](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Depolama boyutu grubu](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[İzleme boyutu grubu](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Yenilikler veya değişenler](../../fin-and-ops/get-started/whats-new-changed.md)

[Maliyet girişleri](cost-entries.md)




