---
title: "Ambardaki stok düzeylerini başlatma"
description: "Bu yordam, eldeki stoğu, stok hareket günlüğü kullanarak el ile nasıl güncelleştirileceğini gösterir."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 3b4685b034f7e6a3af0259fb921230e7b3397754
ms.contentlocale: tr-tr
ms.lasthandoff: 11/02/2017

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="dc7dd-103">Ambardaki stok düzeylerini başlatma</span><span class="sxs-lookup"><span data-stu-id="dc7dd-103">Initialize stock levels in the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc7dd-104">Bu yordam, eldeki stoğu, stok hareket günlüğü kullanarak el ile nasıl güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="dc7dd-105">(Ayrıca, eldeki stoğu, veri varlıklarındaki hareketleri içeri alarak güncelleştirmek mümkündür.) Bu kılavuzu içerisinde , günlük adı, Madde Kurulumu, nakil profilleri, ve mevcut hesapların da arasında olduğu tüm önkoşulları bulunduran, demo veri şirketi USMF verilerini kullanarak çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="dc7dd-106">Bu rehber kullanılan madde ve boyutlar için belirli değerler önerir.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="dc7dd-107">Farklı bir öğeyi seçerseniz, farklı boyutlar için değerler girmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="dc7dd-108">Stok yönetimi > Yevmiye defteri girişleri > Öğeler > Taşıma seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="dc7dd-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-109">Click New.</span></span>
3. <span data-ttu-id="dc7dd-110">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dc7dd-111">IMov'u seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-111">Select IMov.</span></span>
    * <span data-ttu-id="dc7dd-112">Farklı günlük adı şablonlarını farklı ticari amaçlarla kullanmak iyi bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-112">It’s a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="dc7dd-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="dc7dd-114">Mahsup hesabı alanında, '140200' değerlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="dc7dd-115">Bu mahsup hesap, günlük satırlarındaki varsayılan olarak belirlenecek hesaptır.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="dc7dd-116">Her satırda farklı mahsup hesapları atamak için varsayılan geçersiz kılmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="dc7dd-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-117">Click OK.</span></span>
8. <span data-ttu-id="dc7dd-118">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-118">Click New.</span></span>
9. <span data-ttu-id="dc7dd-119">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dc7dd-120">Madde A0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-120">Select item A0001.</span></span>
11. <span data-ttu-id="dc7dd-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dc7dd-122">Stok boyutları sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="dc7dd-123">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dc7dd-124">Saha 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-124">Select site 1.</span></span>
15. <span data-ttu-id="dc7dd-125">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="dc7dd-126">Ambar 13'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="dc7dd-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="dc7dd-128">Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="dc7dd-129">Yer 13'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-129">Select location 13.</span></span>
20. <span data-ttu-id="dc7dd-130">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="dc7dd-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-131">Click Save.</span></span>
22. <span data-ttu-id="dc7dd-132">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-132">Click Post.</span></span>
23. <span data-ttu-id="dc7dd-133">Tüm deftere nakil hatalarını yeni bir günlüğe aktar onay kutusunun işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="dc7dd-134">Bu seçeneği etkinleştirirseniz, deftere nakledilmede başarısız olan satırlar yeni bir günlüğe kopyalanacaktır.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="dc7dd-135">Sorunları düzeltmek ve satırları daha sonra yeniden deftere nakletmek için günlükteki bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="dc7dd-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-136">Click OK.</span></span>
25. <span data-ttu-id="dc7dd-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-137">Close the page.</span></span>
26. <span data-ttu-id="dc7dd-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dc7dd-138">Close the page.</span></span>

