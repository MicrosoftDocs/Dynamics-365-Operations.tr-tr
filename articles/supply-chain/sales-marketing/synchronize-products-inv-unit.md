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
ms.openlocfilehash: 62ed33d101f7d7e47b560c417dc05e5aecc83478
ms.sourcegitcommit: 137e2bd30f0a85bd2e1baf1cf16b993edd2094f9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2020
ms.locfileid: "3546350"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="19376-103">Stok birimli ürünleri Supply Chain Management'tan Field Service'e eşitleme</span><span class="sxs-lookup"><span data-stu-id="19376-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="19376-104">Bu konu, stoklu ürünlerin Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="19376-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="19376-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="19376-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="19376-106">Kullanılan **Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonu, **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="19376-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="19376-107">Daha fazla bilgi için bkz. [Field Service'teki ürünleri Supply Chain Management'taki ürünlere eşitleme](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="19376-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="19376-108">Bu konu, yalnızca iki şablon arasındaki farkı açıklar:</span><span class="sxs-lookup"><span data-stu-id="19376-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="19376-109">**Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Sales'e)**</span><span class="sxs-lookup"><span data-stu-id="19376-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="19376-110">**Field Service Ürünleri (Supply Chain Management'tan Field Service'e)**</span><span class="sxs-lookup"><span data-stu-id="19376-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="19376-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="19376-111">Templates and tasks</span></span>

<span data-ttu-id="19376-112">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="19376-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="19376-113">Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Sales'e)</span><span class="sxs-lookup"><span data-stu-id="19376-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="19376-114">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="19376-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="19376-115">Ürünler</span><span class="sxs-lookup"><span data-stu-id="19376-115">Products</span></span>

<span data-ttu-id="19376-116">**Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonu, **Field Service Ürünleri (Supply Chain Management'tan Field Service'e)** şablonunda yer almayan bir eşleşme içeriyor.</span><span class="sxs-lookup"><span data-stu-id="19376-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="19376-117">Bu eşleme gerekli eşitleme stok düzeyi için stok tutma birimi birlikte sağlanır.</span><span class="sxs-lookup"><span data-stu-id="19376-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="19376-118">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="19376-118">Template mapping in Data integration</span></span>

<span data-ttu-id="19376-119">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="19376-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="19376-120">Stok Birimli Field Service Ürünleri (Supply Chain Management'tan Field Service'e): Ürünler</span><span class="sxs-lookup"><span data-stu-id="19376-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="19376-121">[![Veri tümleştirmede şablon eşleme](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="19376-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
