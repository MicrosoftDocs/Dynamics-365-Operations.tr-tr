---
title: Çok düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)
description: Bu yordam, Maliyetlendirme tablosunu temel alan, çok düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4f3e20d483e2184366c4ee6eb179e12d2e2492e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214378"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="fb86c-103">Çok düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="fb86c-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb86c-104">Bu yordam, Maliyetlendirme tablosunu temel alan, çok düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="fb86c-105">Ürün reçetesi hesaplaması serisindeki yedinci görevdir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="fb86c-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="fb86c-107">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="fb86c-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fb86c-109">Ürün BOM_1 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="fb86c-110">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="fb86c-111">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-111">Click Item price.</span></span>
5. <span data-ttu-id="fb86c-112">Madde maliyetini hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="fb86c-113">Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="fb86c-114">Maliyetlendirme sürümü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="fb86c-115">Planlanan maliyet türü ve Açılım modu Çok Düzeyli olduğu için, Maliyetlendirme sürümü 20'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="fb86c-116">Çok düzeyli açılım modu, planlanan maliyetler ve benzetimler içindir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="fb86c-117">Standart maliyet için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="fb86c-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="fb86c-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-118">Click OK.</span></span>
8. <span data-ttu-id="fb86c-119">Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-119">Click View calculation details.</span></span>
    * <span data-ttu-id="fb86c-120">Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="fb86c-121">Bu durumda, BOM_2'nin hammadde, işlem bu serinin ilk görev kılavuzunda etkinleştirilen 10 standart maliyeti yerine, toplam 29,40 genel gider dikkate alınarak hesaplandığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="fb86c-122">Maliyetlendirme tablosu sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="fb86c-123">Maliyetlendirme tablosu sekmesine geçildiğinde, her maliyet grubunun toplam tutarları önceki görev kılavuzunda yapılan hesaplamalardan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="fb86c-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="fb86c-124">Düzey alanında "Çoklu" seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="fb86c-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="fb86c-125">Çoklu seçenek belirlendiğinde, maliyetler 10'un M1 maliyet grubundan (ITEM_C) ve 15,60'ın da maliyet grubu L2 iken üretiminden türetildiği BOM_2 bileşimine göre sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="fb86c-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="fb86c-126">Dolaylı maliyetler de değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb86c-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="fb86c-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-127">Close the page.</span></span>
12. <span data-ttu-id="fb86c-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fb86c-128">Close the page.</span></span>

