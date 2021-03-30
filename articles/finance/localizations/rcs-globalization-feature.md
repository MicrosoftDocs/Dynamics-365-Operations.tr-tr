---
title: Regulatory Configuration Service (RCS) - Küreselleşme özellikleri
description: Bu konuda, Küreselleşme özellikleri oluşturmak ve kullanmak için Microsoft Regulatory Configuration Services (RCS) ve Genel depoyu nasıl kullanacağınız açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: d5d42bd076ca77c5d2906593d44ae420d954a0b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218866"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="c3974-103">Regulatory Configuration Service (RCS) - Küreselleşme özellikleri</span><span class="sxs-lookup"><span data-stu-id="c3974-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3974-104">Microsoft Regulatory Configuration Service (RCS) kullanarak Globalizasyon hizmetlerinde kullanılabilecek e-faturalama hizmeti gibi bir Globalizasyon özelliği oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3974-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="c3974-105">RCS şu görevleri gerçekleştirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="c3974-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="c3974-106">Bir özelliğin ilgili bileşenlerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="c3974-106">Define related components of a feature.</span></span>
- <span data-ttu-id="c3974-107">Özellik yaşam döngüsünü özelliğin durumuyla yönetin.</span><span class="sxs-lookup"><span data-stu-id="c3974-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="c3974-108">Bir özelliği tanımlanmış ortamlar için kullanılabilir hale getirin.</span><span class="sxs-lookup"><span data-stu-id="c3974-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="c3974-109">Bir özelliği diğer organizasyonlarla paylaşma.</span><span class="sxs-lookup"><span data-stu-id="c3974-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="c3974-110">Aşağıdaki yordamlarda, RCS 'deki bir kullanıcının Globalizasyon özelliği ve ilgili bileşenleri nasıl ekleneceği, özelliğin durumu nasıl güncelleştirileceği ve genelleştirme hizmetlerinde kullanılabilmesi için özelliğin kullanılabilir hale gelen bir Kullanıcı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c3974-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="c3974-111">Yordamları gerçekleştirmeden önce, aşağıdaki görevlerle ilgili adımları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c3974-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="c3974-112">RCS örneğine erişme.</span><span class="sxs-lookup"><span data-stu-id="c3974-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="c3974-113">Bir konfigürasyon sağlayıcısı oluşturma ve etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="c3974-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="c3974-114">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="c3974-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="c3974-115">Finance and Operations uygulamaları örneğiniz için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="c3974-116">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="c3974-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="c3974-117">Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services -Yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="c3974-118">Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu ortama erişmek için sayfa URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3974-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="c3974-119">Globalizasyon özellikleri açma</span><span class="sxs-lookup"><span data-stu-id="c3974-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="c3974-120">RCS örneğiniz üzerinde **Özellik yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="c3974-121">**Özellik Yönetimi** çalışma alanında, listeden **Genelleştirme özellikleri**'ni seçin ve **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Özellik yönetiminde Globalizasyon özellikleri](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="c3974-123">Genelleştirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="c3974-123">Globalization features</span></span>

<span data-ttu-id="c3974-124">Genelleştirme özelliğini kullanmak için, onu Global depodan içe aktarmanız ve kendi sürümünüzü oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3974-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="c3974-125">Genelleştirme özellikleri eklemenin iki yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="c3974-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="c3974-126">Yayımlanmış veya paylaşılan, varolan bir özelliği temel alan türetilmiş bir özellik ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="c3974-127">Sıfırdan oluşturduğunuz yeni bir özellik ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="c3974-128">Globalizasyonu özelliklerine erişme</span><span class="sxs-lookup"><span data-stu-id="c3974-128">Access Globalization features</span></span>

1. <span data-ttu-id="c3974-129">Bu konuda daha önce anlatıldığı gibi, özellik yönetiminde **Genelleştirme özellikleri** özelliğinin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c3974-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="c3974-130">Yeni **Genelleştirme özellikleri** çalışma alanını açın ve sonra **Özellikler** altında **e-faturalama** döşemesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Global Özellikler çalışma alanı](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="c3974-132">**E-faturalama özellikleri** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="c3974-132">The **e-Invoicing Features** page is opened.</span></span>

    ![e-faturalama özellikleri sayfası](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="c3974-134">Türetilmiş Genelleştirme özelliği Ekle</span><span class="sxs-lookup"><span data-stu-id="c3974-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="c3974-135">Yeni bir Genelleştirme özelliğini, yayımlanmış veya paylaşılan varolan bir özellikten türeterek ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3974-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="c3974-136">**Genel havuz sayfasından içe aktarma özelliğini** açmak için **içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Özelliği genel havuz sayfasından içe aktar](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="c3974-138">En son özellikleri almak için **Eşitle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="c3974-139">Eşitlenmiş liste, Microsoft tarafından yayımlandıkları veya başka bir konfigürasyon sağlayıcısı tarafından paylaşıldıklarından dolayı kullanabileceğiniz özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="c3974-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Eşitlenen özellik listesi](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="c3974-141">Listede içe aktarılacak özellikleri seçin ve **içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="c3974-142">Seçilen özellikler başarıyla içe aktarıldığında bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="c3974-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![İleti içe aktarma başarılı](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="c3974-144">**Ekle**'yi seçin ve açılan iletişim kutusunda **varolan sürüme bağlı** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="c3974-145">Özellik için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="c3974-146">Kullanılabilen özellikler listesinde, özelliğin temel sürümünü seçin ve sonra **Özellik Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Türetilmiş özellik ekleme](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="c3974-148">Eklediğiniz Özellik oluşturuldu ve **taslak** durumuna sahip.</span><span class="sxs-lookup"><span data-stu-id="c3974-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Taslak durumunda olan türetilmiş Özellik](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="c3974-150">Güncelleştirmelerin gerekli olup olmadığını belirlemek için özellik bileşenlerini gözden geçirin:</span><span class="sxs-lookup"><span data-stu-id="c3974-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="c3974-151">Elektronik raporlama (ER) biçimlerini ve bunların, özellik sürümü için biçim eşlemeleriyle olan bağlamasını özelleştirmeniz olasılığına karşı konfigürasyonları gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c3974-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="c3974-152">Özellik sürümü için **Eylemler** sekmesini, **uygulanabilirlik kuralları** sekmesini veya **değişkenler** sekmesini özelleştirmeniz gerekebileceği için kurulumu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c3974-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="c3974-153">**Sürümler** sekmesinde, **geçerlilik başlangıç** tarihi seçin ve **Açıklama** alanı boşsa açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="c3974-154">Özelliği tamamlamak için **durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="c3974-155">Tamamlanmış özellikler belirli bir ortam için kullanılabilir duruma getirilebilir, böylece Genelleştirme hizmetlerinde kullanılabilir veya Global havuzda yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="c3974-156">**Yayımlanmış** **özellik sürümü durum** değeri olan Özellikler , harici organizasyonlarla paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="c3974-157">Yeni Genelleştirme özelliği Ekle</span><span class="sxs-lookup"><span data-stu-id="c3974-157">Add a new Globalization feature</span></span>

<span data-ttu-id="c3974-158">Baştan oluşturarak yeni bir Genelleştirme özelliği ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3974-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="c3974-159">**Genel havuzdan içe aktarma özelliği** sayfasında **Ekle** 'yi seçin ve açılan iletişim kutusunda **yeni özellik** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="c3974-160">Özellik için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="c3974-161">**Özellik oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-161">Select **Create feature**.</span></span>

    ![Yeni özellik ekleme](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="c3974-163">**Sürümler** sekmesinde, **geçerlilik tarihi** seçin ve sonra da özelliği tamamlamak için **durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="c3974-164">Tamamlanmış özellikler belirli bir ortam için kullanılabilir duruma getirilebilir, böylece Genelleştirme hizmetlerinde kullanılabilir veya Global havuzda yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="c3974-165">**Yayımlanmış** **özellik sürümü durum** değeri olan Özellikler , harici organizasyonlarla paylaşılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="c3974-166">Özellik bileşenine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c3974-166">Feature component overview</span></span>

<span data-ttu-id="c3974-167">Genelleştirme özelliklerinin birkaç bileşeni vardır:</span><span class="sxs-lookup"><span data-stu-id="c3974-167">Globalization features have several components:</span></span>

- <span data-ttu-id="c3974-168">**Sürüm** – Bu bileşen özellik yaşam döngüsü yönetimini destekler ve kullanıcıların özelliğin farklı sürümleri için durumu yönetmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="c3974-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="c3974-169">**Yapılandırmalar** – Bu bileşen kullanıcıların ilgili ER biçimlerini ve biçim eşlemelerini yönetmesine, görüntülemesine ve düzenlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c3974-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="c3974-170">**Ayarlar** – Bu bileşen, bir e-faturalama hizmeti gibi, Genelleştirme servisleri kullanıcılarının ilgili özellik sürümünün kurulumunu yönetme gibi kullanıcılara olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c3974-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="c3974-171">Bu nedenle, iletişim ve yanıt kurallarının esnek yapımını destekler.</span><span class="sxs-lookup"><span data-stu-id="c3974-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="c3974-172">**Ortam** – Bu bileşen, bir e-faturalama hizmeti gibi Genelleştirme Hizmetleri kullanıcılarının, özellik sürümü kurulumunun kullanıldığı ortamı yönetmesine ve erişimi olacak kullanıcılara yetki vermesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c3974-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="c3974-173">**Kuruluşlar** – Bu bileşen, kullanıcıların özelliği harici organizasyonlarla paylaşmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c3974-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="c3974-174">Özellik bileşenlerini konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="c3974-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="c3974-175">Sürüm ve durum</span><span class="sxs-lookup"><span data-stu-id="c3974-175">Version and status</span></span>

<span data-ttu-id="c3974-176">Sürüm, Genelleştirme özelliği yaşam döngüsünü yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c3974-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="c3974-177">**Durum**, **Sürüm** sekmesinin durum alanında değiştirilebilir  . Aşağıdaki durumlar kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="c3974-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="c3974-178">**Taslak** – özellik yalnızca bu durumda olduğu zaman düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="c3974-179">**Tamamlandı** – özellik ve tüm ilgili bileşenler sonlandırılmalı (tamamlandı) ve düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="c3974-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="c3974-180">**Yayımlandı** – özellik ve ilgili tüm bileşenler Global depoya yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="c3974-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="c3974-181">**Paylaşılan** – özellik ve tüm ilgili bileşenler harici organizasyonlarla paylaşıldı.</span><span class="sxs-lookup"><span data-stu-id="c3974-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="c3974-182">**Etkin** – özellik ve tüm ilgili bileşenler, bir e-faturalama servisi gibi bir Genelleştirme hizmetinde kullanılmak üzere etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="c3974-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="c3974-183">Özelliklerin bazıları bu durumlardan bazıları arasında sırayla hareket etmelidir.</span><span class="sxs-lookup"><span data-stu-id="c3974-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="c3974-184">Bu nedenle, her yaşam döngüsü aşamasında her durum için kullanılabilir olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="c3974-185">Konfigürasyonlar</span><span class="sxs-lookup"><span data-stu-id="c3974-185">Configurations</span></span>

<span data-ttu-id="c3974-186">Yapılandırmalar için şu eylemler mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="c3974-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="c3974-187">**Görüntüle** – herhangi bir güncelleştirme gerektirmeyen temel özellik konfigürasyonlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="c3974-188">**Düzenle** – Biçim tasarımcısında biçim veya biçim eşleştirmesini düzenleyebilmeniz için seçili konfigürasyonun taslak sürümünü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c3974-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="c3974-189">**Sil** – Seçili konfigürasyonu özellikten silin.</span><span class="sxs-lookup"><span data-stu-id="c3974-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="c3974-190">**Yeniden temellendirme** – özelliği yeniden temellendir.</span><span class="sxs-lookup"><span data-stu-id="c3974-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="c3974-191">Daha fazla bilgi için, Bu konunun ilerleyen kısımlarında [türetilen Genelleştirme özellikleri](#rebase) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="c3974-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="c3974-192">Kurulumlar</span><span class="sxs-lookup"><span data-stu-id="c3974-192">Setups</span></span>

<span data-ttu-id="c3974-193">Özellik kurulumları için şu eylemler mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="c3974-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="c3974-194">**EKle** – yeni özellik kurulumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c3974-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="c3974-195">Bu özellik Kurulumu varolan bir özellik kurulumundan türetilebilir veya sıfırdan oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="c3974-196">**Sil** – Seçili bir özellik kurulumunu siler.</span><span class="sxs-lookup"><span data-stu-id="c3974-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="c3974-197">**Görüntüle** – herhangi bir değişiklik gerektirmeyen temel bir özellik kurulumunu görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="c3974-198">**Düzenle** – bir özellik kurulumunun üç ana bileşen bileşeni özniteliklerini oluşturur, siler veya değiştirir:</span><span class="sxs-lookup"><span data-stu-id="c3974-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="c3974-199">Eylemler ve parametreleri</span><span class="sxs-lookup"><span data-stu-id="c3974-199">Actions and their parameters</span></span>
    - <span data-ttu-id="c3974-200">Uygulanabilirlik kuralları</span><span class="sxs-lookup"><span data-stu-id="c3974-200">Applicability rules</span></span>
    - <span data-ttu-id="c3974-201">Değişkenler</span><span class="sxs-lookup"><span data-stu-id="c3974-201">Variables</span></span>

![Özellik sürümü kurulum sayfası](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="c3974-203">Ortamlar</span><span class="sxs-lookup"><span data-stu-id="c3974-203">Environments</span></span>

<span data-ttu-id="c3974-204">Ortamlar için şu eylemler mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="c3974-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="c3974-205">**Etkinleştir** – Seçili bir özellik sürümü için, yayımlanmış bir ortam seçin ve kullanılabilir olması gereken **başlangıç tarihini** seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="c3974-206">Daha fazla bilgi için, Bu konunun ilerleyen kısımlarında [Etkinleştirme için ortamları yapılandırma](#configureenvironment) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="c3974-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="c3974-207">**İptal** – bir özellik kurulumu için ortamı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3974-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="c3974-208">Kuruluşlar</span><span class="sxs-lookup"><span data-stu-id="c3974-208">Organizations</span></span>

<span data-ttu-id="c3974-209">Bir Genelleştirme özelliğini harici bir kuruluşla paylaşmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c3974-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="c3974-210">**E-faturalama özellikleri** sayfasında, paylaşılacak özelliği ve özellik sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="c3974-211">**Kuruluşlar** sekmesinde **Paylaş**'ı seçin ve açılan iletişim kutusunda kuruluşun etki alanı adını girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="c3974-212">**Paylaş**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-212">Select **Share**.</span></span>

    ![Bir kuruluşla özelliği paylaşma](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="c3974-214">Özellik, seçili kuruluşla paylaşılır ve Genel depodaki bu kuruluş tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="c3974-215">Buradan, özellik kuruluşun RCS örneğine veya Dynamics 365 Finance'e kullanılabilmesi için içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="c3974-216">Türetilmiş Genelleştirme özelliklerini yeniden temellendirme</span><span class="sxs-lookup"><span data-stu-id="c3974-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="c3974-217">Türetilmiş Genelleştirme özelliğini yeni veya güncelleştirilmiş temel özellik sürümüne yeniden temellendirerek oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3974-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="c3974-218">Bu şekilde, temel sürümde gerçekleşen değişiklikler otomatik olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="c3974-219">Güncelleştirilmiş temel özellik sürümü kaynak konfigürasyon sağlayıcısı tarafından oluşturulur ve daha sonra yayımlanır veya paylaşılıyor.</span><span class="sxs-lookup"><span data-stu-id="c3974-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Temel özellik sürümü güncelleştirildi](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="c3974-221">Örneğin, oluşturduğunuz bir özelliğin türetilmiş sürümünü yeniden temellendirmek istiyorsanız, önce genel depodan içe aktararak özelliğin en son sürümünü alırsınız.</span><span class="sxs-lookup"><span data-stu-id="c3974-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="c3974-222">**E-faturalama özellikleri** sayfasında **içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="c3974-223">En son özellikleri almak için **Eşitle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="c3974-224">Özellikler listesinde içe aktarılacak özellikleri seçin ve **içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Bir özelliğin en son sürümünü içe aktarma](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="c3974-226">Özellik listesinde, yeniden temellendirme özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="c3974-227">**Sürüm** sekmesinde, taslak sürümünü oluşturmak için **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Yeni taslak sürümü oluşturuldu](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="c3974-229">**Yeniden temellendirme** seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="c3974-230">**Yeniden temellendirme** iletişim kutusunda, tekrar temellendirgitmek için özelliğin en son sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Yeniden temellendirme iletişim kutusu](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="c3974-232">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-232">Select **OK**.</span></span>
9. <span data-ttu-id="c3974-233">Özellik bileşenlerini gözden geçirin ve gerekli değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="c3974-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="c3974-234">Yeniden temellendirilen özelliği tamamlamak için **durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="c3974-235">Yeniden temellendirme tamamlandığı zaman ek eylemler gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3974-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="c3974-236">Örneğin, özelliği yayımlayabilir ve genelleştirme hizmetlerinde kullanılabilir hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3974-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Özellik durumu tamamlandı olarak güncelleştirildi](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="c3974-238">Genelleştirme özellikleri için ortamları konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="c3974-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="c3974-239">Genelleştirme hizmetlerinin kullanıcıları, bir Genelleştirme özelliği ayarlamak ve erişim izni olacak diğer kullanıcılara yetki vermek için ortamı yönetebilir.</span><span class="sxs-lookup"><span data-stu-id="c3974-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="c3974-240">**Genelleştirme özellikleri** çalışma alanında ve sonra **Ortamlar** altında **e-faturalama** döşemesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Globalizasyon Özellikler çalışma alanı](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="c3974-242">**Anahtar kasa parametrelerini** seçin ve sonra bir Azure anahtar kasa parolası oluşturmak için **yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="c3974-243">Anahtar Kasası için bir ad ve açıklama girin ve sonra **anahtar kasa URI** alanına Azure 'Da anahtar kasa kaynağını tanımlayan URL 'yi girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="c3974-244">**Sertifikalar** hızlı sekmesinde, sertifikayı eklemek için **Ekle**'yi seçin ve her bir sertifika için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Sertifika eklendi](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="c3974-246">Yeni bir ortam oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="c3974-247">Depolama için gereken bir ad, açıklama ve paylaşılan erişim imza belirteci gizli girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="c3974-248">Bu ortama erişim izni olacak kullanıcıyı eklemek için, **kullanıcılar** hızlı sekmesinde, **yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="c3974-249">Kullanıcının Kullanıcı kodunu ve e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="c3974-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="c3974-250">Daha fazla kullanıcı eklemek için 7 - 8 arasındaki adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="c3974-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="c3974-251">Ortamı yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c3974-251">Select **Publish** to publish the environment.</span></span>

    ![Yayımlanan ortam](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]