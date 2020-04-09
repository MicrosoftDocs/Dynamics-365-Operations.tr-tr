---
title: Ambardaki stoğu sayma
description: Bu konu, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini açıklar.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e9457074b696efaf5958b3a3b4616f06f5a6ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145783"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="10600-103">Ambardaki stoğu sayma</span><span class="sxs-lookup"><span data-stu-id="10600-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10600-104">Bu konu, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini açıklar.</span><span class="sxs-lookup"><span data-stu-id="10600-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="10600-105">Yordam, "temel depolama" işlevi içindir ve Stok Yönetimi modülünde yer alır; Ambar Yönetimi modülünde bulunan ambarlama işlevi için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="10600-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="10600-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10600-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="10600-107">Kendi verilerinizi kullanıyorsanız, ürünlerin ve yerleşimlerin ayarlandığından ve sayım günlükleri için bir stok günlüğü adı oluşturduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="10600-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="10600-108">Stok sayımı normalde bir ambar çalışanı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="10600-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="10600-109">Stok sayım günlüğü oluşturma</span><span class="sxs-lookup"><span data-stu-id="10600-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="10600-110">**Gezinti bölmesi > Modüller > Stok yönetimi > Günlük girişleri > Ürün sayımı > Sayım**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="10600-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="10600-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-111">Select **New**.</span></span>
3. <span data-ttu-id="10600-112">**Ad** alanında açılır listeden kullanmak istediğini stok sayımı günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="10600-113">Diğer bazı alanlar, seçtiğiniz stok sayımı günlük adı kurulumu temel alınarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="10600-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="10600-114">**Çalışan** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="10600-115">Listede kullanmak istediğiniz çalışanı **Seçin**.</span><span class="sxs-lookup"><span data-stu-id="10600-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="10600-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="10600-117">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="10600-117">Create journal lines</span></span>
1. <span data-ttu-id="10600-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-118">Select **New**.</span></span>
2. <span data-ttu-id="10600-119">**Madde numarası** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="10600-120">Demo verileri şirket USMF'yi kullanıyorsanız, **A0001** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="10600-121">**Tesis** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="10600-122">Demo verileri şirket USMF'yi kullanıyorsanız, tesis **2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="10600-123">**Ambar** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="10600-124">Demo verileri şirket USMF'yi kullanıyorsanız, ambar **24** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="10600-125">**Konum** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="10600-126">Demo verileri şirket USMF'yi kullanıyorsanız, yerleşim **BULK-001** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="10600-127">Sayılan alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="10600-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="10600-128">**Eldeki ürün** alanında gösterilen sayıdan farklı bir sayım rakamı girerseniz **Miktar** alanı uyuşmazlığı gösterecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="10600-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="10600-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="10600-130">Stok sayım günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="10600-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="10600-131">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-131">Select **Post**.</span></span> <span data-ttu-id="10600-132">Bir stok sayım günlüğünü deftere naklettiğinizde, sayım miktarı **Eldeki ürün** alanında belirtilenden farklıysa deftere bir stok girişi veya sorun nakledilir, stok düzeyi ve değer değiştirilir ve genel muhasebe hareketleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="10600-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="10600-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="10600-134">Stok hareketlerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="10600-134">View inventory transactions</span></span>
1. <span data-ttu-id="10600-135">**Stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="10600-136">**Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10600-136">Select **Transactions**.</span></span> <span data-ttu-id="10600-137">Burada, stok sayım günlüğünüzü deftere naklettiğinizde oluşturulacak tüm ilgili hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10600-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

