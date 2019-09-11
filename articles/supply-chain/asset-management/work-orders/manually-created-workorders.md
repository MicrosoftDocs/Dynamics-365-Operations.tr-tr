---
title: El ile oluşturulmuş iş emirleri
description: Bu konuda Varlık Yönetimi'nde el ile iş emirleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875944"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="d870e-103">El ile oluşturulmuş iş emirleri</span><span class="sxs-lookup"><span data-stu-id="d870e-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="d870e-104">İş emirlerini el ile iki şekilde oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="d870e-105">**Tüm iş emirlerinde** veya **Etkin iş emirlerinde**</span><span class="sxs-lookup"><span data-stu-id="d870e-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="d870e-106">**Tüm bakım istekleri** veya **Etkin bakım istekleri** veya **İşlem yapılacak yerleşim bakım isteklerim**'de</span><span class="sxs-lookup"><span data-stu-id="d870e-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="d870e-107">İş emri oluştur</span><span class="sxs-lookup"><span data-stu-id="d870e-107">Create work order</span></span>

1. <span data-ttu-id="d870e-108">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d870e-109">**Yeni** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-109">Click the **New** button.</span></span>

3. <span data-ttu-id="d870e-110">**İş emri oluştur** açılır listesinde, bir iş emri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="d870e-111">Gerekirse, bir açıklama seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-111">If required, select a description.</span></span>

5. <span data-ttu-id="d870e-112">İş emri için varlığı ve bir bakım işi türü seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="d870e-113">Bir varlık seçtiğinizde, kullanılabilir üç sekme bulunur: **Varlıklarım** sekmesi, tahsis edilebileceğiniz (sistemde oturum açan bakım çalışanı) işlem yapılacak yerleşimlerle ilgili varlıkları içerir (şurada ayarlanır: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="d870e-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="d870e-114">[Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md) formundaki bir bakım görevlisi için işlem yapılacak yerleşimler ayarlanmadıysa, **Varlıklarım** sekmesi görünür olmaz.</span><span class="sxs-lookup"><span data-stu-id="d870e-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="d870e-115">**Etkin varlıklar** sekmesi, varlık yaşam döngüsü durumu "Etkin" olan tüm varlıkların listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="d870e-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="d870e-116">**Varlık görünümü** sekmesi, işlem yapılacak yerleşimlerin ve bu yerleşimlerde kurulu olan varlıkların ağaç görünümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="d870e-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="d870e-117">Gerekirse, **Bakım işi türü çeşidi** ve **İşlem**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="d870e-118">Gerekirse, **Servis düzeyi** alanında iş emri hizmet düzeyini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="d870e-119">İlgili alanlarda beklenen başlangıç ve bitiş tarihlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="d870e-120">Yeni iş emri oluşturmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="d870e-121">Gerekirse, iş emrini **Tüm iş emirleri**'nde düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="d870e-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="d870e-122">**Tüm iş emirleri**'nde, **İş emri bakım işleri** hızlı sekmesinde satırlar ekleyerek, Ayrıntılar görünümünde iş emrine birden fazla varlık ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="d870e-123">Bir varlıkta, yalnızca varlık için seçilen varlık türünde tanımlanan bakım işi türlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="d870e-124">Bir iş emrinde kullandıktan sonra bir varlık servis düzeyi veya varlık kritikliğini değiştirdiyseniz (bkz. [Varlık servis düzeyleri](../setup-for-objects/object-priorities.md) ve [Varlık kritiklikleri](../setup-for-objects/object-criticalities.md)), iş emrindeki servis düzeyi veya kritiklik uygun şekilde güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="d870e-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="d870e-125">İş emrindeki kritiklik, iş emrine bir iş emri satırı eklendiğinde veya silindiğinde yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d870e-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="d870e-126">**Tüm iş emirleri** Ayrıntılar görünümü > **Başlık** görünümü > **Zamanlama** hızlı sekmesinde, **Sorumlu grup** veya **Sorumlu** alanlarında bir sorumlu bakım görevlisi grubu veya sorumlu bakım görevlisi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="d870e-127">Bu ayarlar, örneğin iş emri yaşam döngüsü durumu değiştiğinde, iş emri etkin olduğu sürece değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="d870e-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="d870e-128">İş emri oluşturma sırasında otomatik seçim, **Sorumlu bakım görevlileri** kurulumuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="d870e-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="d870e-129">Bir iş emri oluşturduktan sonra iş emri işlerini ekler veya kaldırırsanız ve iş emrini güncelleştirdiğinizde **Sorumlu grup** ve **Sorumlu** alanı boşsa, Varlık Yönetimi kurulum formunda sorumlu bir çalışan grubu veya sorumlu bakım görevlisi için olası bir eşleşme arar.</span><span class="sxs-lookup"><span data-stu-id="d870e-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="d870e-130">İş emrini güncelleştirdiğinizde **Sorumlu grup** veya **Sorumlu** alanı zaten doldurulmuş durumda ise, hiçbir değişiklik yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="d870e-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="d870e-131">**Bakım durumu**'nda gelen ve tamamlanan iş emirleriyle ilgili iş yükünün özetini almak için hesaplama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="d870e-132">**Satır ayrıntıları** hızlı sekmesinde, iş emri işinde seçilen varlığa coğrafi koordinatlar eklemek için **Enlem** ve **Boylam** alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="d870e-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="d870e-133">İlgili iş emri oluştur</span><span class="sxs-lookup"><span data-stu-id="d870e-133">Create related work order</span></span>

<span data-ttu-id="d870e-134">Örneğin, birincil ve ikincil iş emirleriyle çalışmak istiyorsanız, varolan bir iş emri için ilgili iş emrini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="d870e-135">Yeni bir iş emri, varolan bir iş emrinden alınan bir iş emri işine dayalıdır.</span><span class="sxs-lookup"><span data-stu-id="d870e-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="d870e-136">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d870e-137">İlişkili bir iş emri oluşturmak istediğiniz iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="d870e-138">**İlgili iş emri** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="d870e-139">**İlgili iş emri oluştur** açılır iletişim kutusunda, **İş emri işi** alanında ilgili iş emrini oluşturmak istediğiniz iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="d870e-140">**Bakım işi türü** alanında bir bakım işi türü seçin ve gerekirse **Bakım işi türü çeşidi** ve **İşlem** alanlarında ilgili bir bakım işi türü çeşidi ve işlem seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="d870e-141">Bu yaptığınız ilk ilgili iş emriyse, **Yeni iş emri** radyo düğmesine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d870e-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="d870e-142">İlgili alanlarda **İş emri türü** ve **Açıklama** seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="d870e-143">Gerekirse, **Servis düzeyi** alanında iş emri hizmet düzeyini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d870e-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="d870e-144">İlgili alanlarda beklenen başlangıç ve bitiş tarihlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d870e-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="d870e-145">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-145">Click **OK**.</span></span> <span data-ttu-id="d870e-146">Yeni ilgili iş emri **Tüm iş emirleri** listesinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d870e-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="d870e-147">Zaten ilişkili iş emirleri olan bir iş emrinde ilgili bir iş emri oluşturursanız, iş emri işini zaten ilgili bir iş emrine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="d870e-148">Bu işlem, adım 6'da **İlgili çalışma emrine ekle** düğmesine tıklayarak gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d870e-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="d870e-149">Daha sonra, yeni bir iş emri işi eklemek istediğiniz ilgili iş emrini seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="d870e-150">**Hizmet düzeyi**, **Beklenen başlangıç** ve **Beklenen** bitiş alanlarını gerektiği gibi düzenleyin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="d870e-151">İş emri işi varolan ilgili iş emrine eklenir.</span><span class="sxs-lookup"><span data-stu-id="d870e-151">The work order job is added to the existing related work order.</span></span>


![Şekil 1](media/03-work-orders.png)

<span data-ttu-id="d870e-153">**Not:** **Varlık yönetimi parametreleri** > **İş emirleri** bağlantısı > **İlgili iş emri maskesi** alanında ilgili iş emri maskesi ayarlarsanız, iş emri kodları maske ayarına uygun şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d870e-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="d870e-154">İlgili bir iş emri maskesi ayarlanmamışsa, ilgili iş emirleri için sonraki kullanılabilir iş emri kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d870e-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="d870e-155">İş emrini kopyala</span><span class="sxs-lookup"><span data-stu-id="d870e-155">Copy work order</span></span>

<span data-ttu-id="d870e-156">Varolan bir iş emrinden hızlı şekilde yeni bir iş emri oluşturmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="d870e-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="d870e-157">İş emirleriyle çalışmanın bu yolu, bakım planlarını temel alan iş emirleri oluşturmaktan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="d870e-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="d870e-158">Örneğin, farklı varlıklarda düzenli aralıklarla tamamlanması gereken çeşitli işler içeren birçok iş emri işi bulunan bir iş emriniz varsa yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="d870e-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="d870e-159">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d870e-160">İçeriğini kopyalamak istediğiniz iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="d870e-161">**İş emrini kopyala** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-161">Click **Copy work order**.</span></span> <span data-ttu-id="d870e-162">Seçilen iş emrinden alınan iş emri kurulumu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d870e-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="d870e-163">Gerekirse, alanların bazılarını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="d870e-164">Yeni iş emri oluşturmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="d870e-165">Gerekirse, iş emrini **Tüm iş emirleri**'nde düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="d870e-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="d870e-166">Yeni iş emri oluşturulduğunda, bazı bilgiler doğrudan varolan iş emrinden kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="d870e-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="d870e-167">Tahminler, araçlar, bakım denetim listeleri, işlem yapılacak yerleşim, adresler ve zamanlama ile ilgili bilgiler kopyalanmaz, ancak Varlık yönetiminde geçerli kurulumdan başlatılır.</span><span class="sxs-lookup"><span data-stu-id="d870e-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="d870e-168">Bu, ilk iş emri oluşturma zamanından iş emrinin bir kopyasını aldığınız zamana kadar bu verilerde değişiklikler yapılmışsa, bu değişikliklerin oluşturduğunuz yeni iş siparişine dahil edildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d870e-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="d870e-169">Örnekler tahminlerdeki değişiklikler veya güncelleştirilmiş bakım denetim listeleridir.</span><span class="sxs-lookup"><span data-stu-id="d870e-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Şekil 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="d870e-171">Bakım talebine dayalı iş emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d870e-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="d870e-172">**Varlık yönetimi** > **Ortak** > **Bakım talepleri** > **Tüm bakım talepleri** ya da **Etkin bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d870e-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="d870e-173">İş emri oluşturmak istediğiniz bakım talebini seçin ve **Düzenle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="d870e-174">**Tüm talepler**'de **İş emri** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="d870e-175">**İş emri** açılır menüsünü doldurun.</span><span class="sxs-lookup"><span data-stu-id="d870e-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="d870e-176">Bakım talebinde bir bakım işi türü seçilmişse, iş emrini oluştururken gerekirse başka bir bakım işi türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d870e-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="d870e-177">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-177">Click **OK**.</span></span> <span data-ttu-id="d870e-178">İş emrinin oluşturulduğunu bildiren bir ileti görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d870e-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="d870e-179">Bir bakım talebine hangi iş emirlerinin bağlı olduğunu görmek istiyorsanız, **Tüm bakım talepleri** veya **Etkin bakım talepleri** listelerinde bakım talebini seçin ve **İş emirleri** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d870e-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Şekil 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="d870e-181">İş emirleri, bakım planı işlerini planlayarak veya bir varlıkta bakım planlarını veya bakım sıralarını "otomatik oluştur" özelliği ayarlanarak otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="d870e-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="d870e-182">**Bakım zamanlamasında** bakım taleplerinden oluşturulan iş emirleri, bakım taleplerinde seçilen bakım işi türleriyle oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d870e-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

