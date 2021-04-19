---
title: Bulut ve uç ölçek birimleri için ambar siparişleri
description: Bu konuda, ambar ölçek birimi iş yükünün parçası olarak kullanılan ambar siparişi özelliği hakkında bilgi sağlanmaktadır.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2401102ab44f5c24f5cd6f545f30438db0a36cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836698"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="79e7c-103">Bulut ve uç ölçek birimleri için ambar siparişleri</span><span class="sxs-lookup"><span data-stu-id="79e7c-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="79e7c-104">Ölçek birimi iş yükleri kullanıldığında, genel önizlemedeki iş işlevlerin tümü tam olarak desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="79e7c-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="79e7c-105">Ölçek birimlerini kullanıyorsanız yalnızca desteklendiği bu konuda açıkça tanımlanan işlemleri kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="79e7c-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="79e7c-106">Ambar siparişleri nelerdir?</span><span class="sxs-lookup"><span data-stu-id="79e7c-106">What are warehouse orders?</span></span>

<span data-ttu-id="79e7c-107">*Ambar siparişleri*, merkez ve ölçek birimi ambar dağıtımlarını desteklemek için oluşturulan bir sipariş türüdür.</span><span class="sxs-lookup"><span data-stu-id="79e7c-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="79e7c-108">Bunlar, bir ölçek biriminde ambar iş yükü çalıştırırken stok almanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="79e7c-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="79e7c-109">Şu anda yalnızca satınalma siparişleriyle birlikte kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="79e7c-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="79e7c-110">Ambar siparişleri, bir gelen satın alma siparişinin işlenmesi sırasında fiziksel eldeki stoku kaydetmek için Ambar Yönetimi mobil uygulamasının kullanıldığı durumlarda olduğu gibi, ambar yönetimi işleminin bir parçası olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="79e7c-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="79e7c-111">Ambar siparişleri, ambar yönetim işlemlerini kullanmak üzere etkinleştirilen ölçek birimi ambarının ve ürünlerinin belirtildiği satınalma siparişleri için kullanılabilen bir *Ambara serbest bırak* işleminin parçası olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79e7c-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79e7c-112">Ambar siparişleri yalnızca [bulut ve uç ölçek birimleri için ambar yönetimi iş yüklerini](cloud-edge-workload-warehousing.md) kullanan dağıtımlarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="79e7c-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="79e7c-113">Ambar siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="79e7c-113">Create a warehouse order</span></span>

<span data-ttu-id="79e7c-114">Ambar siparişi oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="79e7c-115">Merkezde çalışan Microsoft Dynamics 365 Supply Chain Management kurulumunda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="79e7c-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="79e7c-116">(Merkezde oturumunuz açıkken *Ambara serbest bırak* işlemini başlatmanız gerekir.)</span><span class="sxs-lookup"><span data-stu-id="79e7c-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="79e7c-117">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="79e7c-118">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="79e7c-119">İlgili ambar siparişi satırlarını görüntülemek için ilgili satınalma siparişini açın, **Satınalma siparişi satırları** bölümünde bir satır seçin ve ardından araç çubuğunda **Ambar \> Ambar siparişi satırları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="79e7c-120">Tüm satırları görüntülemek için **Ambar yönetimi \> Sorgular ve raporlar \> Ambar siparişi satırları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="79e7c-121">**Ambar yönetimi > Serbest bırakmadan ambara > Satın alma siparişlerinin otomatik olarak serbest bırakılması**'na giderek de bir toplu işlemden *Ambara serbest bırakma* işlemini tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e7c-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="79e7c-122">Toplu işlemi ayarlarken, sorguya göre belirli satın alma siparişi satırlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e7c-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="79e7c-123">Tipik bir senaryo örneği, ertesi gün gelmesi beklenen tüm onaylanmış satın alma siparişi satırlarını serbest bırakan yinelenen bir toplu işlem ayarlamaktır.</span><span class="sxs-lookup"><span data-stu-id="79e7c-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="79e7c-124">Ambar siparişini iptal etme</span><span class="sxs-lookup"><span data-stu-id="79e7c-124">Cancel a warehouse order</span></span>

<span data-ttu-id="79e7c-125">*Ambara serbest bırak* işlemi kapsamında, satınalma siparişi stok hareketleri ambar siparişlerine bağlıdır ve merkez tarafından güncellenemezler.</span><span class="sxs-lookup"><span data-stu-id="79e7c-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="79e7c-126">Yanlışlıkla ambara serbest bırakırsanız veya başka bir nedenle ambar siparişi satırlarının oluşturulması işlemini tersine çevirmeniz gerekirse ambar siparişi satırlarını iptal etme isteği gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e7c-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="79e7c-127">Ambar siparişi satırlarını iptal etmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="79e7c-128">Merkezde çalışan Supply Chain Management kurulumunda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="79e7c-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="79e7c-129">**Ambar yönetimi \> Sorgular ve raporlar \> Ambar siparişi satırları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="79e7c-130">İlgili satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-130">Select the relevant line.</span></span>
1. <span data-ttu-id="79e7c-131">Eylem Bölmesinde **Ambar siparişi satırlarını iptal et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="79e7c-132">Bekleyen iptal işlemi olan veya iş yükünü ölçek biriminde çalıştıran bir ambarda etkin olarak işlenmekte olan satırlar için satırları iptal etme isteği reddedilir.</span><span class="sxs-lookup"><span data-stu-id="79e7c-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="79e7c-133">Ambar siparişini izleme</span><span class="sxs-lookup"><span data-stu-id="79e7c-133">Monitor a warehouse order</span></span>

<span data-ttu-id="79e7c-134">**Ambar siparişi satırları** görünümünde, **Alınacak miktar** sütunundaki değerleri inceleyerek gelen alım işlemlerinin ilerleme durumunu izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e7c-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="79e7c-135">Ambar Yönetimi mobil uygulaması kullanılarak yapılan çalışmalara ilişkin ayrıntıları görüntülemek için aşağıdaki adımlardan birini izleyin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="79e7c-136">**Ambar yönetimi \> Sorgular ve raporlar \> Ambar satırı siparişleri**'ne gidin ve aradığınız satırları bulmak için filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="79e7c-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="79e7c-137">**Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin ve ilgili satınalma siparişini açın.</span><span class="sxs-lookup"><span data-stu-id="79e7c-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="79e7c-138">**Satınalma siparişi satırları** bölümünde, bir veya daha fazla satır seçin ve araç çubuğunda **Ambar \> Ambar makbuz girişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="79e7c-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]