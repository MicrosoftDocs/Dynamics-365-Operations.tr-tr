---
title: Bakım talebi yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde bakım talebi yaşam döngüsü durumları ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5849e3a8c3c619916c718032579d4fe6444fa49b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889133"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="9b608-103">Bakım talebi yaşam döngüsü durumları</span><span class="sxs-lookup"><span data-stu-id="9b608-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="9b608-104">Bakım talebi yaşam döngüsü durumları bir isteğin gidebileceği aşamaları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9b608-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="9b608-105">Örneğin, **Oluşturulan**, **Etkin**ve **Sona ermiş** örnekler de içerir.</span><span class="sxs-lookup"><span data-stu-id="9b608-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="9b608-106">Bir bakım isteği iş emrine dönüştürüldüğünde, bakım talebinin artık etkin olmadığını göstermek üzere sürdürme isteği yaşam döngüsü durumu **sonlandırıldı** veya **Kapalı** olarak güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9b608-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="9b608-107">**Tüm bakım talepleri** listesi sayfasında, yaşam döngüsü durumlarından bağımsız olarak tüm bakım taleplerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b608-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="9b608-108">Bakım talebi yaşam döngüsü durumlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="9b608-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="9b608-109">**Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü durumları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="9b608-110">Bakım talebi yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="9b608-111">**Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="9b608-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="9b608-112">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="9b608-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="9b608-113">**Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü modelleri** alanı bu yaşam döngüsü durumunu kullanan bakım talebi yaşam döngüsü modellerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b608-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="9b608-114">**Genel** hızlı sekmesinde, bakım talebinin bu yaşam döngüsü durumunda etkin olması gerekiyorsa, **etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b608-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="9b608-115">Gerçek bitiş tarihi ve saatinin bu yaşam döngüsü durumunda olan bir bakım isteğine otomatik olarak girilmesi gerekiyorsa, **Fiili bitiş ayarla** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b608-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="9b608-116">İş emri , bu yaşam döngüsü durumunda olan bir bakım talebinden oluşturulduysa, **İş emrini oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b608-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="9b608-117">Bir bakım talebi bu yaşam döngüsü durumundayken silinebilecekse, **Sil** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b608-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="9b608-118">**Güncelleştirme** hızlı sekmesinde, **Varlık** bölümündeki **Gelen** ve **Giden** seçenekleri depo onarımı görürseniz geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9b608-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="9b608-119">Bakım isteğinde seçilen varlıkların varlık yaşam döngüsü durumunun, bu bakım talebinin bakım talebi yaşam döngüsü durumu **Gelen** veya **Giden** olarak ayarladığında, otomatik olarak **Gelen** veya **Giden** olarak güncelleştirilmesi gerekiyorsa ilgili seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9b608-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="9b608-120">Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü durumları** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9b608-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Bakım talebi yaşam döngüsü durumları sayfası](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="9b608-122">Bakım talebi yaşam döngüsü durumları, yaşam döngüsü durum grupları ve türlerin ilişkili olduğu ve iş emri yaşam döngüsü durumları, yaşam döngüsü durumu grupları ve türlerle aynı şekilde kullanıldığı gibi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b608-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="9b608-123">Bakım talebi yaşam döngüsü modellerini ayarla</span><span class="sxs-lookup"><span data-stu-id="9b608-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="9b608-124">Bakım talepleriniz için gerekli yaşam döngüsü durumları oluşturulduktan sonra, yaşam döngüsü durum gruplarına veya yaşam döngüsü modellerine ayrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9b608-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="9b608-125">Bakım talebi yaşam döngüsü modelleri, farklı türlerde bakım istekleri için kullanılabilecek akışı oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b608-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="9b608-126">En az bir standart bakım talebi yaşam döngüsü modeli oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9b608-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="9b608-127">**Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="9b608-128">Bakım talebi yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="9b608-129">**Yaşam döngüsü modeli** alanında yaşam döngüsü modeli kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="9b608-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="9b608-130">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="9b608-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="9b608-131">**Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü durumları** alanı ilgili yaşam döngüsü modelinde seçili yaşam döngüsü durumlarının sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b608-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="9b608-132">**Bakım talebi türleri** alanı bu yaşam döngüsü modelini kullanan bakım talebi türlerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b608-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="9b608-133">**Yaşam döngüsü durumları** hızlı sekmesinde yaşam döngüsü modeline eklenmesi gereken yaşam döngüsü durumlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="9b608-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="9b608-134">Yaşam döngüsü modelinde bir yaşam döngüsü durumu kullanmak için durumu **Kalan yaşam döngüsü durumları** bölümünden seçin ve sağ ok düğmesini ![Sağ ok](media/03-setup-for-requests.png) seçerek durumu **Seçili yaşam döngüsü durumları** bölümüne taşıyın.</span><span class="sxs-lookup"><span data-stu-id="9b608-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="9b608-135">Yaşam döngüsü modelinde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir durumları seç** düğmesini ![Tüm kullanılabilir durumları seç](media/04-setup-for-requests.png) seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="9b608-136">Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.</span><span class="sxs-lookup"><span data-stu-id="9b608-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="9b608-137">Yaşam döngüsü modelinden bir yaşam döngüsü durumunu kaldırmak için durumu **Seçili yaşam döngüsü durumları** bölümünden seçin ve sol ok düğmesini ![Sol ok](media/05-setup-for-requests.png) seçerek durumu **Kalan yaşam döngüsü durumları** bölümüne taşıyın.</span><span class="sxs-lookup"><span data-stu-id="9b608-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="9b608-138">**Genel** hızlı sekmesinde, depot onarımını kullanırsanız, **Güncelleştirmeler** bölümündeki alanlar geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="9b608-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="9b608-139">**Alınan varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların depot onarımı için alındıkları sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="9b608-140">**Verilen varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların onarımdan sonra döndükleri sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9b608-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="9b608-141">Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü modelleri** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9b608-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Bakım talebi yaşam döngüsü modelleri sayfası](media/06-setup-for-requests.png)
