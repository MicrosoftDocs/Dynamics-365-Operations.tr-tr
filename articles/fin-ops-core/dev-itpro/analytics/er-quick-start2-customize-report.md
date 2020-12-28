---
title: Özel elektronik belge oluşturmak için ER biçimini ayarlama
description: Bu konu, Microsoft tarafından sağlanan elektronik raporlama (ER) biçiminin özel elektronik belge oluşturması için nasıl ayarlanacağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680182"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="422d4-103">Özel elektronik belge oluşturmak için ER biçimini ayarlama</span><span class="sxs-lookup"><span data-stu-id="422d4-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="422d4-104">Bu konudaki yordamlarda, Sistem Yöneticisi veya elektronik raporlama işlevi aracılığıyla çalışan bir kullanıcının bu görevleri nasıl gerçekleştirebileceği açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="422d4-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="422d4-105">[Elektronik raporlama (ER) altyapısını](general-electronic-reporting.md) parametrelerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="422d4-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="422d4-106">Microsoft tarafından sağlanan ve bir [satıcı ödemesi](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) işlenirken bir ödeme dosyası oluşturmak için kullanılan ER konfigürasyonlarını içe aktar.</span><span class="sxs-lookup"><span data-stu-id="422d4-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="422d4-107">Microsoft tarafından sağlanan standart bir ER biçimi yapılandırmasının özel sürümünü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="422d4-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="422d4-108">Özel ER formatı konfigürasyonunu, belirli bir bankanın gereksinimlerine uyan ödeme dosyaları oluşturacak şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="422d4-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="422d4-109">Özel ER biçimi konfigürasyonundaki standart ER biçimi konfigürasyonuna yapılan değişiklikleri benimseme.</span><span class="sxs-lookup"><span data-stu-id="422d4-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="422d4-110">Aşağıdaki yordamların tümü **GBSI** şirketinde yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="422d4-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="422d4-111">Kodlama gerekmez.</span><span class="sxs-lookup"><span data-stu-id="422d4-111">No coding is required.</span></span>

- [<span data-ttu-id="422d4-112">ER altyapısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="422d4-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="422d4-113">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="422d4-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="422d4-114">ER yapılandırma sağlayıcısı etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="422d4-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="422d4-115">ER yapılandırma sağlayıcıları listesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="422d4-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="422d4-116">Yeni bir ER yapılandırması sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="422d4-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="422d4-117">ER yapılandırma sağlayıcısı etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="422d4-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="422d4-118">Standart ER biçimi yapılandırmalarını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="422d4-119">Standart ER yapılandırmalarını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="422d4-120">İçe aktarılan ER yapılandırmalarını gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="422d4-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="422d4-121">İşleme için satıcı ödemesini hazırlayın</span><span class="sxs-lookup"><span data-stu-id="422d4-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="422d4-122">Satıcı hesabı için banka bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="422d4-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="422d4-123">Satıcı ödemesini girin</span><span class="sxs-lookup"><span data-stu-id="422d4-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="422d4-124">Standart ER biçimini kullanarak bir satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="422d4-125">Elektronik ödeme yöntemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="422d4-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="422d4-126">Satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="422d4-127">Standart ER biçimini Özelleştirme</span><span class="sxs-lookup"><span data-stu-id="422d4-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="422d4-128">Özel biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="422d4-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="422d4-129">Özel biçim düzenleme</span><span class="sxs-lookup"><span data-stu-id="422d4-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="422d4-130">Özel biçimi çalıştırılabilir olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="422d4-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="422d4-131">Özel ER biçimini kullanarak bir satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="422d4-132">Elektronik ödeme yöntemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="422d4-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="422d4-133">Satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="422d4-134">Standart ER biçimi yapılandırmalarının yeni sürümlerini içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="422d4-135">Standart ER yapılandırmalarının yeni sürümlerini içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="422d4-136">İçe aktarılan ER biçimi yapılandırmalarını gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="422d4-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="422d4-137">Özel bir biçimde, içe aktarılan bir biçimin yeni sürümündeki Değişiklikleri benimseme</span><span class="sxs-lookup"><span data-stu-id="422d4-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="422d4-138">Özel biçimin geçerli taslak sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="422d4-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="422d4-139">Özel biçimi yeni bir temel sürüme yeniden temellendir</span><span class="sxs-lookup"><span data-stu-id="422d4-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="422d4-140">Yeniden temellendirilen ER biçimini kullanarak bir satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="422d4-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="422d4-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="422d4-142">ER altyapısını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="422d4-142">Configure the ER framework</span></span>

<span data-ttu-id="422d4-143">Elektronik raporlama işlevi ile ilgili bir kullanıcı olarak, standart bir ER biçiminin özel bir sürümünü tasarlamak için ER çerçevesini kullanmaya başlamadan önce en düşük ER alt uygulama parametreleri kümesini konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="422d4-144">ER parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="422d4-144">Configure ER parameters</span></span>

1. <span data-ttu-id="422d4-145">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-146">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Elektronik raporlama parametreleri** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="422d4-147">**Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="422d4-148">**Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="422d4-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="422d4-149">**Konfigürasyonlar** alanında, **USMF** şirketi için **dosya** türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="422d4-150">**İş arşivi**, **Geçici**, **temel** ve **diğer** alanlarında **Dosya** tipini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="422d4-151">ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="422d4-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="422d4-152">ER yapılandırma sağlayıcısı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="422d4-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="422d4-153">Eklenen her ER yapılandırması bir ER konfigürasyon sağlayıcısı tarafından sahiplenilimli olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="422d4-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="422d4-154">**Elektronik raporlama** çalışma alanında etkinleştirilen ER yapılandırma sağlayıcısı Bu amaçla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="422d4-155">Bu nedenle, ER konfigürasyonlarını eklemeye veya düzenlemeye başlamadan önce, **elektronik raporlama** çalışma alanında bir er yapılandırma sağlayıcısını etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="422d4-156">Yalnızca ER yapılandırmasının sahibi bunu düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="422d4-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="422d4-157">Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="422d4-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="422d4-158">ER yapılandırma sağlayıcıları listesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="422d4-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="422d4-159">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-160">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="422d4-161">**Yapılandırma sağlayıcısı tablosu** sayfasında, her sağlayıcı kaydının benzersiz bir adı ve URL'si vardır.</span><span class="sxs-lookup"><span data-stu-id="422d4-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="422d4-162">Bu sayfanın içeriğini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="422d4-162">Review the contents of this page.</span></span> <span data-ttu-id="422d4-163">**Litware, Inc.** (`https://www.litware.com`) için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleyin](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="422d4-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="422d4-164">Yeni bir ER yapılandırması sağlayıcısı ekleme</span><span class="sxs-lookup"><span data-stu-id="422d4-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="422d4-165">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-166">**Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="422d4-167">**Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="422d4-168">**Ad** alanına **Litware, Inc.** yazın.</span><span class="sxs-lookup"><span data-stu-id="422d4-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="422d4-169">**İnternet adresi** alanına `https://www.litware.com` girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="422d4-170">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="422d4-171">ER yapılandırma sağlayıcısı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="422d4-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="422d4-172">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-173">**Yerelleştirme konfigürasyonları** sayfasında, **Konfigürasyon sağlayıcıları** bölümünde, **Litware, Inc.** döşemesini seçin ve sonra **etkin ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="422d4-174">ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="422d4-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="422d4-175">Standart ER biçimi yapılandırmalarını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="422d4-176">Standart ER yapılandırmalarını içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-176">Import the standard ER configurations</span></span>

<span data-ttu-id="422d4-177">Microsoft Dynamics 365 Finance'un geçerli örneğine standart ER yapılandırmalarını eklemek için onları o örnek için yapılandırılmış olan ER [deposundan](general-electronic-reporting.md#Repository) içe aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="422d4-178">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-179">**Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve Microsoft sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="422d4-180">**Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="422d4-181">Regulatory Configuration Service bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="422d4-182">**Konfigürasyon depoları** sayfasında, sol bölmedeki yapılandırma ağacında, **BACS (UK)** biçim yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="422d4-183">**Sürümler** FastTab üzerinde, seçili ER biçim yapılandırmasının gerekli **1.1** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="422d4-184">Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Yapılandırma havuzu sayfası](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="422d4-186">[Global depoya](er-download-configurations-global-repo.md) erişmede sorun yaşıyorsanız, Microsoft Dynamics Lifecycle Services'den (LCS) gelen [yapılandırmaları karşıdan yükleyebilirsiniz](download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="422d4-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="422d4-187">İçe aktarılan ER yapılandırmalarını gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="422d4-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="422d4-188">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-189">**Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="422d4-190">**Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="422d4-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="422d4-191">Seçili **BACS (UK)** ER biçimine ek olarak, gerekli diğer acil yapılandırmalar konfigürasyonlarının da içe aktarıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="422d4-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="422d4-192">Aşağıdaki ER yapılandırmaların konfigürasyon ağacında kullanılabilir durumda olduğundan emin olun:</span><span class="sxs-lookup"><span data-stu-id="422d4-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="422d4-193">**Ödeme modeli** – Bu konfigürasyon, ödeme iş etki alanının veri yapısını temsil eden [veri modeli](general-electronic-reporting.md#data-model-and-model-mapping-components) bileşeni bileşenini içerir.</span><span class="sxs-lookup"><span data-stu-id="422d4-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="422d4-194">**Ödeme modeli eşleştirmesi 1611** – Bu konfigürasyon, veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulduğunu açıklayan [model eşleme](general-electronic-reporting.md#data-model-and-model-mapping-components) bileşeni içerir.</span><span class="sxs-lookup"><span data-stu-id="422d4-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="422d4-195">**BACS (UK)** – Bu konfigürasyon [Biçim](general-electronic-reporting.md#FormatComponentOutbound) ve biçim eşleme bileşenlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="422d4-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="422d4-196">Format bileşeni rapor düzenini belirtir.</span><span class="sxs-lookup"><span data-stu-id="422d4-196">The format component specifies the report layout.</span></span> <span data-ttu-id="422d4-197">Biçim eşleme bileşeni model veri kaynağını içerir ve çalışma süresinde bu veri kaynağı kullanılarak rapor düzeninin nasıl doldurulacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="422d4-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Yapılandırma sayfası](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="422d4-199">İşleme için satıcı ödemesini hazırlayın</span><span class="sxs-lookup"><span data-stu-id="422d4-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="422d4-200">Satıcı hesabı için banka bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="422d4-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="422d4-201">Bir satıcı hesabının, daha sonra kayıtlı bir ödemede başvurulacak banka bilgilerini eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="422d4-202">**Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="422d4-203">**Tüm satıcılar** sayfasında, **GB_SI_000001** satıcı hesabını seçin ve eylem bölmesinde, **satıcı** sekmesinde, **kurulumu** gerçekleştir grubunda **Banka hesapları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="422d4-204">**Satıcı banka hesapları** sayfasında, **Yeni**'yi seçin ve aşağıdaki bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="422d4-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="422d4-205">**Banka hesabı** alanında **GBP OPER** öğesini girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="422d4-206">**Banka grupları** alanında, **BankGBP** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="422d4-207">**Banka hesabı numarası** alanında **202015** girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="422d4-208">**SWIFT kodu** alanına <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="422d4-209">**IBAN** alanına **GB33BUKB20201555555555** girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="422d4-210">**Rota numarası** alanında, <a id="DefineRoutingNumber"></a>**123456** varsayılan değerini saklayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Satıcı banka hesapları sayfası](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="422d4-212">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-212">Select **Save**.</span></span>
5. <span data-ttu-id="422d4-213">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="422d4-213">Close the page.</span></span>
6. <span data-ttu-id="422d4-214">**Tüm satıcılar** sayfasında, **GB_SI_000001** satıcı hesabını açın.</span><span class="sxs-lookup"><span data-stu-id="422d4-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="422d4-215">Satıcı ayrıntıları sayfasında, gerekirse sayfayı düzenlenebilir yapmak için **Düzenle** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="422d4-216">**Ödeme** hızlı sekmesinde, **Banka hesabı** alanında, **GBP Operasyon** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Satıcı ayrıntıları sayfası](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="422d4-218">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-218">Select **Save**.</span></span>
10. <span data-ttu-id="422d4-219">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="422d4-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="422d4-220">Satıcı ödemesini girin</span><span class="sxs-lookup"><span data-stu-id="422d4-220">Enter a vendor payment</span></span>

<span data-ttu-id="422d4-221">[Ödeme teklifi](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal) kullanarak yeni satıcı ödemesi girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="422d4-222">**Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="422d4-223">**Satıcı ödeme günlüğü** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="422d4-224">**Ad** alanına **VendPay** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="422d4-225">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-225">Select **Lines**.</span></span>
5. <span data-ttu-id="422d4-226">**Ödeme teklifi** \> **Ödeme teklifi oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="422d4-227">**Satıcı ödeme teklifi** iletişim kutusunda, yalnızca **GB_SI_000001** satıcı hesabına ait kayıtları filtrelemek üzere koşulları konfigüre edin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="422d4-228">**00000007_Inv** fatura için satırı seçin ve sonra **ödeme oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Satıcı ödeme teklifi iletişim kutusu](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="422d4-230">Girilen ödemenin **elektronik** ödeme yöntemini kullanacak şekilde konfigüre edilmiş olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Satıcı ödemeleri sayfası](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="422d4-232">Standart ER biçimini kullanarak bir satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="422d4-233">Elektronik ödeme yöntemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="422d4-233">Set up the electronic payment method</span></span>

<span data-ttu-id="422d4-234">Elektronik ödeme yöntemini içe aktarılan ER biçim konfigürasyonu kullanacak şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="422d4-235">**Borç hesapları** \> **Ödeme kurulumu** \> **Ödeme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="422d4-236">**Ödeme yöntemleri - satıcılar** sayfasında, sol bölmedeki **elektronik** ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="422d4-237">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-237">Select **Edit**.</span></span>
4. <span data-ttu-id="422d4-238">**Dosya formatları** Hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="422d4-239">**Dışa aktarma biçimi yapılandırması** alanında, **BACS (UK)** biçim yapılandırması seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Ödeme yöntemleri - satıcılar sayfası](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="422d4-241">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="422d4-242">Satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-242">Process a vendor payment</span></span>

1. <span data-ttu-id="422d4-243">**Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="422d4-244">**Satıcı ödeme günlüğü** sayfasında, önceden eklediğiniz ödeme günlüğünü ve ardından **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="422d4-245">**Satıcı ödemeleri** sayfasında, **ödemeleri oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="422d4-246">**Ödemeler oluşturun** iletişim kutusuna, aşağıdaki bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="422d4-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="422d4-247">**Ödeme yöntemi** alanında **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="422d4-248">**Banka hesabı** alanında **GBSI OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="422d4-249">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-249">Select **OK**.</span></span>
6. <span data-ttu-id="422d4-250">**Elektronik rapor parametreleri** iletişim kutusunda, **yazdırma denetimi raporu** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Elektronik rapor parametreleri iletişim kutusu sayfası](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="422d4-252">Ödeme dosyasına ek olarak, artık kontrol raporu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="422d4-253">Zip dosyasını karşıdan yükleyin ve sonra aşağıdaki dosyaları dosyadan ayıklayın:</span><span class="sxs-lookup"><span data-stu-id="422d4-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="422d4-254">Excel biçimindeki denetim raporu</span><span class="sxs-lookup"><span data-stu-id="422d4-254">The control report in Excel format</span></span>
    - <span data-ttu-id="422d4-255">TXT biçiminde ödeme dosyası</span><span class="sxs-lookup"><span data-stu-id="422d4-255">The payment file in TXT format</span></span>

        <span data-ttu-id="422d4-256">Sağlanan er biçiminin [yapısına](#PositionRoutingNumber) uygun olarak, oluşturulan dosyadaki ödeme satırının konfigüre edilen Banka hesabı için [tanımlanan](#DefineRoutingNumber) rota numarasıyla başladığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![TXT biçiminde ödeme dosyası](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="422d4-258">Standart ER biçimini Özelleştirme</span><span class="sxs-lookup"><span data-stu-id="422d4-258">Customize the standard ER format</span></span>

<span data-ttu-id="422d4-259">Bu bölümde gösterilen örnek için, BACS formatında satıcı ödeme dosyaları oluşturmak üzere Microsoft tarafından sağlanan ER konfigürasyonlarını kullanmak istiyorsunuz, ancak belirli bir bankanın gereksinimlerini destekleyecek bir özelleştirme eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="422d4-260">Ayrıca, ER konfigürasyonlarının yeni sürümleri kullanılabilir olduğunda da özel biçiminizi yükseltebilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="422d4-261">Ancak, yükseltme yapabilmek için en düşük maliyette olmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="422d4-262">Bu durumda, Litware, Inc. temsilcisi olarak, **BACS (UK)** Microsoft tarafından temel olarak sağlanan bir yapılandırmayı tkullanarak yeni bir ER biçim konfigürasyonu oluşturmanız (türetmeniz) gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="422d4-263">Özel biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="422d4-263">Create a custom format</span></span>

1. <span data-ttu-id="422d4-264">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="422d4-265">**Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK)** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="422d4-266">Litwin, Inc. özel sürümün temeli olarak bu ER biçim yapılandırmasının sürüm 1,1 ' sini kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="422d4-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="422d4-267">Açılır iletişim kutusunu açmak için **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="422d4-268">Bu iletişim kutusunu, özel ödeme biçimi için yeni bir konfigürasyon oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="422d4-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="422d4-269">**Yeni** alan grubunda, **Addan türetilen: BACS (UK), Microsoft** seçeneği.</span><span class="sxs-lookup"><span data-stu-id="422d4-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="422d4-270">**Ad** alanına, **BACS (UK özel)** girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Yapılandırma oluşturma açılan iletişim kutusu](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="422d4-272">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-272">Select **Create configuration**.</span></span>

<span data-ttu-id="422d4-273">**BACS (Birleşik Krallık özel)** ER biçimi yapılandırmasının sürüm 1.1.1 oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="422d4-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="422d4-274">Bu sürüm **taslak** [durumuna](general-electronic-reporting.md#component-versioning) sahip ve düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="422d4-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="422d4-275">Özel ER biçiminizin geçerli içeriğinin,  Microsoft tarafından sağlanan biçimin içeriğiyle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="422d4-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Yapılandırma sayfası](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="422d4-277">Özel biçim düzenleme</span><span class="sxs-lookup"><span data-stu-id="422d4-277">Edit a custom format</span></span>

<span data-ttu-id="422d4-278">Özel biçiminizi, bankaya özel gereksinimleri karşılayacak şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="422d4-279">Örneğin bir banka, oluşturulan ödeme dosyalarının, bir bankanın işlenmiş olan satıcı ödemesine atanan, tüm dünyada Interbank Financial telekomünikasyon (SWIFT) kodu için Society içermesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="422d4-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="422d4-280">SWIFT kodları, tüm dünyada belirli bankaların tanımlanmasında kullanılan uluslararası banka kodlarıdır.</span><span class="sxs-lookup"><span data-stu-id="422d4-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="422d4-281">Bunlar banka tanımlayıcı kodları (BIC'ler) olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="422d4-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="422d4-282">SWIFT kodu 11 karakter uzunluğunda olmalıdır ve oluşturulan bir ödeme dosyasındaki her bir ödeme satırının başına girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="422d4-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="422d4-283">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="422d4-284">**Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK özel)** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="422d4-285">**Sürümler** FastTab üzerinde, seçili yapılandırmasının gerekli **1.1.1** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="422d4-286">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-286">Select **Designer**.</span></span>
5. <span data-ttu-id="422d4-287">**Biçim tasarımcısı** sayfasında Format öğeleriyle ilgili daha fazla bilgi görüntülemek için **ayrıntıları göster** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="422d4-288">Aşağıdaki öğeleri genişletip gözden geçirin:</span><span class="sxs-lookup"><span data-stu-id="422d4-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="422d4-289">**Klasör** türünün **bacsreportsfolder** öğesi.</span><span class="sxs-lookup"><span data-stu-id="422d4-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="422d4-290">Bu öge ZIP biçiminde çıktı oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="422d4-291">**Dosya** türünün **dosya** öğesi.</span><span class="sxs-lookup"><span data-stu-id="422d4-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="422d4-292">Bu öge TXT biçiminde ödeme dosyası oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="422d4-293">**Sıra** türünün **işlemler** öğesi.</span><span class="sxs-lookup"><span data-stu-id="422d4-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="422d4-294">Bu öge, ödeme dosyası tekli ödeme oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="422d4-295">**Sıra** türünün **işlem** öğesi.</span><span class="sxs-lookup"><span data-stu-id="422d4-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="422d4-296">Bu öge, tekli ödeme satırınsa ayrı alanlar oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="422d4-297">**İşlem** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-297">Select the **transaction** element.</span></span>

    ![ER işlemleri tasarımcısında işlem ögesi](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="422d4-299">Sağlanan rapor, <a id="PositionRoutingNumber"></a>her ödeme satırının Banka rota numarasıyla başlaması için konfigüre edilir.</span><span class="sxs-lookup"><span data-stu-id="422d4-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="422d4-300">**Vendbankroutenum** biçim öğesi bu amaçla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="422d4-301">**Ekle**'i seçin ve sonra eklemekte olduğunuz Format öğesinin **metin\\dizesi** türünü seçin:</span><span class="sxs-lookup"><span data-stu-id="422d4-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="422d4-302">**Ad** alanına **vendBankSWIFT** yazın.</span><span class="sxs-lookup"><span data-stu-id="422d4-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="422d4-303">**Minimum uzunluk** alanında **11** girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="422d4-304">**Maksimum uzunluk** alanında **11** girin.</span><span class="sxs-lookup"><span data-stu-id="422d4-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="422d4-305">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="422d4-306">**vendBankSWIFT** öğesi, oluşturulan dosyalardaki satıcı bankasının SWIFT kodunu girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="422d4-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="422d4-307">Biçim yapısı ağacında, **vendBankSWIFT** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="422d4-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="422d4-308">Seçili biçim öğesini bir düzey yukarı taşımak için **yukarı taşı** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="422d4-309">Bu adımı, **vendBankSWIFT** öğesi <a id="PositionSWIFTCode"></a>ana **işlem** öğesinin altındaki ilk öğe olana kadar tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![ER İşlemleri tasarımcısında işlemin altındaki ilk öğe olarak VendBankSWIFT](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="422d4-311">Biçim yapısı ağacında **vendBankSWIFT** 'un hala seçili olmasına karşın, **eşleme** sekmesini seçin ve **model** veri kaynağını genişletin.</span><span class="sxs-lookup"><span data-stu-id="422d4-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="422d4-312">**model.Payment** \> **model.Payment.CreditorAgent** genişletin ve **model.Payment.CreditorAgent.BICFI** veri kaynağı alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="422d4-313">Bu veri kaynağı alanı, işlenmiş satıcı ödemesine aracı rolü atanan satıcı bankasının SWIFT kodunu sunar.</span><span class="sxs-lookup"><span data-stu-id="422d4-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="422d4-314">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-314">Select **Bind**.</span></span> <span data-ttu-id="422d4-315">**vendBankSWIFT** format ögesi artık **model.Payment.CreditorAgent.BICFI** veri kaynağı alanıyla bağlıdır, böylece oluşturulan ödeme dosyalarına SWIFT kodları girilecaktır.</span><span class="sxs-lookup"><span data-stu-id="422d4-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![vendBankSWIFT biçim öğesi ER işlemleri tasarımcısında model.Payment.CreditorAgent.BICFI veri kaynağı alanıyla ilişkilidir](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="422d4-317">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-317">Select **Save**.</span></span>
15. <span data-ttu-id="422d4-318">Tasarımcı sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="422d4-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="422d4-319">Özel biçimi çalıştırılabilir olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="422d4-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="422d4-320">Şimdi özel biçimin ilk sürümü oluşturulduğundan ve **taslak** durumunda olduğundan, bunu test amacıyla çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="422d4-321">Raporu çalıştırmak için, özel işlem biçiminizi ifade eden ödeme yöntemini kullanarak bir satıcı ödemesini işlemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="422d4-322">Varsayılan olarak, uygulamadan ER biçimini çağırdığınızda yalnızca **Tamamlandı** ve **Paylaşıldı** durumuna sahip sürümler [dikkate alınır](general-electronic-reporting.md#component-versioning).</span><span class="sxs-lookup"><span data-stu-id="422d4-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="422d4-323">Bu davranış, bitmemiş tasarımları bulunan ER biçimlerinin kullanılmasını önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="422d4-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="422d4-324">Ancak, test çalışmalarınız için, uygulamayı **taslak** durumunda olan ER formatının biçimini kullanmaya zorlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="422d4-325">Bu şekilde, herhangi bir değişiklik gerekiyorsa geçerli biçim sürümünü ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="422d4-326">Daha fazla bilgi için bkz. [Uygulanabilirlik](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="422d4-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="422d4-327">ER biçiminin taslak sürümünü kullanmak için, ER biçimini açık olarak işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="422d4-328">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="422d4-329">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="422d4-330">**Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="422d4-331">Geçerli sayfayı düzenlemeye hazır hale getirmek için gerektiğinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="422d4-332">Sol bölmedeki konfigürasyon ağacında, **BACS (UK özel)** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="422d4-333">**Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Yapılandırmalar sayfasında Taslak seçeneğini Çalıştır](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="422d4-335">Özel ER biçimini kullanarak bir satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="422d4-336">Elektronik ödeme yöntemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="422d4-336">Set up the electronic payment method</span></span>

<span data-ttu-id="422d4-337">Satıcı ödemelerini işlemek için özel ER formatının kullanılabilmesi için elektronik ödeme yöntemini konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="422d4-338">**Borç hesapları** \> **Ödeme kurulumu** \> **Ödeme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="422d4-339">**Ödeme yöntemleri - satıcılar** sayfasında, sol bölmedeki **elektronik** ödeme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="422d4-340">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-340">Select **Edit**.</span></span>
4. <span data-ttu-id="422d4-341">**Dosya formatı** Hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="422d4-342">**Dışa aktarma biçimi yapılandırması** alanında, **BACS (UK özel)** biçim yapılandırması seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Ödeme yöntemleri - satıcılar sayfası](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="422d4-344">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="422d4-345">Satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-345">Process a vendor payment</span></span>

1. <span data-ttu-id="422d4-346">**Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="422d4-347">**Satıcı ödeme günlüğü** sayfasında, önceden oluşturduğunuz ödeme günlüğünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="422d4-348">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-348">Select **Lines**.</span></span>
4. <span data-ttu-id="422d4-349">**Satıcı ödemeleri** sayfasında, kılavuzun üstünde, **ödeme durumu** \> **yok** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="422d4-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="422d4-350">**Ödeme oluştur** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="422d4-351">**Ödemeler oluşturun** iletişim kutusuna, aşağıdaki bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="422d4-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="422d4-352">**Ödeme yöntemi** alanında **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="422d4-353">**Banka hesabı** alanında **GBSI OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="422d4-354">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-354">Select **OK**.</span></span>
8. <span data-ttu-id="422d4-355">**Elektronik rapor parametreleri** iletişim kutusunda, **yazdırma denetimi raporu** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="422d4-356">Ödeme dosyasına ek olarak, artık kontrol raporu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="422d4-357">Zip dosyasını karşıdan yükleyin ve sonra aşağıdaki dosyaları dosyadan ayıklayın:</span><span class="sxs-lookup"><span data-stu-id="422d4-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="422d4-358">Excel biçimindeki denetim raporu</span><span class="sxs-lookup"><span data-stu-id="422d4-358">The control report in Excel format</span></span>
    - <span data-ttu-id="422d4-359">TXT biçiminde ödeme dosyası</span><span class="sxs-lookup"><span data-stu-id="422d4-359">The payment file in TXT format</span></span>

        <span data-ttu-id="422d4-360">Özel ER formatının yapısına uygun olarak, oluşturulan dosyadaki ödeme satırı şimdi, ödemesi işlenmiş olan Satıcının banka hesabı için [girilen](#DefineSWIFTCode) SWIFT koduyla [başlar](#PositionSWIFTCode).</span><span class="sxs-lookup"><span data-stu-id="422d4-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![TXT biçiminde ödeme dosyası](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="422d4-362">Standart ER biçimi yapılandırmalarının yeni sürümlerini içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="422d4-363">Bu bölümde gösterilen örnek için, Bilgi Bankası makalesi [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) hakkında bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="422d4-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="422d4-364">Bu bildirim, Microsoft tarafından yayımlanmış olan **BACS (UK)** ER biçiminin yeni sürümü hakkında sizi bilgilendirir.</span><span class="sxs-lookup"><span data-stu-id="422d4-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="422d4-365">Kontrol raporuna ek olarak, bu yeni sürüm, bir satıcı ödemesi işlenirken kullanıcıların ödeme önerisi raporunu ve ilişkili Not raporunu oluşturmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="422d4-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="422d4-366">Bu işlevi kullanmaya başlamak istediğinizde.</span><span class="sxs-lookup"><span data-stu-id="422d4-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="422d4-367">Standart ER yapılandırmalarının yeni sürümlerini içe aktarın</span><span class="sxs-lookup"><span data-stu-id="422d4-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="422d4-368">Geçerli Finans örneğine standart ER yapılandırmalarının yeni sürümlerini eklemek için onları o örnek için yapılandırılmış olan ER [deposundan](general-electronic-reporting.md#Repository) içe aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="422d4-369">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-370">**Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve Microsoft sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="422d4-371">**Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="422d4-372">Regulatory Configuration Service bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="422d4-373">**Konfigürasyon depoları** sayfasında, sol bölmedeki yapılandırma ağacında, **BACS (UK)** biçim yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="422d4-374">**Sürümler** FastTab üzerinde, seçili ER biçim yapılandırmasının gerekli **3.3** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="422d4-375">Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Yapılandırma havuzu sayfası](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="422d4-377">[Global depoya](er-download-configurations-global-repo.md) erişmede sorun yaşıyorsanız, bunun yerine LCS'den gelen [yapılandırmaları karşıdan yükleyebilirsiniz](download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="422d4-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="422d4-378">İçe aktarılan ER biçimi yapılandırmalarını gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="422d4-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="422d4-379">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-380">**Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="422d4-381">**Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK)** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="422d4-382">**Sürümler** hızlı sekmesinde, sürüm **3.3**' i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="422d4-383">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-383">Select **Designer**.</span></span>
6. <span data-ttu-id="422d4-384">**Biçim tasarımcısı** sayfasında **BACSReportsFolder** biçim öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="422d4-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="422d4-385">3,3 sürümü, satıcı ödemesi işlenirken bir ödeme önerisi raporu oluşturmak için kullanılan **PaymentAdviceReport** biçim öğesini içerir.</span><span class="sxs-lookup"><span data-stu-id="422d4-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![PaymentAdviceReport biçimi ER işlemleri tasarımcısında işlem ögesi](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="422d4-387">Tasarımcı sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="422d4-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="422d4-388">Özel bir biçimde, içe aktarılan bir biçimin yeni sürümündeki Değişiklikleri benimseme</span><span class="sxs-lookup"><span data-stu-id="422d4-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="422d4-389">Özel biçimin geçerli taslak sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="422d4-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="422d4-390">Özel biçimizin geçerli durumunu korumak istiyorsanız, **taslak** durumundan **tamamlandı** durumuna değiştirerek draft sürüm 1.1.1'ı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="422d4-391">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="422d4-392">**Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="422d4-393">**Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK)** seçin ve **BACS (UK özel)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="422d4-394">**Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="422d4-395">Sürüm 1.1.1 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="422d4-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="422d4-396">Yeni bir düzenlenebilir sürüm olan 1.1.2 eklendi ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="422d4-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="422d4-397">Bu sürümü, özel ER biçiminiz üzerinde başka değişiklikler yapmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="422d4-398">Özel biçimi yeni bir temel sürüme yeniden temellendir</span><span class="sxs-lookup"><span data-stu-id="422d4-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="422d4-399">Özelleştirmenizin 3,3 **BACS (Birleşik Krallık)** biçiminin yeni işlevlerini kullanmaya başlamak için , özel konfigürasyon, **BACS (Birleşik Krallık özel)** için temel konfigürasyon sürümünü değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="422d4-400">Bu işlem [yeniden temelleme](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)olarak bilinmektedir.</span><span class="sxs-lookup"><span data-stu-id="422d4-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="422d4-401">**BACS (UK)** 1.1 sürümü yerine yeni sürüm 3.3 kullanın.</span><span class="sxs-lookup"><span data-stu-id="422d4-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="422d4-402">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="422d4-403">**Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK özel)** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="422d4-404">**Sürümler** hızlı sekmesinde, sürüm **1.1.2** seçin ve yeniden **temellendir** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="422d4-405">**Yeniden temellendirme** iletişim kutusunda, **hedef sürüm** alanında, bunu yeni temel olarak uygulamak ve konfigürasyonu güncelleştirmek için kullanmak üzere temel yapılandırmanın **3,3** sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Yeniden temellendirme iletişim kutusu](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="422d4-407">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-407">Select **OK**.</span></span>
6. <span data-ttu-id="422d4-408">Taslak sürümün sayısının temel sürümdeki değişikliği yansıtmak için **1.1.2** olan sayının **3.3.2** olarak değiştiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="422d4-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="422d4-409">Otomatik olarak birleştirilemeyen bazı biçim değişikliklerini temsil eden, yeni temel sürüm ile özel sürümün birleştirilmesi sırasında bazı çakışmaların ortaya çıktığını göz önünde tutun.</span><span class="sxs-lookup"><span data-stu-id="422d4-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Yapılandırmalar sayfasındaki çakışmalarıyla yeniden esaslı konfigürasyon](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="422d4-411">Çakışmalar keşfedildiğinde, biçim Tasarımcısı 'nda el ile çözülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="422d4-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="422d4-412">**Sürümler** hızlı sekmesinde, sürüm **3.3.2**' i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="422d4-413">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-413">Select **Designer**.</span></span>
9. <span data-ttu-id="422d4-414">**Biçim Tasarımcısı** sayfasında, **Ayrıntılar** hızlı sekmesinde, yeniden temellendirme çakışma kaydını seçin ve **temel değer Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![ER Operations Designer 'da çakışma kaydını yeniden temellendir](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="422d4-416">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-416">Select **Save**.</span></span>

    <span data-ttu-id="422d4-417">Yeniden temellendirme çakışma kaydı **Ayrıntılar** hızlı sekmesinde artık görünolmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="422d4-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![ER Operations Designer'da çözümlenen çakışma](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="422d4-419">Bu ER biçiminde temel modelin sürüm 3'ün kullanılması gerektiğini onaylayarak çakışmayı çözdünüz.</span><span class="sxs-lookup"><span data-stu-id="422d4-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="422d4-420">**BACSReportsFolder** \> **dosya** \> **işlemler** \> **işlem**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="422d4-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="422d4-421">**Eşleme** sekmesinde, özel ER biçimlendirmenizin 3.3.2 sürümü hem özelleştirmenizi (**vendBankSWIFT** biçim öğesi ve bağlaması) içerir, hem de Microsoft (**PaymentAdviceReport** biçim öğesi iç içe geçirilmiş öğeler ve yapılandırılmış bağlamalar ile birlikte) tarafından sağlanan temel ER biçiminin sürüm 3,3 ' inin yeni işlevselliğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="422d4-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="422d4-422">Yalnızca birkaç fare tıklatmasıyla, özelleştirmeyle birleştirerek yeni bir temel sürümün değişikliklerini benimsemiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="422d4-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![ER Işlem tasarımcısında birleştirilmiş biçim](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="422d4-424">Tasarımcı sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="422d4-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="422d4-425">Yeniden temellendirme eylemi geri alınamaz.</span><span class="sxs-lookup"><span data-stu-id="422d4-425">The rebase action is reversible.</span></span> <span data-ttu-id="422d4-426">Bu yeniden temellendirme iptal etmek için, **sürümler** hızlı sekmesinde **BACS (Birleşik Krallık özel)** biçiminin sürüm **1.1.1** öğesini seçin ve sonra **Bu sürümü Al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="422d4-427">Daha sonra 3.3.2 sürüm 1.1.2 yeniden numaralandırılır ve taslak sürümü 1.1.2 içeriği sürüm 1.1.1 içeriğiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="422d4-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="422d4-428">Yeniden temellendirilen ER biçimini kullanarak bir satıcı ödemesini işleme</span><span class="sxs-lookup"><span data-stu-id="422d4-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="422d4-429">**Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="422d4-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="422d4-430">**Satıcı ödeme günlüğü** sayfasında, önceden oluşturduğunuz ödeme günlüğünü seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="422d4-431">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-431">Select **Lines**.</span></span>
4. <span data-ttu-id="422d4-432">**Satıcı ödemeleri** sayfasında, kılavuzun üstünde, **ödeme durumu** \> **yok** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="422d4-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="422d4-433">**Ödeme oluştur** seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="422d4-434">**Ödemeler oluşturun** iletişim kutusuna, aşağıdaki bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="422d4-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="422d4-435">**Ödeme yöntemi** alanında **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="422d4-436">**Banka hesabı** alanında **GBSI OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="422d4-437">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-437">Select **OK**.</span></span>
8. <span data-ttu-id="422d4-438">**Elektronik rapor parametreleri** iletişim kutusuna, aşağıdaki bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="422d4-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="422d4-439">**Kontrol raporu yazdır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="422d4-440">**Ödeme önerisi yazdır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="422d4-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Elektronik rapor parametreleri iletişim kutusu](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="422d4-442">Ödeme dosyasına ek olarak, artık hem denetim raporunu hem de ödeme önerisi raporunu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="422d4-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="422d4-443">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="422d4-443">Select **OK**.</span></span>
10. <span data-ttu-id="422d4-444">Zip dosyasını karşıdan yükleyin ve sonra aşağıdaki dosyaları dosyadan ayıklayın:</span><span class="sxs-lookup"><span data-stu-id="422d4-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="422d4-445">Excel biçimindeki denetim raporu</span><span class="sxs-lookup"><span data-stu-id="422d4-445">The control report in Excel format</span></span>
    - <span data-ttu-id="422d4-446">Excel biçimindeki ödeme önerisi raporu</span><span class="sxs-lookup"><span data-stu-id="422d4-446">The payment advice report in Excel format</span></span>

        ![Excel biçimindeki ödeme önerisi raporu](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="422d4-448">TXT biçiminde ödeme dosyası</span><span class="sxs-lookup"><span data-stu-id="422d4-448">The payment file in TXT format</span></span>

        <span data-ttu-id="422d4-449">Özel ER formatının yapısına uygun olarak, oluşturulan dosyadaki ödeme satırı şimdi, ödemesi işlenmiş olan Satıcının banka hesabı için girilen SWIFT koduyla başlar.</span><span class="sxs-lookup"><span data-stu-id="422d4-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![TXT biçiminde ödeme dosyası](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="422d4-451">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="422d4-451">Additional resources</span></span>

- [<span data-ttu-id="422d4-452">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="422d4-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="422d4-453">Lifecycle Services'dan ER yapılandırma indirme</span><span class="sxs-lookup"><span data-stu-id="422d4-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="422d4-454">Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir</span><span class="sxs-lookup"><span data-stu-id="422d4-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
