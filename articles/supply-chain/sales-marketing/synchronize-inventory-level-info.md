---
title: "Stok düzeyi bilgisini Finance and Operations'tan Field Service'a eşitlemek"
description: "Bu konu, stok düzeyi bilgisini Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="bd5cd-103">Stok düzeyi bilgisini Finance and Operations'tan Field Service'a eşitlemek</span><span class="sxs-lookup"><span data-stu-id="bd5cd-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="bd5cd-104">Bu konu, stok düzeyi bilgisini Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="bd5cd-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="bd5cd-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="bd5cd-106">Templates and tasks</span></span>
<span data-ttu-id="bd5cd-107">Aşağıdaki şablon, stok eldeki düzeyleri eşitlemelerini Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="bd5cd-108">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="bd5cd-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="bd5cd-109">Ürün Stoku (Finance and Operations'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="bd5cd-110">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="bd5cd-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="bd5cd-111">Ürün stoku</span><span class="sxs-lookup"><span data-stu-id="bd5cd-111">Product inventory</span></span>

<span data-ttu-id="bd5cd-112">Aşağıdaki eşitleme görevlerinin, stok düzeylerinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="bd5cd-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="bd5cd-113">Ambarlar (Finance and Operations'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="bd5cd-114">Stok birimli Field Service Ürünleri (Finance and Operations'tan Sales'a)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="bd5cd-115">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="bd5cd-115">Entity set</span></span>

| <span data-ttu-id="bd5cd-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="bd5cd-116">Field Service</span></span>                      | <span data-ttu-id="bd5cd-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="bd5cd-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="bd5cd-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="bd5cd-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="bd5cd-119">CDS ambara göre eldeki stok</span><span class="sxs-lookup"><span data-stu-id="bd5cd-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="bd5cd-120">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="bd5cd-120">Entity flow</span></span>
<span data-ttu-id="bd5cd-121">Finance and Operations'tan stok seviyesi bilgisi Field Service'a seçilen ürünler için gönderilir.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="bd5cd-122">Düzey Stok bilgileri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="bd5cd-122">The inventory level information include:</span></span> 
- <span data-ttu-id="bd5cd-123">Eldeki miktarı (geçerli kayıtlı fiziksel olarak ambarda miktar)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="bd5cd-124">Sipariş miktarı (toplam kaydedilen siparişindeki miktar - başka bir deyişle Satış siparişleri)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="bd5cd-125">Sipariş edilen toplam miktar (toplam kaydedilen sipariş tutarı - başka bir deyişle satınalma siparişleri)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="bd5cd-126">Bu bilgiler her ambar için serbest bırakılan ürün başına yakalanan ve stok düzeyini değiştiğinde, değişiklik izlemeyi dayalı eşitlenmiş.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="bd5cd-127">Field Service servis düzeyleri ve Finance and Operations işlemleri eşleştirmek için düzeyin almak için delta Stok günlüklerini tümleştirme çözümü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="bd5cd-128">Finance and Operations, stok düzeyleri için üst görevi görür.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="bd5cd-129">Bu nedenle Field Service'tan Finance and Operations'a iş emirleri, aktarmalar ve ayarlamalar için kurulum tümleştirmesi, bu özellik Field Service'ta Finance and Operations'tan stok düzeyleri eşitlemesi ile kullanılıyorsa, önemlidir.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="bd5cd-130">Stok düzeylerinin Finance and Operations'tan üstlenildiği ürünler ve ambarlar, Gelişmiş Sorgu ve Filtreleme (Power Query) ile kontrol edilebilir.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="bd5cd-131">Not: Field Service'ta birden fazla ambar (Harici Korunan = Hayır) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="bd5cd-132">Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="bd5cd-133">Bu durumda Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="bd5cd-134">Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede ve Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek istiyorsanız ek bilgiye bakın.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="bd5cd-135">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="bd5cd-135">Field Service CRM solution</span></span>
<span data-ttu-id="bd5cd-136">Harici ürün bilgisi yalnızca arka uç içinde tümleştirme için kullanılan yeni bir varlık bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="bd5cd-137">Finance and Operations ve stok düzeyi değerlerinin birleştirilmesinde alır ve daha sonra bu ambarı stok ürünler sonra değişen Manuel Stok günlüklerini değerlere dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="bd5cd-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="bd5cd-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="bd5cd-139">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="bd5cd-139">In the Data Integration project</span></span>
<span data-ttu-id="bd5cd-140">Gelişmiş Sorgu ve Filtreleme ile filtreler uygulayın, böylece yalnızca istenilen ürünler ve ambarlar stok düzeyi bilgisine Finance and Operations'tan Field Service'a gönderilir.</span><span class="sxs-lookup"><span data-stu-id="bd5cd-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bd5cd-141">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="bd5cd-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="bd5cd-142">Ürün Stoku (Finance and Operations'tan Field Service'a): Ürün stoku</span><span class="sxs-lookup"><span data-stu-id="bd5cd-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="bd5cd-143">[![Veri tümleştirmede şablon eşleme](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="bd5cd-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

