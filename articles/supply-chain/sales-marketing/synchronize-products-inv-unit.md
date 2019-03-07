---
title: Finance and Operations'tan Field Service'a stok birim ile ürünleri eşitlemek
description: Bu konu, stoklu ürünlerin Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "359256"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cffaf-103">Stok birimli ürünleri Finance and Operations'dan Field Service'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="cffaf-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cffaf-104">Bu konu, stoklu ürünlerin Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="cffaf-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cffaf-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="cffaf-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="cffaf-106">Kullanılan **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Finance and Operations'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="cffaf-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="cffaf-107">Daha fazla bilgi için bkz. [Ürünler (Finance and Operations'tan Sales'e) – Doğrudan](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="cffaf-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="cffaf-108">Bu konu yalnızca **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** ile **Field Service Ürünleri (Finance and Operations'tan Sales'e)** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="cffaf-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cffaf-109">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="cffaf-109">Templates and tasks</span></span>

<span data-ttu-id="cffaf-110">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="cffaf-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cffaf-111">Stok birimli Field Service Ürünleri (Finance and Operations'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="cffaf-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="cffaf-112">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="cffaf-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cffaf-113">Ürünler</span><span class="sxs-lookup"><span data-stu-id="cffaf-113">Products</span></span>

<span data-ttu-id="cffaf-114">**Stok birimli Field Service Ürünleri (Finance and Operations'tan Field Service)** şablonu, **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** içinde dahil olmayan bir eşleştirme içerir.</span><span class="sxs-lookup"><span data-stu-id="cffaf-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="cffaf-115">Bu eşleme gerekli eşitleme stok düzeyi için stok tutma birimi birlikte sağlanır.</span><span class="sxs-lookup"><span data-stu-id="cffaf-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cffaf-116">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="cffaf-116">Template mapping in Data integration</span></span>

<span data-ttu-id="cffaf-117">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="cffaf-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="cffaf-118">Stok birimli Field Service Ürünleri (Finance and Operations'tan Field Service'a): Ürünler</span><span class="sxs-lookup"><span data-stu-id="cffaf-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="cffaf-119">[![Veri tümleştirmede şablon eşleme](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="cffaf-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
