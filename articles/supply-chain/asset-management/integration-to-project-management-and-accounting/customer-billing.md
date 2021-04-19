---
title: Müşteriye ait kıymetler için bakım faturası
description: Bu konuda, müşterilerinize ait kıymetler üzerinde yapılan bakım işini oluşturma, işleme ve faturlandırma açıklanmaktadır.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5532f1ce14239002022f487f227286efe10abf12
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813809"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="52072-103">Müşteriye ait kıymetler için bakım faturası</span><span class="sxs-lookup"><span data-stu-id="52072-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52072-104">*İş emri faturalama* özelliği, müşterilerine kıymetler üzerinde yapılan bakım işini oluşturmanıza, işlemenize ve faturalamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="52072-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="52072-105">Bu özellik, aşağıdaki görevleri yerine getirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="52072-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="52072-106">Müşterileri sahip oldukları kıymetlere bağlama.</span><span class="sxs-lookup"><span data-stu-id="52072-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="52072-107">İş emri oluştururken müşteri seçme ve müşteriye ait kıymetleri görüntüleme.</span><span class="sxs-lookup"><span data-stu-id="52072-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="52072-108">Her müşteri için bir ana proje ayarlama.</span><span class="sxs-lookup"><span data-stu-id="52072-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="52072-109">İş emri için saat, malzeme, gider ve ücret kaydetme ve ardından müşteri için fatura teklifi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="52072-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="52072-110">Ayrıca bu özellik, aşağıdaki işlevleri de sunar:</span><span class="sxs-lookup"><span data-stu-id="52072-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="52072-111">Proje sözleşmesi, müşterinin ana projesinden otomatik olarak ilgili iş emri projesine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="52072-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="52072-112">Artık kıymet yönetimi, hem iş emri tahminlerinde hem de iş emri günlüklerinde *ücret* proje hareketi türünü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="52072-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="52072-113">Müşteri faturalandırma özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="52072-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="52072-114">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52072-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="52072-115">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="52072-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="52072-116">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="52072-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="52072-117">**Modül:** *Proje yönetimi ve muhasebe*</span><span class="sxs-lookup"><span data-stu-id="52072-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="52072-118">**Özellik adı**: *İş emri faturalama*</span><span class="sxs-lookup"><span data-stu-id="52072-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="52072-119">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="52072-119">Example scenario</span></span>

<span data-ttu-id="52072-120">Bu özelliğin nasıl çalıştığını öğrenmek için aşağıdaki örnek senaryo ile çalışın.</span><span class="sxs-lookup"><span data-stu-id="52072-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="52072-121">Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52072-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="52072-122">Başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52072-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="52072-123">Bu senaryodan, üretim sisteminde çalışırken özelliği kullanmaya yönelik kılavuz olarak da yararlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52072-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="52072-124">Ancak, bu durumda kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.</span><span class="sxs-lookup"><span data-stu-id="52072-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="52072-125">1. Adım: Müşteri için yeni proje sözleşmesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="52072-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="52072-126">**Proje yönetimi ve muhasebe \> Projeler \> Proje sözleşmeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="52072-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="52072-127">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="52072-128">**Yeni proje sözleşmesi** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="52072-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="52072-129">**Ad:** *Pelikan Toptan Satış*</span><span class="sxs-lookup"><span data-stu-id="52072-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="52072-130">**Finansman türü**: *Müşteri*</span><span class="sxs-lookup"><span data-stu-id="52072-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="52072-131">**Finansman kaynağı:** *ABD-013* (*Pelikan Toptan Satış*)</span><span class="sxs-lookup"><span data-stu-id="52072-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="52072-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="52072-133">2. Adım: Müşteri için yeni bir ana proje oluşturma</span><span class="sxs-lookup"><span data-stu-id="52072-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="52072-134">Burada oluşturduğunuz ana proje, müşterinin iş emirleri oluşturulurken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52072-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="52072-135">**Proje yönetimi ve muhasebe \> Projeler \> Tüm projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="52072-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="52072-136">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="52072-137">**Yeni proje** iletişim kutusunda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52072-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="52072-138">**Proje türü:** *Zaman ve malzeme*</span><span class="sxs-lookup"><span data-stu-id="52072-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="52072-139">**Proje adı:** *Pelikan Toptan Satış iş emirleri*</span><span class="sxs-lookup"><span data-stu-id="52072-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="52072-140">**Proje grubu:** *TM*</span><span class="sxs-lookup"><span data-stu-id="52072-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="52072-141">**Proje sözleşmesi kodu:** *Pelikan Toptan Satış* (daha önce oluşturduğunuz sözleşme)</span><span class="sxs-lookup"><span data-stu-id="52072-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="52072-142">**Başlangıç tarihi:** Bugünün tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="52072-143">**Proje oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-143">Select **Create project**.</span></span>
1. <span data-ttu-id="52072-144">Yeni proje açılır.</span><span class="sxs-lookup"><span data-stu-id="52072-144">The new project is opened.</span></span> <span data-ttu-id="52072-145">**Proje kodu** değerini not edin.</span><span class="sxs-lookup"><span data-stu-id="52072-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="52072-146">Bu değeri daha sonra girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52072-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="52072-147">3. Adım: Kıymet yönetimi'nde yeni iş emri türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="52072-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="52072-148">**Kıymet yönetimi \> Kurulum \> İş emri \> İş emri türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="52072-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="52072-149">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="52072-150">Listeye yeni bir kayıt eklenir.</span><span class="sxs-lookup"><span data-stu-id="52072-150">A new record is added to the list.</span></span> <span data-ttu-id="52072-151">Bu kayıt için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="52072-151">Set the following values for it:</span></span>

    - <span data-ttu-id="52072-152">**İş emri türü:** *Servis*</span><span class="sxs-lookup"><span data-stu-id="52072-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="52072-153">**Ad:** *Servis iş emirleri*</span><span class="sxs-lookup"><span data-stu-id="52072-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="52072-154">**İş emri yaşam döngüsü durumu:** *Standart*</span><span class="sxs-lookup"><span data-stu-id="52072-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="52072-155">4. Adım: Müşteri hesabını ana projeye bağlama</span><span class="sxs-lookup"><span data-stu-id="52072-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="52072-156">Şimdi Kıymet yönetimi'ndeki proje kurulumunda müşteri hesabını ana projeye bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52072-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="52072-157">**Kıymet yönetimi \> Kurulum \> İş emirleri \> Proje kurulumu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="52072-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="52072-158">**Ana proje** sekmesinde, satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="52072-159">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="52072-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="52072-160">**Müşteri hesabı:** *ABD-013* (*Pelikan Toptan Satış*)</span><span class="sxs-lookup"><span data-stu-id="52072-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="52072-161">**Proje kodu:** Daha önce not ettiğiniz proje kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="52072-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="52072-162">5. Adım: Proje grubunu ve türünü iş emri projesine bağlama</span><span class="sxs-lookup"><span data-stu-id="52072-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="52072-163">Hala **Proje kurulumu** sayfasında (**Kıymet yönetimi \> Kurulum \> İş emirleri \> Proje kurulumu**) olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52072-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="52072-164">**Proje grubu** sekmesinde, satır eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="52072-165">Yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="52072-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="52072-166">**İş emri türü:** *Servis* (daha önce oluşturduğunuz iş emri türü)</span><span class="sxs-lookup"><span data-stu-id="52072-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="52072-167">**Proje grubu:** *TM*</span><span class="sxs-lookup"><span data-stu-id="52072-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="52072-168">İş emri projesindeki proje sözleşmesi her zaman ana projeden devralınır.</span><span class="sxs-lookup"><span data-stu-id="52072-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="52072-169">6. Adım: Bir kıymeti müşteri koduna bağlama</span><span class="sxs-lookup"><span data-stu-id="52072-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="52072-170">**Kıymet yönetimi \> Kıymetler \> Etkin kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="52072-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="52072-171">**Filtre** alanına *VE-102* ifadesini girin ve **Kıymet**'e göre filtrelemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="52072-172">Ayarlarını açmak için kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="52072-173">**Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını *ABD-013* (*Pelikan Toptan Satış*) olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52072-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="52072-174">**Ad** alanı, otomatik olarak *Pelikan Toptan Satış* olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="52072-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="52072-175">7. Adım: Kıymette yeni iş emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="52072-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="52072-176">**Kıymet yönetimi \> İş emirleri \> Etkin iş emirleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="52072-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="52072-177">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="52072-178">**İş emri oluşturun** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="52072-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="52072-179">**İş emri türü:** *Servis*</span><span class="sxs-lookup"><span data-stu-id="52072-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="52072-180">**Açıklama:** *Kamyon Onarımı*</span><span class="sxs-lookup"><span data-stu-id="52072-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="52072-181">**Müşteri hesabı:** *ABD-013* (*Pelikan Toptan Satış*)</span><span class="sxs-lookup"><span data-stu-id="52072-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="52072-182">**Kıymet:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="52072-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="52072-183">Aramada yalnızca seçili müşteri hesabına bağlı olan kıymetler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="52072-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="52072-184">**Bakım işi türü:** *Onarım*</span><span class="sxs-lookup"><span data-stu-id="52072-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="52072-185">**Meslek:** *Tamirci*</span><span class="sxs-lookup"><span data-stu-id="52072-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="52072-186">**Servis düzeyi:** *4*</span><span class="sxs-lookup"><span data-stu-id="52072-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="52072-187">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="52072-188">8. Adım: İş emrini inceleme ve üzerinde çalışmaya başlama</span><span class="sxs-lookup"><span data-stu-id="52072-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="52072-189">Bu bölümde, önceki bölümde oluşturduğunuz iş emri üzerinde çalışacaksınız.</span><span class="sxs-lookup"><span data-stu-id="52072-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="52072-190">Ana projenin *Pelikan toptan satış İş emri* projesi olduğunu doğrulamak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="52072-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="52072-191">**İş emri bakım işleri** bölümünde satır seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="52072-192">**Satır ayrıntıları** hızlı sekmesinde **Proje kodu** değerini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="52072-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="52072-193">Bu değer, *\<Parent-Project-ID\>-\<Project-ID\>* biçiminde tireyle ayrılmış bir sayı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52072-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="52072-194">Bu değer bir bağlantıdır.</span><span class="sxs-lookup"><span data-stu-id="52072-194">This value is a link.</span></span>
    1. <span data-ttu-id="52072-195">Ana proje ve proje adlarını görüntüleyebileceğiniz bir sayfa açmak için proje kodu bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="52072-196">Eylem Bölmesinde **İş emri** sekmesindeki **Yaşam döngüsü durumu** grubunda **İş emri durumunu güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="52072-197">**İş emri durumunu güncelleştirin** iletişim kutusundaki **Seç** sütununda, **Yaşam döngüsü durumu** alanının *Devam ediyor* olarak ayarlandığı satır için onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="52072-198">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-198">Select **OK**.</span></span>
1. <span data-ttu-id="52072-199">**Yaşam döngüsü durumu: InProgress** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="52072-200">9. Adım: İş emrinde harcanan saatleri deftere nakletme ve yeni fatura teklifi oluşturma</span><span class="sxs-lookup"><span data-stu-id="52072-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="52072-201">Bu bölümde, önceki bölümde üzerinde çalıştığınız iş emri üzerinde çalışmaya devam edeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="52072-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="52072-202">Eylem Bölmesi'nde, **İş emri** sekmesinde, **Proje** grubunda, **Günlükler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="52072-203">**İş emri günlükleri** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="52072-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="52072-204">Burada, iş emri üzerinde harcadığınız süreyi kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52072-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="52072-205">**Saatler** hızlı sekmesinde **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="52072-206">Yeni satırda **Saatler** alanını *4* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52072-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="52072-207">Eylem Bölmesinde **Günlükleri deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="52072-208">İş emrine dönmek için **İş emri günlükleri** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="52072-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="52072-209">Eylem Bölmesi'ndeki **Faturalama** sekmesinde, **Yeni fatura teklifi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="52072-210">**Fatura teklifi oluştur** iletişim kutusundaki **Proje hareketleri** bölümünde, faturalandırmak istediğiniz her satır için **Seç** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="52072-211">İletişim kutusunu kapatmak ve yeni fatura teklifini görüntülemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52072-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]