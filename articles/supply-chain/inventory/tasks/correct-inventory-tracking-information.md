--- 
title: "Stok izleme bilgilerini düzeltme"
description: "Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar."
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: cfe0f6995598757dcea824e1bb4f7ef8ab54a67b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="7d793-103">Stok izleme bilgilerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="7d793-103">Correct inventory tracking information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d793-104">Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="7d793-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="7d793-105">Bu örnekte, başka bir toplu iş için yanlış kaydedilmiş bir toplu iş değiştirerek denetlenen toplu iş ürününün bilgileri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7d793-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="7d793-106">Bu yordamı, USPI demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d793-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="7d793-107">Kendi verilerinizi kullanıyorsanız, toplu iş etkin olan bir ürününüz olması ve yerleşim denetimli olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d793-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="7d793-108">Stok transferleri için ayarlanmış bir stok günlüğü adı da olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7d793-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="7d793-109">Bu görevler normalde ambar personeli tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="7d793-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="7d793-110">Bir stok transferi günlüğü yaratma</span><span class="sxs-lookup"><span data-stu-id="7d793-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="7d793-111">Transfer'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7d793-111">Go to Transfer.</span></span>
2. <span data-ttu-id="7d793-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-112">Click New.</span></span>
3. <span data-ttu-id="7d793-113">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="7d793-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="7d793-115">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="7d793-115">Create journal lines</span></span>
1. <span data-ttu-id="7d793-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-116">Click New.</span></span>
2. <span data-ttu-id="7d793-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7d793-118">USPI kullanıyorsanız, M5003 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="7d793-119">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d793-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="7d793-120">Stok boyutları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="7d793-121">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="7d793-122">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="7d793-123">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="7d793-124">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7d793-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="7d793-125">Günlüğü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="7d793-125">Post the journal</span></span>
1. <span data-ttu-id="7d793-126">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-126">Click Post.</span></span>
2. <span data-ttu-id="7d793-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="7d793-128">İzleme bilgilerini denetleme</span><span class="sxs-lookup"><span data-stu-id="7d793-128">Check tracing information</span></span>
1. <span data-ttu-id="7d793-129">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7d793-129">Click Inventory.</span></span>
2. <span data-ttu-id="7d793-130">İzle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7d793-130">Click Trace.</span></span>
3. <span data-ttu-id="7d793-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-131">Click OK.</span></span>
    * <span data-ttu-id="7d793-132">Bu izleme bilgilerini kullanarak stoktan düzeltilen toplu işi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d793-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="7d793-133">Bu bilgileri görmek için Ürün izleme sayfasını da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d793-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="7d793-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7d793-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="7d793-135">Stok hareketlerini denetleme</span><span class="sxs-lookup"><span data-stu-id="7d793-135">Check inventory transactions</span></span>
1. <span data-ttu-id="7d793-136">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7d793-136">Click Inventory.</span></span>
2. <span data-ttu-id="7d793-137">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d793-137">Click Transactions.</span></span>
    * <span data-ttu-id="7d793-138">Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d793-138">Here you can see the transactions that were created when you posted your journal.</span></span>   


