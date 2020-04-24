---
title: El ile oluşturulmuş iş emirleri
description: Bu konuda Varlık Yönetimi'nde el ile iş emirleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 80593ddaaa5f327513781dbdd4e3163de4212ced
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208121"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="ba0cb-103">El ile oluşturulmuş iş emirleri</span><span class="sxs-lookup"><span data-stu-id="ba0cb-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="ba0cb-104">İş emirlerini el ile iki şekilde oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="ba0cb-105">**Tüm iş emirleri** veya **Etkin iş emirleri** sayfasında</span><span class="sxs-lookup"><span data-stu-id="ba0cb-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="ba0cb-106">**Tüm bakım istekleri** veya **Etkin bakım istekleri** veya **İşlem yapılacak yerleşim bakım isteklerim** sayfasında</span><span class="sxs-lookup"><span data-stu-id="ba0cb-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="ba0cb-107">İş emri oluştur</span><span class="sxs-lookup"><span data-stu-id="ba0cb-107">Create work order</span></span>

1. <span data-ttu-id="ba0cb-108">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ba0cb-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-109">Select **New**.</span></span>

3. <span data-ttu-id="ba0cb-110">**İş emri oluştur** iletişim kutusunda **İş emri türü** alanında bir iş emri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="ba0cb-111">Gerekirse, bir **Açıklama** seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="ba0cb-112">**Varlık** alanında varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="ba0cb-113">Bir varlık seçtiğinizde, **Varlık** açılan menüsünde üç sekme bulunabilir:</span><span class="sxs-lookup"><span data-stu-id="ba0cb-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="ba0cb-114">**Etkin varlıklar** - Bu sekme, varlık yaşam döngüsü durumu "Etkin" olan tüm varlıkların listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="ba0cb-115">**Varlık görünümü** - Bu sekme, işlem yapılacak yerleşimlerin ve bu yerleşimlerde kurulu olan varlıkların ağaç görünümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="ba0cb-116">**Varlıklarım** - Bu sekme, sizin (sistemde oturum açan çalışan) tahsis edilmiş olabileceğiniz işlevsel yerleşimlerle ilgili varlıkları içerir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="ba0cb-117">(Kurulum hakkında bilgi için bkz. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).) [Bakım görevlileri ve çalışan gruplarındaki](../setup-for-objects/workers-and-worker-groups.md) bir çalışanla ilgili işlem yapılacak yerleşim yoksa, **Varlıklarım** sekmesi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="ba0cb-118">**Bakım işi türü** alanında iş emri için bakım işi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="ba0cb-119">Gerekirse, **Bakım işi türü çeşidi** ve **İşlem**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="ba0cb-120">Gerekirse, **Servis düzeyi** alanında iş emri hizmet düzeyini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="ba0cb-121">İlgili alanlarda **Beklenen başlangıç** ve **Beklenen bitiş** tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="ba0cb-122">İş emri oluşturmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="ba0cb-123">**Tüm iş emirleri** liste sayfasında, iş emrini gerektiği gibi düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="ba0cb-124">Aaşağıdaki noktaları unutmayın:</span><span class="sxs-lookup"><span data-stu-id="ba0cb-124">Note the following points:</span></span>

- <span data-ttu-id="ba0cb-125">**Tüm iş emirleri** liste sayfasının ayrıntılar görünümünde **İş emri bakım işleri** hızlı sekmesinde satırlar ekleyerek, iş emrine birden çok varlık ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="ba0cb-126">Bir varlıkta, yalnızca varlık için seçilen varlık türünde tanımlanan bakım işi türlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="ba0cb-127">Bir iş emri üzerinde kullandıktan sonra bir varlık hizmet düzeyini veya varlık kritikliğini değiştirirseniz, iş emrindeki hizmet düzeyi veya kritiklik buna göre güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="ba0cb-128">Hizmet düzeyleri ve kritiklikler hakkında daha fazla bilgi için bkz. [Varlık hizmet düzeyleri](../setup-for-objects/object-priorities.md) ve [Varlık kritiklik türleri](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="ba0cb-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="ba0cb-129">İş emrindeki kritiklik, iş emrine bir iş emri işi eklendiğinde veya silindiğinde yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="ba0cb-130">**Tüm iş emirleri** ayrıntılar görünümünde > **Başlık** sekmesinde > **Zamanlama** hızlı sekmesindeki **Sorumlu grup** veya **Sorumlu** alanında bir sorumlu bakım görevlisi grubu veya sorumlu bakım görevlisi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="ba0cb-131">İş emri etkinken bu ayarlar değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="ba0cb-132">Örneğin, iş emri yaşam döngüsü durumu değiştiğinde değiştirilebilirler.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="ba0cb-133">İş emri oluşturma sırasında yapılan otomatik seçim, **Sorumlu bakım görevlileri** sayfasındaki kurulumu temel alır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="ba0cb-134">Bir iş emri oluşturduktan sonra iş emri işlerini ekler veya kaldırırsanız ve iş emrini güncelleştirdiğinizde **Sorumlu grup** ve **Sorumlu** alanı boşsa, Varlık Yönetimi kurulum formunda sorumlu bir bakım görevlisi grubu veya sorumlu bakım görevlisi için olası bir eşleşme arar.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="ba0cb-135">İş emrini güncelleştirdiğinizde **Sorumlu grup** veya **Sorumlu** alanı zaten ayarlanmış durumda ise, hiçbir değişiklik yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="ba0cb-136">Sorumlu bakım görevlileri ve görevli gruplarıyla ilgili daha fazla bilgi için bkz: [Sorumlu bakım görevlileri](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="ba0cb-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="ba0cb-137">[Bakım durumu](../controlling-and-reporting/maintenance-status.md) sayfasından gelen ve tamamlanan iş emirleriyle ilgili iş yükünün özetini almak için hesaplama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="ba0cb-138">**Tüm iş emirleri** sayfasının ayrıntılar görünümünde **Aatır ayrıntıları** hızlı sekmesinde, iş emri işinde seçilen varlık için coğrafi koordinatlar eklemek amacıyla **Enlem** ve **Boylam** alanlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="ba0cb-139">İlgili iş emri oluştur</span><span class="sxs-lookup"><span data-stu-id="ba0cb-139">Create related work order</span></span>

<span data-ttu-id="ba0cb-140">Var olan bir iş emriyle ilgili bir iş emri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="ba0cb-141">Bu özellik, örneğin birincil ve ikincil iş emirleriyle çalışmak istiyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="ba0cb-142">Yeni bir iş emri, var olan bir iş emrinden alınan bir iş emri işine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="ba0cb-143">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ba0cb-144">İlgili iş emri oluşturulacak iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="ba0cb-145">Eylem Bölmesinde **İş emri** sekmesindeki **Yeni** grubunda **İlgili iş emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="ba0cb-146">**İlgili iş emri oluştur** iletişim kutusunda, **İş emri işi** alanında ilgili iş emri oluşturmak istediğiniz iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="ba0cb-147">**Bakım işi türü** alanında bakım işi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="ba0cb-148">**Bakım işi türü çeşidi** ve **Zanaat** alanlarında gerektiği şekilde ilgili bir bakım işi türü çeşidi ve zanaat seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="ba0cb-149">Bu iş emri, seçili iş emri için oluşturulan ilk ilgili iş emriyse, şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ba0cb-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="ba0cb-150">**Yeni iş emri** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="ba0cb-151">**İş emri türü** alanında bir iş emri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="ba0cb-152">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="ba0cb-153">**Hizmet düzeyi** alanında iş emri hizmet düzeyini gereken şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="ba0cb-154">**Beklenen başlangıç** ve **Beklenen bitiş** alanlarında, beklenen başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="ba0cb-155">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-155">Select **OK**.</span></span> <span data-ttu-id="ba0cb-156">Yeni ilgili iş emri **Tüm iş emirleri** liste sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="ba0cb-157">Bu ilişkili iş emrini oluşturduğunuz iş emrinin zaten ilgili iş emirleri varsa, var olan bir ilgili iş emrine yeni bir iş emri işi eklemek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ba0cb-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="ba0cb-158">**İlgili iş emrine ekle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="ba0cb-159">**İş emri** alanında, yeni bir iş emri işi ekleyeceğiniz ilgili iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="ba0cb-160">**Hizmet düzeyi** alanında iş emri hizmet düzeyini gereken şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="ba0cb-161">**Beklenen başlangıç** ve **Beklenen bitiş** alanlarında, beklenen başlangıç ve bitiş tarihlerini gereken şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="ba0cb-162">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-162">Select **OK**.</span></span> <span data-ttu-id="ba0cb-163">İş emri işi var olan ilgili iş emrine eklenir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="ba0cb-164">Aşağıdaki şekilde **İlgili iş emri oluştur** iletişim kutusu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Şekil 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="ba0cb-166">**Varlık yönetimi parametreleri** > **İş emirleri** sekmesi > **İlgili iş emri maskesi** alanında ilgili iş emri maskesi ayarlarsanız, iş emri kodları maske ayarına uygun şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="ba0cb-167">İlgili bir iş emri maskesi ayarlanmamışsa, ilgili iş emirleri için sonraki kullanılabilir iş emri kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="ba0cb-168">İş emri kopyalama</span><span class="sxs-lookup"><span data-stu-id="ba0cb-168">Copy a work order</span></span>

<span data-ttu-id="ba0cb-169">Var olan bir iş emrinden hızlı şekilde yeni bir iş emri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="ba0cb-170">İş emirleriyle çalışmanın bu yolu, [bakım planlarını](../preventive-and-reactive-maintenance/maintenance-plans.md) temel alan iş emirleri oluşturmaktan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="ba0cb-171">Örneğin, farklı varlıklarda düzenli aralıklarla tamamlanması gereken çeşitli işler içeren birçok iş emri işi bulunan bir iş emri varsa yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="ba0cb-172">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="ba0cb-173">İçeriği kopyalamak istediğiniz iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="ba0cb-174">Eylem Bölmesinde >**İş emri** sekmesinde > **Yeni** grubunda **İş emrini kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="ba0cb-175">Seçilen iş emrinden alınan iş emri kurulumu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="ba0cb-176">Alanların bazılarını istediğiniz şekilde düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="ba0cb-177">Yeni iş emri oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="ba0cb-178">**Tüm iş emirleri** liste sayfasında, iş emrini gerektiği gibi düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="ba0cb-179">Yeni iş emri oluşturulduğunda, bazı bilgiler doğrudan var olan iş emrinden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="ba0cb-180">Tahminler, araçlar, bakım denetim listeleri, işlem yapılacak yerleşim, adresler ve zamanlama hakkındaki bilgiler kopyalanmaz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="ba0cb-181">Bunun yerine, Varlık Yönetiminde geçerli kurulumdan başlatılır.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="ba0cb-182">Bu nedenle, ilk iş emrinin oluşturulduğu zaman ile iş emrinin kopyasını oluşturduğunuz zaman arasında bilgiler değiştirilirse, değişiklikler yeni iş emrine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="ba0cb-183">Örnekler tahminlerdeki değişiklikleri veya bakım denetim listelerindeki güncelleştirmelerdir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="ba0cb-184">Aşağıdaki örnekte **İş emrini kopyala** iletişim kutusunun bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Şekil 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="ba0cb-186">Bakım isteğine dayalı iş emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="ba0cb-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="ba0cb-187">**Varlık yönetimi** > **Ortak** > **Bakım talepleri** > **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="ba0cb-188">İş emri oluşturmak istediğiniz bakım talebini seçin ve **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="ba0cb-189">Eylem Bölmesinde >**Bakım talebi** sekmesinde > **Yeni** grubunda **İş emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="ba0cb-190">**İş emri** iletişim kutusunda, alanları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="ba0cb-191">Bakım talebinde bir bakım işi türü seçilmişse, iş emrini oluştururken gerekirse farklı bir bakım işi türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="ba0cb-192">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-192">Select **OK**.</span></span> <span data-ttu-id="ba0cb-193">Bir ileti, bir satış siparişinin oluşturulduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="ba0cb-194">Bir bakım talebine bağlı iş emirlerini görüntülemek için **Tüm bakım talepleri** veya **Etkin bakım talepleri** liste sayfasında bakım talebini seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="ba0cb-195">Ardında Eylem Bölmesinde **Bakım talebi** sekmesinde **Görüntüle** grubunda **İş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="ba0cb-196">Aşağıdaki çizimde **İş emri oluştur** iletişim kutusunun bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Şekil 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="ba0cb-198">İş emirlerinin otomatik oluşturulmasını isterseniz, bakım planı işlerini planlayabilir veya bir varlıkta [bakım planlarını](../preventive-and-reactive-maintenance/maintenance-plans.md) veya [bakım sıralarını](../preventive-and-reactive-maintenance/maintenance-rounds.md) "otomatik oluştur" özelliğini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="ba0cb-199">**Tüm bakım zamanlamaları** liste sayfasındaki bakım taleplerinden oluşturulan iş emirleri, bakım taleplerinde seçilen bakım işi türlerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

