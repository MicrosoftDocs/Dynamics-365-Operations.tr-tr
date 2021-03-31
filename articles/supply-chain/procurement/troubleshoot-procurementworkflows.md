---
title: Satın alma ve kaynak hizmetleri iş akışları ile ilgili sorunları giderme
description: Bu konu, satın alma ve kaynak hizmetleri iş akışları ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d5d688c5769a62580e48908117d0562b26eab10a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222837"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="4c25f-103">Satın alma ve kaynak hizmetleri iş akışları ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="4c25f-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="4c25f-104">Bu konu, satın alma ve kaynak hizmetleri iş akışları ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4c25f-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="4c25f-105">Bir değişiklikten sonra bir satınalma siparişi iş akışına yeniden gönderilirken hata oluştu: "Değişiklik yönetimi etkinleştirildiğinde X satınalma siparişinde yapılan değişikliklere, yalnızca Taslak durumunda izin verilir"</span><span class="sxs-lookup"><span data-stu-id="4c25f-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="4c25f-106">Bu sorun yalnızca satınalma siparişi siz değişiklikleri talep etmeden önce *Onaylandı* durumdaysa oluşur.</span><span class="sxs-lookup"><span data-stu-id="4c25f-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="4c25f-107">Satınalma siparişi *Onaylandı* durumunda iken değişiklik istediğinizde, iş akışı başarıyla işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="4c25f-108">Hata açıklaması</span><span class="sxs-lookup"><span data-stu-id="4c25f-108">Error description</span></span>

<span data-ttu-id="4c25f-109">Bir satınalma siparişinin bir değişiklikten sonra yeniden gönderilmesi halinde, iş akışında aşağıdaki hata oluşur:</span><span class="sxs-lookup"><span data-stu-id="4c25f-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="4c25f-110">Durduruldu (hata): X + + Özel durumu: PO0000569 numaralı satınalma siparişinde yapılan değişikliklere yalnızca değişiklik yönetiminin etkinleştirildiği Taslak durumunda izin verilir</span><span class="sxs-lookup"><span data-stu-id="4c25f-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="4c25f-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="4c25f-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="4c25f-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="4c25f-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="4c25f-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="4c25f-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="4c25f-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="4c25f-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c25f-115">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4c25f-115">Issue resolution</span></span>

<span data-ttu-id="4c25f-116">Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="4c25f-117">Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="4c25f-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="4c25f-118">Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="4c25f-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="4c25f-119">Sorun, [Microsoft Bilgi Bankası (KB) makalesi](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138) ile düzeltilecektir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="4c25f-120">Bir veya daha fazla muhasebe dağıtımı fazla dağıtılmış veya eksik dağıtılmış.</span><span class="sxs-lookup"><span data-stu-id="4c25f-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="4c25f-121">Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="4c25f-122">Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="4c25f-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="4c25f-123">Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="4c25f-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="4c25f-124">Değişiklik yönetiminin açık olduğu bir satınalma siparişinde teslimat kalanı iptal edilirse, satınalma siparişi Onaylı durumuna geçer.</span><span class="sxs-lookup"><span data-stu-id="4c25f-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c25f-125">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4c25f-125">Issue description</span></span>

<span data-ttu-id="4c25f-126">Değişiklik yönetimine bağlı bir satınalma siparişi için, istenen tek değişiklik bir veya daha fazla satırda kalan teslimatın iptali ise, onaylandığında satınalma siparişi doğrudan *Onaylandı* durumuna geçer ve hiçbir günlük oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="4c25f-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c25f-127">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4c25f-127">Issue resolution</span></span>

<span data-ttu-id="4c25f-128">Bir teslim işleminin geri kalanının iptal edilmesi onay günlüğünün içeriğini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="4c25f-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="4c25f-129">Bu işlev, satır kısmen alındığında kullanılmalıdır ve satınalma siparişi satıcıyla onaylandıktan sonra işlem adımında geri kalan miktarı iptal edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="4c25f-130">Bu, satınalma siparişi teyidini yansıtılacağından, onayın gerekli olabilmesi için satınalma siparişi satırında miktar ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4c25f-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="4c25f-131">Bunun yerine, satırda hiçbir şey alınmadığında, miktar kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="4c25f-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="4c25f-132">Bu durumda, yeniden onay gerekir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="4c25f-133">İptal edilen satınalma siparişleri Satınalma siparişi hazırlama çalışma alanındaki taslak listesinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4c25f-134">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="4c25f-134">Issue description</span></span>

<span data-ttu-id="4c25f-135">*Onaylanmış* durumda olan satınalma siparişlerini iptal ettikten sonra, iptal edilen satınalma siparişleri **Satınalma siparişi hazırlama** çalışma alanındaki taslak satınalma siparişleri listesinde görünmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="4c25f-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4c25f-136">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="4c25f-136">Issue resolution</span></span>

<span data-ttu-id="4c25f-137">Bu sorun yalnızca değişiklik yönetimine bağlı satınalma siparişlerinde oluşur.</span><span class="sxs-lookup"><span data-stu-id="4c25f-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="4c25f-138">Bunun nedeni, iptal işleminin onaylanması gereken bir değişiklik olduğu kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="4c25f-139">Onay, sistem tarafından otomatik olarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="4c25f-140">Bu nedenle işlem, iptal edilen satınalma siparişinin onay iş akşına gönderilmesidir. Böylece *Onaylı* durumuna geçebilir.</span><span class="sxs-lookup"><span data-stu-id="4c25f-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="4c25f-141">Bu noktada, satınalma siparişi artık **Satınalma siparişi hazırlama** çalışma alanındaki taslak satınalma siparişleri listesinde görünmez.</span><span class="sxs-lookup"><span data-stu-id="4c25f-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]