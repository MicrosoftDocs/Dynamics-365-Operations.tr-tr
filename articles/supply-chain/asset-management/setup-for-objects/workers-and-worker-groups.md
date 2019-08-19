---
title: Bakım görevlileri ve çalışan grupları
description: Bu konuda Kıymet Yönetimi'nde bakım görevlileri ve çalışan grupları açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c85fc24cdf0b3cd1a188ccf0f477ffbfa5fab960
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783646"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="5ecc2-103">Bakım görevlileri ve çalışan grupları</span><span class="sxs-lookup"><span data-stu-id="5ecc2-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5ecc2-104">Bu konuda Kıymet Yönetimi'nde bakım görevlileri ve çalışan grupları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="5ecc2-105">Kıymet Yönetimi'nde bakım çalışanlarını işlem yapılacak yerleşimlerle bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="5ecc2-106">(İşlem yapılacak yerleşimler hakkında daha fazla bilgi için bkz. [İşlem yapılacak yerleşimleri oluşturma](../functional-locations/create-functional-locations.md).) Bu işlev işlem yapılacak yerleşim 01'de bulunan bir makinede bakım işi zamanlarken ve işi gerçekleştirmesi için aynı konumdan bakım görevlilerini tahsis etmek istediğinizde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="5ecc2-107">Ayrıca bakım görevlisi grupları oluşturabilir ve bakım görevlilerini bu gruplarla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="5ecc2-108">Bu işlev basit bir iş emri planlaması yaparken ve bir iş emrinde bakım görevlileri grubunu planlamak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="5ecc2-109">Bakım görevlilerini ve bakım görevlisi gruplarını tercih edilen bakım görevlileri ve sorumlu bakım görevlilerini ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="5ecc2-110">Çalışanlar oluştur</span><span class="sxs-lookup"><span data-stu-id="5ecc2-110">Create workers</span></span>

1. <span data-ttu-id="5ecc2-111">**Kıymet yönetimi** \> **Kurulum** \> **Çalışanlar** \> **Çalışanlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="5ecc2-112">Listeye yeni bir çalışan eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="5ecc2-113">**Çalışan** alanında çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="5ecc2-114">İş emirlerinde çalışanı planlamak için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="5ecc2-115">**Genel** hızlı sekmesinde, çalışan için bir kaynak seçilmişse **Kaynak** ve **Açıklama** alanları otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="5ecc2-116">**Kaynaklar** sayfasında (**Kuruluş yönetimi** \> **Kaynaklar** \> **Kaynaklar**) çalışanı bir kaynak olarak ayarlayıp bu kaynağa bir takvim tahsis ettiğinizde **Takvim** alanı otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="5ecc2-117">**Gruplar** hızlı sekmesinde, **Ekle**'yi ve ardından çalışan için bir bakım görevlisi grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="5ecc2-118">Bir çalışan birden fazla grupla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="5ecc2-119">Standart kurulumda bir çalışanın bir grupla ilişkisi grubu eklediğiniz tarihte başlar ve hiçbir zaman sona ermez.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="5ecc2-120">Bu tarih **Etkinlik tarihi** alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="5ecc2-121">**Etkinlik tarihi** alanını görmek için **Görünüm** \> **Tümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="5ecc2-122">Çalışanın bir grupla ilişkisinin belirli bir dönemle sınırlanması gerekiyorsa bu dönemi tanımlamak için **Etkinlik tarihi** ve **Bitiş tarihi** alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="5ecc2-123">**İşlem yapılacak yerleşimler** hızlı sekmesinde **Ekle**'yi ive ardından bakım görevlisi için bir işlem yapılacak yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="5ecc2-124">Ayrıca çalışan için birincil işlem yapılacak yerleşimi belirtin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ecc2-125">Bir çalışana işlem yapılacak yerleşimler eklediğinizde bu işlem yapılan yerleşimlerle ilgili tüm etkin kıymetler **Etkin kıymetlerim** ve **Etkin işlem yapılacak yerleşimlerim** gibi çeşitli menü öğelerinde görünür.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="5ecc2-126">Ayrıca yeni bir kıymet, bakım talebi veya iş emri oluşturduğunuzda gösterilen kıymet aramalarında da görünür.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="5ecc2-127">**Ayrıntılar** hızlı sekmesindeki alanlar bakım görevlisi gruplarının ve seçili bakım çalışanının ilgili olduğu işlem yapılacak yerleşimlerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="5ecc2-128">Çalışan grupları oluştur</span><span class="sxs-lookup"><span data-stu-id="5ecc2-128">Create worker groups</span></span>

1. <span data-ttu-id="5ecc2-129">**Kıymet yönetimi** \> **Kurulum** \> **Çalışanlar** \> **Bakım görevlisi grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="5ecc2-130">Listeye bir çalışan grubu eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="5ecc2-131">**Bakım çalışanı grubu** alanına bir grup kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="5ecc2-132">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="5ecc2-133">**Çalışanlar** hızlı sekmesinde, **Ekle**'yi ve ardından çalışan grubu için bir bakım görevlisi grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="5ecc2-134">**Etkinlik tarihi** ve **Bitiş tarihi** alanları hakkında bilgi için önceki yordamda adım 6'ya bakın.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="5ecc2-135">Bir kaynak grubunun seçili bakım görevlisi grubuyla ilgili olması gerekiyorsa **Kaynak gruptan kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="5ecc2-136">**Grup** alanında takvim ayarlarının kopyalanacağı kaynak grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="5ecc2-137">Ardından **Çalışan grubu** alanında kaynak grubunun takvim ayarlarının kopyalanacağı çalışan grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="5ecc2-138">Bu adımı yalnızca iş emri planlaması sırasında bakım görevlilerinin bir kaynakla (iş merkezi) ilgili takvimi kullanmalarını istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="5ecc2-139">**Ayrıntılar** hızlı sekmesindeki alan seçili bakım çalışanı grubunda ayarlanmış bakım görevlilerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ecc2-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
