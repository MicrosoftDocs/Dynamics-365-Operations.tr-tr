---
title: Tesis için plan oluşturma
description: Üretim planlayıcısı, belirli bir maddenin üretim için malzeme ve kapasite gereksinimlerini hesaplar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "364776"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="9b474-103">Tesis için plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b474-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b474-104">Üretim planlayıcısı, belirli bir maddenin üretim için malzeme ve kapasite gereksinimlerini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="9b474-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="9b474-105">Kaynak kullanımı önerileri oluşturduktan sonra, acil olanlardan başlanarak, planlama yapılan saha için siparişler ve sipariş tarihleri seçilir.</span><span class="sxs-lookup"><span data-stu-id="9b474-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="9b474-106">En acil siparişler, güncel tarih olarak belirlenmesi gereken siparişlerdir.</span><span class="sxs-lookup"><span data-stu-id="9b474-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="9b474-107">Bu görevleri gerçekleştirmek için USMF demo veri şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9b474-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="9b474-108">Bir madde için bir malzeme ve kapasite planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b474-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="9b474-109">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-109">Click Master planning.</span></span>
    * <span data-ttu-id="9b474-110">Varsayılan Panoya gitmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b474-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="9b474-111">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-111">Click Run.</span></span>
3. <span data-ttu-id="9b474-112">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9b474-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="9b474-113">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-113">Click Filter.</span></span>
5. <span data-ttu-id="9b474-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9b474-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="9b474-115">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9b474-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9b474-116">Örnek: D0001</span><span class="sxs-lookup"><span data-stu-id="9b474-116">Example: D0001</span></span>  
7. <span data-ttu-id="9b474-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-117">Click OK.</span></span>
8. <span data-ttu-id="9b474-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-118">Click OK.</span></span>
    * <span data-ttu-id="9b474-119">Bu işlem birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="9b474-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="9b474-120">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="9b474-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="9b474-121">Madde için acil planlanan siparişleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="9b474-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="9b474-122">Madde numarası sütunu filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="9b474-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="9b474-123">"Madde numarası" alanında "ile başlar" filtre işlecini kullanan "D0001" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="9b474-124">Sipariş tarihi sütun filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="9b474-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="9b474-125">"tam olarak" filtresi işlecini kullanarak, "Sipariş tarihi" alanına bir güncel tarih değeriyle bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="9b474-126">Madde için tüm acil siparişleri kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="9b474-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="9b474-127">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9b474-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="9b474-128">Kesinleştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-128">Click Firm.</span></span>
3. <span data-ttu-id="9b474-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9b474-129">Click OK.</span></span>

