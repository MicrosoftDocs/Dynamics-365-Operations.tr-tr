--- 
title: "Serbest bırakılan ana ürünün temel kurulumunu tamamlama"
description: "Bu yordam, ana ürünün, ürün reçetelerinde kullanılmadan önce yerine getirilmesi gereken minimum kurulumun nasıl tamamlanacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 35ca13f157537087346a5bcf9c6ccdd659a0d772
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="5874c-103">Serbest bırakılan ana ürünün temel kurulumunu tamamlama</span><span class="sxs-lookup"><span data-stu-id="5874c-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5874c-104">Bu yordam, ana ürünün, ürün reçetelerinde kullanılmadan önce yerine getirilmesi gereken minimum kurulumun nasıl tamamlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5874c-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="5874c-105">Bu, boyut tabanlı yapılandırma birleşimlerini nasıl oluşturulacağını açıklayan sekiz prosedür arasındaki üçüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="5874c-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="5874c-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="5874c-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5874c-107">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="5874c-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5874c-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5874c-109">İkinci yordamda serbest bıraktığınız ana ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="5874c-110">Bu ana ürün, boyut tabanlı yapılandırma teknolojisi ile oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5874c-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="5874c-111">Eylem Bölmesinde, Ürün'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="5874c-112">İletişim kutusunu açmak için Boyut grupları'ına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="5874c-113">Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5874c-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5874c-115">Depolama boyutları grubu, ürün hareketi için kullanılacak depolama boyutlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="5874c-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="5874c-116">Bu yordam için Tesis seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="5874c-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5874c-118">İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5874c-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5874c-120">İzleme boyutları grubu, ürün hareketi için kullanılacak izleme boyutlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="5874c-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="5874c-121">Bu yordam için Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="5874c-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5874c-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-123">Click OK.</span></span>
12. <span data-ttu-id="5874c-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5874c-125">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-125">Click Edit.</span></span>
    * <span data-ttu-id="5874c-126">Kurulum görevine devam etmek için serbest bırakılmış ürün ayrıntıları formunu açın.</span><span class="sxs-lookup"><span data-stu-id="5874c-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="5874c-127">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5874c-128">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5874c-129">Madde modeli grupları, maddelerin madde girişlerinde ve çıkışlarında kontrol edilme ve işlenme biçimini belirleyen ayarları içerir.</span><span class="sxs-lookup"><span data-stu-id="5874c-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="5874c-130">Ayrıca, bunlar madde tüketiminin hesaplanma şeklini de belirler.</span><span class="sxs-lookup"><span data-stu-id="5874c-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="5874c-131">Bu yordam için   FIFO seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="5874c-132">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="5874c-133">Maliyet yönetimi bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="5874c-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="5874c-134">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="5874c-135">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5874c-136">Stok maddelerini gruplara ayırarak stoku yönetmek için madde grupları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5874c-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="5874c-137">Bu yordam için   CarAudio'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="5874c-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5874c-139">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="5874c-140">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5874c-140">Click Default order settings.</span></span>
23. <span data-ttu-id="5874c-141">Varsayılan sipariş türü alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="5874c-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="5874c-142">Bu ana ürünün varsayılan tedarik seçeneğinin üretim olduğunu belirtmek için Üretim seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5874c-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="5874c-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5874c-143">Close the page.</span></span>
25. <span data-ttu-id="5874c-144">Serbest bırakılan ürün detayları formunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="5874c-144">Close the Released product details form.</span></span>


