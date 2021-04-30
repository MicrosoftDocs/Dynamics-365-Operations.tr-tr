---
title: Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme
description: Bu konu ürünleri, Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910003"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="83c68-103">Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="83c68-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="83c68-104">Bu konuda, ürünleri Dynamics 365 Field Service'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="83c68-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="83c68-105">Kullanılan **Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="83c68-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="83c68-106">Daha fazla bilgi için bkz. [Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="83c68-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="83c68-107">Bu konu yalnızca **Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** ile **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="83c68-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="83c68-108">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="83c68-108">Templates and tasks</span></span>

<span data-ttu-id="83c68-109">**Veri tümleştirmesindeki şablonun adı**</span><span class="sxs-lookup"><span data-stu-id="83c68-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="83c68-110">Field Service Ürünleri (Supply Chain Management'tan Field Service'e)</span><span class="sxs-lookup"><span data-stu-id="83c68-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="83c68-111">**Veri tümleştirme projesindeki görevin adı**</span><span class="sxs-lookup"><span data-stu-id="83c68-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="83c68-112">Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="83c68-112">Products - Products</span></span>

<span data-ttu-id="83c68-113">**Field Service Ürünleri (Supply Chain Management'tan Field Service'a)** şablonu, **Ürünler (Supply Chain Management'tan Sales'e) – Doğrudan** şablonunda bulunmayam bir eşleme içerir.</span><span class="sxs-lookup"><span data-stu-id="83c68-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="83c68-114">Bu eşleme, Field Service'a özel gerekli alan olan **Hizmet Ürün Türü**'nün doğru ayarlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="83c68-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="83c68-115">Aşağıdaki değer eşlemesi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83c68-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="83c68-116">Supply Chain Management'da **Satılabilir serbest bırakılmış ürünler** veri varlığındaki **Field Service ürün türü** değeri aşağıdaki şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="83c68-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="83c68-117">**Stok:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Doğru</span><span class="sxs-lookup"><span data-stu-id="83c68-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="83c68-118">**NonInventory:** Ürün türü = Ürün ve Madde model grubu, Stoğu tutulan ürün = Yanlış</span><span class="sxs-lookup"><span data-stu-id="83c68-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="83c68-119">**Hizmet:** Ürün türü = Hizmet</span><span class="sxs-lookup"><span data-stu-id="83c68-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="83c68-120">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="83c68-120">Template mapping in Data integration</span></span>

<span data-ttu-id="83c68-121">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="83c68-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="83c68-122">Field Service Ürünleri (Supply Chain Management'tan Field Service'e): Ürünler - Ürünler</span><span class="sxs-lookup"><span data-stu-id="83c68-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="83c68-123">[![Veri tümleştirmede şablon eşleme](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="83c68-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]