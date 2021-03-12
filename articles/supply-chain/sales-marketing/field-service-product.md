---
title: Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme
description: Bu konu ürünleri, Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ffa0616d51127a024bea526c5926a182c0449971
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996752"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme

[!include[banner](../includes/banner.md)]

Bu konuda, ürünleri Dynamics 365 Field Service'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.

Kullanılan **Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonunu temel alır. Daha fazla bilgi için bkz. [Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Bu konu yalnızca **Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** ile **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

**Veri tümleştirmesindeki şablonun adı**

- Field Service Ürünleri (Supply Chain Management'tan Field Service'e)

**Veri tümleştirme projesindeki görevin adı**

- Ürünler - Ürünler

**Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** şablonu, **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonunda bulunmayam bir eşleme içerir. Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Aşağıdaki değer eşlemesi kullanılır.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Supply Chain Management'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:

- **Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru
- **NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış
- **Hizmet:** Ürün türü = Hizmet

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service Ürünleri (Supply Chain Management'tan Field Service'e): Ürünler - Ürünler

[![Veri tümleştirmede şablon eşleme](./media/FSProduct.png)](./media/FSProduct.png)
