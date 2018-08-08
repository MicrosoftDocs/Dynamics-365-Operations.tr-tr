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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="a766e-103">Finance and Operations'taki ürünleri Field Service'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="a766e-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a766e-104">Bu konu, ürünleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="a766e-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a766e-105">Kullanılan **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="a766e-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="a766e-106">Daha fazla bilgi için bkz. [Ürünler (Fin and Ops'tan Sales'e) – Doğrudan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="a766e-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="a766e-107">Bu konu yalnızca **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** ile **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="a766e-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a766e-108">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="a766e-108">Templates and tasks</span></span>

<span data-ttu-id="a766e-109">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="a766e-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="a766e-110">Field Service Ürünleri (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="a766e-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="a766e-111">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="a766e-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="a766e-112">Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="a766e-112">Products - Products</span></span>

<span data-ttu-id="a766e-113">**Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonuna dahil olmayan bir eşleme içerir.</span><span class="sxs-lookup"><span data-stu-id="a766e-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="a766e-114">Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="a766e-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="a766e-115">Aşağıdaki değer eşlemesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a766e-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="a766e-116">Finance and Operations'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="a766e-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="a766e-117">**Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru</span><span class="sxs-lookup"><span data-stu-id="a766e-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="a766e-118">**NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış</span><span class="sxs-lookup"><span data-stu-id="a766e-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="a766e-119">**Hizmet:** Ürün türü = Hizmet</span><span class="sxs-lookup"><span data-stu-id="a766e-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a766e-120">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="a766e-120">Template mapping in Data integration</span></span>

<span data-ttu-id="a766e-121">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="a766e-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="a766e-122">Field Service Ürünleri (Fin and Ops'tan Field Service'a): Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="a766e-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="a766e-123">[![Veri tümleştirmede şablon eşleme](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="a766e-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>

