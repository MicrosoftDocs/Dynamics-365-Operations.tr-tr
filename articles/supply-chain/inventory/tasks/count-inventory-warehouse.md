---
title: Ambardaki stoğu sayma
description: Bu yordam, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "353483"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="bcb16-103">Ambardaki stoğu sayma</span><span class="sxs-lookup"><span data-stu-id="bcb16-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bcb16-104">Bu yordam, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="bcb16-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="bcb16-105">Yordam, "temel depolama" işlevi içindir ve Stok Yönetimi modülünde yer alır; Ambar Yönetimi modülünde bulunan ambarlama işlevi için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="bcb16-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="bcb16-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcb16-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="bcb16-107">Kendi verilerinizi kullanıyorsanız, ürünlerin ve yerleşimlerin ayarlandığından ve sayım günlükleri için bir stok günlüğü adı oluşturduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="bcb16-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="bcb16-108">Stok sayımı normalde bir ambar çalışanı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bcb16-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="bcb16-109">Stok sayım günlüğü oluşturma</span><span class="sxs-lookup"><span data-stu-id="bcb16-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="bcb16-110">Stok Yönetimi > Günlük girişleri > Ürün sayımı > Sayım'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="bcb16-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-111">Click New.</span></span>
3. <span data-ttu-id="bcb16-112">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bcb16-113">Listede, kullanmak istediğiniz stok sayım günlüğünün adını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="bcb16-114">Diğer bazı alanlar, seçtiğiniz stok sayımı günlük adı kurulumu temel alınarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="bcb16-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="bcb16-115">Çalışan alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bcb16-116">Listede kullanmak istediğiniz çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="bcb16-117">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-117">Click Select.</span></span>
8. <span data-ttu-id="bcb16-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="bcb16-119">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="bcb16-119">Create journal lines</span></span>
1. <span data-ttu-id="bcb16-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-120">Click New.</span></span>
2. <span data-ttu-id="bcb16-121">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bcb16-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bcb16-123">Demo verileri şirket USMF'yi kullanıyorsanız, 'A0001' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="bcb16-124">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bcb16-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bcb16-126">Demo verileri şirket USMF'yi kullanıyorsanız, tesis '2' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="bcb16-127">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bcb16-128">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bcb16-129">Demo verileri şirket USMF'yi kullanıyorsanız, ambar '24' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="bcb16-130">Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="bcb16-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bcb16-132">Demo verileri şirket USMF'yi kullanıyorsanız, yerleşim 'BULK-001' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="bcb16-133">Sayılan alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bcb16-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="bcb16-134">Eldeki ürün alanında gösterilen sayıdan farklı bir sayım rakamı girerseniz, Miktar alanı uyuşmazlığı gösterecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bcb16-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="bcb16-135">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="bcb16-136">Stok sayım günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="bcb16-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="bcb16-137">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-137">Click Post.</span></span>
    * <span data-ttu-id="bcb16-138">Bir stok sayım günlüğünü deftere naklettiğinizde, sayım miktarı Eldeki ürün alanında belirtilenden farklıysa deftere bir stok girişi veya sorun nakledilir, stok düzeyi ve değer değiştirilir ve genel muhasebe hareketleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bcb16-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="bcb16-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="bcb16-140">Stok hareketlerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="bcb16-140">View inventory transactions</span></span>
1. <span data-ttu-id="bcb16-141">Stok'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-141">Click Inventory.</span></span>
2. <span data-ttu-id="bcb16-142">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcb16-142">Click Transactions.</span></span>
    * <span data-ttu-id="bcb16-143">Burada, stok sayım günlüğünüzü deftere naklettiğinizde oluşturulacak tüm ilgili hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bcb16-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

