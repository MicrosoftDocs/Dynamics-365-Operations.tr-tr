---
title: Eldeki stok verisi varlıklarını genişletme
description: Bu konuda, INVENTORSITEONHANDENTITY ve INVENTWAREHOUSEONHANDENTITY görünümlerine genişletilmiş alanlar eklemeye ve eldeki stok verisi varlıklarının uzantılarla çalışabilme özelliklerine ilişkin bir örnek sunulmaktadır.
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 2e805b9379c73f7b7eb2820662fad70e28181ebf
ms.sourcegitcommit: f59df61799915f6a79aec7e3e8664c02df6597da
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/22/2021
ms.locfileid: "5043405"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Eldeki stok verisi varlıklarını genişletme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, [tablolara uzantı aracılığıyla alanlar eklemenize](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md) olanak tanıyan [genişletilebilirlik](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) özellikleri sunar. Bu konuda, `INVENTORSITEONHANDENTITY` ve `INVENTWAREHOUSEONHANDENTITY` görünümlerine genişletilmiş alanlar eklemeye ve eldeki stok verisi varlıklarının uzantılarla çalışabilme özelliklerine ilişkin bir örnek sunulmaktadır. Veri varlıkları hakkında daha fazla bilgi için bkz. [Veri yönetimine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Eldeki stok veri varlıklarının bazılarını içeren listeyi aşağıda bulabilirsiniz:
>
> - Tesise göre eldeki stok
> - Tesise göre eldeki stok V2
> - Ambara göre eldeki stok
> - Ambara göre eldeki stok v2

`inventSiteOnHandView` görünümü tarafından kullanılan tablolara alanlar ekledikten sonra, uzantıların doğru tanınması için altyapıyı eşitlemeniz gerekir.

1. `InventSiteOnHandView` görünümünü uzantı alanı ekleyerek genişletin.
1. `InventSiteOnHandAggregatedView` görünümünü uzantı alanlarıyla genişletin.
1. `InventSiteOnHandAggregatedViewBuilder` viewBuilder sınıfını `getExtensionFields()` yöntemini değiştirerek genişletin. Bu şekilde, viewBuilder eşitlemesi çalıştırıldığında eski görünüm alanlarını yeni görünüm alanlarıyla eşlersiniz.

Örneğin, `InventTable` tablosuna uzantı yoluyla aşağıdaki dört alanı eklediniz:

- Özel alan 1
- Özel alan 2
- Özel alan 3
- Özel alan 4

Bu durumda, `getExtensionFields()` yöntemini aşağıdaki şekilde değiştirmeniz gerekir.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Bu adımları tamamladıktan sonra, yeni alanları ekleyerek tesise göre eldeki stok ve ambara göre eldeki stok veri varlıklarıı genişletebilirsiniz. Bu şekilde, genişletilmiş alanların bu veri varlıklarını kullanan veri taşıma sırasında tanınıp eklendiğinden emin olursunuz.
