---
title: Kısıtlanmış plan oluşturma
description: Bu konu, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8b9d5712dd1b4f9958de775e1a2224b64485d05
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987226"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="e3a28-103">Kısıtlanmış plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3a28-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3a28-104">Bu konu, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e3a28-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="e3a28-105">Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e3a28-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="e3a28-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="e3a28-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e3a28-107">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="e3a28-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="e3a28-108">Kısıtlı bir plan ayarlayın</span><span class="sxs-lookup"><span data-stu-id="e3a28-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="e3a28-109">Giriş sayfasında, **Master planlama** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="e3a28-110">Çalışma alanının en sağ ucundaki bağlantı listesinde **Master planlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="e3a28-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="e3a28-112">Örnek: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="e3a28-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="e3a28-113">**Sınırlı kapasite** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="e3a28-114">**Sınırlı kapasite zaman dilimi** alanına `30` girin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="e3a28-115">**Gün cinsinden zaman dilimleri** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="e3a28-116">**Kapasite** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="e3a28-117">**Kapasite planlama zaman dilimi (gün)** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="e3a28-118">Örnek: `60`</span><span class="sxs-lookup"><span data-stu-id="e3a28-118">Example: `60`</span></span>  
9. <span data-ttu-id="e3a28-119">**Hesaplanan gecikmeler** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="e3a28-120">**Gecikme zaman dilimini (gün)** hesapla alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="e3a28-121">Örnek: `60`</span><span class="sxs-lookup"><span data-stu-id="e3a28-121">Example: `60`</span></span> 
11. <span data-ttu-id="e3a28-122">**Hesaplanan gecikmeler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="e3a28-123">**Hesaplanan gecikmeyi gereksinim tarihine ekle** alanlarında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="e3a28-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3a28-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="e3a28-125">Sınırlandırılmış bir plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3a28-125">Create a constrained plan</span></span>
1. <span data-ttu-id="e3a28-126">**Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-126">Select **Run**.</span></span>
2. <span data-ttu-id="e3a28-127">**Master plan** alanında, sınırlamalarını ayarladığınız planı girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="e3a28-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-128">Select **OK**.</span></span>
4. <span data-ttu-id="e3a28-129">**Planlı siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3a28-129">Select **Planned orders**.</span></span>

