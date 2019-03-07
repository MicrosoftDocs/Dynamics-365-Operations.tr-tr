---
title: Eski ürün çeşitlerini bulma
description: Bu yordam eski ürünleri veya ürün çeşitlerini nasıl bulabileceğinizi ve bir ürün yaşam döngüsü durumunu eski ürünlerle nasıl ilişkilendirebileceğinizi gösterir.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4641d24cfa24722f5411da8943bfe4095a9546a4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "360199"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="e352c-103">Eski ürün çeşitlerini bulma</span><span class="sxs-lookup"><span data-stu-id="e352c-103">Find obsolete product variants</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e352c-104">Bu yordam eski ürünleri veya ürün çeşitlerini nasıl bulabileceğinizi ve bir ürün yaşam döngüsü durumunu eski ürünlerle nasıl ilişkilendirebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e352c-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="e352c-105">Önkoşul: Bu görev kılavuzunu çalıştırmadan önce etkin durumda olmayan en az bir ürün yaşam döngüsü durumu tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e352c-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="e352c-106">Benzetimi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e352c-106">Run a simulation</span></span>
1. <span data-ttu-id="e352c-107">Ürün yönetimi bilgileri > Periyodik görevler > Eski ürünler için yaşam döngüsü durumunu değiştir öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e352c-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="e352c-108">Yeni ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e352c-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="e352c-109">Ürün verilerini güncelleştirmeden benzetimi çalıştır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e352c-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="e352c-110">Bu sayıda gün içinde oluşturulan ürünleri hariç tut alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e352c-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="e352c-111">Hareketlerde (belirtilen sayıda gün içinde) kullanılan ürünleri hariç tut alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e352c-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="e352c-112">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e352c-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="e352c-113">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e352c-113">Click Filter.</span></span>
8. <span data-ttu-id="e352c-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e352c-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e352c-115">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e352c-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="e352c-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e352c-116">Click OK.</span></span>
11. <span data-ttu-id="e352c-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e352c-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="e352c-118">Çok sayıda ürün araması yapılmasını bekliyorsanız simülsayonu toplu işte çalıştırmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="e352c-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="e352c-119">Ayrıca, simülasyonun şirketin en yoğun çalıştığı saatlerde çalışmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="e352c-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="e352c-120">Benzetim sonuçlarını inceleme</span><span class="sxs-lookup"><span data-stu-id="e352c-120">Review the simulation results</span></span>
1. <span data-ttu-id="e352c-121">Ürün bilgileri yönetimi >Sorgular ve raporlar > Ürün yaşam döngüsü durumu bakım geçmişi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e352c-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="e352c-122">Bu sayfada, benzetim sonuçlarını inceleyebilir ve benzetim olmadan güncelleştirme çalıştırıldığında ne kadar ürün ve ürün çeşidinin yeni bir ürün yaşam döngüsü durumuyla ilişkilendirileceğini değerlendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e352c-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="e352c-123">Eski ürünler için ürün yaşam döngüsü durumu güncelleştirmesini çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e352c-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="e352c-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e352c-124">Close the page.</span></span>
2. <span data-ttu-id="e352c-125">Ürün yönetimi bilgileri > Periyodik görevler > Eski ürünler için yaşam döngüsü durumunu değiştir öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e352c-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="e352c-126">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e352c-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="e352c-127">Son seçimin kaydedildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e352c-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="e352c-128">Ürün verilerini güncelleştirmeden benzetimi çalıştır alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e352c-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="e352c-129">Arka planda çalıştır bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e352c-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="e352c-130">Kaç ürün ve ürün çeşidinin etkilendiğine bağlı olarak, bu işi toplu iş olarak çalıştırmayı düşünün.</span><span class="sxs-lookup"><span data-stu-id="e352c-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="e352c-131">Büyük bir güncelleştirme işini şirketin yoğun olduğu saatlerde çalıştırmadığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e352c-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="e352c-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e352c-132">Click OK.</span></span>
7. <span data-ttu-id="e352c-133">Ürün bilgileri yönetimi >Sorgular ve raporlar > Ürün yaşam döngüsü durumu bakım geçmişi öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e352c-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="e352c-134">Değiştirilen serbest bırakılmış ürünleri ve ürün çeşitlerini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="e352c-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="e352c-135">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e352c-135">In the list, find and select the desired record.</span></span>

