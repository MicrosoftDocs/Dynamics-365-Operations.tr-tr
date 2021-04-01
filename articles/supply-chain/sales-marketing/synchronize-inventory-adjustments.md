---
title: Stok transferlerini ve düzeltmelerini Field Service'ten Supply Chain Management'a eşitleme
description: Bu konu stok düzeltmelerini ve aktarmalarını Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: fce407a66c339f2ece4bbc37b30243a2ed172d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251901"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="51428-103">Stok transferlerini ve düzeltmelerini Field Service'ten Supply Chain Management'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="51428-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="51428-104">Bu konu stok düzeltmelerini ve aktarmalarını Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="51428-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="51428-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="51428-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="51428-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="51428-106">Templates and tasks</span></span>
<span data-ttu-id="51428-107">Aşağıdaki şablon ve temel görevler, stok düzeltmelerini ve transferlerini Field Service'ten Supply Chain Management'a eşitlemede kullanılır.</span><span class="sxs-lookup"><span data-stu-id="51428-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="51428-108">**Veri Tümleştirmesindeki Şablonlar**</span><span class="sxs-lookup"><span data-stu-id="51428-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="51428-109">Stok Düzeltmesi (Field Service'ten Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="51428-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="51428-110">Stok Transferleri (Field Service'ten Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="51428-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="51428-111">**Veri tümleştirme projelerindeki görevler**</span><span class="sxs-lookup"><span data-stu-id="51428-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="51428-112">Stok Düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="51428-112">Inventory Adjustments</span></span>
- <span data-ttu-id="51428-113">Stok Transferleri</span><span class="sxs-lookup"><span data-stu-id="51428-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="51428-114">Tablo kümesi</span><span class="sxs-lookup"><span data-stu-id="51428-114">Table set</span></span>
| <span data-ttu-id="51428-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="51428-115">Field Service</span></span>                     | <span data-ttu-id="51428-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="51428-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="51428-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="51428-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="51428-118">Dataverse Stok ayarlama günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="51428-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="51428-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="51428-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="51428-120">Dataverse stok transfer günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="51428-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="51428-121">Tablo akışı</span><span class="sxs-lookup"><span data-stu-id="51428-121">Table flow</span></span>
<span data-ttu-id="51428-122">Field Service'ta gerçekleştirilen stok düzeltmeleri ve transferleri, **Deftere nakil durumu**, **Oluşturuldu**'dan **Deftere Nakledildi**'ye değiştirildikten sonra Supply Chain Management'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="51428-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="51428-123">Bu durumda, ayarlama veya transfer emri kilitlenir ve salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="51428-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="51428-124">Bu, düzeltmelerin ve transferlerin Supply Chain Management'ta deftere nakledilebileceği, ancak değiştirilemeyeceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="51428-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="51428-125">Supply Chain Management'ta, tümleştirme ile oluşturulmuş düzeltmeler ve hareketler sırasında stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51428-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="51428-126">Toplu işi etkinleştirmenin ayrıntıları için aşağıdaki önkoşullara bakın.</span><span class="sxs-lookup"><span data-stu-id="51428-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="51428-127">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="51428-127">Field Service CRM solution</span></span> 
<span data-ttu-id="51428-128">**Stok birimi** sütunu, **Ürün** tablosuna eklendi.</span><span class="sxs-lookup"><span data-stu-id="51428-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="51428-129">Bu sütun, Satış ve Stok birimi her zaman Supply Chain Management'ta olmadığından ve Stok Birimi, Supply Chain Management'ta Ambar Stoku için gerekli olduğundan gereklidir.</span><span class="sxs-lookup"><span data-stu-id="51428-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="51428-130">Hem stok ayarlama hem de stok aktarma için bir ürünü bir stok ayarlama ürünü üzerinde ayarladığınızda, birim, stok ürün değerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="51428-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="51428-131">**Birim** sütununda bir değer bulunursa, sütun Stok ayarlama ürününde kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="51428-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="51428-132">**Deftere nakil durumu** sütunu, hem **Stok ayarlama** tablosuna hem de **Stok transferi** tablosuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="51428-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="51428-133">Bu sütun, Supply Chain Management'a bir düzeltme veya transfer gönderildiğinde filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="51428-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="51428-134">Bu sütun için varsayılan değer Oluşturuldu (1) değeridir ancak Supply Chain Management'a gönderilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="51428-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="51428-135">Değeri Deftere Nakledildi (2) olarak güncelleştirirseniz Supply Chain Management'a gönderilir ancak bundan sonra düzeltme ve transfer edemezsiniz veya yeni satırlar ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="51428-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="51428-136">**Numara serisi** sütunu, **Stok ayarlama ürünü** tablosuna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="51428-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="51428-137">Bu sütun, tümleştirmenin benzersiz bir numaraya sahip olmasını sağlar, böylece tümleştirme düzeltmeyi oluşturabilir ve güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="51428-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="51428-138">İlk stok ayarlama ürününüzü oluşturduğunuzda, **P2C AutoNumber** tablosunda yeni bir kayıt oluşturarak numara serisini ve kullanılan ön eki korur.</span><span class="sxs-lookup"><span data-stu-id="51428-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="51428-139">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="51428-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="51428-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="51428-140">Supply Chain Management</span></span>
<span data-ttu-id="51428-141">Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş kullanarak otomatik olarak deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="51428-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="51428-142">Bu, şuradan etkinleştirilir: **Stok yönetimi > Periyodik görevler > Dataverse tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri**.</span><span class="sxs-lookup"><span data-stu-id="51428-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="51428-143">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="51428-143">Template mapping in Data integration</span></span>

<span data-ttu-id="51428-144">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="51428-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="51428-145">Stok düzeltmesi (Field Service'ten Supply Chain Management'a): Stok düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="51428-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="51428-146">[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="51428-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="51428-147">Stok transferi (Field Service'ten Supply Chain Management'a): Stok transferi</span><span class="sxs-lookup"><span data-stu-id="51428-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="51428-148">[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="51428-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]