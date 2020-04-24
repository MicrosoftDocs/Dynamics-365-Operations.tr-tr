---
title: Tek düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)
description: Bu yordam, Maliyetlendirme tablosunu temel alan, tek düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7c2c34474cada787b7a7ba720ba177aa8dc125f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214373"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="8b5a5-103">Tek düzeyli yapı kullanarak ürün reçetesi hesaplama (Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="8b5a5-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b5a5-104">Bu yordam, Maliyetlendirme tablosunu temel alan, tek düzeyli açılım kullanarak tamamlanmış bir ürünün maliyetinin nasıl hesaplanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="8b5a5-105">Bu, Ürün reçetesi hesaplaması serisindeki altıncı görevdir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="8b5a5-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="8b5a5-107">Serbest bırakılan ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-107">Go to Released products.</span></span>
2. <span data-ttu-id="8b5a5-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8b5a5-109">Ürün BOM_1 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="8b5a5-110">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="8b5a5-111">Madde fiyatı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-111">Click Item price.</span></span>
5. <span data-ttu-id="8b5a5-112">Madde maliyetini hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="8b5a5-113">Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="8b5a5-114">Maliyetlendirme sürümü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8b5a5-115">Bu tanıtım için, 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-115">For this demo, select 10.</span></span> <span data-ttu-id="8b5a5-116">Bu, bileşenlere maliyet fiyatını eklemek için kullanılan aynı maliyetlendirme sürümüdür.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="8b5a5-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-117">Click OK.</span></span>
8. <span data-ttu-id="8b5a5-118">Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-118">Click View calculation details.</span></span>
    * <span data-ttu-id="8b5a5-119">Üst menüde bu seçeneği görmek için üç noktaya (...) tıklamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="8b5a5-120">Maliyetin bileşimi buradadır:  •    10 ITEM_A'dan, 10 ITEM_B'den ve 10 BOM_2'den türetilir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-120">Here's the composition of the cost:  \*    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="8b5a5-121">Bu durumda, BOM_2 için ayrıntı bulunmamaktadır çünkü 10'un standart maliyeti olarak girilmiş ve hesaplama sonunda yapılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="8b5a5-122">\*  Hazırlık süresinden, sabit bir maliyet olan 7 ve çalışma zamanı işleminden (İşlem) ek olarak 7 türetilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-122">\*    7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="8b5a5-123">\*   Dolaylı maliyetlere karşılık gelen başka tutarlar da vardır.</span><span class="sxs-lookup"><span data-stu-id="8b5a5-123">\*    There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="8b5a5-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="8b5a5-124">@SysTaskRecorder:_RequestClose</span></span>

