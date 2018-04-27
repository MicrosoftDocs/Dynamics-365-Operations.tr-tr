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

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="136ef-103">Finance and Operations'taki ürünleri Field Service'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="136ef-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="136ef-104">Bu konu, ürünleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="136ef-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="136ef-105">Kullanılan **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="136ef-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="136ef-106">Daha fazla bilgi için bkz. [Ürünler (Fin and Ops'tan Sales'e) – Doğrudan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="136ef-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="136ef-107">Bu konu yalnızca **Field Service Ürünleri (Fin and Ops'tan Field Service'a)** ile **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="136ef-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="136ef-108">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="136ef-108">Templates and tasks</span></span>

<span data-ttu-id="136ef-109">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="136ef-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="136ef-110">Field Service Ürünleri (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="136ef-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="136ef-111">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="136ef-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="136ef-112">Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="136ef-112">Products - Products</span></span>

<span data-ttu-id="136ef-113">**Field Service Ürünleri (Fin and Ops'tan Field Service'a)** şablonu **Ürünler (Fin and Ops'tan Sales'e) – Doğrudan** şablonuna dahil olmayan bir eşleme içerir.</span><span class="sxs-lookup"><span data-stu-id="136ef-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="136ef-114">Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="136ef-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="136ef-115">Aşağıdaki değer eşlemesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="136ef-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="136ef-116">Finance and Operations'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="136ef-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="136ef-117">**Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru</span><span class="sxs-lookup"><span data-stu-id="136ef-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="136ef-118">**NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış</span><span class="sxs-lookup"><span data-stu-id="136ef-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="136ef-119">**Hizmet:** Ürün türü = Hizmet</span><span class="sxs-lookup"><span data-stu-id="136ef-119">**Service:** Product type = Service</span></span>

