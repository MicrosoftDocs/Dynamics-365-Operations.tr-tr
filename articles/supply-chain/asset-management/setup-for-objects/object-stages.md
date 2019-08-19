---
title: Kıymet yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde kıymet yaşam döngüsü durumları ve yaşam döngüsü modelleri açıklanmaktadır.
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
ms.openlocfilehash: 2dc72c61ed4dbb04122c6859123307dc79f2b233
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783647"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="53df4-103">Kıymet yaşam döngüsü durumları</span><span class="sxs-lookup"><span data-stu-id="53df4-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="53df4-104">Bu konuda Kıymet Yönetimi'nde kıymet yaşam döngüsü durumları ve yaşam döngüsü modelleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="53df4-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="53df4-105">Kıymet yaşam döngüsü durumları kıymetin etkin mi yoksa devre dışı mı olduğunu tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="53df4-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="53df4-106">Örneğin, **Oluşturuldu**, **Etkin** ve **Sonlandırıldı** gibi kıymet yaşam döngüsü durumları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53df4-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="53df4-107">Talep yaşam döngüsü durumları kıymet yaşam döngüsü durumlarına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="53df4-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="53df4-108">Bu nedenle bir talep yeni talep yaşam döngüsü durumuna değiştirildiğinde, talebe iliştirilmiş kıymet yeni kıymet yaşam döngüsü durumuna değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="53df4-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="53df4-109">Örneğin bir talebin yaşam döngüsü durumu **Gelen** olarak değiştirilirse, iliştirilmiş kıymetin yaşam döngüsü durumu **Kıymet yaşam döngüsü durumu modelleri** sayfasının **Kıymet yaşam döngüsü durumu** hızlı sekmesindeki **Gelen yaşam döngüsü durumu** alanında seçili yaşam döngüsü durumuna değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="53df4-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="53df4-110">Kıymet yaşam döngüsü durumları kıymet yaşam döngüsü modellerinde ayarlanabilir. Buradan çeşitli kıymet türleri için gerekli yaşam döngüsü durumlarını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53df4-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="53df4-111">Önce yaşam döngüsü durumlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="53df4-111">You first set up lifecycle states.</span></span> <span data-ttu-id="53df4-112">Daha sonra bir yaşam döngüsü modeli oluşturun ve bu model için yaşam döngüsü durumlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="53df4-113">**Kıymet yönetimi** \> **Kurulum** \> **Kıymetler** \> **Yaşam döngüsü durumları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="53df4-114">Yeni bir kıymet yaşam döngüsü durumu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="53df4-115">**Yaşam döngüsü durumu** alanında yaşam döngüsü durumu kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="53df4-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="53df4-116">**Ad** alanında, bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="53df4-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="53df4-117">**Yaşam döngüsü modelleri** alanı kıymet yaşam döngüsü durumunu kullanan kıymet yaşam döngüsü modellerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="53df4-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="53df4-118">Bu yaşam döngüsü durumunun etkin yaşam döngüsü durumunda olması gerekiyorsa (yani bu yaşam döngüsü durumunki kıymetler için iş emirleri oluşturulabilecekse) **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="53df4-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="53df4-119">**Oluşturuldu** yaşam döngüsü durumunda bir kıymeti olan açık kıymet takvim satılarının bu yaşam döngüsü durumundayken silinmeleri gerekiyorsa **Açık takvim satırlarını sil** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="53df4-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="53df4-120">Bu ayar, artık kıymetle ilgili olmayan açık bakım zamanlamalarını temizlemek istediğinizde (örneğin kıymet artık etkin olmadığında) yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="53df4-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="53df4-121">Kıymet yaşam döngüsü durumları, kıymet yaşam döngüsü modelleri ve kıymet türleri ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="53df4-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="53df4-122">Bunlar iş emri yaşam döngüsü durumları, iş emri yaşam döngüsü modelleri ve iş emri türleri ile aynı şekilde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="53df4-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="53df4-123">Gerekli kıymet yaşam döngüsü durumlarını oluşturduktan sonra kıymet yaşam döngüsü modellerinde yaşam döngüsü durumlarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53df4-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="53df4-124">**Kıymet yönetimi** \> **Kurulum** \> **kıymetler** \> **yaşam döngüsü modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="53df4-125">Yeni bir kıymet yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="53df4-126">**Yaşam döngüsü modeli** alanında yaşam döngüsü modeli kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="53df4-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="53df4-127">**Ad** alanında, bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="53df4-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="53df4-128">**Yaşam döngüsü durumları** alanı kıymet yaşam döngüsü modelinde seçili kıymet yaşam döngüsü durumlarının sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="53df4-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="53df4-129">**Kıymet türleri** alanı yaşam döngüsü modelini kullanan kıymet türlerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="53df4-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="53df4-130">**Yaşam döngüsü durumları** hızlı sekmesinde kıymet yaşam döngüsü modeline eklenmesi gereken kıymet yaşam döngüsü durumlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="53df4-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="53df4-131">Modelde bir yaşam döngüsü durumu kullanmak için durumu **Kalan yaşam döngüsü durumları** bölümünden seçin ve sağ ok düğmesini ![Sağ ok](media/15-setup-for-objects.png) seçerek durumu **Seçili yaşam döngüsü durumları** bölümüne taşıyın.</span><span class="sxs-lookup"><span data-stu-id="53df4-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="53df4-132">Modelde tüm kullanılabilir yaşam döngüsü durumlarını kullanmak için **Tüm kullanılabilir yaşam döngüsü durumları** düğmesini ![Tüm kullanılabilir yaşam döngüsü durumları](media/20-setup-for-objects.png) seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="53df4-133">Tüm yaşam döngüsü durumları **Seçili yaşam döngüsü durumları** bölümüne aktarılır.</span><span class="sxs-lookup"><span data-stu-id="53df4-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="53df4-134">Modelden bir yaşam döngüsü durumunu kaldırmak için durumu **seçili yaşam döngüsü durumları** bölümünden seçin ve sol ok düğmesini ![Sol ok](media/16-setup-for-objects.png) seçerek durumu **Kalan yaşam döngüsü durumları** bölümüne taşıyın.</span><span class="sxs-lookup"><span data-stu-id="53df4-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="53df4-135">Seçili yaşam döngüsü durumunu takip edebilecek kıymet yaşam döngüsü durumlarını tanımlamak için **Yaşam döngüsü durumu güncelleştirmeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="53df4-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="53df4-136">Onarım için aldığınız kıymetleri işlerken **Kıymet durumu** hızlı sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="53df4-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="53df4-137">**Gelen/giden** bölümünde onarım için aldığınız bir kıymetin iş akışını göstermek için kıymet yaşam döngüsü durumlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53df4-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="53df4-138">Müşterilere veya departmanlara ödünç kıymet sunuyorsanız **Ödünç verilenler** bölümünde ödünç verilen kıymetler için yaşam döngüsü durumlarını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53df4-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
