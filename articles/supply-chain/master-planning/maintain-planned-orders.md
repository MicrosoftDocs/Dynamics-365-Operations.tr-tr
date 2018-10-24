---
title: "Planlı siparişleri koruma"
description: "Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar."
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.contentlocale: tr-tr
ms.lasthandoff: 10/08/2018

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="e85ed-104">Planlı siparişleri koruma</span><span class="sxs-lookup"><span data-stu-id="e85ed-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e85ed-105">Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır.</span><span class="sxs-lookup"><span data-stu-id="e85ed-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="e85ed-106">Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e85ed-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="e85ed-107">Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e85ed-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="e85ed-108">İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e85ed-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="e85ed-109">Aşağıdaki değerler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="e85ed-109">The following values are used:</span></span>

-   <span data-ttu-id="e85ed-110">Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.</span><span class="sxs-lookup"><span data-stu-id="e85ed-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="e85ed-111">Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e85ed-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="e85ed-112">Planlı bir siparişi kesinleştirmeye karar verdiğinizde, durumunu **Onaylandı** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e85ed-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="e85ed-113">Bu durum, planlı siparişin kesinleştirilmesini onayladığınızı ama henüz kesinleştirmediğinizi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e85ed-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="e85ed-114">**Not:** Onaylanan bir planlı sipariş geçerli durumunda sonraki master planlama hesaplamasına transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="e85ed-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="e85ed-115">Planlı siparişleri **Kesinleştir** seçeneğine tıklayarak kesinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e85ed-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="e85ed-116">Aşağıdaki planlı siparişleri kesinleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e85ed-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="e85ed-117">Seçilen planlı sipariş.</span><span class="sxs-lookup"><span data-stu-id="e85ed-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="e85ed-118">Birden çok planlı sipariş.</span><span class="sxs-lookup"><span data-stu-id="e85ed-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="e85ed-119">**Açılım** sayfasından bir açılımla üretilen planlı siparişler.</span><span class="sxs-lookup"><span data-stu-id="e85ed-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="e85ed-120">**Planlı siparişler** seçeneğine tıklayın, planlı siparişi seçin, sonra da **Kesinleştir** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e85ed-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="e85ed-121">Planlı bir sipariş kesinleştirildiğinde, ilgili modülün siparişler bölümüne taşınır.</span><span class="sxs-lookup"><span data-stu-id="e85ed-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="e85ed-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e85ed-122">Additional resources</span></span>
--------

[<span data-ttu-id="e85ed-123">Master planlar</span><span class="sxs-lookup"><span data-stu-id="e85ed-123">Master plans</span></span>](master-plans.md)




