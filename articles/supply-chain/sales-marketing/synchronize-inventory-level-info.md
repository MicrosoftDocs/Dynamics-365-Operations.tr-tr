---
title: Stok düzeyi bilgilerini Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu stok düzey bilgisini Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910292"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="e26a3-103">Stok düzeyi bilgilerini Supply Chain Management'tan Field Service'e eşitleme</span><span class="sxs-lookup"><span data-stu-id="e26a3-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e26a3-104">Bu konu stok düzey bilgisini Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="e26a3-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="e26a3-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="e26a3-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e26a3-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="e26a3-106">Templates and tasks</span></span>
<span data-ttu-id="e26a3-107">Aşağıdaki şablon ve temel görevler, eldeki stok düzeylerini Supply Chain Management'tan Field Service'e eşitlemede kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e26a3-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="e26a3-108">**Veri Tümleştirmesindeki Şablon**</span><span class="sxs-lookup"><span data-stu-id="e26a3-108">**Template in Data integration**</span></span>
- <span data-ttu-id="e26a3-109">Ürün Stoku (Supply Chain Management'tan Field Service'e)</span><span class="sxs-lookup"><span data-stu-id="e26a3-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="e26a3-110">**Veri tümleştirme projesindeki görev**</span><span class="sxs-lookup"><span data-stu-id="e26a3-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="e26a3-111">Ürün stoku</span><span class="sxs-lookup"><span data-stu-id="e26a3-111">Product inventory</span></span>

<span data-ttu-id="e26a3-112">Aşağıdaki eşitleme görevlerinin, stok düzeylerinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="e26a3-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="e26a3-113">Ambarlar (Supply Chain Management'tan Field Service'e)</span><span class="sxs-lookup"><span data-stu-id="e26a3-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="e26a3-114">Stok birimli Field Service ürünleri (Supply Chain Management'tan Sales'e)</span><span class="sxs-lookup"><span data-stu-id="e26a3-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="e26a3-115">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="e26a3-115">Entity set</span></span>

| <span data-ttu-id="e26a3-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="e26a3-116">Field Service</span></span>                      | <span data-ttu-id="e26a3-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e26a3-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="e26a3-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="e26a3-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="e26a3-119">Dataverse ambara göre eldeki stok</span><span class="sxs-lookup"><span data-stu-id="e26a3-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="e26a3-120">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="e26a3-120">Entity flow</span></span>
<span data-ttu-id="e26a3-121">Finance and Operations'tan stok seviyesi bilgisi Field Service'a seçilen ürünler için gönderildi.</span><span class="sxs-lookup"><span data-stu-id="e26a3-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="e26a3-122">Düzey Stok bilgileri şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="e26a3-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="e26a3-123">Eldeki miktarı (geçerli kayıtlı fiziksel olarak ambarda miktar)</span><span class="sxs-lookup"><span data-stu-id="e26a3-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="e26a3-124">Sipariş miktarı (toplam kaydedilen siparişindeki miktar - satış siparişleri gibi)</span><span class="sxs-lookup"><span data-stu-id="e26a3-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="e26a3-125">Sipariş edilen toplam miktar (toplam kaydedilen sipariş tutarı - satınalma siparişleri gibi)</span><span class="sxs-lookup"><span data-stu-id="e26a3-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="e26a3-126">Bu bilgiler her ambar için serbest bırakılan ürün başına yakalanan ve stok düzeyini değiştiğinde, değişiklik izlemeyi dayalı eşitlenmiş.</span><span class="sxs-lookup"><span data-stu-id="e26a3-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="e26a3-127">Field Service'teki düzeylerin Supply Chain Management'taki düzeylerle eşleşmesi için, Field Service'te, tümleştirme çözümü, delta için stok günlükleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e26a3-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="e26a3-128">Supply Chain Management, stok düzeyleri için üst görevi görür.</span><span class="sxs-lookup"><span data-stu-id="e26a3-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="e26a3-129">Bu nedenle Field Service'ten Supply Chain Management'a iş emirleri, aktarmalar ve ayarlamalar için kurulum tümleştirmesi, bu özellik Field Service'te Supply Chain Management'tan stok düzeyleri eşitlemesi ile kullanılıyorsa, önemlidir.</span><span class="sxs-lookup"><span data-stu-id="e26a3-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="e26a3-130">Stok düzeylerinin Supply Chain Management'tan üstlenildiği ürünler ve ambarlar, Gelişmiş Sorgu ve Filtreleme (Power Query) ile denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="e26a3-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="e26a3-131">Field Services'te birden fazla ambar (**Harici Korunan = Hayır**) oluşturmak ve bunları Supply Chain Management'ta tek bir ambara eşlemek Gelişmiş sorgu ve filtreleme işlevleriyle mümkündür.</span><span class="sxs-lookup"><span data-stu-id="e26a3-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e26a3-132">Bu, Field Service'in ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Supply Chain Management'a göndermesini istediğiniz durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e26a3-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="e26a3-133">Bu durumda, Field Service, Supply Chain Management'tan stok düzeyi güncelleştirmeleri almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="e26a3-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="e26a3-134">Daha fazla bilgi için bkz. [Field Service'ten Supply Chain Management'a stok ayarlamalarını eşitleme](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Field Service'teki iş emirlerini Supply Chain Management'taki projeyle bağlantılı satış siparişlerine eşitleme](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="e26a3-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e26a3-135">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="e26a3-135">Field Service CRM solution</span></span>
<span data-ttu-id="e26a3-136">**Harici ürün stoku** varlığı yalnızca arka uç tümleştirmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e26a3-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="e26a3-137">Bu varlık tümleştirmedeki Supply Chain Management'tan stok düzeyi değerlerini alır ve bu değerleri, Ambardaki Stok ürünlerini değiştiren Manuel stok günlüklerine dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="e26a3-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e26a3-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="e26a3-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="e26a3-139">Veri tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="e26a3-139">Data integration</span></span>
<span data-ttu-id="e26a3-140">Projenin çalışması için, Tümleştirme anahtarının msdynce_externalproductinventories için güncelleştirilmiş olduğundan emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e26a3-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="e26a3-141">**Veri tümleştirmesi > Bağlantı kümeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e26a3-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="e26a3-142">Kullanılan Bağlantı kümesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e26a3-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="e26a3-143">**Tümleştirme anahtarı** sekmesinde, aşağıdaki anahtarların msdynce_externalproductinventories öğesine eklendiğinden emin olun:</span><span class="sxs-lookup"><span data-stu-id="e26a3-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="e26a3-144">msdynce_productnumber (Ürün Numarası)</span><span class="sxs-lookup"><span data-stu-id="e26a3-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="e26a3-145">msdynce_warehouseid (Ambar Kodu)</span><span class="sxs-lookup"><span data-stu-id="e26a3-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="e26a3-146">Veri tümleştirme projesi</span><span class="sxs-lookup"><span data-stu-id="e26a3-146">Data integration project</span></span>
<span data-ttu-id="e26a3-147">Gelişmiş Sorgu ve Filtreleme ile filtreler uygulayarak yalnızca belirli ürünler ve ambarların Supply Chain Management'tan Field Service'e stok düzeyi bilgileri göndermesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e26a3-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e26a3-148">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="e26a3-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="e26a3-149">Ürün stoku (Supply Chain Management'tan Field Service'e): Ürün stoku</span><span class="sxs-lookup"><span data-stu-id="e26a3-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="e26a3-150">[![Veri tümleştirmede şablon eşleme](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="e26a3-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]