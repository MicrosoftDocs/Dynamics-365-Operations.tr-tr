---
title: Varlık yönetimini sabit kıymetlerle tümleştirme
description: Bu konu, sabit kıymetleri bakım yapılan varlıklarla bağlamak için Varlık Yönetimi ve Sabit kıymetler modüllerinin nasıl tümleştirileceğini açıklamaktadır.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439189"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="60de0-103">Varlık yönetimini sabit kıymetlerle tümleştirme</span><span class="sxs-lookup"><span data-stu-id="60de0-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60de0-104">**Varlık Yönetimi** ve **Sabit kıymetler** modüllerini tümleştirerek sabit kıymetler ile bakım yapılan varlıkları bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60de0-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="60de0-105">Sabit kıymet kullanıcıları daha sonra yeni veya varolan sabit kıymetten bir bakım yapılan varlık oluşturabilir ve Varlık yönetimi kullanıcıları bakım yapılan varlığı varolan bir sabit kıymetle ilişkilendirebilir.</span><span class="sxs-lookup"><span data-stu-id="60de0-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="60de0-106">Bu özellik, Sabit kıymetler kullanıcılarının ilgili bakım varlıklarının iş emirlerinden deftere nakledilen maliyetleri görüntülemesini de kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="60de0-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="60de0-107">Bu konuda, *bakım yapılan varlıklar* **Varlık Yönetimi** modülündeki varlıkları, *sabit kıymetler* ise **Sabit kıymetler** modülündeki varlıkları ifade eder.</span><span class="sxs-lookup"><span data-stu-id="60de0-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="60de0-108">Sabit kıymetlerden oluşturulan yeni bakım yapılan varlıklar için varsayılan konum ayarlama (isteğe bağlı)</span><span class="sxs-lookup"><span data-stu-id="60de0-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="60de0-109">Bu isteğe bağlı yapılandırma, sabit kıymetlerden oluşturulan yeni bakım yapılan varlıklar için varsayılan bir işlem yapılacak yerleşim ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="60de0-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="60de0-110">Tam olarak tamamlamanız koşuluyla bu yapılandırmayı tipik olarak yalnızca bir kez tamamlarsınız.</span><span class="sxs-lookup"><span data-stu-id="60de0-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="60de0-111">Bu yapılandırmayı tamamlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="60de0-112">**Varlık yönetimi \> Kurulum \> Varlık yönetimi parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="60de0-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="60de0-113">**Sabit kıymetler** sekmesinde, **İşlem yapılacak yerleşim** alanında, varsayılan yerleşimi seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="60de0-114">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="60de0-115">Tümleştirilmiş bakım yapılan varlıklar ve sabit kıymetlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="60de0-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="60de0-116">Bu bölümde, tümleşik Varlık yönetimi ve Sabit kıymetler özellikleriyle çalışabileceğiniz çeşitli yöntemleri gösteren bir grup yordam sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="60de0-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="60de0-117">Varolan bir bakım yapılan varlığı sabit kıymetle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="60de0-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="60de0-118">Mevcut bir bakım yapılan varlığı sabit kıymetle ilişkilendirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="60de0-119">**Varlık yönetimi \> Varlıklar \> Tüm varlıklar** (veya **Etkin varlıklar**'ı) seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="60de0-120">Bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-120">Select an asset.</span></span>
1. <span data-ttu-id="60de0-121">**Sabit kıymet** hızlı sekmesinde, **Sabit kıymet numarası** alanında, mevcut bir sabit kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="60de0-122">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="60de0-123">Seçili bakım yapılan varlık ile ilişkilendirilen sabit kıymeti görüntüleme</span><span class="sxs-lookup"><span data-stu-id="60de0-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="60de0-124">Seçili bakım yapılan varlık ile ilişkilendirilen sabit kıymeti görüntülemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="60de0-125">**Varlık yönetimi \> Varlıklar \> Tüm varlıklar** (veya **Etkin varlıklar**'ı) seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="60de0-126">Bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-126">Select an asset.</span></span>
1. <span data-ttu-id="60de0-127">**Sabit kıymet** hızlı sekmesinde, **Sabit kıymet numarası** alanında, bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="60de0-128">Seçili varlıkla ilgili **Sabit kıymetler** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="60de0-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="60de0-129">(Bu sayfa genellikle **Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler** konumunda bulunur.)</span><span class="sxs-lookup"><span data-stu-id="60de0-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="60de0-130">Seçili sabit kıymetle ile ilişkilendirilen bakım yapılan varlığı görüntüleme</span><span class="sxs-lookup"><span data-stu-id="60de0-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="60de0-131">Seçili sabit kıymet ile ilişkilendirilen bakım yapılan varlığı görüntülemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="60de0-132">**Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="60de0-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="60de0-133">Bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-133">Select an asset.</span></span>
1. <span data-ttu-id="60de0-134">Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Görüntüle** grubunda **Bakım yapılan varlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="60de0-135">Seçili sabit kıymet ile ilişkilendirilen varlığın **Bakım yapılan varlık** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="60de0-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="60de0-136">(Bu sayfa genellikle **Varlık yönetimi \> Varlıklar \> Tüm varlıklar** konumunda bulunur.)</span><span class="sxs-lookup"><span data-stu-id="60de0-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="60de0-137">Sabit kıymetle ilişkili bakım maliyetlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="60de0-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="60de0-138">Varlık yönetimi iş emirleri bakım yapılan varlıklar için deftere nakledilebilir ve bu iş emirlerinin her biri genellikle bir maliyete sahiptir.</span><span class="sxs-lookup"><span data-stu-id="60de0-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="60de0-139">Sabit kıymet bakım yapılan varlık ile ilişkilendirildiğinde, ilgili maliyetleri görmek için doğrudan sabit kıymetten gidebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="60de0-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="60de0-140">Sabit kıymet ile ilişkilendirilen bakım maliyetlerini görüntülemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="60de0-141">**Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="60de0-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="60de0-142">Bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-142">Select an asset.</span></span>
1. <span data-ttu-id="60de0-143">Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Görüntüle** grubunda **Bakım maliyeti** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="60de0-144">**Bakım maliyeti** sayfası açılır ve ilgili maliyetleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="60de0-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="60de0-145">Mevcut bir sabit kıymet için yeni bir bakım yapılan varlık oluşturma</span><span class="sxs-lookup"><span data-stu-id="60de0-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="60de0-146">Mevcut bir sabit kıymet için yeni bir bakım yapılan varlık oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="60de0-147">**Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="60de0-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="60de0-148">Bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-148">Select an asset.</span></span>
1. <span data-ttu-id="60de0-149">Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Yeni** grubunda **Bakım yapılan varlık oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="60de0-150">(Bu seçenek kullanılamıyorsa, bakım yapılan varlık zaten seçili sabit kıymetle ilişkilendirilmiş olabilir.)</span><span class="sxs-lookup"><span data-stu-id="60de0-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="60de0-151">Varlık oluşturma işlemini [Varlık oluşturma](../objects/create-an-object.md)'da açıklandığı şekilde tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="60de0-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="60de0-152">Yeni sabit kıymet oluşturma ve bunun için yeni bir bakım yapılan varlık ekleme</span><span class="sxs-lookup"><span data-stu-id="60de0-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="60de0-153">Yeni bir sabit kıymet oluşturmak ve bunun için yeni bir bakım yapılan varlık eklemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="60de0-154">**Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="60de0-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="60de0-155">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="60de0-156">Sabit kıymet oluşturma işlemini [Sabit kıymet oluşturma](../../../finance/fixed-assets/tasks/create-fixed-asset.md)'da açıklandığı şekilde tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="60de0-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="60de0-157">Eylem Bölmesinde **Varlık yönetimi** sekmesinde **Yeni** grubunda **Bakım yapılan varlık oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="60de0-158">Varlık oluşturma işlemini [Varlık oluşturma](../objects/create-an-object.md)'da açıklandığı şekilde tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="60de0-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="60de0-159">İki varlık arasındaki ilişkilendirmeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="60de0-159">Remove the association between two assets</span></span>

<span data-ttu-id="60de0-160">Bazı durumlarda, bakım yapılan varlığın sabit kıymetiyle ilişkisini kaldırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="60de0-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="60de0-161">Örneğin, bir sabit kıymetten [yeni bir bakım yapılan varlık oluşturmak](#new-maintenance-from-fixed) istiyorsanız, önce mevcut ilişkilendirmeyi kaldırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="60de0-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="60de0-162">Bakım yapılan varlık ile sabit kıymet arasındaki mevcut ilişkilendirmeyi kaldırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="60de0-163">**Varlık yönetimi \> Varlıklar \> Tüm varlıklar** (veya **Etkin varlıklar**'ı) seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="60de0-164">Sabit kıymeti bulun ve açın.</span><span class="sxs-lookup"><span data-stu-id="60de0-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="60de0-165">**Sabit kıymet** hızlı sekmesinde, **İşlem yapılacak yerleşim** alanındaki değeri temizleyin.</span><span class="sxs-lookup"><span data-stu-id="60de0-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="60de0-166">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="60de0-166">On the Action Pane, select **Save**.</span></span>
