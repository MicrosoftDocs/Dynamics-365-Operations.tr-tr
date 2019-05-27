---
title: Stok hareketlerini ve ayarlamaları Field Service'tan Finance and Operations'a eşitlemek
description: Bu konu stok düzeltmelerini ve aktarmalarını Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: e94fa87c2f8b66574d6c5b2930cebf2e1b144fea
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536308"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="68913-103">Stok ayarlamalarını Field Service'tan Finance and Operations'a eşitlemek</span><span class="sxs-lookup"><span data-stu-id="68913-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68913-104">Bu konu stok düzeltmelerini ve aktarmalarını Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="68913-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="68913-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="68913-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="68913-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="68913-106">Templates and tasks</span></span>
<span data-ttu-id="68913-107">Aşağıdaki şablon ve altındaki görevler, stok düzeltmelerini ve aktarmalarını Microsoft Dynamics 365 for Field Service üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68913-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="68913-108">**Veri Tümleştirmesindeki Şablonlar**</span><span class="sxs-lookup"><span data-stu-id="68913-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="68913-109">Stok Ayarlama (Field Service'ten Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="68913-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="68913-110">Stok Aktarmaları (Field Service'ten Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="68913-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="68913-111">**Veri tümleştirme projelerindeki görevler**</span><span class="sxs-lookup"><span data-stu-id="68913-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="68913-112">Stok Düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="68913-112">Inventory Adjustments</span></span>
- <span data-ttu-id="68913-113">Stok Transferleri</span><span class="sxs-lookup"><span data-stu-id="68913-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="68913-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="68913-114">Entity set</span></span>
| <span data-ttu-id="68913-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="68913-115">Field Service</span></span>                     | <span data-ttu-id="68913-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68913-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="68913-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="68913-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="68913-118">CDS Stok ayarlama günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="68913-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="68913-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="68913-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="68913-120">CDS stok transfer günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="68913-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="68913-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="68913-121">Entity flow</span></span>
<span data-ttu-id="68913-122">Field Service'ta gerçekleştirilen stok düzeltmeleri ve aktarmaları, **Deftere nakil durumu**, **Oluşturuldu**'dan **Deftere Nakledildi**'ye değiştirildikten sonra Finance and Operations'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="68913-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="68913-123">Bu durumda, ayarlama veya transfer emri kilitlenir ve salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="68913-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="68913-124">Bu, düzeltmelerin ve aktarmaların Finance and Operations içinde deftere nakledilebileceği, ancak değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="68913-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="68913-125">Finance and Operations'ta, tümleştirme ile oluşturulmuş ayarlamalar ve hareketler sırasında stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68913-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="68913-126">Toplu işi etkinleştirmenin ayrıntıları için aşağıdaki önkoşullara bakın.</span><span class="sxs-lookup"><span data-stu-id="68913-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="68913-127">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="68913-127">Field Service CRM solution</span></span> 
<span data-ttu-id="68913-128">**Stok birimi** alanı, **Ürün** varlığına eklendi.</span><span class="sxs-lookup"><span data-stu-id="68913-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="68913-129">Bu alan, Satış ve Stok birimi her zaman Finance and Operations içinde olmadığından ve Stok Birimi, Finance and Operations içinde Ambar Stoku için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="68913-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="68913-130">Hem stok ayarlama hem de stok aktarma için bir ürünü bir stok ayarlama ürünü üzerinde ayarladığınızda, birim, stok ürün değerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="68913-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="68913-131">**Birim** alanında bir değer bulunursa, alan Stok ayarlama ürününde kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="68913-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="68913-132">**Deftere Nakil Durumu** alanı, hem **Stok Ayarlama** varlığına hem de **Stok aktarma** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="68913-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="68913-133">Bu alan, bir ayarlama veya aktarma Finance and Operations'a gönderildiğinde filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68913-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="68913-134">Bu alan için varsayılan Oluşturuldu (1), ancak Finance and Operations'a gönderilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="68913-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="68913-135">Değeri Deftere Nakledildi (2) olarak güncelleştirirseniz, Finance and Operations'a gönderilir, ancak bundan sonra düzeltme ve transfer edemeyeceksiniz veya yeni satırlar ekleyemeyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="68913-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="68913-136">**Numara serisi** alanı, **Stok ayarlama ürünü** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="68913-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="68913-137">Bu alan, tümleştirmenin benzersiz bir numaraya sahip olmasını sağlar, böylece tümleştirme düzeltmeyi oluşturabilir ve güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="68913-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="68913-138">İlk stok ayarlama ürününüzü oluşturduğunuzda, **P2C AutoNumber** varlığında yeni bir kayıt oluşturarak numara serisini ve kullanılan öneki korur.</span><span class="sxs-lookup"><span data-stu-id="68913-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="68913-139">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="68913-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="68913-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68913-140">Finance and Operations</span></span>
<span data-ttu-id="68913-141">Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş kullanarak otomatik olarak deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="68913-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="68913-142">Bu, şuradan etkinleştirilir: **Stok yönetimi > Periyodik görevler > CDS tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri**.</span><span class="sxs-lookup"><span data-stu-id="68913-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="68913-143">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="68913-143">Template mapping in Data integration</span></span>

<span data-ttu-id="68913-144">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="68913-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="68913-145">Stok ayarlama (Field Service'tan Fin and Ops'a): Stok ayarlama</span><span class="sxs-lookup"><span data-stu-id="68913-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="68913-146">[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="68913-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="68913-147">Stok aktarma (Field Service'tan Fin and Ops'a): Stok aktarma</span><span class="sxs-lookup"><span data-stu-id="68913-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="68913-148">[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="68913-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
