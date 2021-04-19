---
title: Stok izleme bilgilerini düzeltme
description: Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d7bbb1f2e6128b1dea2be8dc737d5ae526195f08
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834085"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="eaac7-103">Stok izleme bilgilerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="eaac7-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eaac7-104">Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="eaac7-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="eaac7-105">Bu örnekte, başka bir toplu iş için yanlış kaydedilmiş bir toplu iş değiştirerek denetlenen toplu iş ürününün bilgileri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="eaac7-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="eaac7-106">Bu yordamı, USPI demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaac7-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="eaac7-107">Kendi verilerinizi kullanıyorsanız, toplu iş etkin olan bir ürününüz olması ve yerleşim denetimli olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="eaac7-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="eaac7-108">Stok transferleri için ayarlanmış bir stok günlüğü adı da olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="eaac7-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="eaac7-109">Bu görevler normalde ambar personeli tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="eaac7-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="eaac7-110">Bir stok transferi günlüğü yaratma</span><span class="sxs-lookup"><span data-stu-id="eaac7-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="eaac7-111">Transfer'e gidin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-111">Go to Transfer.</span></span>
2. <span data-ttu-id="eaac7-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-112">Click New.</span></span>
3. <span data-ttu-id="eaac7-113">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="eaac7-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="eaac7-115">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="eaac7-115">Create journal lines</span></span>
1. <span data-ttu-id="eaac7-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-116">Click New.</span></span>
2. <span data-ttu-id="eaac7-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="eaac7-118">USPI kullanıyorsanız, M5003 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="eaac7-119">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="eaac7-120">Stok boyutları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="eaac7-121">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="eaac7-122">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="eaac7-123">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="eaac7-124">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="eaac7-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="eaac7-125">Günlüğü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="eaac7-125">Post the journal</span></span>
1. <span data-ttu-id="eaac7-126">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-126">Click Post.</span></span>
2. <span data-ttu-id="eaac7-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="eaac7-128">İzleme bilgilerini denetleme</span><span class="sxs-lookup"><span data-stu-id="eaac7-128">Check tracing information</span></span>
1. <span data-ttu-id="eaac7-129">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-129">Click Inventory.</span></span>
2. <span data-ttu-id="eaac7-130">İzle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-130">Click Trace.</span></span>
3. <span data-ttu-id="eaac7-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-131">Click OK.</span></span>
    * <span data-ttu-id="eaac7-132">Bu izleme bilgilerini kullanarak stoktan düzeltilen toplu işi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaac7-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="eaac7-133">Bu bilgileri görmek için Ürün izleme sayfasını da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaac7-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="eaac7-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="eaac7-135">Stok hareketlerini denetleme</span><span class="sxs-lookup"><span data-stu-id="eaac7-135">Check inventory transactions</span></span>
1. <span data-ttu-id="eaac7-136">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-136">Click Inventory.</span></span>
2. <span data-ttu-id="eaac7-137">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="eaac7-137">Click Transactions.</span></span>
    * <span data-ttu-id="eaac7-138">Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eaac7-138">Here you can see the transactions that were created when you posted your journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]