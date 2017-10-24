--- 
title: "Satış siparişlerinden yalın ilişkilendirme"
description: "Bu yordam, satış satırındaki maddenin kanbanlar ile üretildiği bir pegging ağacını onaylamaya odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3aa8cd2c0be56875904158f041cf120c466d9e9a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="28cee-103">Satış siparişlerinden yalın ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="28cee-103">Lean pegging from sales orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28cee-104">Bu yordam, satış satırındaki maddenin kanbanlar ile üretildiği bir pegging ağacını onaylamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="28cee-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="28cee-105">Pegging ağacı doğrulandıktan sonra tüm kanban işleri planlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="28cee-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="28cee-106">Bu durum sipariş alan kişinin üretimin hemen başlayabildiğinden emin olmasının gerektiği senaryolar için faydalıdır.</span><span class="sxs-lookup"><span data-stu-id="28cee-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="28cee-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="28cee-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="28cee-108">Bu yordam, yalın bir şirkette çalışan gelişmiş siparişi alıcı içindir.</span><span class="sxs-lookup"><span data-stu-id="28cee-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="28cee-109">Kanban kontrollü madde için bir satış siparişi oluşturun</span><span class="sxs-lookup"><span data-stu-id="28cee-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="28cee-110">Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="28cee-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="28cee-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cee-111">Click New.</span></span>
3. <span data-ttu-id="28cee-112">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="28cee-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="28cee-113">Kullanım ABD-001.</span><span class="sxs-lookup"><span data-stu-id="28cee-113">Use US-001.</span></span>  
4. <span data-ttu-id="28cee-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cee-114">Click OK.</span></span>
5. <span data-ttu-id="28cee-115">Madde numarası alanına 'L0001' girin.</span><span class="sxs-lookup"><span data-stu-id="28cee-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="28cee-116">Miktarı '30' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="28cee-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="28cee-117">Olay kanban kuralını tetiklemek için miktarın 24'ten daha yüksek olması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="28cee-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="28cee-118">Bir ilişkilendirme ağacı açmak</span><span class="sxs-lookup"><span data-stu-id="28cee-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="28cee-119">Ürün ve tedarik seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="28cee-119">Click Product and supply.</span></span>
2. <span data-ttu-id="28cee-120">İlişkilendirme ağacını görüntüle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="28cee-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="28cee-121">Pegging ağacının satış emri satırındaki gerekli tüm pegginglerin seviyelerini gösterdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="28cee-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="28cee-122">Bu durumda, iki düzeyde kanban mevcuttur ve hepsi gerekli bileşenlerdir.</span><span class="sxs-lookup"><span data-stu-id="28cee-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="28cee-123">İlişkilendirme ağacını planla</span><span class="sxs-lookup"><span data-stu-id="28cee-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="28cee-124">Ağaçta 'Satış satırı 000832\Kanban 000558' seçin.</span><span class="sxs-lookup"><span data-stu-id="28cee-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="28cee-125">Kanban işleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="28cee-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="28cee-126">Kanban işi için iş durumunun planlanmadı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="28cee-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="28cee-127">Tüm ilişkilendirme ağacını planla'ya tıkla.</span><span class="sxs-lookup"><span data-stu-id="28cee-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="28cee-128">Bu, iş değiştirme ilişkilendirme ağacındaki tüm kanban işlerinin iş durumunu planlanmadı'dan planlandı'ya değiştirecektir.</span><span class="sxs-lookup"><span data-stu-id="28cee-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="28cee-129">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="28cee-129">Refresh the page.</span></span>
    * <span data-ttu-id="28cee-130">Kanban iş durumunun planlanmadı'dan planlandı'ya dönüştüğüne dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="28cee-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="28cee-131">Ağaçta, 'Satış 000832\Kanban 000558\Issue L0001\Kanban 000559 için satır' seçin.</span><span class="sxs-lookup"><span data-stu-id="28cee-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="28cee-132">İkinci kanban için de iş planlanmıştır çünkü tüm pegging ağacı planlıdır.</span><span class="sxs-lookup"><span data-stu-id="28cee-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="28cee-133">Kanban iş durumunun planlanmadı'dan planlandı'ya dönüştüğüne dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="28cee-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


