---
title: Bakım talebi yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde bakım talebi yaşam döngüsü durumları ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f68e11a1cd14bc35282b957a4262cbecdd627b3b
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790550"
---
# <a name="maintenance-request-states"></a><span data-ttu-id="0deee-103">Bakım talebi durumları</span><span class="sxs-lookup"><span data-stu-id="0deee-103">Maintenance request states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="0deee-104">Bakım talebi yaşam döngüsü durumları bir isteğin gidebileceği aşamaları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0deee-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="0deee-105">Örneğin, **Oluşturulan**, **Etkin**ve **Sona ermiş** örnekler de içerir.</span><span class="sxs-lookup"><span data-stu-id="0deee-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="0deee-106">Bir bakım isteği iş emrine dönüştürüldüğünde, bakım talebinin artık etkin olmadığını göstermek üzere sürdürme isteği yaşam döngüsü durumu **sonlandırıldı** veya **Kapalı** olarak güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="0deee-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="0deee-107">**Tüm bakım talepleri** listesi sayfasında, yaşam döngüsü durumlarından bağımsız olarak tüm bakım taleplerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0deee-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="0deee-108">Bakım talebi yaşam döngüsü durumlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="0deee-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="0deee-109">**Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü durumları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="0deee-110">Bakım talebi yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="0deee-111">**Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="0deee-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="0deee-112">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="0deee-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="0deee-113">**Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü modelleri** alanı bu yaşam döngüsü durumunu kullanan bakım talebi yaşam döngüsü modellerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0deee-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="0deee-114">**Genel** hızlı sekmesinde, bakım talebinin bu yaşam döngüsü durumunda etkin olması gerekiyorsa, **etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0deee-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="0deee-115">Gerçek bitiş tarihi ve saatinin bu yaşam döngüsü durumunda olan bir bakım isteğine otomatik olarak girilmesi gerekiyorsa, **fiili bitiş** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0deee-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="0deee-116">İş emri , bu yaşam döngüsü durumunda olan bir bakım talebinden oluşturulduysa, **İş emrini oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0deee-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="0deee-117">Bir bakım talebi bu yaşam döngüsü durumundayken silinebilecekse, **Sil** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0deee-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="0deee-118">**Güncelleştir** hızlı sekmesinde, depo onarımını kullanırsanız ,**Varlık** bölümündeki **gelen** ve **giden** seçenekleri geçerlidir. Bakım talebinde seçilen varlıkların yaşam döngüsü durumu otomatik olarak **Gelen** ya da **Giden** olarak güncelleştirilecekse ilgili seçeneği **Evet** olarak ayarlayın; söz konusu bakım talebinin bakım talebi yaşam döngüsü durumu **Gelen** ya da **Giden** olarak ayarlandığında.</span><span class="sxs-lookup"><span data-stu-id="0deee-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="0deee-119">Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü durumları** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0deee-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Şekil 1](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="0deee-121">Bakım talebi yaşam döngüsü durumları, yaşam döngüsü durum grupları ve türlerin ilişkili olduğu ve iş emri yaşam döngüsü durumları, yaşam döngüsü durumu grupları ve türlerle aynı şekilde kullanıldığı gibi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0deee-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="0deee-122">Bakım talebi yaşam döngüsü modellerini ayarla</span><span class="sxs-lookup"><span data-stu-id="0deee-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="0deee-123">Bakım talepleriniz için gerekli yaşam döngüsü durumları oluşturulduktan sonra, yaşam döngüsü durum gruplarına veya yaşam döngüsü modellerine ayrılabilir.</span><span class="sxs-lookup"><span data-stu-id="0deee-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="0deee-124">Bakım talebi yaşam döngüsü modelleri, farklı türlerde bakım istekleri için kullanılabilecek akışı oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0deee-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="0deee-125">En az bir standart bakım talebi yaşam döngüsü modeli oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0deee-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="0deee-126">**Kıymet yönetimi** \> **Kurulum** \> **Bakım talepleri** \> **Yaşam döngüsü modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="0deee-127">Bakım talebi yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="0deee-128">**Yaşam döngüsü modeli** alanında yaşam döngüsü modeli kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="0deee-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="0deee-129">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="0deee-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="0deee-130">**Ayrıntılar** hızlı sekmesinde, **Yaşam döngüsü durumları** alanı ilgili yaşam döngüsü modelinde seçili yaşam döngüsü durumlarının sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0deee-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="0deee-131">**Bakım talebi türleri** alanı bu yaşam döngüsü modelini kullanan bakım talebi türlerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0deee-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="0deee-132">**Yaşam döngüsü durumları** hızlı sekmesinde yaşam döngüsü modeline eklenmesi gereken yaşam döngüsü durumlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="0deee-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="0deee-133">Yaşam döngüsü modelinde bir yaşam döngüsü durumu kullanmak için durumu **Kalan yaşam döngüsü durumları** bölümünden seçin ve sağ ok düğmesini ![Sağ ok](media/03-setup-for-requests.png) seçerek durumu **Seçili yaşam döngüsü durumları** bölümüne taşıyın.</span><span class="sxs-lookup"><span data-stu-id="0deee-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="0deee-134">Yaşam döngüsü modelinde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir durumları seç** düğmesini ![Tüm kullanılabilir durumları seç](media/04-setup-for-requests.png) seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="0deee-135">Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.</span><span class="sxs-lookup"><span data-stu-id="0deee-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="0deee-136">Yaşam döngüsü modelinden bir yaşam döngüsü durumunu kaldırmak için durumu **Seçili yaşam döngüsü durumları** bölümünden seçin ve sol ok düğmesini ![Sol ok](media/05-setup-for-requests.png) seçerek durumu **Kalan yaşam döngüsü durumları** bölümüne taşıyın.</span><span class="sxs-lookup"><span data-stu-id="0deee-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="0deee-137">**Genel** hızlı sekmesinde, depot onarımını kullanırsanız, **Güncelleştirmeler** bölümündeki alanlar geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="0deee-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="0deee-138">**Alınan varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların depot onarımı için alındıkları sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="0deee-139">**Verilen varlığın yaşam döngüsü durumu** alanında, bir bakım talebinde seçilen varlıkların onarımdan sonra döndükleri sırada otomatik olarak güncelleştirilmesi gereken varlık yaşam döngüsü durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0deee-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="0deee-140">Aşağıdaki çizimde bir **Bakım talebi yaşam döngüsü modelleri** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0deee-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Şekil 2](media/06-setup-for-requests.png)
