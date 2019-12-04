---
title: Stok birimli ürünleri Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu, stoklu ürünlerin Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
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
ms.openlocfilehash: 18bedcc99d7d70875ec363a97e4e6eccbace3a9c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814211"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Stok birimli ürünleri Supply Chain Management'tan Field Service'e eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, stoklu ürünlerin Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.

[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Kullanılan **Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonu, **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonuna dayanır. Daha fazla bilgi için bkz. [Field Service'teki ürünleri Supply Chain Management'taki ürünlere eşitleme](field-service-product.md).

Bu konu, yalnızca iki şablon arasındaki farkı açıklar: 
- **Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Sales'e)**
- **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** 

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı:**

- Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Sales'e)

**Veri tümleştirme projesindeki görevin adı:**

- Ürünler

**Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonu, **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonunda yer almayan bir eşleşme içeriyor. Bu eşleme gerekli eşitleme stok düzeyi için stok tutma birimi birlikte sağlanır.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e): Ürünler

[![Veri tümleştirmede şablon eşleme](./media/FSProduct1.png)](./media/FSProduct1.png)
