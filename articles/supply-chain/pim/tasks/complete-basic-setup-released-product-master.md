---
title: Serbest bırakılan ana ürünün temel kurulumunu tamamlama
description: Bu konu, ana ürünün, ürün reçetelerinde kullanılmadan önce yerine getirilmesi gereken minimum kurulumun nasıl tamamlanacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986419"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="593fb-103">Serbest bırakılan ana ürünün temel kurulumunu tamamlama</span><span class="sxs-lookup"><span data-stu-id="593fb-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="593fb-104">Bu konu, ana ürünün, ürün reçetelerinde kullanılmadan önce yerine getirilmesi gereken minimum kurulumun nasıl tamamlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="593fb-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="593fb-105">Bu, boyut tabanlı yapılandırma birleşimlerini nasıl oluşturulacağını açıklayan sekiz prosedür arasındaki üçüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="593fb-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="593fb-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="593fb-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="593fb-107">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="593fb-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="593fb-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="593fb-109">İkinci yordamda serbest bıraktığınız ana ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="593fb-110">Bu ana ürün, boyut tabanlı yapılandırma teknolojisi ile oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="593fb-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="593fb-111">Eylem Bölmesinde, **Ürün**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="593fb-112">İletişim kutusunu açmak için **Boyut grupları**'ını seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="593fb-113">**Depolama boyutu grubu**'nda, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="593fb-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="593fb-115">Depolama boyutları grubu, ürün hareketi için kullanılacak depolama boyutlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="593fb-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="593fb-116">Bu yordam için **Tesis**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="593fb-117">**İzleme boyutu grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="593fb-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="593fb-119">İzleme boyutları grubu, ürün hareketi için kullanılacak izleme boyutlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="593fb-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="593fb-120">Bu prosedür için **Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="593fb-121">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="593fb-121">Click **OK**.</span></span>
10. <span data-ttu-id="593fb-122">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="593fb-122">Click **Edit**.</span></span>
11. <span data-ttu-id="593fb-123">**Madde modeli grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="593fb-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="593fb-125">Madde modeli grupları, maddelerin madde girişlerinde ve çıkışlarında kontrol edilme ve işlenme biçimini belirleyen ayarları içerir.</span><span class="sxs-lookup"><span data-stu-id="593fb-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="593fb-126">Ayrıca, bunlar madde tüketiminin hesaplanma şeklini de belirler.</span><span class="sxs-lookup"><span data-stu-id="593fb-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="593fb-127">Bu prosedür için **FIFO**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="593fb-128">**Maliyetleri yönet** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="593fb-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="593fb-129">**Madde grubu** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="593fb-130">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="593fb-131">Stok maddelerini gruplara ayırarak stoku yönetmek için madde grupları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="593fb-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="593fb-132">Bu prosedür için **CarAudio**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="593fb-133">Eylem Bölmesinde, **Plan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="593fb-134">**Ürün varsayılan sipariş ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="593fb-135">**Varsayılan sipariş türü** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="593fb-136">Bu ana ürünün varsayılan tedarik seçeneğinin üretim olduğunu belirtmek için **Üretim** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="593fb-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="593fb-137">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="593fb-137">Select **Save**.</span></span>
20. <span data-ttu-id="593fb-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="593fb-138">Close the page.</span></span>
21. <span data-ttu-id="593fb-139">**Serbest bırakılan ürün detayları** formunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="593fb-139">Close the **Released product details** form.</span></span>

