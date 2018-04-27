---
title: "Finance and Operations'taki ürünleri Field Service'teki ürünlerle eşitleme"
description: "Bu konu, ürünleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: tr-tr
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Finance and Operations'taki ürünleri Field Service'teki ürünlerle eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, ürünleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

Kullanılan **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonunu temel alır. Daha fazla bilgi için bkz. [Ürünler (Fin and Ops'tan Sales'e) – Doğrudan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

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

