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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439369"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="b5c70-103">Eldeki stok verisi varlıklarını genişletme</span><span class="sxs-lookup"><span data-stu-id="b5c70-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5c70-104">Microsoft Dynamics 365 Supply Chain Management, [tablolara uzantı aracılığıyla alanlar eklemenize](../../fin-ops-core/dev-itpro/extensibility/add-field-extension) olanak tanıyan [genişletilebilirlik](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) özellikleri sunar.</span><span class="sxs-lookup"><span data-stu-id="b5c70-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="b5c70-105">Bu konuda, `INVENTORSITEONHANDENTITY` ve `INVENTWAREHOUSEONHANDENTITY` görünümlerine genişletilmiş alanlar eklemeye ve eldeki stok verisi varlıklarının uzantılarla çalışabilme özelliklerine ilişkin bir örnek sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b5c70-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="b5c70-106">Veri varlıkları hakkında daha fazla bilgi için bkz. [Veri yönetimine genel bakış](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="b5c70-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b5c70-107">Eldeki stok veri varlıklarının bazılarını içeren listeyi aşağıda bulabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b5c70-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="b5c70-108">Tesise göre eldeki stok</span><span class="sxs-lookup"><span data-stu-id="b5c70-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="b5c70-109">Tesise göre eldeki stok V2</span><span class="sxs-lookup"><span data-stu-id="b5c70-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="b5c70-110">Ambara göre eldeki stok</span><span class="sxs-lookup"><span data-stu-id="b5c70-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="b5c70-111">Ambara göre eldeki stok v2</span><span class="sxs-lookup"><span data-stu-id="b5c70-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="b5c70-112">`inventSiteOnHandView` görünümü tarafından kullanılan tablolara alanlar ekledikten sonra, uzantıların doğru tanınması için altyapıyı eşitlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5c70-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="b5c70-113">`InventSiteOnHandView` görünümünü uzantı alanı ekleyerek genişletin.</span><span class="sxs-lookup"><span data-stu-id="b5c70-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="b5c70-114">`InventSiteOnHandAggregatedView` görünümünü uzantı alanlarıyla genişletin.</span><span class="sxs-lookup"><span data-stu-id="b5c70-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="b5c70-115">`InventSiteOnHandAggregatedViewBuilder` viewBuilder sınıfını `getExtensionFields()` yöntemini değiştirerek genişletin.</span><span class="sxs-lookup"><span data-stu-id="b5c70-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="b5c70-116">Bu şekilde, viewBuilder eşitlemesi çalıştırıldığında eski görünüm alanlarını yeni görünüm alanlarıyla eşlersiniz.</span><span class="sxs-lookup"><span data-stu-id="b5c70-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="b5c70-117">Örneğin, `InventTable` tablosuna uzantı yoluyla aşağıdaki dört alanı eklediniz:</span><span class="sxs-lookup"><span data-stu-id="b5c70-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="b5c70-118">Özel alan 1</span><span class="sxs-lookup"><span data-stu-id="b5c70-118">Custom field 1</span></span>
- <span data-ttu-id="b5c70-119">Özel alan 2</span><span class="sxs-lookup"><span data-stu-id="b5c70-119">Custom field 2</span></span>
- <span data-ttu-id="b5c70-120">Özel alan 3</span><span class="sxs-lookup"><span data-stu-id="b5c70-120">Custom field 3</span></span>
- <span data-ttu-id="b5c70-121">Özel alan 4</span><span class="sxs-lookup"><span data-stu-id="b5c70-121">Custom field 4</span></span>

<span data-ttu-id="b5c70-122">Bu durumda, `getExtensionFields()` yöntemini aşağıdaki şekilde değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5c70-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

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

<span data-ttu-id="b5c70-123">Bu adımları tamamladıktan sonra, yeni alanları ekleyerek tesise göre eldeki stok ve ambara göre eldeki stok veri varlıklarıı genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5c70-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="b5c70-124">Bu şekilde, genişletilmiş alanların bu veri varlıklarını kullanan veri taşıma sırasında tanınıp eklendiğinden emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="b5c70-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
