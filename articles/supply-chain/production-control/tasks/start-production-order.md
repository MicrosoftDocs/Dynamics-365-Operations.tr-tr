---
title: Üretim emrini başlatma
description: Bu yordam, üretim emirlerinin atölyede nasıl başlatılacağını gösterir.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "346238"
---
# <a name="start-a-production-order"></a><span data-ttu-id="4c9b0-103">Üretim emrini başlatma</span><span class="sxs-lookup"><span data-stu-id="4c9b0-103">Start a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c9b0-104">Bu yordam, üretim emirlerinin atölyede nasıl başlatılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="4c9b0-105">Bu işlemde, zaman ve malzeme tüketimi bildirilir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="4c9b0-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4c9b0-107">Bu, üretim emri ömrünü açıklayan yedi yordamdan beşincisidir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="4c9b0-108">Üretim emrini başlatma</span><span class="sxs-lookup"><span data-stu-id="4c9b0-108">Start a production order</span></span>
1. <span data-ttu-id="4c9b0-109">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="4c9b0-110">Serbest bırakılmış durumunda olan bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="4c9b0-111">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="4c9b0-112">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-112">Click Start.</span></span>
    * <span data-ttu-id="4c9b0-113">Bu sayfada, üretim emrinin başlatılmasını onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="4c9b0-114">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-114">Click the General tab.</span></span>
5. <span data-ttu-id="4c9b0-115">Operasyon Numarası</span><span class="sxs-lookup"><span data-stu-id="4c9b0-115">In the From Oper.</span></span> <span data-ttu-id="4c9b0-116">Hayır.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-116">No.</span></span> <span data-ttu-id="4c9b0-117">alanına '10' girin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-117">field, enter '10'.</span></span>
6. <span data-ttu-id="4c9b0-118">Otomatik rota tüketimi alanında, 'Her zaman' seçin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="4c9b0-119">Nakletme Rota kartını şimdi onaylayın kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="4c9b0-120">Otomatik malzeme listesi tüketimi alanında, 'Her zaman' seçin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="4c9b0-121">Malzeme çekme listesini şimdi naklet kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="4c9b0-122">Malzeme çekme listesini yazdır kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="4c9b0-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-123">Click OK.</span></span>
    * <span data-ttu-id="4c9b0-124">Bu, üretim emri için kullanılan malzemeleri gösteren yazılı malzeme çekme listesidir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="4c9b0-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="4c9b0-126">Malzeme çekme listesini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="4c9b0-126">Validate the picking list</span></span>
1. <span data-ttu-id="4c9b0-127">Eylem Bölmesinde, Görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="4c9b0-128">Malzeme çekme listesi'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-128">Click Picking list.</span></span>
3. <span data-ttu-id="4c9b0-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="4c9b0-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4c9b0-131">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-131">Click Edit.</span></span>
6. <span data-ttu-id="4c9b0-132">Tüketim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="4c9b0-133">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-133">Click Post.</span></span>
8. <span data-ttu-id="4c9b0-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-134">Click OK.</span></span>
    * <span data-ttu-id="4c9b0-135">Üretim emri tarafından tüketilen malzemeler, malzeme çekme listesi günlüğü defterine nakledilir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="4c9b0-136">Günlüğü deftere nakletmeden önce, tahmin edilen miktar ve gerçek tüketilen miktar arasında bir fark varsa gerekli ayarlamaları yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="4c9b0-137">GridPanel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="4c9b0-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="4c9b0-139">Rota kartı günlüğünü doğrulayın</span><span class="sxs-lookup"><span data-stu-id="4c9b0-139">Verify the route card journal</span></span>
1. <span data-ttu-id="4c9b0-140">Eylem Bölmesinde, Görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="4c9b0-141">Rota kartı'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-141">Click Route card.</span></span>
3. <span data-ttu-id="4c9b0-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="4c9b0-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4c9b0-144">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-144">Click Edit.</span></span>
6. <span data-ttu-id="4c9b0-145">Saatler alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="4c9b0-146">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-146">Click Post.</span></span>
8. <span data-ttu-id="4c9b0-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-147">Click OK.</span></span>
    * <span data-ttu-id="4c9b0-148">Tekil operasyonlar için harcanan zaman rota kartı günlüğünde kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="4c9b0-149">İyi ve hata miktarı da bildirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4c9b0-149">Good and error quantity can also be reported.</span></span>  
