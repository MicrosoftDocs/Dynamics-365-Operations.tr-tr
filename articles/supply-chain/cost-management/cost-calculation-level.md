---
title: Maliyet hesaplama düzeyi
description: Bu konuda, maliyet hesaplama düzeyi olarak adlandırılan ürün reçetesi (BOM) düzeyi açıklanmaktadır. Bu ürün reçetesi düzeyi, üretim ve toplu iş emirlerini hesaplamalarından çıkarır.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839499"
---
# <a name="cost-calculation-level"></a>Maliyet hesaplama düzeyi

**Maliyet hesaplama düzeyi** adlı ürün reçetesi düzeyi, üretim emirlerini ve toplu iş emirlerini hesaplamalarından çıkarır. Sistem bu düzeyi, maliyetlendirme sürümlerindeki maliyet hesaplamalarını çalıştırdığında kullanır. Yeniden hesaplama ve stok kapanışı gibi işlemlerde, sistem bunun yerine **maliyetlendirme düzeyi** BOM düzeyini kullanır.

Aşağıdaki basit senaryo, **maliyet hesaplama düzeyi** BOM düzeyi ile **Maliyetlendirme düzeyi** BOM düzeyi arasındaki farkları gösterir.

Üç ürününüz var: A, B ve C. Ürün C, ürün B'nin bileşenidir ve B ürünü, A ürününün bileşenidir.

- **Maliyetlendirme düzeyi** aşağıdaki BOM düzeylerini atar:

    - **Ürün A:** 0
    - **Ürün B:** 1
    - **Ürün C:** 2

- **Maliyet hesaplama düzeyi** aşağıdaki BOM düzeylerini atar:

    - **Ürün A:** 0
    - **Ürün B:** 1
    - **Ürün C:** 2

Daha sonra ürün C'nin üretim emri oluşturulur ve üretim emri ürün reçetesine bir ürün A eklenir. Sipariş tahmini yapıldıktan sonra, BOM düzeyleri aşağıdaki şekilde güncelleştirilir:

- **Maliyetlendirme düzeyi** aşağıdaki BOM düzeylerini atar:

    - **Ürün B:** 1
    - **Ürün C:** 2
    - **Ürün A:** 3

- **Maliyet hesaplama düzeyi** aşağıdaki BOM düzeylerini atar:

    - **Ürün A:** 0
    - **Ürün B:** 1
    - **Ürün C:** 2

Bu davranış, üretim emri ürün reçeteleri üzerindeki değişikliklerin sonraki maliyet hesaplamalarını etkilememesini sağlar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]