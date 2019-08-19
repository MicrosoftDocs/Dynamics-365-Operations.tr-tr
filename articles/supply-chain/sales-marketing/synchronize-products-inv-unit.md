---
title: Finance and Operations'tan Field Service'a stok birim ile ürünleri eşitlemek
description: Bu konu, stoklu ürünlerin Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835706"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Stok birimli ürünleri Finance and Operations'dan Field Service'a eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, stoklu ürünlerin Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Kullanılan **Stok birimli Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu, **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu üzerine dayanır. Daha fazla bilgi için bkz. [Field Service Ürünleri (Finance and Operations'tan Field Service'a)](field-service-product.md).

Bu konu, yalnızca iki şablon arasındaki farkı açıklar: 
- **Stok birimli Field Service Ürünleri (Fin and Ops'tan Sales'a)**
- **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** 

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı:**

- Stok birimli Field Service Ürünleri (Fin and Ops'tan Sales'a)

**Veri tümleştirme projesindeki görevin adı:**

- Ürünler

**Stok birimli Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu, **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** içinde dahil olmayan bir eşleştirme içerir. Bu eşleme gerekli eşitleme stok düzeyi için stok tutma birimi birlikte sağlanır.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Stok birimli Field Service Ürünleri (Fin and Ops'tan Field Service'a): Ürünler

[![Veri tümleştirmede şablon eşleme](./media/FSProduct1.png)](./media/FSProduct1.png)
