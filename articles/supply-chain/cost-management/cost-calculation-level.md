---
title: Maliyet hesaplama düzeyi
description: Bu makalede, maliyet hesaplama düzeyi olarak adlandırılan ürün reçetesi (BOM) düzeyi açıklanmaktadır. Bu ürün reçetesi düzeyi, üretim ve toplu iş emirlerini hesaplamalarından çıkarır.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334970"
---
# <a name="cost-calculation-level"></a>Maliyet hesaplama düzeyi

[!include [banner](../includes/banner.md)]

**Maliyet hesaplama düzeyi** adlı ürün reçetesi düzeyi, üretim emirlerini ve toplu iş emirlerini hesaplamalarından çıkarır. Sistem bu düzeyi, maliyetlendirme sürümlerindeki maliyet hesaplamalarını çalıştırdığında kullanır. Yeniden hesaplama ve stok kapanışı gibi işlemlerde, sistem bunun yerine **maliyetlendirme düzeyi** BOM düzeyini kullanır.

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>Maliyet hesaplama düzeyi özelliğini açma veya kapatma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.29 itibarıyla özellik varsayılan olarak açıktır. Yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Maliyet hesaplama düzeyi* özelliğini bularak bu işlevi açabilir veya kapatabilir.

## <a name="example-scenario"></a>Örnek senaryo

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