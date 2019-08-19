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
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="aff84-103">Finance and Operations'taki ürünleri Field Service'daki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="aff84-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="aff84-104">Bu konu ürünleri, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.</span><span class="sxs-lookup"><span data-stu-id="aff84-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="aff84-105">Kullanılan **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="aff84-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="aff84-106">Daha fazla bilgi için bkz. [Ürünler (Fin and Ops'tan Sales'e) – Doğrudan](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="aff84-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="aff84-107">Bu konu yalnızca **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** ile **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="aff84-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="aff84-108">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="aff84-108">Templates and tasks</span></span>

<span data-ttu-id="aff84-109">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="aff84-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="aff84-110">Field Service Ürünleri (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="aff84-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="aff84-111">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="aff84-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="aff84-112">Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="aff84-112">Products - Products</span></span>

<span data-ttu-id="aff84-113">**Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonuna dahil olmayan bir eşleme içerir.</span><span class="sxs-lookup"><span data-stu-id="aff84-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="aff84-114">Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="aff84-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="aff84-115">Aşağıdaki değer eşlemesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aff84-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="aff84-116">Finance and Operations'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="aff84-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="aff84-117">**Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru</span><span class="sxs-lookup"><span data-stu-id="aff84-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="aff84-118">**NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış</span><span class="sxs-lookup"><span data-stu-id="aff84-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="aff84-119">**Hizmet:** Ürün türü = Hizmet</span><span class="sxs-lookup"><span data-stu-id="aff84-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="aff84-120">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="aff84-120">Template mapping in Data integration</span></span>

<span data-ttu-id="aff84-121">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="aff84-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="aff84-122">Field Service Ürünleri (Fin and Ops'tan Field Service'a): Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="aff84-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="aff84-123">[![Veri tümleştirmede şablon eşleme](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="aff84-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
