---
title: Tamamlanmış ürün oluşturma (yalnızca Şubat 2016)
description: Bu görev, bitmiş bir ürün oluşturmaya odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f9693e04160ffe9307de5e454d8269ca883679
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570869"
---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="ad328-103">Tamamlanmış ürün oluşturma (yalnızca Şubat 2016)</span><span class="sxs-lookup"><span data-stu-id="ad328-103">Create a finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad328-104">Bu görev, bitmiş bir ürün oluşturmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="ad328-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="ad328-105">Ürün Reçetesi hesaplama serisindeki ilk görevdir.</span><span class="sxs-lookup"><span data-stu-id="ad328-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="ad328-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ad328-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="ad328-107">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="ad328-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ad328-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad328-108">Click New.</span></span>
3. <span data-ttu-id="ad328-109">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ad328-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ad328-110">Tanıtım için BOM_1 yazın.</span><span class="sxs-lookup"><span data-stu-id="ad328-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="ad328-111">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-112">STD öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-112">Select STD.</span></span> <span data-ttu-id="ad328-113">STD, standart maliyet anlamına gelir ve maliyet hesaplamalarıyla çalışırken en yaygın olarak kullanılan modeldir.</span><span class="sxs-lookup"><span data-stu-id="ad328-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="ad328-114">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-115">Örneğin, Ses'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-115">For example, select Audio.</span></span> <span data-ttu-id="ad328-116">Bunun, maliyet hesaplamaları üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="ad328-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="ad328-117">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-118">SiteWH'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-118">Select SiteWH.</span></span> <span data-ttu-id="ad328-119">Tanıtım için yalnızca Tesis ve Ambar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ad328-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="ad328-120">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-121">Bu örnek için izleme boyutları kullanılmaz. Hiçbiri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="ad328-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad328-122">Click OK.</span></span>
9. <span data-ttu-id="ad328-123">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad328-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="ad328-124">Varsayılan sipariş ayarlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ad328-124">Click Default order settings.</span></span>
11. <span data-ttu-id="ad328-125">Varsayılan sipariş türü alanında, "Üretim" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="ad328-126">Bu, üretilecek olan bitmiş bir ürün olduğundan Üretim'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="ad328-127">Satınalma tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-128">Tanıtım için Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="ad328-129">Stok tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-130">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="ad328-131">Satış tesisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ad328-132">Bu örnek için, Tesis 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ad328-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="ad328-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ad328-133">Close the page.</span></span>

