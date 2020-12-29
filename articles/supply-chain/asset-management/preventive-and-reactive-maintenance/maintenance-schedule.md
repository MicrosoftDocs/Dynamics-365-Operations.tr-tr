---
title: Bakım zamanlaması
description: Bu konuda Varlık Yönetimi'nde bakım zamanlaması açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 351e088ece0512fee1bb5f9dad020f32f7728fe4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439329"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="c47db-103">Bakım zamanlaması</span><span class="sxs-lookup"><span data-stu-id="c47db-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c47db-104">Bakım zamanlaması, gerçekleştirilecek tüm beklenen önleyici bakım planlarının, bakım isteklerinin ve bakım kayıtlarının bir listesini içerir. Bazı zamanlama satırları iş emirlerine dönüştürülmüş olabilir.</span><span class="sxs-lookup"><span data-stu-id="c47db-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="c47db-105">Dört bakım zamanlaması görünümü, görmek istediğiniz bakım zamanlaması satırlarına bağlı olarak birbirinden biraz farklıdır.</span><span class="sxs-lookup"><span data-stu-id="c47db-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="c47db-106">Menü Öğesi</span><span class="sxs-lookup"><span data-stu-id="c47db-106">Menu item</span></span>                  | <span data-ttu-id="c47db-107">İçeriklerin açıklaması</span><span class="sxs-lookup"><span data-stu-id="c47db-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47db-108">Tüm bakım zamanlamaları</span><span class="sxs-lookup"><span data-stu-id="c47db-108">All maintenance schedule</span></span>       | <span data-ttu-id="c47db-109">Tüm bakım zamanlaması satırları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c47db-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="c47db-110">Kıymet planım</span><span class="sxs-lookup"><span data-stu-id="c47db-110">My asset schedule</span></span>        | <span data-ttu-id="c47db-111">Çalışan olarak ilgili olduğunuz (şurada ayarlanır: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md)) işlem yapılacak yerleşimlerde yüklü olan varlıkları içeren tüm bakım zamanlaması satırları bu listede gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c47db-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="c47db-112">Bakım zamanlaması satırlarını aç</span><span class="sxs-lookup"><span data-stu-id="c47db-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="c47db-113">"oluşturuldu" durumundaki bakım zamanlaması satırları (henüz iş emrine dönüştürülmemiş veya atılmamış) bu listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c47db-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="c47db-114">Bakım zamanlaması havuzlarını aç</span><span class="sxs-lookup"><span data-stu-id="c47db-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="c47db-115">Bir iş emri havuzuyla ilgili bakım zamanlaması satırları bu listede gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c47db-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="c47db-116">Bakım zamanlaması satırı birkaç iş emri havuzuna dahil edilirse (bkz. [İş emri havuzları](../work-orders/work-order-pools.md)) bir kayıt her bir havuz için **Bakım zamanlaması havuzları aç** seçeneğinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c47db-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="c47db-117">Bu işlem, iş emri havuzlarındaki filtre seçeneklerini en iyi duruma getirmek için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c47db-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="c47db-118">Bakım zamanlamasını açmak için:</span><span class="sxs-lookup"><span data-stu-id="c47db-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="c47db-119">**Varlık yönetimi** > **Ortak** > **Bakım zamanlaması** > **Tüm bakım zamanlamaları** veya **Bakım zamanlaması satırlarını aç** veya **Bakım zamanlaması havuzlarını aç** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c47db-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="c47db-120">Bakım zamanlamasını güncelleştirmek için **Bakım planı** veya **Bakım sıraları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c47db-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="c47db-121">Bir bakım zamanlaması satırını, satırı seçip **Düzenle**'ye tıklayarak düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="c47db-122">Örneğin, servis düzeyini veya işin sorumlu çalışanını kolayca güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="c47db-123">Yalnızca henüz bir iş emrine bağlanmamış bakım çizelgesi satırlarını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="c47db-124">Bir bakım zamanlaması satırını, liste sayfasında seçip **Sil**'i tıklatarak silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="c47db-125">Bir bakım zamanlaması satırını, liste sayfasında seçip **At**'ı tıklatarak atabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="c47db-126">Örneğin, bir varlığın 2.000 km bakım planı ve 10.000 km bakım planı varsa, bu işlev yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="c47db-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="c47db-127">Daha sonra, 2.000 km bakım planından oluşturulan satırı 10.000 km, 20.000 km, 30.000 km vb. ile oluşturulan satırla denk geldiğinde atmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="c47db-128">Bir bakım planıyla ilgili bakım zamanlaması satırını iptal ederseniz, bu satır bu bakım planı zamanlandığında tekrar görünmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="c47db-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="c47db-129">Tüm seçili satırların aynı iş emri havuzuna dahil edilmesini istiyorsanız **Tüm bakım zamanlamaları** ve **İş emri havuzu**'ndaki çok sayıda bakım zamanlaması satırı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="c47db-130">**Tüm bakım zamanlamaları** veya **Bakım zamanlaması satırlarını aç** ya da **Bakım zamanlaması havuzlarını aç**'ta bir dizi bakım zamanlaması satırı seçebilir ve birçok satırda aynı düzenlemeyi yapmak istiyorsanız **Zamanlamayı ayarla**'ya tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="c47db-131">Seçilen bakım zamanlaması satırlarıyla ilgili beklenen başlangıç ve bitiş tarihlerini, hizmet düzeyini ve sorumlu bakım çalışanı grubunu veya sorumlu bakım görevlisini değiştirebilisiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="c47db-132">Bir bakım zamanlaması satırı bir iş emriyle ilişkili olduğunda, iş emri kodu **İş emri** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c47db-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="c47db-133">**Tüm varlıklar** ayrıntılı görünümünde > **Varlık bakım planları** hızlı sekmesinde, varlık için bakım planlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="c47db-134">Daha sonra, **Tüm Varlıklar**'da bir varlıkla ilgili bakım planı satırını silerseniz, bu bakım planını temel alarak oluşturulan "Oluşturuldu" durumundaki tüm bakım zamanlaması satırlarını da otomatik olarak silersiniz.</span><span class="sxs-lookup"><span data-stu-id="c47db-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="c47db-135">Ayrıca bkz. [Varlık oluşturma](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="c47db-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="c47db-136">Aşağıdaki çizimde **Tüm bakım zamanlamaları** liste sayfası gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c47db-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Şekil 1](media/16-preventive-maintenance.png)

