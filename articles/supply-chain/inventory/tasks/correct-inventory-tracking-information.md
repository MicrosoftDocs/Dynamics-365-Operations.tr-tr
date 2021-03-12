---
title: Stok izleme bilgilerini düzeltme
description: Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c70dba7d21eab372cec235efa5a4be19587a409
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000146"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="7fd60-103">Stok izleme bilgilerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="7fd60-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7fd60-104">Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="7fd60-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="7fd60-105">Bu örnekte, başka bir toplu iş için yanlış kaydedilmiş bir toplu iş değiştirerek denetlenen toplu iş ürününün bilgileri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7fd60-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="7fd60-106">Bu yordamı, USPI demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fd60-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="7fd60-107">Kendi verilerinizi kullanıyorsanız, toplu iş etkin olan bir ürününüz olması ve yerleşim denetimli olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7fd60-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="7fd60-108">Stok transferleri için ayarlanmış bir stok günlüğü adı da olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7fd60-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="7fd60-109">Bu görevler normalde ambar personeli tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="7fd60-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="7fd60-110">Bir stok transferi günlüğü yaratma</span><span class="sxs-lookup"><span data-stu-id="7fd60-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="7fd60-111">Transfer'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-111">Go to Transfer.</span></span>
2. <span data-ttu-id="7fd60-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-112">Click New.</span></span>
3. <span data-ttu-id="7fd60-113">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="7fd60-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="7fd60-115">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="7fd60-115">Create journal lines</span></span>
1. <span data-ttu-id="7fd60-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-116">Click New.</span></span>
2. <span data-ttu-id="7fd60-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="7fd60-118">USPI kullanıyorsanız, M5003 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="7fd60-119">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="7fd60-120">Stok boyutları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="7fd60-121">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="7fd60-122">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="7fd60-123">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="7fd60-124">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7fd60-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="7fd60-125">Günlüğü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="7fd60-125">Post the journal</span></span>
1. <span data-ttu-id="7fd60-126">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-126">Click Post.</span></span>
2. <span data-ttu-id="7fd60-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="7fd60-128">İzleme bilgilerini denetleme</span><span class="sxs-lookup"><span data-stu-id="7fd60-128">Check tracing information</span></span>
1. <span data-ttu-id="7fd60-129">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-129">Click Inventory.</span></span>
2. <span data-ttu-id="7fd60-130">İzle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-130">Click Trace.</span></span>
3. <span data-ttu-id="7fd60-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-131">Click OK.</span></span>
    * <span data-ttu-id="7fd60-132">Bu izleme bilgilerini kullanarak stoktan düzeltilen toplu işi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fd60-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="7fd60-133">Bu bilgileri görmek için Ürün izleme sayfasını da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fd60-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="7fd60-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="7fd60-135">Stok hareketlerini denetleme</span><span class="sxs-lookup"><span data-stu-id="7fd60-135">Check inventory transactions</span></span>
1. <span data-ttu-id="7fd60-136">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-136">Click Inventory.</span></span>
2. <span data-ttu-id="7fd60-137">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fd60-137">Click Transactions.</span></span>
    * <span data-ttu-id="7fd60-138">Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7fd60-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

