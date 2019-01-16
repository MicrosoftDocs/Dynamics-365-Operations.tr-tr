---
title: "Stok hareketlerini ve ayarlamaları Field Service'tan Finance and Operations'a eşitlemek"
description: "Bu konu, stok ayarlamaları ve aktarmaları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="cb1a9-103">Stok ayarlamalarını Field Service'tan Finance and Operations'a eşitlemek</span><span class="sxs-lookup"><span data-stu-id="cb1a9-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cb1a9-104">Bu konu, stok ayarlamaları ve aktarmaları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cb1a9-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="cb1a9-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cb1a9-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="cb1a9-106">Templates and tasks</span></span>
<span data-ttu-id="cb1a9-107">Aşağıdaki şablon, stok ayarlamaları ve aktarmaları eşitlemelerini Microsoft Dynamics 365 for Field Service'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="cb1a9-108">**Veri tümleştirmesindeki şablonların adı:**</span><span class="sxs-lookup"><span data-stu-id="cb1a9-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="cb1a9-109">Stok Ayarlama (Field Service'ten Finance and Operations'a)</span><span class="sxs-lookup"><span data-stu-id="cb1a9-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="cb1a9-110">Stok Aktarma (Field Service'ten Finance and Operations'a)</span><span class="sxs-lookup"><span data-stu-id="cb1a9-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="cb1a9-111">**Veri tümleştirme projelerindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="cb1a9-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="cb1a9-112">Stok Düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="cb1a9-112">Inventory Adjustments</span></span>
- <span data-ttu-id="cb1a9-113">Stok Transferleri</span><span class="sxs-lookup"><span data-stu-id="cb1a9-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="cb1a9-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="cb1a9-114">Entity set</span></span>
| <span data-ttu-id="cb1a9-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="cb1a9-115">Field Service</span></span>                     | <span data-ttu-id="cb1a9-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cb1a9-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="cb1a9-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="cb1a9-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="cb1a9-118">CDS Stok ayarlama günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="cb1a9-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="cb1a9-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="cb1a9-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="cb1a9-120">CDS stok transfer günlüğü başlıkları ve satırları</span><span class="sxs-lookup"><span data-stu-id="cb1a9-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="cb1a9-121">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="cb1a9-121">Entity flow</span></span>
<span data-ttu-id="cb1a9-122">Field Service'ta gerçekleştirilen stok düzeltmeleri ve aktarmaları, **Deftere nakil durumu**, Oluşturuldu'dan Deftere Nakledildi'ye değiştirildiğinde Finance and Operations'a eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="cb1a9-123">Bu gerçekleştiğinde, ayarlama veya aktarma emri kilitlenir ve salt okunur olur çünkü ayarlamalar ve aktarmalar Finance and Operations'a deftere nakledilebilir ve bu nedenle değiştirilemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="cb1a9-124">Finance and Operations'ta, tümleştirme ile oluşturulmuş ayarlamalar ve hareketler stok günlüklerini otomatik deftere nakletmek üzere bir toplu iş ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="cb1a9-125">Toplu işi etkinleştirmek hakkında ayrıntılar için gereksinimleri aşağıda görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cb1a9-126">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="cb1a9-126">Field Service CRM solution</span></span> 
<span data-ttu-id="cb1a9-127">Stok Birimi alanı, Ürün varlığına eklendi.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="cb1a9-128">Bu alan, Satış ve Stok Birimi her zaman aynı Operasyonlarda olmadığı için gereklidir ve operasyonlardaki Ambar Stoku için Stok Biriminine ihtiyaç duyarız.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="cb1a9-129">Hem Stok Ayarlama hem de Stok Aktarma için bir Ürünü bir Stok Ayarlama Ürünü üzerinde ayarladığınızda, Birim, Ürünler Stok Ürün değerinden alınır.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="cb1a9-130">Birim alanında bir değer bulunursa, alan Stok Ayarlama Ürününde kilitlenir</span><span class="sxs-lookup"><span data-stu-id="cb1a9-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="cb1a9-131">Deftere Nakil Durumu alanı, hem Stok Ayarlama varlığına hem de Stok Aktarma varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="cb1a9-132">Bu alan, bir ayarlama veya aktarma Operasyonlara gönderildiğinde filtre olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="cb1a9-133">Bu alan Oluşturuldu (1) olarak varsayılan alınır ve Operasyonlara gönderilmez.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="cb1a9-134">Değiştirdikleriniz, Deftere Nakledildi (2) olur, operasyonlara gönderilir ancak Ayarlama veya Aktarmada hiçbir şey değiştiremezsiniz veya buna yeni satırlar ekleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="cb1a9-135">Stok Ayarlama Ürün varlığına Numara Serisi alanı eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="cb1a9-136">Bu alan, tümleştirmenin Benzersiz bir sayıya sahip olmasına yardımcı olur, böylece tümleştirme oluşturmaları ve güncelleştirmeleri ne zaman yapacağını bilir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="cb1a9-137">İlk Stok Ayarlama Ürününüzü oluşturduğunuzda, P2C AutoNumber varlığında yeni bir kayıt oluşturarak numara serisini ve kullanılan öneki korur.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cb1a9-138">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="cb1a9-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="cb1a9-139">Finance and Operations'ta</span><span class="sxs-lookup"><span data-stu-id="cb1a9-139">In Finance and Operations</span></span>
<span data-ttu-id="cb1a9-140">Tümleştirme tarafından oluşturulan tümleştirme stok günlükleri, bir toplu iş ile otomatik olarak deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="cb1a9-141">Bu, şuradan etkinleştirilir: Stok yönetimi > Periyodik görevler > CDS tümleştirmesi > Deftere nakletme tümleştirme stok günlükleri</span><span class="sxs-lookup"><span data-stu-id="cb1a9-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cb1a9-142">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="cb1a9-142">Template mapping in Data integration</span></span>

<span data-ttu-id="cb1a9-143">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb1a9-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="cb1a9-144">Stok Ayarlama (Field Service'tan Finance and Operations'a): Stok Ayarlama</span><span class="sxs-lookup"><span data-stu-id="cb1a9-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="cb1a9-145">[![Veri tümleştirmede şablon eşleme](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="cb1a9-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="cb1a9-146">Stok Aktarma (Field Service'tan Finance and Operations'a): Stok Aktarma</span><span class="sxs-lookup"><span data-stu-id="cb1a9-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="cb1a9-147">[![Veri tümleştirmede şablon eşleme](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="cb1a9-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

