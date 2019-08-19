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
ms.openlocfilehash: a0909625f31d15fe6b1387ff9ab7fd5d9a9135f4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836468"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="34f47-103">Ambardaki stoğu sayma</span><span class="sxs-lookup"><span data-stu-id="34f47-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34f47-104">Bu konu, ambarda bir yerleşimdeki belirli bir ürünün sayımını yapmak için stok sayım günlüğü oluşturma ve deftere nakletme işlemini açıklar.</span><span class="sxs-lookup"><span data-stu-id="34f47-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="34f47-105">Yordam, "temel depolama" işlevi içindir ve Stok Yönetimi modülünde yer alır; Ambar Yönetimi modülünde bulunan ambarlama işlevi için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="34f47-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="34f47-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34f47-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="34f47-107">Kendi verilerinizi kullanıyorsanız, ürünlerin ve yerleşimlerin ayarlandığından ve sayım günlükleri için bir stok günlüğü adı oluşturduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="34f47-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="34f47-108">Stok sayımı normalde bir ambar çalışanı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="34f47-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="34f47-109">Stok sayım günlüğü oluşturma</span><span class="sxs-lookup"><span data-stu-id="34f47-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="34f47-110">**Gezinti bölmesi > Modüller > Stok yönetimi > Günlük girişleri > Ürün sayımı > Sayım**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="34f47-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="34f47-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-111">Select **New**.</span></span>
3. <span data-ttu-id="34f47-112">**Ad** alanında açılır listeden kullanmak istediğini stok sayımı günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="34f47-113">Diğer bazı alanlar, seçtiğiniz stok sayımı günlük adı kurulumu temel alınarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="34f47-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="34f47-114">**Çalışan** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="34f47-115">Listede kullanmak istediğiniz çalışanı **Seçin**.</span><span class="sxs-lookup"><span data-stu-id="34f47-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="34f47-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="34f47-117">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="34f47-117">Create journal lines</span></span>
1. <span data-ttu-id="34f47-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-118">Select **New**.</span></span>
2. <span data-ttu-id="34f47-119">**Madde numarası** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="34f47-120">Demo verileri şirket USMF'yi kullanıyorsanız, **A0001** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="34f47-121">**Tesis** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="34f47-122">Demo verileri şirket USMF'yi kullanıyorsanız, tesis **2** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="34f47-123">**Ambar** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="34f47-124">Demo verileri şirket USMF'yi kullanıyorsanız, ambar **24** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="34f47-125">**Konum** alanında, açılır menü listesinden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="34f47-126">Demo verileri şirket USMF'yi kullanıyorsanız, yerleşim **BULK-001** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="34f47-127">Sayılan alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="34f47-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="34f47-128">**Eldeki ürün** alanında gösterilen sayıdan farklı bir sayım rakamı girerseniz **Miktar** alanı uyuşmazlığı gösterecek şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="34f47-128">If you enter a counted number that’s different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="34f47-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="34f47-130">Stok sayım günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="34f47-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="34f47-131">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-131">Select **Post**.</span></span> <span data-ttu-id="34f47-132">Bir stok sayım günlüğünü deftere naklettiğinizde, sayım miktarı **Eldeki ürün** alanında belirtilenden farklıysa deftere bir stok girişi veya sorun nakledilir, stok düzeyi ve değer değiştirilir ve genel muhasebe hareketleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34f47-132">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="34f47-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="34f47-134">Stok hareketlerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="34f47-134">View inventory transactions</span></span>
1. <span data-ttu-id="34f47-135">**Stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="34f47-136">**Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34f47-136">Select **Transactions**.</span></span> <span data-ttu-id="34f47-137">Burada, stok sayım günlüğünüzü deftere naklettiğinizde oluşturulacak tüm ilgili hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34f47-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

