---
title: İş emirleri oluşturma
description: Bu konuda Varlık Yönetimi'nde iş emirleri oluşturma işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836746"
---
# <a name="creating-work-orders"></a><span data-ttu-id="c47e8-103">İş emirleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="c47e8-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c47e8-104">Önleyici bakım işlerini planladıktan sonra, bir sonraki adım bunlar için iş emirleri oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="c47e8-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="c47e8-105">Bu adımı bakım zamanlamalarından birini kullanarak tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47e8-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="c47e8-106">Bakım zamanlamasındaki zamanlanmış işler, aşağıdaki tabloda açıklanan şekilde farklı başvuru türlerine sahip olabilir:</span><span class="sxs-lookup"><span data-stu-id="c47e8-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="c47e8-107">Referans türü</span><span class="sxs-lookup"><span data-stu-id="c47e8-107">Reference type</span></span> | <span data-ttu-id="c47e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c47e8-108">Description</span></span> |
|---|---|
| <span data-ttu-id="c47e8-109">Bakım planları</span><span class="sxs-lookup"><span data-stu-id="c47e8-109">Maintenance plans</span></span> | <span data-ttu-id="c47e8-110">*Süre* veya *Sayaç* bakım planı türüne bağlı olan önleyici bakım işleri.</span><span class="sxs-lookup"><span data-stu-id="c47e8-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="c47e8-111">Bakım sıraları</span><span class="sxs-lookup"><span data-stu-id="c47e8-111">Maintenance rounds</span></span> | <span data-ttu-id="c47e8-112">Benzer bir bakım türü gerektiren birkaç kıymeti içeren önleyici bakım işleri.</span><span class="sxs-lookup"><span data-stu-id="c47e8-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="c47e8-113">Bakım talebi</span><span class="sxs-lookup"><span data-stu-id="c47e8-113">Maintenance request</span></span> | <span data-ttu-id="c47e8-114">Bir kıymetin bakımı veya onarımı için el ile oluşturulmuş bir istek.</span><span class="sxs-lookup"><span data-stu-id="c47e8-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="c47e8-115">Bu istek bir iş emrine dönüştürülebilir.</span><span class="sxs-lookup"><span data-stu-id="c47e8-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="c47e8-116">Bakım zamanlamanıza göre iş emirleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="c47e8-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="c47e8-117">Bakım zamanlamanızı temel alan iş emirleri oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="c47e8-118">İş emirlerinizden zamanlama öğelerini nasıl seçmek istediğinize bağlı olarak, aşağıdaki sayfalardan birini açın:</span><span class="sxs-lookup"><span data-stu-id="c47e8-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="c47e8-119">Tüm bakım zamanlamaları (**Kıymet yönetimi \> Yönetim zamanlaması \> Tüm bakım zamanlamaları**)</span><span class="sxs-lookup"><span data-stu-id="c47e8-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="c47e8-120">Bakım zamanlaması satırlarını aç (**Kıymet yönetimi \> Yönetim zamanlaması \> Bakım zamanlaması satırlarını aç**)</span><span class="sxs-lookup"><span data-stu-id="c47e8-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="c47e8-121">Bakım zamanlaması havuzlarını aç (**Kıymet yönetimi \> Yönetim zamanlaması \> Bakım zamanlaması havuzlarını aç**)</span><span class="sxs-lookup"><span data-stu-id="c47e8-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="c47e8-122">Izgarada, iş emri oluşturmak istediğiniz her zamanlanmış bakım işi için onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="c47e8-123">Ardından, Eylem Bölmesi'nde **İş emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="c47e8-124">**İş emri oluşturun** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c47e8-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="c47e8-125">**Bakım tahmini saatleri** alanında, seçili satırlar için tahmini saatlerin toplam sayısı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c47e8-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![İş emri oluşturun iletişim kutusu](media/18-preventive-maintenance.png)

1. <span data-ttu-id="c47e8-127">**Parametreler** bölümünde, oluşturulması gereken iş emirlerinin sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="c47e8-128">Aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="c47e8-128">Select one of the following options:</span></span>

    - <span data-ttu-id="c47e8-129">**Satır başına bir iş emri**: Her bakım zamanlaması satırı için bir iş emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c47e8-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="c47e8-130">**Şuna göre bir iş emri**: Bu seçeneği belirlediğinizde sunulan diğer seçeneklerin ayarlarına göre gruplandırılmış iş emirleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c47e8-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="c47e8-131">**İş emri türü** alanında, oluşturduğunuz tüm iş emirleri için kullanılacak iş emri türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="c47e8-132">Ayarlarınıza göre iş emirlerini oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="c47e8-133">Bakım planı çalışırken otomatik olarak oluşturulan iş emri satırlarını gruplandırma</span><span class="sxs-lookup"><span data-stu-id="c47e8-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

<span data-ttu-id="c47e8-134">Bu özellik, sistem bir bakım planına göre otomatik olarak iş emirleri oluşturmak üzere ayarlandığında, iş emri satırlarını tek bir iş emri altında gruplandırmak için kurallar tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="c47e8-134">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="c47e8-135">Daha önce otomatik olarak oluşturulan iş emirleri yalnızca tek bir satır içerebiliyordu.</span><span class="sxs-lookup"><span data-stu-id="c47e8-135">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="c47e8-136">Ancak, şu anda iş emirlerini kıymet, kıymet türü veya işlem yapılacak yerleşim gibi ölçütlere göre gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c47e8-136">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="c47e8-137">(Elle oluşturulan iş emirleri bu konunun önceki bölümünde açıklandığı gibi zaten bu şekilde gruplandırılabilir.)</span><span class="sxs-lookup"><span data-stu-id="c47e8-137">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="c47e8-138">Otomatik oluşturulan iş emirleri için gruplandırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c47e8-138">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="c47e8-139">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c47e8-139">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c47e8-140">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c47e8-140">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="c47e8-141">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="c47e8-141">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c47e8-142">**Modül:** *Kıymet Yönetimi*</span><span class="sxs-lookup"><span data-stu-id="c47e8-142">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="c47e8-143">**Özellik adı:** *Bakım planı çalıştırırken iş emirlerini gruplandırmak için kural uygulama*</span><span class="sxs-lookup"><span data-stu-id="c47e8-143">**Feature name:** *Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="c47e8-144">Otomatik oluşturulan iş emirleri için gruplandırmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="c47e8-144">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="c47e8-145">Otomatik oluşturulan iş emirleri için gruplandırmayı ayarlamak üzere şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c47e8-145">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="c47e8-146">**Kıymet yönetimi \> Kurulum \> Önleyici bakım \> Bakım planları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-146">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="c47e8-147">Gruplandırılmış iş emirleri oluşturmak istediğiniz her plan için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="c47e8-147">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="c47e8-148">Liste bölmesinde planı seçin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-148">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="c47e8-149">**Satırlar** hızlı sekmesinde, her satırda **Otomatik oluştur** onay kutusunun seçili olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c47e8-149">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="c47e8-150">**Kıymet yönetimi \> Dönemsel \> Önleyici bakım \> Bakım planlarını zamanla** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-150">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="c47e8-151">**Bakım planlarını zamanlayın** iletişim kutusundaki **Dönem** bölümünde, plan için değerlendirme tarihini (iş oluşturulacak zamanlanmış bakım işlerini bulmak için ne kadar süre sonraya bakılması gerektiğini) belirtin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-151">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="c47e8-152">**Zamanlamayı kullanarak iş emrini otomatik olarak oluştur** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c47e8-152">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="c47e8-153">**İş emri** bölümünde aşağıdaki seçeneklerden birini belirleyin:</span><span class="sxs-lookup"><span data-stu-id="c47e8-153">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="c47e8-154">**Satır başına bir iş emri**: Her bakım zamanlaması satırı için bir iş emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c47e8-154">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="c47e8-155">(Bu seçenek, *Bakım planı çalıştırırken iş emirlerini gruplandırmak için kural uygula* özelliği kapalıyken kullanılabilen işlevle aynı işlevi sağlar.)</span><span class="sxs-lookup"><span data-stu-id="c47e8-155">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="c47e8-156">**Şuna göre bir iş emri**: Bu seçeneği belirlediğinizde sunulan diğer seçeneklerin ayarlarına göre gruplandırılmış iş emirleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c47e8-156">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="c47e8-157">Seçeneklerin yalnızca bakım planlarınızın bazılarını çalıştırırken geçerli olmasını istiyorsanız **Eklenecek kayıtlar** hızlı sekmesinde, Microsoft Dynamics 365 Supply Chain Management'taki diğer toplu işlerde yapacağınız gibi gerekli filtreleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-157">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="c47e8-158">**Arka planda çalıştır** hızlı sekmesinde, Supply Chain Management'taki diğer toplu işler için yapacağınız şekilde, ihtiyaç duyduğunuz toplu iş ve zamanlama seçeneklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c47e8-158">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="c47e8-159">Seçili bakım planlarını çalıştırmak ve/veya zamanlamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c47e8-159">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]