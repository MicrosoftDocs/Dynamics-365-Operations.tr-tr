---
title: Planlı siparişleri görüntüleme, yönetme ve onaylama
description: Bu konu, planlama optimizasyonunda planlı siparişlerin nasıl görüntüleneceği, yönetileceği ve onaylanacağı hakkında bilgi sağlar.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935669"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="7dec1-103">Planlı siparişleri görüntüleme, yönetme ve onaylama</span><span class="sxs-lookup"><span data-stu-id="7dec1-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7dec1-104">Bu konu, planlama optimizasyonunda planlı siparişlerin nasıl görüntüleneceği, yönetileceği ve onaylanacağı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7dec1-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="7dec1-105">Planlı siparişleri görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="7dec1-105">View and manage planned orders</span></span>

<span data-ttu-id="7dec1-106">Planlı siparişleri, planlı siparişler listesi sayfasında görüntüleyebilir ve yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dec1-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="7dec1-107">Çalışmak istediğiniz planlı siparişlerin türüne bağlı olarak aşağıdaki konumlardan birine gidin:</span><span class="sxs-lookup"><span data-stu-id="7dec1-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="7dec1-108">Master planlama \> Çalışma alanları \> Master planlama</span><span class="sxs-lookup"><span data-stu-id="7dec1-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="7dec1-109">Master planlama \> Master planlama \> Planlı siparişler</span><span class="sxs-lookup"><span data-stu-id="7dec1-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="7dec1-110">Üretim denetimi \> Üretim emirleri \> Planlı üretim emirleri</span><span class="sxs-lookup"><span data-stu-id="7dec1-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="7dec1-111">Tedarik ve kaynak atama \> Satınalma siparişleri \> Planlı satınalma siparişleri</span><span class="sxs-lookup"><span data-stu-id="7dec1-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="7dec1-112">Stok Yönetimi \> Gelen siparişler \> Planlı transferler</span><span class="sxs-lookup"><span data-stu-id="7dec1-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="7dec1-113">Stok Yönetimi \> Giden siparişler \> Planlı transferler</span><span class="sxs-lookup"><span data-stu-id="7dec1-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="7dec1-114">Planlanan sipariş durumlarını görüntüleme ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="7dec1-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="7dec1-115">İlerlemenizi izlemeye veya planlı siparişin nasıl işlendiğini değiştirmenizi sağlamak için planlı siparişlerin **Durum** alanlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dec1-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="7dec1-116">Aşağıdaki **Durum** değerleri mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="7dec1-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="7dec1-117">**İşlem görmedi** – Master planlama, planlı siparişler ürettiğinde siparişlere bu durum verilir.</span><span class="sxs-lookup"><span data-stu-id="7dec1-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="7dec1-118">Bu duruma sahip planlı siparişler sonraki planlama çalışmasında silinir.</span><span class="sxs-lookup"><span data-stu-id="7dec1-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="7dec1-119">**Tamamlandı** – Bu durum, planlı siparişin tamamlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7dec1-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="7dec1-120">Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu *Tamamlandı* olarak manuel bir şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dec1-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="7dec1-121">Sistemin, *İşlenmemiş* ve *Tamamlandı* durumlarını aynı şekilde kabul ettiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7dec1-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="7dec1-122">**Onaylandı** – Bu durum, planlı siparişin kesinleştirme için onaylandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7dec1-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="7dec1-123">Planlı bir siparişi kesinleştirmek isterseniz siparişin durumunu *Onaylandı* olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7dec1-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="7dec1-124">Planlı bir siparişte yapılmış düzenlemeleri tutmak istiyorsanız veya planlı bir siparişi kesinleştirmeyi planlıyorsanız siparişin durumunu *Onaylandı* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="7dec1-125">*Onaylandı* durumdaki planlı siparişler sabit olarak kabul edilir ve master planlama bunların tedarik edilmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="7dec1-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="7dec1-126">Bu nedenle, daha sonra master planlama çalışması sırasında değiştirilmez veya silinmezler.</span><span class="sxs-lookup"><span data-stu-id="7dec1-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="7dec1-127">Bu davranışı başarmak için, planlama mantığı, master planlama sırasında eski plan versiyonundaki *Onaylandı* durumuna sahip planlı siparişleri yeni plan sürümüne kopyalar.</span><span class="sxs-lookup"><span data-stu-id="7dec1-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="7dec1-128">*Onaylandı* durumuna sahip planlı siparişlerinin yalnızca belirli master plan içinde tedarik edildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7dec1-128">Note that planned orders that have a status of *Approved*\* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="7dec1-129">Tek bir planlı siparişin durumunu değiştirmek için [herhangi bir planlı sipariş listesi sayfasını açın ](#view-planned-orders), siparişi açın ve ardından aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="7dec1-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="7dec1-130">**Genel** hızlı sekmesinde, **Durum** alanının değerini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="7dec1-131">Eylem Bölmesi'nde, **Planlı sipariş** sekmesindeki **İşlem** grubunda **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="7dec1-132">Siparişi onaylamak için Eylem Bölmesinde **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="7dec1-133">Birkaç planlı siparişin durumunu aynı anda değiştirmek için, [herhangi bir planlı sipariş listesi sayfasını açın ](#view-planned-orders), değiştirmek istediğiniz siparişlerin onay kutularını işaretleyin ve sonra aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="7dec1-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="7dec1-134">Eylem Bölmesi'nde, **Planlı sipariş** sekmesindeki **İşlem** grubunda **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="7dec1-135">Siparişleri onaylamak için Eylem Bölmesinde **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="7dec1-136">Planlı siparişleri onaylama</span><span class="sxs-lookup"><span data-stu-id="7dec1-136">Approve planned orders</span></span>

<span data-ttu-id="7dec1-137">Planlı siparişlerden kesinleştirilmiş sipariş oluşturma işleminde planlı siparişlerin onayını isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="7dec1-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="7dec1-138">Aşağıdaki resim, onay iş akışı uygulamak için her bir planlı siparişe atanan **Durum** değerini nasıl kullanabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="7dec1-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="7dec1-139">Onay işlemi uygulamak için, önceki bölümde açıklandığı şekilde her bir planlı sipariş için **Durum** değerini manuel olarak düzeltin.</span><span class="sxs-lookup"><span data-stu-id="7dec1-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Planlı sipariş akışı](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="7dec1-141">Değiştirilmiş planlı siparişleri onaylamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="7dec1-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="7dec1-142">Aksi takdirde, düzenlemeler bir sonraki planlama çalıştırması tarafından yok sayılacaktır ve bunların üzerine yazılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7dec1-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7dec1-143">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7dec1-143">Additional resources</span></span>

- [<span data-ttu-id="7dec1-144">Kesinleşmiş planlı siparişler</span><span class="sxs-lookup"><span data-stu-id="7dec1-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
