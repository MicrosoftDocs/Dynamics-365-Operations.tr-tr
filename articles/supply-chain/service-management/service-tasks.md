---
title: Servis görevlerine genel bakış
description: Servis görevlerini, servis siparişi sırasında tamamlanacak görevleri açıklamak için kullanın. Teknisyenler ve müşteriler bu bilgileri görebilir.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebad3a5fdd65155eb822dcd69a1d2624a1891337
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835834"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="7da17-104">Servis görevlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7da17-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7da17-105">Servis görevlerini, servis siparişi sırasında tamamlanacak görevleri açıklamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="7da17-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="7da17-106">Teknisyenler ve müşteriler bu bilgileri görebilir.</span><span class="sxs-lookup"><span data-stu-id="7da17-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="7da17-107">Servis görevlerini **Servis görevleri** sayfasında oluşturur ve servis görevi ilişkileri oluşturarak bu görevleri belirli bir servis sözleşmesi veya servis siparişiyle ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da17-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="7da17-108">Servis görevi ilişkisi oluşturduğunuz her durumda aşağıdakileri oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7da17-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="7da17-109">Görevle ilgili olarak, görev hakkında teknisyenin bilmesi gereken ayrıntılı teknik talepler gibi dahili notlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da17-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="7da17-110">Müşterinin görebildiği harici notlar.</span><span class="sxs-lookup"><span data-stu-id="7da17-110">External notes that the customer can see.</span></span> <span data-ttu-id="7da17-111">Bunlar, müşteriyle servis şirketi arasındaki sözleşme uyarınca tamamlanması gereken görevin daha az teknik olan bir açıklamasını sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="7da17-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="7da17-112">Servis göreviyle servis siparişi veya servis sözleşmesi arasında servis görevi ilişkisini ayarladığınızda, geçerli servis siparişi veya servis sözleşmesi için servis siparişi satırları veya servis sözleşmesi satırları oluştururken bu servis görevini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da17-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="7da17-113">Servis sözleşmesinden servis siparişleri oluştururken, servis siparişi satırlarını servis siparişleri halinde gruplandırmak için her servis sözleşmesi satırına atanmış servis görevlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da17-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="7da17-114">Servis görevi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7da17-114">Create a service task</span></span>

1. <span data-ttu-id="7da17-115">**Servis yönetimi** \> **Kurulum** \> **Servis görevleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7da17-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="7da17-116">Yeni satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7da17-116">Create a new line.</span></span>
3. <span data-ttu-id="7da17-117">Servis kodu ile açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="7da17-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="7da17-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="7da17-118">Example</span></span>

<span data-ttu-id="7da17-119">Teknisyenin müşterinin tesisinde bir dişli kutusu (servis nesnesi GB-1234) üzerinde iki iş tamamlaması gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="7da17-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="7da17-120">Müşteri için bir servis sözleşmesi oluşturulur ve birkaç hareket işlerle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="7da17-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="7da17-121">İki iş için servis sözleşmesi ve servis sözleşmesi satırları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="7da17-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="7da17-122">Servis sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="7da17-122">Service agreement</span></span>

| <span data-ttu-id="7da17-123">Proje</span><span class="sxs-lookup"><span data-stu-id="7da17-123">Project</span></span> | <span data-ttu-id="7da17-124">Servis sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="7da17-124">Service agreement</span></span> | <span data-ttu-id="7da17-125">Tanım</span><span class="sxs-lookup"><span data-stu-id="7da17-125">Description</span></span>                                  | <span data-ttu-id="7da17-126">Grup</span><span class="sxs-lookup"><span data-stu-id="7da17-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="7da17-127">9012</span><span class="sxs-lookup"><span data-stu-id="7da17-127">9012</span></span>    | <span data-ttu-id="7da17-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="7da17-128">000008\_001</span></span>       | <span data-ttu-id="7da17-129">İnceleme ve rutin değiştirme – GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="7da17-130">Prim</span><span class="sxs-lookup"><span data-stu-id="7da17-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="7da17-131">Servis sözleşmesi maddeleri</span><span class="sxs-lookup"><span data-stu-id="7da17-131">Service agreement lines</span></span>

| <span data-ttu-id="7da17-132">Tanım</span><span class="sxs-lookup"><span data-stu-id="7da17-132">Description</span></span>             | <span data-ttu-id="7da17-133">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="7da17-133">Transaction type</span></span> | <span data-ttu-id="7da17-134">Servis nesnesi</span><span class="sxs-lookup"><span data-stu-id="7da17-134">Service object</span></span> | <span data-ttu-id="7da17-135">Servis görevi</span><span class="sxs-lookup"><span data-stu-id="7da17-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="7da17-136">İnceleme ve temizleme</span><span class="sxs-lookup"><span data-stu-id="7da17-136">Inspection and cleaning</span></span> | <span data-ttu-id="7da17-137">Saat</span><span class="sxs-lookup"><span data-stu-id="7da17-137">Hour</span></span>             | <span data-ttu-id="7da17-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-138">GB-1234</span></span>        | <span data-ttu-id="7da17-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-139">I/C - GB1234</span></span> |
| <span data-ttu-id="7da17-140">Seyahat</span><span class="sxs-lookup"><span data-stu-id="7da17-140">Travel</span></span>                  | <span data-ttu-id="7da17-141">Gider</span><span class="sxs-lookup"><span data-stu-id="7da17-141">Expense</span></span>          | <span data-ttu-id="7da17-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-142">GB-1234</span></span>        | <span data-ttu-id="7da17-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-143">I/C - GB1234</span></span> |
| <span data-ttu-id="7da17-144">Malzemeler</span><span class="sxs-lookup"><span data-stu-id="7da17-144">Materials</span></span>               | <span data-ttu-id="7da17-145">Madde</span><span class="sxs-lookup"><span data-stu-id="7da17-145">Item</span></span>             | <span data-ttu-id="7da17-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-146">GB-1234</span></span>        | <span data-ttu-id="7da17-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-147">I/C - GB1234</span></span> |
| <span data-ttu-id="7da17-148">Rutin değiştirme</span><span class="sxs-lookup"><span data-stu-id="7da17-148">Routine replacement</span></span>     | <span data-ttu-id="7da17-149">Saat</span><span class="sxs-lookup"><span data-stu-id="7da17-149">Hour</span></span>             | <span data-ttu-id="7da17-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-150">GB-1234</span></span>        | <span data-ttu-id="7da17-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-151">RR - GB1234</span></span>  |
| <span data-ttu-id="7da17-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="7da17-152">GR-1</span></span>                    | <span data-ttu-id="7da17-153">Madde</span><span class="sxs-lookup"><span data-stu-id="7da17-153">Item</span></span>             | <span data-ttu-id="7da17-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-154">GB-1234</span></span>        | <span data-ttu-id="7da17-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-155">RR - GB1234</span></span>  |
| <span data-ttu-id="7da17-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="7da17-156">GR-5</span></span>                    | <span data-ttu-id="7da17-157">Madde</span><span class="sxs-lookup"><span data-stu-id="7da17-157">Item</span></span>             | <span data-ttu-id="7da17-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="7da17-158">GB-1234</span></span>        | <span data-ttu-id="7da17-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-159">RR - GB1234</span></span>  |

<span data-ttu-id="7da17-160">İki işin servis sözleşmesi satırlarına eklenmiş iki servis görevi vardır.</span><span class="sxs-lookup"><span data-stu-id="7da17-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="7da17-161">Servis görevleri, her işe ait olan hareketleri belirler.</span><span class="sxs-lookup"><span data-stu-id="7da17-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="7da17-162">İlk durumda, I/C - GB1234 servis görevi, GB-1234 parçasını inceleme ve temizleme işlemleri kapsamındaki tüm servis sözleşmesi satırlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="7da17-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="7da17-163">İkinci durumda, RR - GB1234 servis görevi rutin değiştirme görevinin tamamlanması kapsamındaki tüm servis sözleşmesi satırlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="7da17-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="7da17-164">Servis görevlerini bu belirli anlaşmaya bağlayan servis görevi ilişkileri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7da17-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="7da17-165">Servis görevleri</span><span class="sxs-lookup"><span data-stu-id="7da17-165">Service tasks</span></span>

| <span data-ttu-id="7da17-166">Servis görevi</span><span class="sxs-lookup"><span data-stu-id="7da17-166">Service task</span></span> | <span data-ttu-id="7da17-167">Açıklama</span><span class="sxs-lookup"><span data-stu-id="7da17-167">Description</span></span>                             | <span data-ttu-id="7da17-168">Dahili not</span><span class="sxs-lookup"><span data-stu-id="7da17-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="7da17-169">Harici not</span><span class="sxs-lookup"><span data-stu-id="7da17-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="7da17-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-170">I/C - GB1234</span></span> | <span data-ttu-id="7da17-171">GB-1234 vites kutusunun denetlenmesi</span><span class="sxs-lookup"><span data-stu-id="7da17-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="7da17-172">GB-1234 vites kutusunu görsel ve mekanik olarak inceleme ve temizleme</span><span class="sxs-lookup"><span data-stu-id="7da17-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="7da17-173">Vites kutusunun rutin denetimi</span><span class="sxs-lookup"><span data-stu-id="7da17-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="7da17-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="7da17-174">RR - GB1234</span></span>  | <span data-ttu-id="7da17-175">GB-1234 içindeki parçaların rutin değiştirilmesi</span><span class="sxs-lookup"><span data-stu-id="7da17-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="7da17-176">GR-1 ve GR-5 bileşenlerinin rutin servis değiştirmesi (2002'den önce üretilmiş vites kutularında GR-2 bileşeni de değiştirilsin)</span><span class="sxs-lookup"><span data-stu-id="7da17-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="7da17-177">Parçaları rutin olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="7da17-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="7da17-178">Servis siparişlerini gruplama</span><span class="sxs-lookup"><span data-stu-id="7da17-178">Group service orders</span></span>

<span data-ttu-id="7da17-179">Servis siparişlerini otomatik olarak oluşturduğunuzda, servis görevlerini gruplandırma ölçütleri olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7da17-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="7da17-180">Servis siparişlerini belirli servis görevlerine göre gruplandırmak için, servis sözleşmesini temel alan servis siparişlerinin gruplandırılmasında ilk gruplandırma ölçütü olarak servis görevi kodunun kullanılacağını servis sözleşmesinde tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="7da17-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="7da17-181">**Servis görevine göre gruplandırma**</span><span class="sxs-lookup"><span data-stu-id="7da17-181">**Group by service task**</span></span>

1. <span data-ttu-id="7da17-182">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7da17-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="7da17-183">**Kurulum** sekmesinde, **Servis siparişlerini birleştir** alanında **Servis görevine göre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7da17-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]