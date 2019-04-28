---
title: Stok düzeyi bilgisini Finance and Operations'tan Field Service'a eşitlemek
description: Bu konu stok düzey bilgisini Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 6b2bdf1ca6f6ae43cd85c8a1353ee8305052761d
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "842568"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="fdfcf-103">Stok düzeyi bilgilerini Field Service'dan Finance and Operations'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="fdfcf-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fdfcf-104">Bu konu stok düzey bilgisini Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="fdfcf-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fdfcf-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="fdfcf-106">Templates and tasks</span></span>
<span data-ttu-id="fdfcf-107">Aşağıdaki şablon ve altındaki görevler, eldeki stok düzeylerini Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="fdfcf-108">**Veri Tümleştirmesindeki Şablon**</span><span class="sxs-lookup"><span data-stu-id="fdfcf-108">**Template in Data integration**</span></span>
- <span data-ttu-id="fdfcf-109">Ürün envanteri (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="fdfcf-110">**Veri tümleştirme projesindeki görev**</span><span class="sxs-lookup"><span data-stu-id="fdfcf-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="fdfcf-111">Ürün stoku</span><span class="sxs-lookup"><span data-stu-id="fdfcf-111">Product inventory</span></span>

<span data-ttu-id="fdfcf-112">Aşağıdaki eşitleme görevlerinin, stok düzeylerinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="fdfcf-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="fdfcf-113">Ambarlar (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="fdfcf-114">Stok birimli Field Service ürünleri (Fin and Ops'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="fdfcf-115">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="fdfcf-115">Entity set</span></span>

| <span data-ttu-id="fdfcf-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="fdfcf-116">Field Service</span></span>                      | <span data-ttu-id="fdfcf-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fdfcf-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="fdfcf-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="fdfcf-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="fdfcf-119">CDS ambara göre eldeki stok</span><span class="sxs-lookup"><span data-stu-id="fdfcf-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="fdfcf-120">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="fdfcf-120">Entity flow</span></span>
<span data-ttu-id="fdfcf-121">Finance and Operations'tan stok seviyesi bilgisi Field Service'a seçilen ürünler için gönderildi.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="fdfcf-122">Düzey Stok bilgileri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="fdfcf-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="fdfcf-123">Eldeki miktarı (geçerli kayıtlı fiziksel olarak ambarda miktar)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="fdfcf-124">Sipariş miktarı (toplam kaydedilen siparişindeki miktar - satış siparişleri gibi)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="fdfcf-125">Sipariş edilen toplam miktar (toplam kaydedilen sipariş tutarı - satınalma siparişleri gibi)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="fdfcf-126">Bu bilgiler her ambar için serbest bırakılan ürün başına yakalanan ve stok düzeyini değiştiğinde, değişiklik izlemeyi dayalı eşitlenmiş.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="fdfcf-127">Field Service servis düzeyleri ve Finance and Operations işlemleri eşleştirmek için düzeyin almak için delta Stok günlüklerini tümleştirme çözümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="fdfcf-128">Finance and Operations, stok düzeyleri için üst görevi görür.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="fdfcf-129">Bu nedenle Field Service'tan Finance and Operations'a iş emirleri, aktarmalar ve ayarlamalar için kurulum tümleştirmesi, bu özellik Field Service'ta Finance and Operations'tan stok düzeyleri eşitlemesi ile kullanılıyorsa, önemlidir.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="fdfcf-130">Stok düzeylerinin Finance and Operations'tan üstlenildiği ürünler ve ambarlar, Gelişmiş Sorgu ve Filtreleme (Power Query) ile kontrol edilebilir.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="fdfcf-131">Field Services'ta birden fazla ambar (**Harici Korunan = Hayır**) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="fdfcf-132">Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="fdfcf-133">Bu durumda, Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="fdfcf-134">Daha fazla bilgi için bkz. [Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="fdfcf-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="fdfcf-135">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="fdfcf-135">Field Service CRM solution</span></span>
<span data-ttu-id="fdfcf-136">**Harici ürün stoku** varlığı yalnızca arka uç tümleştirmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="fdfcf-137">Finance and Operations ve stok düzeyi değerlerinin birleştirilmesinde alır ve daha sonra bu ambarı stok ürünler sonra değişen Manuel Stok günlüklerini değerlere dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="fdfcf-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="fdfcf-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="fdfcf-139">Veri tümleştirme projesi</span><span class="sxs-lookup"><span data-stu-id="fdfcf-139">Data integration project</span></span>
<span data-ttu-id="fdfcf-140">Gelişmiş Sorgu ve Filtreleme ile filtreler uygulayabilirsiniz, böylece yalnızca istenilen ürünler ve ambarlar stok düzeyi bilgisine Finance and Operations'tan Field Service'a gönderilir.</span><span class="sxs-lookup"><span data-stu-id="fdfcf-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fdfcf-141">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="fdfcf-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="fdfcf-142">Ürün stoku (Fin and Ops'tan Field Service'a): Ürün stoku</span><span class="sxs-lookup"><span data-stu-id="fdfcf-142">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="fdfcf-143">[![Veri tümleştirmede şablon eşleme](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="fdfcf-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
