---
title: Maliyet nesneleri
description: "Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8043c81057b5bb79f405642b199f80fc2fbcd8d4
ms.lasthandoff: 03/31/2017


---

# <a name="cost-objects"></a>Maliyet nesneleri

Bu makalede, maliyet nesneleri hakkında bilgiler verilmekte, maliyetlerin ve miktarların nasıl biriktirildiği açıklanmaktadır. Maliyet nesnesi, maliyetlerin ve miktarların toplandığı bir varlıktır. Maliyet nesnesi varlığı, bir ürün veya ürün çeşidi (stil, renk vb.) olabilir.  

<a name="cost-objects"></a>Maliyet nesneleri
------------

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

**Not:** ** fiziksel değeri dahil et ** parametre yukarıdaki hesaplamalar üzerinde hiçbir etkisi vardır.

<a name="see-also"></a>Ayrıca bkz.
--------

[Product dimension group](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Storage dimension group](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Tracking dimension group](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Yeni veya değiştirilmiş Microsoft Dynamics AX'te nedir](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Cost entries](cost-entries.md)


