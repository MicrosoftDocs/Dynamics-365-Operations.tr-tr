---
title: Üretim emrini planlama
description: Bu yordam, bir üretim emrini nasıl planlayacağınızı gösterir.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7ee023f39cc5d02b0f5b80fbb3ae3ad0c9774
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "346376"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="b33c8-103">Üretim emrini planlama</span><span class="sxs-lookup"><span data-stu-id="b33c8-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b33c8-104">Bu yordam, bir üretim emrini nasıl planlayacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="b33c8-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="b33c8-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="b33c8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b33c8-106">Bu, üretim emri ömrünü açıklayan yedi yordamın üçüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="b33c8-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="b33c8-107">Üretim emrini planlama</span><span class="sxs-lookup"><span data-stu-id="b33c8-107">Schedule a production order</span></span>
1. <span data-ttu-id="b33c8-108">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b33c8-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="b33c8-109">Tahmini durumunda olan bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="b33c8-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="b33c8-110">Eylem Bölmesinde, Planla öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="b33c8-111">İşleri planla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="b33c8-112">Zamanlama için parametreler bu sayfada ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b33c8-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="b33c8-113">Belirli kullanıcılar veya tüm kullanıcılar için parametreler ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b33c8-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="b33c8-114">İş planlama çizelgeleme yönü alanında 'Bugünden İleriye doğru' seçin.</span><span class="sxs-lookup"><span data-stu-id="b33c8-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="b33c8-115">Planlama tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="b33c8-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="b33c8-116">Sınırlı kapasite kutusunu gerektiği gibi seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="b33c8-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="b33c8-117">Sınırlı malzeme kutusunu gerektiği gibi seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="b33c8-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="b33c8-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="b33c8-119">Planlama sonuçlarını görüntüle</span><span class="sxs-lookup"><span data-stu-id="b33c8-119">View the scheduling results</span></span>
1. <span data-ttu-id="b33c8-120">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b33c8-121">Tüm işleri çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-121">Click All jobs.</span></span>
    * <span data-ttu-id="b33c8-122">Bu sayfa, yalnızca oluşturduğunuz zamanlanmış işleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b33c8-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="b33c8-123">Planlama bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="b33c8-124">Planlama FastTab'inde, planlanan tarih ve saati görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b33c8-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="b33c8-125">Sorgulamalar’ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-125">Click Inquiries.</span></span>
5. <span data-ttu-id="b33c8-126">Kapasite yükü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-126">Click Capacity load.</span></span>
    * <span data-ttu-id="b33c8-127">Kapasite yükü sayfası; iş planlaması üzerinden ayrılan kapasiteyi, kaynakta geçerli olarak ayrılan toplam saat sayısını ve kaynak iş planlaması için kalan saat sayısını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b33c8-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="b33c8-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-128">Close the page.</span></span>
7. <span data-ttu-id="b33c8-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b33c8-129">Close the page.</span></span>

