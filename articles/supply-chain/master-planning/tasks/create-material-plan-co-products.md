--- 
title: "Ortak ürünler için malzeme planı oluşturma"
description: "Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: adc1e520ce9ec705555939f29008d7fc4494999a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="47db5-103">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="47db5-103">Create a material plan for co-products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47db5-104">Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.</span><span class="sxs-lookup"><span data-stu-id="47db5-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="47db5-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="47db5-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="47db5-106">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="47db5-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="47db5-107">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="47db5-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="47db5-108">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="47db5-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="47db5-109">Click New.</span></span>
4. <span data-ttu-id="47db5-110">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-110">Click Sales order.</span></span>
5. <span data-ttu-id="47db5-111">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47db5-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="47db5-112">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="47db5-112">Example: US-001</span></span>  
6. <span data-ttu-id="47db5-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-113">Click OK.</span></span>
7. <span data-ttu-id="47db5-114">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47db5-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="47db5-115">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="47db5-115">Example: P6003</span></span>  
8. <span data-ttu-id="47db5-116">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="47db5-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="47db5-117">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="47db5-117">Example: 50000</span></span>  
9. <span data-ttu-id="47db5-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="47db5-119">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="47db5-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="47db5-120">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-120">Click Master planning.</span></span>
2. <span data-ttu-id="47db5-121">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="47db5-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="47db5-123">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="47db5-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="47db5-124">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-124">Click Run.</span></span>
5. <span data-ttu-id="47db5-125">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="47db5-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="47db5-126">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-126">Click Filter.</span></span>
7. <span data-ttu-id="47db5-127">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="47db5-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="47db5-128">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="47db5-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="47db5-129">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="47db5-129">Example: P6003</span></span>  
9. <span data-ttu-id="47db5-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-130">Click OK.</span></span>
10. <span data-ttu-id="47db5-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-131">Click OK.</span></span>
11. <span data-ttu-id="47db5-132">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-132">Click Planned orders.</span></span>
12. <span data-ttu-id="47db5-133">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="47db5-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="47db5-134">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="47db5-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="47db5-135">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="47db5-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="47db5-136">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="47db5-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="47db5-137">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="47db5-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="47db5-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="47db5-139">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="47db5-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="47db5-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47db5-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="47db5-141">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="47db5-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="47db5-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="47db5-142">Close the page.</span></span>


