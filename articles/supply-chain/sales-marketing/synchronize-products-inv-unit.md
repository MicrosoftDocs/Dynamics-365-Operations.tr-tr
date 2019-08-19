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
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="f83ed-103">Stok birimli ürünleri Finance and Operations'dan Field Service'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="f83ed-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f83ed-104">Bu konu, stoklu ürünlerin Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="f83ed-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f83ed-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="f83ed-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="f83ed-106">Kullanılan **Stok birimli Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu, **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu üzerine dayanır.</span><span class="sxs-lookup"><span data-stu-id="f83ed-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="f83ed-107">Daha fazla bilgi için bkz. [Field Service Ürünleri (Finance and Operations'tan Field Service'a)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="f83ed-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="f83ed-108">Bu konu, yalnızca iki şablon arasındaki farkı açıklar:</span><span class="sxs-lookup"><span data-stu-id="f83ed-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="f83ed-109">**Stok birimli Field Service Ürünleri (Fin and Ops'tan Sales'a)**</span><span class="sxs-lookup"><span data-stu-id="f83ed-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="f83ed-110">**Field Service Ürünleri (Fin and Ops'tan Field Service'a)**</span><span class="sxs-lookup"><span data-stu-id="f83ed-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="f83ed-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="f83ed-111">Templates and tasks</span></span>

<span data-ttu-id="f83ed-112">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="f83ed-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="f83ed-113">Stok birimli Field Service Ürünleri (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="f83ed-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="f83ed-114">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="f83ed-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="f83ed-115">Ürünler</span><span class="sxs-lookup"><span data-stu-id="f83ed-115">Products</span></span>

<span data-ttu-id="f83ed-116">**Stok birimli Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu, **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** içinde dahil olmayan bir eşleştirme içerir.</span><span class="sxs-lookup"><span data-stu-id="f83ed-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="f83ed-117">Bu eşleme gerekli eşitleme stok düzeyi için stok tutma birimi birlikte sağlanır.</span><span class="sxs-lookup"><span data-stu-id="f83ed-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f83ed-118">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="f83ed-118">Template mapping in Data integration</span></span>

<span data-ttu-id="f83ed-119">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f83ed-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="f83ed-120">Stok birimli Field Service Ürünleri (Fin and Ops'tan Field Service'a): Ürünler</span><span class="sxs-lookup"><span data-stu-id="f83ed-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="f83ed-121">[![Veri tümleştirmede şablon eşleme](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="f83ed-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
