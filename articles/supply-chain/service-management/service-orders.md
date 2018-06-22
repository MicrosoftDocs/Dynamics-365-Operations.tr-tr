---
title: "Servis siparişleri"
description: "Bir servis siparişi, bir servis teknisyeninin belirli bir tarihte müşteri tesisine yaptığı ziyareti gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 647bbe9cca0167d33048ad07e092708f90b41fc3
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="service-orders"></a><span data-ttu-id="b24ff-103">Servis siparişleri</span><span class="sxs-lookup"><span data-stu-id="b24ff-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b24ff-104">Bir servis siparişi, bir servis teknisyeninin belirli bir tarihte müşteri tesisine yaptığı ziyareti gösterir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="b24ff-105">Her servis siparişi bir veya daha fazla servis siparişi satırından oluşur.</span><span class="sxs-lookup"><span data-stu-id="b24ff-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="b24ff-106">Servis siparişi satırları servis teknisyeninin gerçekleştirmesi gereken saat sayısını ve ilgili maddeleri, giderleri ve ücretleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="b24ff-107">Servis siparişi satırına görevleri ve nesneleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="b24ff-108">Servis siparişi satırlarını daha sonra göreve ya da nesneye göre gruplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="b24ff-109">Ayrıca, stokta listelenen maddeleri servis siparişi satırlarına iliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="b24ff-110">Servis siparişleri oluştur</span><span class="sxs-lookup"><span data-stu-id="b24ff-110">Create service orders</span></span>

<span data-ttu-id="b24ff-111">Servis siparişlerini servis sözleşmesini ve sözleşmede yer alan satırları temel alarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="b24ff-112">Ancak, bir servis sözleşmesiyle ilişkili olan servis siparişlerini yalnızca sözleşmede belirtilen dönemde oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="b24ff-113">Örneğin, bir servis sözleşmesi 2011 takvim yılı için geçerliyse, sözleşme için 1 Ocak 2011 ve 31 Aralık 2011 arasında servis siparişleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="b24ff-114">Servis siparişlerini, sözleşmeyle ilişkilendirmeden tek tek de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="b24ff-115">Bu servis siparişleri zamanlanmamış veya bir defalık servis ziyaretlerini işlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="b24ff-116">Örneğin, Mart ayında müşteriniz servis sözleşmesinde belirtilenlere ek olarak iki makineye servis yapılmasın ister.</span><span class="sxs-lookup"><span data-stu-id="b24ff-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="b24ff-117">Bu görev için servis siparişlerini oluşturursunuz ancak bunları sözleşmeyle ilişkilendirmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b24ff-118">Bir servis sözleşmesiyle ilişkilendirilmemiş servis siparişleri oluşturmak için <STRONG>Servis yönetimi parametreleri</STRONG> formunda <STRONG>Servis sözleşmesi olmadan izin ver</STRONG> onay kutusunu işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="b24ff-119">**Senaryo**</span><span class="sxs-lookup"><span data-stu-id="b24ff-119">**Scenario**</span></span>

<span data-ttu-id="b24ff-120">Aşağıdaki senaryo bir servis sözleşmesiyle ilişkili olmayan bir servis siparişi oluşturmanın yararlı olacağı başka bir durumu açıklar.</span><span class="sxs-lookup"><span data-stu-id="b24ff-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="b24ff-121">Şirket dağıtıcısı bir asansöre acil servis yapılmasını talep eden bir arama alır.</span><span class="sxs-lookup"><span data-stu-id="b24ff-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="b24ff-122">Bir servis sözleşmesi ve servis için bir proje ayarlamak için zaman yoktur.</span><span class="sxs-lookup"><span data-stu-id="b24ff-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="b24ff-123">Bu nedenle dağıtıcı bir servis siparişini doğrudan **servis siparişleri** formunda oluşturur, servis siparişini varolan bir projeye ekler ve servis siparişi satırları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b24ff-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="b24ff-124">Dağıtıcı servis sözleşmesiyle ilişkili olmayan işleri kaydetmek üzere mevcut bir servis siparişi için bir görev veya nesne ilişkisi oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="b24ff-125">Daha fazla bilgi için bkz. [Servis siparişlerini el ile oluşturma](create-service-orders-manually.md) ve [Servis görevi ilişkileri oluşturma](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="b24ff-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="b24ff-126">Servis siparişlerinin ilerlemesini izleme</span><span class="sxs-lookup"><span data-stu-id="b24ff-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="b24ff-127">Farklı takımlar ve iş süreçleri üzerinden bir satış siparişi ilerlemesini izlemek için servis siparişleri aşamaları ve neden kodları için bir sistem ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="b24ff-128">Her aşama için izin verilen eylemleri belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="b24ff-129">Daha fazla bilgi için bkz. [Neden kodları oluşturma](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b24ff-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="b24ff-130">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="b24ff-130">**Example**</span></span>

<span data-ttu-id="b24ff-131">Bir servis siparişi dağıtıcı tarafından onaylanır.</span><span class="sxs-lookup"><span data-stu-id="b24ff-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="b24ff-132">Dağıtıcı servis siparişi aşamasını güncelleştirir ve servis siparişinin servis teknisyenine serbest bırakıldığını belirten bir neden kodu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="b24ff-133">Teknisyen müşteri tesisine gider ve servisi yerine getirir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="b24ff-134">Servis siparişleri için madde gereksinimleri belirtme</span><span class="sxs-lookup"><span data-stu-id="b24ff-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="b24ff-135">Servis siparişleri için gerekli olan stok maddeleri belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="b24ff-136">Bununla birlikte, servis siparişi bir proje ile ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b24ff-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="b24ff-137">Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="b24ff-138">**Örnek**</span><span class="sxs-lookup"><span data-stu-id="b24ff-138">**Example**</span></span>

<span data-ttu-id="b24ff-139">Servis sözleşmesinden oluşturulan servis siparişleri sevk memuru tarafından işlenir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="b24ff-140">Birinci servis siparişinde, dağıtıcı servis teknisyenin eldeki stokta bulunmayan önemli bir yedek parçaya gereksinimi olduğunu fark eder.</span><span class="sxs-lookup"><span data-stu-id="b24ff-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="b24ff-141">Bu nedenle, dağıtıcı yedek parça için doğrudan servis siparişinden bir madde gereksinimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b24ff-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="b24ff-142">Satırları taşıma ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="b24ff-142">Move and post lines</span></span>

<span data-ttu-id="b24ff-143">Servis teknisyeni servis ziyaretinden döner ve sonra değişikliklere göre servis siparişi satırlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="b24ff-144">Servis ziyaretindeyken teknisyen bir sonraki servis ziyaretinde yapılması planlanan bir servis işini gerçekleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="b24ff-145">Bu nedenle, teknisyen sonraki servis ziyaretindeki satırları geçerli servis ziyaretine taşır.</span><span class="sxs-lookup"><span data-stu-id="b24ff-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="b24ff-146">Teknisyen ardından servis siparişini deftere nakleder.</span><span class="sxs-lookup"><span data-stu-id="b24ff-146">The technician then posts the service order.</span></span> <span data-ttu-id="b24ff-147">Daha fazla bilgi için bkz. [Servis siparişi satırlarını taşıma](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="b24ff-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="b24ff-148">Servis siparişlerini iptal et</span><span class="sxs-lookup"><span data-stu-id="b24ff-148">Cancel service orders</span></span>

<span data-ttu-id="b24ff-149">Söz konusu işin iptal edilmesi nedeniyle, Ocak ayı için oluşturulan diğer servis siparişlerinden biri geçersiz hale gelmiştir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="b24ff-150">Bu nedenle, servis dağıtıcısı servis siparişini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b24ff-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="b24ff-151">Daha fazla bilgi için bkz. [Servis siparişlerini iptal etme](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="b24ff-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="b24ff-152">Projelerden deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="b24ff-152">Post from projects</span></span>

<span data-ttu-id="b24ff-153">Her haftanın sonunda, dağıtıcı belirli bir projeye iliştirilmiş tüm servis siparişlerini deftere nakletmek ister.</span><span class="sxs-lookup"><span data-stu-id="b24ff-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="b24ff-154">Bu nedenle, dağıtıcı **Projeler** formunda ilgili projeyi bulur ve tamamlanan servis siparişlerini deftere nakleder.</span><span class="sxs-lookup"><span data-stu-id="b24ff-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="b24ff-155">Daha fazla bilgi için bkz. [Servis siparişlerini deftere nakletme (sınıf formu)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="b24ff-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="b24ff-156">Servis siparişlerini sil</span><span class="sxs-lookup"><span data-stu-id="b24ff-156">Delete service orders</span></span>

<span data-ttu-id="b24ff-157">Yılın ikinci yarısında müşteriniz servis ziyaretlerinin çok az sıklıkta gerçekleştiğine karar verir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="b24ff-158">Servis anlaşmasındaki geri kalan süre için yeni ve daha sık bir servis ziyaretleri dizisi oluşturmanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="b24ff-159">Bu nedenle, mevcut servis siparişlerini silmeniz ve yeni servis siparişleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b24ff-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="b24ff-160">Daha fazla bilgi için bkz. [Servis siparişlerini silme](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="b24ff-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b24ff-161">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b24ff-161">See also</span></span>

<span data-ttu-id="b24ff-162">[Servis siparişleri (form)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b24ff-162">[Service orders (form)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span></span>

  


