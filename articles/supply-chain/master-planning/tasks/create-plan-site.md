--- 
title: "Tesis için plan oluşturma"
description: "Üretim planlayıcısı, belirli bir maddenin üretim için malzeme ve kapasite gereksinimlerini hesaplar."
author: ShylaThompson
manager: AnnBe
ms.date: 06/10/2016
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
ms.openlocfilehash: f22b7271432316aa745e0c4cd3f1ed533805403e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="3a095-103">Tesis için plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a095-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a095-104">Üretim planlayıcısı, belirli bir maddenin üretim için malzeme ve kapasite gereksinimlerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="3a095-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="3a095-105">Kaynak kullanımı önerileri oluşturduktan sonra, acil olanlardan başlanarak, planlama yapılan saha için siparişler ve sipariş tarihleri seçilir.</span><span class="sxs-lookup"><span data-stu-id="3a095-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="3a095-106">En acil siparişler, güncel tarih olarak belirlenmesi gereken siparişlerdir.</span><span class="sxs-lookup"><span data-stu-id="3a095-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="3a095-107">Bu görevleri gerçekleştirmek için USMF demo veri şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a095-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="3a095-108">Bir madde için bir malzeme ve kapasite planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a095-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="3a095-109">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-109">Click Master planning.</span></span>
    * <span data-ttu-id="3a095-110">Varsayılan Panoya gitmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a095-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="3a095-111">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-111">Click Run.</span></span>
3. <span data-ttu-id="3a095-112">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3a095-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="3a095-113">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-113">Click Filter.</span></span>
5. <span data-ttu-id="3a095-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3a095-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="3a095-115">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3a095-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3a095-116">Örnek: D0001</span><span class="sxs-lookup"><span data-stu-id="3a095-116">Example: D0001</span></span>  
7. <span data-ttu-id="3a095-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-117">Click OK.</span></span>
8. <span data-ttu-id="3a095-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-118">Click OK.</span></span>
    * <span data-ttu-id="3a095-119">Bu işlem birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="3a095-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="3a095-120">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="3a095-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="3a095-121">Madde için acil planlanan siparişleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="3a095-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="3a095-122">Madde numarası sütunu filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="3a095-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="3a095-123">"Madde numarası" alanında "ile başlar" filtre işlecini kullanan "D0001" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="3a095-124">Sipariş tarihi sütun filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="3a095-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="3a095-125">"tam olarak" filtresi işlecini kullanarak, "Sipariş tarihi" alanına bir güncel tarih değeriyle bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="3a095-126">Madde için tüm acil siparişleri kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="3a095-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="3a095-127">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="3a095-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="3a095-128">Kesinleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-128">Click Firm.</span></span>
3. <span data-ttu-id="3a095-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a095-129">Click OK.</span></span>


