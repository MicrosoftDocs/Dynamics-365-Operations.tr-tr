---
title: Ambardaki stok düzeylerini ayarlama (temel ambarlama)
description: Bu yordam, ürünlerin ambardaki stok düzeylerini ayarlamak için bir stok ayarlama günlüğünü oluşturma ve deftere nakletme işlemini size gösterecektir.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834157"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="62ac0-103">Ambardaki stok düzeylerini ayarlama (temel ambarlama)</span><span class="sxs-lookup"><span data-stu-id="62ac0-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="62ac0-104">Bu yordam, ürünlerin ambardaki stok düzeylerini ayarlamak için bir stok ayarlama günlüğünü oluşturma ve deftere nakletme işlemini size gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="62ac0-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="62ac0-105">Buna başlamadan önce stok düzeltmeleri için ayarlanmış bir stok günlüğü adı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="62ac0-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="62ac0-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62ac0-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="62ac0-107">Bu görevler normalde ambar personeli tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="62ac0-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="62ac0-108">Bir stok düzeltme günlüğünü yaratmak</span><span class="sxs-lookup"><span data-stu-id="62ac0-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="62ac0-109">Stok yönetimi > Yevmiye defteri girişleri > Öğeler > Stok düzeltmesi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="62ac0-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="62ac0-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-110">Click New.</span></span>
3. <span data-ttu-id="62ac0-111">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="62ac0-112">Listede, kullanmak istediğiniz stok ayarlama günlük adını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="62ac0-113">Diğer bazı alanlar, seçtiğiniz stok ayarlama günlük adı kurulumu temel alınarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="62ac0-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="62ac0-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="62ac0-115">Günlük satırları oluştur</span><span class="sxs-lookup"><span data-stu-id="62ac0-115">Create journal lines</span></span>
1. <span data-ttu-id="62ac0-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-116">Click New.</span></span>
2. <span data-ttu-id="62ac0-117">Listede madde numarası alanını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="62ac0-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="62ac0-118">Madde numarası alanında bir maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="62ac0-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="62ac0-119">Demo verileri şirket USMF'yi kullanıyorsanız, 'D0001' yazın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="62ac0-120">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="62ac0-121">Listede, bir tesis seçin.</span><span class="sxs-lookup"><span data-stu-id="62ac0-121">In the list, select a site.</span></span>
6. <span data-ttu-id="62ac0-122">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="62ac0-123">Listede bir ambar seçin.</span><span class="sxs-lookup"><span data-stu-id="62ac0-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="62ac0-124">Bir öğe için zorunlu boyut olarak konum seçtiyseniz, burada konumu belirtmeniz gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="62ac0-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="62ac0-125">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="62ac0-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="62ac0-126">Maliyet fiyatı alanı, stok girişleriyle bağlantılı olarak birim başına maliyeti belirtir.</span><span class="sxs-lookup"><span data-stu-id="62ac0-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="62ac0-127">Madde numarası için maliyetin belirtilmemiş olması veya bunu el ile değiştirmek istemeniz durumunda, bunu burada yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62ac0-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="62ac0-128">Stok düzeltme günlüğünü geçerli kılın ve nakledin</span><span class="sxs-lookup"><span data-stu-id="62ac0-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="62ac0-129">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-129">Click Validate.</span></span>
2. <span data-ttu-id="62ac0-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-130">Click OK.</span></span>
3. <span data-ttu-id="62ac0-131">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-131">Click Post.</span></span>
    * <span data-ttu-id="62ac0-132">Bu tür bir günlüğü naklettiğinizde stok girişi veya çıkışı nakledilir, stok düzeyi ve değeri değiştirilir ve genel muhasebe hareketleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="62ac0-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="62ac0-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-133">Click OK.</span></span>
5. <span data-ttu-id="62ac0-134">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-134">Close the form.</span></span>
6. <span data-ttu-id="62ac0-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="62ac0-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]