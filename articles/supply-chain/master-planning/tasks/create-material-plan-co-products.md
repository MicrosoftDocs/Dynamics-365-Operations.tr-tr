--- 
title: "Ortak ürünler için malzeme planı oluşturma"
description: "Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7ba6c-103">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ba6c-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ba6c-104">Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="7ba6c-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7ba6c-106">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="7ba6c-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="7ba6c-107">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="7ba6c-108">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="7ba6c-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-109">Click New.</span></span>
4. <span data-ttu-id="7ba6c-110">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-110">Click Sales order.</span></span>
5. <span data-ttu-id="7ba6c-111">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="7ba6c-112">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="7ba6c-112">Example: US-001</span></span>  
6. <span data-ttu-id="7ba6c-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-113">Click OK.</span></span>
7. <span data-ttu-id="7ba6c-114">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7ba6c-115">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="7ba6c-115">Example: P6003</span></span>  
8. <span data-ttu-id="7ba6c-116">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="7ba6c-117">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="7ba6c-117">Example: 50000</span></span>  
9. <span data-ttu-id="7ba6c-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7ba6c-119">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7ba6c-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="7ba6c-120">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-120">Click Master planning.</span></span>
2. <span data-ttu-id="7ba6c-121">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7ba6c-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7ba6c-123">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="7ba6c-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="7ba6c-124">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-124">Click Run.</span></span>
5. <span data-ttu-id="7ba6c-125">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="7ba6c-126">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-126">Click Filter.</span></span>
7. <span data-ttu-id="7ba6c-127">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="7ba6c-128">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="7ba6c-129">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="7ba6c-129">Example: P6003</span></span>  
9. <span data-ttu-id="7ba6c-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-130">Click OK.</span></span>
10. <span data-ttu-id="7ba6c-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-131">Click OK.</span></span>
11. <span data-ttu-id="7ba6c-132">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-132">Click Planned orders.</span></span>
12. <span data-ttu-id="7ba6c-133">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7ba6c-134">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7ba6c-135">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="7ba6c-136">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7ba6c-137">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="7ba6c-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="7ba6c-139">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="7ba6c-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7ba6c-141">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="7ba6c-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7ba6c-142">Close the page.</span></span>


