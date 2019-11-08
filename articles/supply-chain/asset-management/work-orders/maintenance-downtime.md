---
title: Bakım kesinti süresi
description: Bu konuda Varlık Yönetimi'ndeki bakım kesinti süresini açıklar.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad9f1b2a0e63b4fb0d6daceb451c3a1dc1ec7de7
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626167"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="8c009-103">Bakım kesinti süresi</span><span class="sxs-lookup"><span data-stu-id="8c009-103">Maintenance downtime</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="8c009-104">Bir iş emrinde seçilen kıymet üzerinde bakım kesinti süresi kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c009-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="8c009-105">Bu özellik, üretim alanındaki bir veya daha fazla makinede bakım kapalı kalma süresini kaydetmek istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="8c009-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="8c009-106">Önce, kullanmak istediğiniz bakım kesinti süresi nedeni kodlarını (örneğin, **Döküm** ve **Planlı durdurma**) oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="8c009-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="8c009-107">Bu adım, **Bakım kesinti süresi sebep kodları** sayfasında gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8c009-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="8c009-108">**Bakım kesinti süresi** sayfasında bakım kesinti süresi kayıtları oluşturabilir ve ilgili bakım kesinti süresi neden kodlarını ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c009-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="8c009-109">Bakım kesinti süresi sebep kodları oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c009-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="8c009-110">**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Bakım kesinti süresi neden kodları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="8c009-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-111">Select **New**.</span></span>

3. <span data-ttu-id="8c009-112">**Bakım kesinti süresi neden kodu** alanına bakım kesinti süresi neden kodu için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="8c009-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="8c009-113">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8c009-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="8c009-114">Neden kodunun varlığın temel performans göstergeleri (KPI) hesaplamalarına dahil edilmesi gerekiyorsa, **KPI dahil et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="8c009-115">Genel olarak, planlanan üretim durakları beklenen performansı etkilemediği için KPI hesaplamalarına dahil edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8c009-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="8c009-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-116">Select **Save**.</span></span>

<span data-ttu-id="8c009-117">Aşağıdaki şekilde bir **Bakım kesinti süresi neden kodları** sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8c009-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![Şekil 1](media/15-work-orders.png)

<span data-ttu-id="8c009-119">Kullanmak istediğiniz bakım kesinti süresi nedeni kodlarını oluşturduktan sonra, iş emirleri ve varlıklar için bakım kesinti süresi kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c009-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="8c009-120">Bakım kesinti süresi kayıtları oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c009-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="8c009-121">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c009-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8c009-122">İş emrini seçin ve **İş emri** sekmesinde, **Varlık** grubunda **Bakım kesinti süresi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="8c009-123">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-123">Select **New**.</span></span>

4. <span data-ttu-id="8c009-124">**Başlangıç** ve **Bitiş** alanlarında bakım kesinti süresi kaydı için tarih ve saat aralığını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="8c009-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="8c009-125">**Giden** alanından çıktığınızda, saatlerin süresi otomatik olarak **Süre** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="8c009-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="8c009-126">**Bakım kesinti süresi neden kodu** alanında bir neden kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="8c009-127">Daha fazla kayıt eklemek için 3 ile 5. adımlar arasındaki işlemleri tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="8c009-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="8c009-128">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c009-128">Select **Save**.</span></span>

<span data-ttu-id="8c009-129">Aşağıdaki şekilde bir bakım kesinti süresi kaydı örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8c009-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![Şekil 2](media/16-work-orders.png)

<span data-ttu-id="8c009-131">Bakım kapalı kalma süresini hesaplamak için kullanılan takvim, varlıklar ve parametreler kurulumunda yaptığınız seçime bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8c009-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="8c009-132">**Tüm varlıklar** sayfasının **Sabit kıymetler** hızlı sekmesindeki **Kaynak** alanındaki bir varlıkta kaynak seçildiyse, ilişkili kaynak grubu için takvim kurulumu aşağıdaki şekildeki gibi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8c009-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![Şekil 3](media/17-work-orders.png)

<span data-ttu-id="8c009-134">Varlık üzerinde bir kaynak seçilmemişse, **Varlık yönetimi parametreleri** sayfasında seçilen standart takvim içinde kullanılır, aşağıdaki şekilde görüntülendiği gibi.</span><span class="sxs-lookup"><span data-stu-id="8c009-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![Şekil 4](media/18-work-orders.png)

<span data-ttu-id="8c009-136">**Varlık yönetimi** > **Sorgular** > **Bakım kesinti süresi**'ne tıklayarak tüm bakım kesinti süresi kayıtlarına genel bir bakışı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c009-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="8c009-137">**Varlık Yönetimi** modülü içinde kullanılan tüm takvimler, **Kuruluş yönetimi** > **Kurulum** > **Takvimler** > **Takvimler** içinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8c009-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

