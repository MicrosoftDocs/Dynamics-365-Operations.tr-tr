---
title: Finance and Operations'taki ürünleri Field Service'teki ürünlerle eşitleme
description: Bu konu ürünleri, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 06d7ff272ecb79abded3c3d3ade1f6bc0ef1f095
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742367"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Finance and Operations'taki ürünleri Field Service'daki ürünlerle eşitleme

[!include[banner](../includes/banner.md)]

Bu konu ürünleri, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.

Kullanılan **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonunu temel alır. Daha fazla bilgi için bkz. [Ürünler (Fin and Ops'tan Sales'e) – Doğrudan](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Bu konu yalnızca **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** ile **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı:**

- Field Service Ürünleri (Fin and Ops'tan Field Service'a)

**Veri tümleştirme projesindeki görevin adı:**

- Ürünler - Ürünler

**Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonuna dahil olmayan bir eşleme içerir. Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Aşağıdaki değer eşlemesi kullanılır.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Finance and Operations'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:

- **Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru
- **NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış
- **Hizmet:** Ürün türü = Hizmet

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service Ürünleri (Fin and Ops'tan Field Service'a): Ürünler - Ürünler

[![Veri tümleştirmede şablon eşleme](./media/FSProduct.png)](./media/FSProduct.png)
