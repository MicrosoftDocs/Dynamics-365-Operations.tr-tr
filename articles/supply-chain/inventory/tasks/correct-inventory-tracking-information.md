---
title: "Stok izleme bilgilerini düzeltme"
description: "Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: e28d10646f01604098de8cedc30c8c7a7c89866b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/12/2017

---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="fbb74-103">Stok izleme bilgilerini düzeltme</span><span class="sxs-lookup"><span data-stu-id="fbb74-103">Correct inventory tracking information</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbb74-104">Bu yordam, stok izleme bilgilerini düzeltmek için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="fbb74-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="fbb74-105">Bu örnekte, başka bir toplu iş için yanlış kaydedilmiş bir toplu iş değiştirerek denetlenen toplu iş ürününün bilgileri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fbb74-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="fbb74-106">Bu yordamı, USPI demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbb74-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="fbb74-107">Kendi verilerinizi kullanıyorsanız, toplu iş etkin olan bir ürününüz olması ve yerleşim denetimli olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fbb74-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="fbb74-108">Stok transferleri için ayarlanmış bir stok günlüğü adı da olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fbb74-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="fbb74-109">Bu görevler normalde ambar personeli tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="fbb74-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="fbb74-110">Bir stok transferi günlüğü yaratma</span><span class="sxs-lookup"><span data-stu-id="fbb74-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="fbb74-111">Transfer'e gidin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-111">Go to Transfer.</span></span>
2. <span data-ttu-id="fbb74-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-112">Click New.</span></span>
3. <span data-ttu-id="fbb74-113">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="fbb74-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="fbb74-115">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="fbb74-115">Create journal lines</span></span>
1. <span data-ttu-id="fbb74-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-116">Click New.</span></span>
2. <span data-ttu-id="fbb74-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="fbb74-118">USPI kullanıyorsanız, M5003 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="fbb74-119">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="fbb74-120">Stok boyutları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="fbb74-121">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="fbb74-122">Tesis alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="fbb74-123">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="fbb74-124">Ürün numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb74-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="fbb74-125">Günlüğü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="fbb74-125">Post the journal</span></span>
1. <span data-ttu-id="fbb74-126">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-126">Click Post.</span></span>
2. <span data-ttu-id="fbb74-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="fbb74-128">İzleme bilgilerini denetleme</span><span class="sxs-lookup"><span data-stu-id="fbb74-128">Check tracing information</span></span>
1. <span data-ttu-id="fbb74-129">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-129">Click Inventory.</span></span>
2. <span data-ttu-id="fbb74-130">İzle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-130">Click Trace.</span></span>
3. <span data-ttu-id="fbb74-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-131">Click OK.</span></span>
    * <span data-ttu-id="fbb74-132">Bu izleme bilgilerini kullanarak stoktan düzeltilen toplu işi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbb74-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="fbb74-133">Bu bilgileri görmek için Ürün izleme sayfasını da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbb74-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="fbb74-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="fbb74-135">Stok hareketlerini denetleme</span><span class="sxs-lookup"><span data-stu-id="fbb74-135">Check inventory transactions</span></span>
1. <span data-ttu-id="fbb74-136">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-136">Click Inventory.</span></span>
2. <span data-ttu-id="fbb74-137">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb74-137">Click Transactions.</span></span>
    * <span data-ttu-id="fbb74-138">Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fbb74-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

