---
title: Maliyet hesaplama düzeyi
description: Bu konuda, maliyet hesaplama düzeyi olarak adlandırılan ürün reçetesi (BOM) düzeyi açıklanmaktadır. Bu ürün reçetesi düzeyi, üretim ve toplu iş emirlerini hesaplamalarından çıkarır.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410990"
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