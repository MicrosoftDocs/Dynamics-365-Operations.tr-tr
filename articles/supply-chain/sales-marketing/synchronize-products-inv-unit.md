---
title: Stok birimli ürünleri Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu, stoklu ürünlerin Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3485e4f284218924cee01e45d5248f5af1a64010
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215965"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="adb2a-103">Stok birimli ürünleri Supply Chain Management'tan Field Service'e eşitleme</span><span class="sxs-lookup"><span data-stu-id="adb2a-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="adb2a-104">Bu konu, stoklu ürünlerin Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="adb2a-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="adb2a-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="adb2a-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="adb2a-106">Kullanılan **Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonu, **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="adb2a-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="adb2a-107">Daha fazla bilgi için bkz. [Field Service'teki ürünleri Supply Chain Management'taki ürünlere eşitleme](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="adb2a-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="adb2a-108">Bu konu, yalnızca iki şablon arasındaki farkı açıklar:</span><span class="sxs-lookup"><span data-stu-id="adb2a-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="adb2a-109">**Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Sales'e)**</span><span class="sxs-lookup"><span data-stu-id="adb2a-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="adb2a-110">**Field Service Ürünleri (Supply Chain Management'tan Field Service'e)**</span><span class="sxs-lookup"><span data-stu-id="adb2a-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="adb2a-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="adb2a-111">Templates and tasks</span></span>

<span data-ttu-id="adb2a-112">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="adb2a-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="adb2a-113">Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Sales'e)</span><span class="sxs-lookup"><span data-stu-id="adb2a-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="adb2a-114">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="adb2a-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="adb2a-115">Ürünler</span><span class="sxs-lookup"><span data-stu-id="adb2a-115">Products</span></span>

<span data-ttu-id="adb2a-116">**Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonu, **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonunda yer almayan bir eşleşme içeriyor.</span><span class="sxs-lookup"><span data-stu-id="adb2a-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="adb2a-117">Bu eşleme gerekli eşitleme stok düzeyi için stok tutma birimi birlikte sağlanır.</span><span class="sxs-lookup"><span data-stu-id="adb2a-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="adb2a-118">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="adb2a-118">Template mapping in Data integration</span></span>

<span data-ttu-id="adb2a-119">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="adb2a-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="adb2a-120">Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e): Ürünler</span><span class="sxs-lookup"><span data-stu-id="adb2a-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="adb2a-121">[![Veri tümleştirmede şablon eşleme](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="adb2a-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
