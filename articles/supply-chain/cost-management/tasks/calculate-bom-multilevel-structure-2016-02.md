--- 
title: "Çok düzeyli yapı kullanarak ürün reçetesini hesaplama (yalnızca Şubat 2016)"
description: "Bu yordam, Maliyetlendirme tablosunu temel alan, çok düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f8190eaedf9aff7eda690542bb6b14e701d9a008
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a><span data-ttu-id="a0d86-103">Çok düzeyli yapı kullanarak ürün reçetesini hesaplama (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="a0d86-103">Calculate a BOM by using a multilevel structure (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0d86-104">Bu yordam, Maliyetlendirme tablosunu temel alan, çok düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="a0d86-105">Ürün reçetesi hesaplaması serisindeki yedinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="a0d86-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="a0d86-107">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a0d86-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a0d86-109">Ürün BOM_1 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="a0d86-110">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="a0d86-111">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-111">Click Item price.</span></span>
5. <span data-ttu-id="a0d86-112">Madde maliyetini hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="a0d86-113">Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="a0d86-114">Maliyetlendirme sürümü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="a0d86-115">Planlanan maliyet türü ve Açılım modu Çok Düzeyli olduğu için, Maliyetlendirme sürümü 20'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="a0d86-116">Çok düzeyli açılım modu, planlanan maliyetler ve benzetimler içindir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="a0d86-117">Standart maliyet için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="a0d86-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="a0d86-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-118">Click OK.</span></span>
8. <span data-ttu-id="a0d86-119">Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-119">Click View calculation details.</span></span>
    * <span data-ttu-id="a0d86-120">Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="a0d86-121">Bu durumda, BOM_2'nin hammadde, işlem bu serinin ilk görev kılavuzunda etkinleştirilen 10 standart maliyeti yerine, toplam 29,40 genel gider dikkate alınarak hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="a0d86-122">Maliyetlendirme tablosu sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="a0d86-123">Maliyetlendirme tablosu sekmesine geçildiğinde, her maliyet grubunun toplam tutarları önceki görev kılavuzunda yapılan hesaplamalardan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="a0d86-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="a0d86-124">Düzey alanında "Çoklu" seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a0d86-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="a0d86-125">Çoklu seçenek belirlendiğinde, maliyetler 10'un M1 maliyet grubundan (ITEM_C) ve 15,60'ın da maliyet grubu L2 iken üretiminden türetildiği BOM_2 bileşimine göre sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="a0d86-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="a0d86-126">Dolaylı maliyetler de değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0d86-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="a0d86-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-127">Close the page.</span></span>
12. <span data-ttu-id="a0d86-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a0d86-128">Close the page.</span></span>


