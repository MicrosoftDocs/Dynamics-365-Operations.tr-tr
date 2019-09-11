---
title: Bakım kesinti süresi
description: Bu konuda Varlık Yönetimi'ndeki bakım kesinti süresini açıklar.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918256"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="3bc5b-103">Bakım kesinti süresi</span><span class="sxs-lookup"><span data-stu-id="3bc5b-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3bc5b-104">Bir iş emrinde seçilen kıymet üzerinde bakım kapalı kalma kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="3bc5b-105">Bu, üretim alanındaki bir veya daha fazla makinede bakım kapalı kalma süresini kaydetmek istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="3bc5b-106">Önce, kullanmak istediğiniz bakım kapalı kalma nedeni kodlarını (örneğin, döküm ve planlı durak) oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="3bc5b-107">Bu, **Bakım kesinti süresi sebep kodları** içinde gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="3bc5b-108">Ardından **bakım kapalı kalma süresi** ve ilgili neden kodlarını ekleyebileceğiniz bakım süresi kaydı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="3bc5b-109">Bakım kesinti süresi sebep kodları oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bc5b-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="3bc5b-110">**Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Bakım kesinti süresi sebep kodları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="3bc5b-111">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-111">Click **New**.</span></span>

3. <span data-ttu-id="3bc5b-112">**Bakım kesinti nedeni kodu** alanına bir kimlik ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="3bc5b-113">**Ad** alanında sebep kodu için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="3bc5b-114">**KPI dahil et** onay kutusunu, sebep kodu varlık KPI hesaplamalarına dahil edilecekse seçin.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="3bc5b-115">Genel olarak, planlanan üretim durakları beklenen performansı etkilemediği için KPI hesaplamalarına dahil edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="3bc5b-116">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-116">Click **Save**.</span></span>

![Şekil 1](media/15-work-orders.png)


<span data-ttu-id="3bc5b-118">Kullanmak istediğiniz bakım kapalı kalma nedeni kodlarını oluşturduğunuzda, iş emirleri ve varlıklar için bakım kapalı kalma kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="3bc5b-119">Bakım kesinti süresi kayıtları oluşturma</span><span class="sxs-lookup"><span data-stu-id="3bc5b-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="3bc5b-120">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3bc5b-121">İş emrini seçin ve **bakım kapalı kalma süresini** tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="3bc5b-122">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-122">Click **New**.</span></span>

4. <span data-ttu-id="3bc5b-123">**Başlangıç** ve **Bitiş** alanlarında bakım kesinti süresi için tarih ve saat aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="3bc5b-124">**Giden** alanından çıktığınızda, saatlerin süresi otomatik olarak **Süre** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="3bc5b-125">**Bakım kesinti süresi sebep kodu** alanında bir sebep kodu girin.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="3bc5b-126">Daha fazla kayıt eklemek istiyorsanız, 3-6 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="3bc5b-127">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-127">Click **Save**.</span></span>


![Şekil 2](media/16-work-orders.png)


<span data-ttu-id="3bc5b-129">Bakım kapalı kalma süresini hesaplamak için kullanılan takvim, kıymetler ve parametreler kurulumunda yaptığınız seçime bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="3bc5b-130">Kaynak **Tüm varlıklar** > **Sabit varlıklar** Hızlı sekmesi > **Kaynak** alanındaki bir varlıkta seçildiyse, ilişkili kaynak grubu için takvim kurulumu aşağıdaki şekildeki gibi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![Şekil 3](media/17-work-orders.png)


<span data-ttu-id="3bc5b-132">Varlık üzerinde bir kaynak seçilmemişse, **Varlık yönetimi parametreleri** içinde seçilen standart takvim içinde kullanılır, aşağıdaki şekilde görüntülendiği gibi.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![Şekil 4](media/18-work-orders.png)


<span data-ttu-id="3bc5b-134">**Kurumsal varlık yönetimi** > **Sorgular** > **Bakım kesinti süresi** üzerine tıklayarak tüm bakım kesinti süresi kayıtlarının bir genel bakışını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="3bc5b-135">**Varlık Yönetimi** modülü içinde kullanılan tüm takvimler, **Kuruluş yönetimi** > **Kurulum** > **Takvimler** > **Takvimler** içinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

