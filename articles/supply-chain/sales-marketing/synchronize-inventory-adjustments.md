---
title: Stok transferlerini ve düzeltmelerini Field Service'ten Supply Chain Management'a eşitleme
description: Bu konu stok düzeltmelerini ve aktarmalarını Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: d76adf10b9df48f5a7a5196e0469bb7cb1dbb34f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552245"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="682db-103">Stok transferlerini ve düzeltmelerini Field Service'ten Supply Chain Management'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="682db-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="682db-104">Bu konu stok düzeltmelerini ve aktarmalarını Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="682db-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="682db-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="682db-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="682db-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="682db-106">Templates and tasks</span></span>
<span data-ttu-id="682db-107">Aşağıdaki şablon ve temel görevler, stok düzeltmelerini ve transferlerini Field Service'ten Supply Chain Management'a eşitlemede kullanılır.</span><span class="sxs-lookup"><span data-stu-id="682db-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="682db-108">**Veri Tümleştirmesindeki Şablonlar**</span><span class="sxs-lookup"><span data-stu-id="682db-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="682db-109">Stok Düzeltmesi (Field Service'ten Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="682db-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="682db-110">Stok Transferleri (Field Service'ten Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="682db-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="682db-111">**Veri tümleştirme projelerindeki görevler**</span><span class="sxs-lookup"><span data-stu-id="682db-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="682db-112">Stok Düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="682db-112">Inventory Adjustments</span></span>
- <span data-ttu-id="682db-113">Stok Transferleri</span><span class="sxs-lookup"><span data-stu-id="682db-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="682db-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="682db-114">Entity set</span></span>
| <span data-ttu-id="682db-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="682db-115">Field Service</span></span>                     | <span data-ttu-id="682db-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="682db-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="682db-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="682db-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="682db-118">CDS Stok ayarlama günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="682db-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="682db-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="682db-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="682db-120">CDS stok transfer günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="682db-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="682db-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="682db-121">Entity flow</span></span>
<span data-ttu-id="682db-122">Field Service'ta gerçekleştirilen stok düzeltmeleri ve transferleri, **Deftere nakil durumu**, **Oluşturuldu**'dan **Deftere Nakledildi**'ye değiştirildikten sonra Supply Chain Management'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="682db-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="682db-123">Bu durumda, ayarlama veya transfer emri kilitlenir ve salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="682db-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="682db-124">Bu, düzeltmelerin ve transferlerin Supply Chain Management'ta deftere nakledilebileceği, ancak değiştirilemeyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="682db-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="682db-125">Supply Chain Management'ta, tümleştirme ile oluşturulmuş düzeltmeler ve hareketler sırasında stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="682db-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="682db-126">Toplu işi etkinleştirmenin ayrıntıları için aşağıdaki önkoşullara bakın.</span><span class="sxs-lookup"><span data-stu-id="682db-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="682db-127">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="682db-127">Field Service CRM solution</span></span> 
<span data-ttu-id="682db-128">**Stok birimi** alanı, **Ürün** varlığına eklendi.</span><span class="sxs-lookup"><span data-stu-id="682db-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="682db-129">Bu alan, Satış ve Stok birimi her zaman Supply Chain Management'ta olmadığından ve Stok Birimi, Supply Chain Management'ta Ambar Stoku için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="682db-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="682db-130">Hem stok ayarlama hem de stok aktarma için bir ürünü bir stok ayarlama ürünü üzerinde ayarladığınızda, birim, stok ürün değerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="682db-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="682db-131">**Birim** alanında bir değer bulunursa, alan Stok ayarlama ürününde kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="682db-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="682db-132">**Deftere Nakil Durumu** alanı, hem **Stok Ayarlama** varlığına hem de **Stok aktarma** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="682db-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="682db-133">Bu alan, Supply Chain Management'a bir düzeltme veya transfer gönderildiğinde filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="682db-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="682db-134">Bu alan için varsayılan değer Oluşturuldu'dur (1) ancak Supply Chain Management'a gönderilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="682db-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="682db-135">Değeri Deftere Nakledildi (2) olarak güncelleştirirseniz Supply Chain Management'a gönderilir ancak bundan sonra düzeltme ve transfer edemezsiniz veya yeni satırlar ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="682db-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="682db-136">**Numara serisi** alanı, **Stok ayarlama ürünü** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="682db-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="682db-137">Bu alan, tümleştirmenin benzersiz bir numaraya sahip olmasını sağlar, böylece tümleştirme düzeltmeyi oluşturabilir ve güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="682db-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="682db-138">İlk stok ayarlama ürününüzü oluşturduğunuzda, **P2C AutoNumber** varlığında yeni bir kayıt oluşturarak numara serisini ve kullanılan öneki korur.</span><span class="sxs-lookup"><span data-stu-id="682db-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="682db-139">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="682db-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="682db-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="682db-140">Supply Chain Management</span></span>
<span data-ttu-id="682db-141">Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş kullanarak otomatik olarak deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="682db-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="682db-142">Bu, şuradan etkinleştirilir: **Stok yönetimi > Periyodik görevler > CDS tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri**.</span><span class="sxs-lookup"><span data-stu-id="682db-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="682db-143">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="682db-143">Template mapping in Data integration</span></span>

<span data-ttu-id="682db-144">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="682db-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="682db-145">Stok düzeltmesi (Field Service'ten Supply Chain Management'a): Stok düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="682db-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="682db-146">[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="682db-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="682db-147">Stok transferi (Field Service'ten Supply Chain Management'a): Stok transferi</span><span class="sxs-lookup"><span data-stu-id="682db-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="682db-148">[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="682db-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
