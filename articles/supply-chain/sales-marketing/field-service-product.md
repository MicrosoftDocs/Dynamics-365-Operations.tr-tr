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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d96d1cd91bad4f950868074d9558cb403821d73f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439460"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="07cca-103">Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="07cca-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="07cca-104">Bu konuda, ürünleri Dynamics 365 Field Service'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="07cca-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="07cca-105">Kullanılan **Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="07cca-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="07cca-106">Daha fazla bilgi için bkz. [Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="07cca-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="07cca-107">Bu konu yalnızca **Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** ile **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="07cca-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="07cca-108">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="07cca-108">Templates and tasks</span></span>

<span data-ttu-id="07cca-109">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="07cca-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="07cca-110">Field Service Ürünleri (Supply Chain Management'tan Field Service'e)</span><span class="sxs-lookup"><span data-stu-id="07cca-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="07cca-111">**Veri tümleştirme projesindeki görevin adı**</span><span class="sxs-lookup"><span data-stu-id="07cca-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="07cca-112">Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="07cca-112">Products - Products</span></span>

<span data-ttu-id="07cca-113">**Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** şablonu, **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonunda bulunmayam bir eşleme içerir.</span><span class="sxs-lookup"><span data-stu-id="07cca-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="07cca-114">Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="07cca-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="07cca-115">Aşağıdaki değer eşlemesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="07cca-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="07cca-116">Supply Chain Management'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="07cca-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="07cca-117">**Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru</span><span class="sxs-lookup"><span data-stu-id="07cca-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="07cca-118">**NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış</span><span class="sxs-lookup"><span data-stu-id="07cca-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="07cca-119">**Hizmet:** Ürün türü = Hizmet</span><span class="sxs-lookup"><span data-stu-id="07cca-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="07cca-120">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="07cca-120">Template mapping in Data integration</span></span>

<span data-ttu-id="07cca-121">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="07cca-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="07cca-122">Field Service Ürünleri (Supply Chain Management'tan Field Service'e): Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="07cca-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="07cca-123">[![Veri tümleştirmede şablon eşleme](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="07cca-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
