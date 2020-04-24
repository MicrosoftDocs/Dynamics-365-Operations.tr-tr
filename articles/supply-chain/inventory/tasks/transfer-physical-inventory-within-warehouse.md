---
title: Ambar içindeki fiziksel stoğu transfer etme
description: Bu yordam, bir ürünün bir yerleşimden başka bir yerleşimdeki ambara taşınması kaydı için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cdb66620d5d57a42ce6a2dc443a9276a2e3ca0ae
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203998"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="9626b-103">Ambar içindeki fiziksel stoğu transfer etme</span><span class="sxs-lookup"><span data-stu-id="9626b-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9626b-104">Bu yordam, bir ürünün bir yerleşimden başka bir yerleşimdeki ambara taşınması kaydı için bir stok transfer günlüğü oluşturma ve deftere nakletme işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="9626b-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="9626b-105">Buna başlamadan önce stok transferleri için ayarlanmış bir stok günlüğü adı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9626b-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="9626b-106">USMF demo verisi şirketindeki bu yordam ile gösterilen örnek değerleri nasıl kullanacağınızı veya ayarlanmış ürün ve yerleşimleriniz varsa kendi verilerinizi nasıl kullanacağınızı adım adım görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="9626b-107">Bu görevler normalde ambar personeli tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="9626b-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="9626b-108">Bir stok transferi günlüğü yaratma</span><span class="sxs-lookup"><span data-stu-id="9626b-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="9626b-109">**Gezinti bölmesinde**, **Stok yönetimi > Maddelerin girdileri> Maddeler > Aktarma** üzerine gidin.</span><span class="sxs-lookup"><span data-stu-id="9626b-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="9626b-110">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9626b-110">Click **New**.</span></span>
3. <span data-ttu-id="9626b-111">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="9626b-112">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9626b-112">Click **OK**.</span></span> <span data-ttu-id="9626b-113">Her bir günlük satırının 'Başlangıç' ve 'Bitiş' boyutlarını belirtmek için seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="9626b-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="9626b-114">Bu günlük türü için bunlar önemlidir.</span><span class="sxs-lookup"><span data-stu-id="9626b-114">These are essential for this journal type.</span></span> <span data-ttu-id="9626b-115">Ürünleri yerleşimlere farklı kurallar kullanarak transfer edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="9626b-116">Bu örnekte, aynı ambar içindeki bir ürün bir plaka denetimli olan bir yerleşimden plaka denetimli olmayan bir yerleşime transfer ediliyor.</span><span class="sxs-lookup"><span data-stu-id="9626b-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="9626b-117">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="9626b-117">Create journal lines</span></span>
1. <span data-ttu-id="9626b-118">**Günlük satırları hızlı sekmesi** içinde **Yeni** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9626b-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="9626b-119">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="9626b-120">USMF kullanıyorsanız, 'A0001' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="9626b-121">**Kaynak tesis** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="9626b-122">USMF kullanıyorsanız, '2' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="9626b-123">**Hedef tesis** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="9626b-124">USMF kullanıyorsanız, '2' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="9626b-125">**Kaynak ambar** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="9626b-126">USMF kullanıyorsanız, '24' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="9626b-127">**Hedef ambar** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="9626b-128">USMF kullanıyorsanız, '24' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="9626b-129">**Çıkış yerleşimi** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="9626b-130">USMF kullanıyorsanız, 'FL-001' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="9626b-131">**Hedef yerleşim** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="9626b-132">USMF kullanıyorsanız, 'BULK-001' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="9626b-133">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9626b-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="9626b-134">**Satır ayrıntıları** hızlı sekmesinde, **Stok boyutları** sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9626b-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="9626b-135">**Giden stok boyutları** içinde, **Lisans plakası** alanında, bir değer girin ya da seçin.</span><span class="sxs-lookup"><span data-stu-id="9626b-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="9626b-136">USMF kullanıyorsanız, '24' öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="9626b-137">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9626b-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="9626b-138">Stok transfer günlüğünü deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="9626b-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="9626b-139">**Eylem bölmesinde** **Deftere naklet** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9626b-139">On the **Action pane**, click **Post**.</span></span>
2. <span data-ttu-id="9626b-140">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9626b-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="9626b-141">Stok hareketlerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="9626b-141">View inventory transactions</span></span>
1. <span data-ttu-id="9626b-142">**Stok**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9626b-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="9626b-143">**Hareketler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9626b-143">Click **Transactions**.</span></span> <span data-ttu-id="9626b-144">Burada, günlüğünüzü deftere naklettiğinizde oluşturulan hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9626b-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

