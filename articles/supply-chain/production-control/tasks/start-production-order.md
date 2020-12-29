---
title: Üretim emrini başlatma
description: Bu yordam, üretim emirlerinin atölyede nasıl başlatılacağını gösterir.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47915a93151b1adc99ddb4e3facb29bf8db49dd6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439218"
---
# <a name="start-a-production-order"></a><span data-ttu-id="f61a6-103">Üretim emrini başlatma</span><span class="sxs-lookup"><span data-stu-id="f61a6-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f61a6-104">Bu yordam, üretim emirlerinin atölyede nasıl başlatılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="f61a6-105">Bu işlemde, zaman ve malzeme tüketimi bildirilir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="f61a6-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f61a6-107">Bu, üretim emri ömrünü açıklayan yedi yordamdan beşincisidir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="f61a6-108">Üretim emrini başlatma</span><span class="sxs-lookup"><span data-stu-id="f61a6-108">Start a production order</span></span>
1. <span data-ttu-id="f61a6-109">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="f61a6-110">Serbest bırakılmış durumunda olan bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="f61a6-111">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="f61a6-112">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-112">Click Start.</span></span>
    * <span data-ttu-id="f61a6-113">Bu sayfada, üretim emrinin başlatılmasını onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f61a6-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="f61a6-114">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-114">Click the General tab.</span></span>
5. <span data-ttu-id="f61a6-115">Operasyon Numarası</span><span class="sxs-lookup"><span data-stu-id="f61a6-115">In the From Oper.</span></span> <span data-ttu-id="f61a6-116">Hayır.</span><span class="sxs-lookup"><span data-stu-id="f61a6-116">No.</span></span> <span data-ttu-id="f61a6-117">alanına '10' girin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-117">field, enter '10'.</span></span>
6. <span data-ttu-id="f61a6-118">Otomatik rota tüketimi alanında, 'Her zaman' seçin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="f61a6-119">Nakletme Rota kartını şimdi onaylayın kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="f61a6-120">Otomatik malzeme listesi tüketimi alanında, 'Her zaman' seçin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="f61a6-121">Malzeme çekme listesini şimdi naklet kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="f61a6-122">Malzeme çekme listesini yazdır kutusunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="f61a6-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-123">Click OK.</span></span>
    * <span data-ttu-id="f61a6-124">Bu, üretim emri için kullanılan malzemeleri gösteren yazılı malzeme çekme listesidir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="f61a6-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="f61a6-126">Malzeme çekme listesini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="f61a6-126">Validate the picking list</span></span>
1. <span data-ttu-id="f61a6-127">Eylem Bölmesinde, Görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f61a6-128">Malzeme çekme listesi'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-128">Click Picking list.</span></span>
3. <span data-ttu-id="f61a6-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f61a6-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f61a6-131">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-131">Click Edit.</span></span>
6. <span data-ttu-id="f61a6-132">Tüketim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="f61a6-133">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-133">Click Post.</span></span>
8. <span data-ttu-id="f61a6-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-134">Click OK.</span></span>
    * <span data-ttu-id="f61a6-135">Üretim emri tarafından tüketilen malzemeler, malzeme çekme listesi günlüğü defterine nakledilir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="f61a6-136">Günlüğü deftere nakletmeden önce, tahmin edilen miktar ve gerçek tüketilen miktar arasında bir fark varsa gerekli ayarlamaları yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f61a6-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="f61a6-137">GridPanel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="f61a6-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="f61a6-139">Rota kartı günlüğünü doğrulayın</span><span class="sxs-lookup"><span data-stu-id="f61a6-139">Verify the route card journal</span></span>
1. <span data-ttu-id="f61a6-140">Eylem Bölmesinde, Görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f61a6-141">Rota kartı'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-141">Click Route card.</span></span>
3. <span data-ttu-id="f61a6-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f61a6-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f61a6-144">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-144">Click Edit.</span></span>
6. <span data-ttu-id="f61a6-145">Saatler alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f61a6-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="f61a6-146">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-146">Click Post.</span></span>
8. <span data-ttu-id="f61a6-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f61a6-147">Click OK.</span></span>
    * <span data-ttu-id="f61a6-148">Tekil operasyonlar için harcanan zaman rota kartı günlüğünde kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="f61a6-149">İyi ve hata miktarı da bildirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f61a6-149">Good and error quantity can also be reported.</span></span>  
