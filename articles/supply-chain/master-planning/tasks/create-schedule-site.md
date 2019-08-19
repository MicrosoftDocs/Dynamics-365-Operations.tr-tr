---
title: Tesis için zaman çizelgesi oluşturma
description: Bu prosedürde bir saha için henüz başlamamış üretim emirlerinin nasıl zamanlanacağı açıklanmıştır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51c9ca8c402880f93a5998605d946b881d5ccdf5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835898"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="766e3-103">Tesis için zaman çizelgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="766e3-103">Create a schedule for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="766e3-104">Bu prosedürde bir saha için henüz başlamamış üretim emirlerinin nasıl zamanlanacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="766e3-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="766e3-105">Bu prosedürün tamamlanması için USMF demo veri şirketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="766e3-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="766e3-106">Başlamamış üretim emirlerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="766e3-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="766e3-107">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="766e3-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="766e3-108">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="766e3-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="766e3-109">Örneğin, Saha alanına '1' değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="766e3-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="766e3-110">1, USMF'deki bir sahayı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="766e3-110">1 represents a site in USMF.</span></span> <span data-ttu-id="766e3-111">USMF'yi kullanmıyorsanız, kendi şirketinizden bir saha seçin.</span><span class="sxs-lookup"><span data-stu-id="766e3-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="766e3-112">Durum sütunu filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="766e3-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="766e3-113">"tam olarak" filtre işleci kullanılarak bir "Zamanlanmış" değeriyle "Durum" alanına bir filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="766e3-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="766e3-114">Bir zamanlama oluşturma</span><span class="sxs-lookup"><span data-stu-id="766e3-114">Create a schedule</span></span>
1. <span data-ttu-id="766e3-115">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="766e3-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="766e3-116">Eylem Bölmesinde, Planla öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="766e3-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="766e3-117">İşleri planla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="766e3-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="766e3-118">İş planlama çizelgeleme yönü alanında 'Teslimat tarihinden geriye doğru' seçin.</span><span class="sxs-lookup"><span data-stu-id="766e3-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="766e3-119">Sınırlı kapasite alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="766e3-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="766e3-120">Sınırlı malzeme alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="766e3-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="766e3-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="766e3-121">Click OK.</span></span>
    * <span data-ttu-id="766e3-122">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="766e3-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="766e3-123">Zamanlanmış üretim emirlerinin sonuçlarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="766e3-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="766e3-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="766e3-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="766e3-125">Herhangi bir sırayı işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="766e3-125">You can mark any row.</span></span>  
2. <span data-ttu-id="766e3-126">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="766e3-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="766e3-127">Tüm işleri çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="766e3-127">Click All jobs.</span></span>
    * <span data-ttu-id="766e3-128">Bu sayfada, işlerin listesini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="766e3-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="766e3-129">Zamanlama sekmesinde, bir iş için Başlangıç tarihini ve Bitiş tarihini görüntülenebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="766e3-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="766e3-130">Malzemeler öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="766e3-130">Click Materials.</span></span>
    * <span data-ttu-id="766e3-131">Bu sayfada, üretim emri ve güncel kullanılabilir stok üzerindeki işlemler için tahmini malzeme tüketimini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="766e3-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

