---
title: Dynamics 365 Commerce değerlendirme ortamı sağlama
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl sağlanacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e5ce2002c66a1c36d5647d3c76684b394fc1ff79
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599862"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="7af61-103">Dynamics 365 Commerce değerlendirme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="7af61-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7af61-104">Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl sağlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="7af61-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="7af61-105">Başlamadan önce, işlemin gerek duyduğu bir fikir almak için bu konu hakkında hızlı bir tarama yapmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="7af61-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="7af61-106">Commerce değerlendirme ortamları genel olarak kullanıma sunulmamıştır ve iş ortakları ile müşterilere istek üzerine sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7af61-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="7af61-107">Daha fazla bilgi için Microsoft iş ortağı ilgili kişisine ulaşın.</span><span class="sxs-lookup"><span data-stu-id="7af61-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="7af61-108">Özet</span><span class="sxs-lookup"><span data-stu-id="7af61-108">Overview</span></span>

<span data-ttu-id="7af61-109">Commerce değerlendirme ortamını başarıyla sağlamak için, belirli bir ürün adı ve türü olan bir proje oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7af61-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="7af61-110">Ortam ve Commerce Scale Unit'te (CSU), ayrıca, e-Ticaret'i daha sonra sağlamayı düşündüğünüzde kullanmanız gereken belirli parametreler de vardır.</span><span class="sxs-lookup"><span data-stu-id="7af61-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="7af61-111">Bu konudaki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="7af61-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="7af61-112">Sağlama başarılı olduktan sonra, Commerce değerlendirme ortamınızı kullanmak üzere hazırlamak için almanız gereken birkaç son işlem adımı vardır.</span><span class="sxs-lookup"><span data-stu-id="7af61-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="7af61-113">Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7af61-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="7af61-114">İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7af61-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="7af61-115">Commerce değerlendirme ortamını yapılandırma hakkında bilgi için bkz. [Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="7af61-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="7af61-116">Commerce değerlendirme ortamınızla ilgili isteğe bağlı özellikleri yapılandırmak için, bkz. [Commerce değerlendirme ortamınız için isteğe bağlı özellikler yapılandırma](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="7af61-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7af61-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7af61-117">Prerequisites</span></span>

<span data-ttu-id="7af61-118">Commerce değerlendirme ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların yerinde olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="7af61-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="7af61-119">Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var</span><span class="sxs-lookup"><span data-stu-id="7af61-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="7af61-120">Varolan Microsoft Dynamics 365 ortağı veya müşterisiyseniz ve Dynamics 365 Commerce proje oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7af61-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="7af61-121">Microsoft Azure aboneliğinize yönetici erişiminiz var veya gerektiğinde size yardımcı olabilecek bir abonelik Yöneticisi ile temas kuruyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="7af61-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="7af61-122">Azure Active Directory (Azure AD) kiracı kimliğiniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7af61-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="7af61-123">E-ticaret sistem yöneticileri grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="7af61-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="7af61-124">Derecelendirme ve incelemeler grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="7af61-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="7af61-125">(Bu güvenlik grubu e-ticaret Sistem Yöneticisi grubuyla aynı olabilir.)</span><span class="sxs-lookup"><span data-stu-id="7af61-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="7af61-126">Bu listenin kapsamlı olmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7af61-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="7af61-127">Herhangi bir sorunla karşılaşırsanız, yardım için Microsoft iş ortağınıza başvurun.</span><span class="sxs-lookup"><span data-stu-id="7af61-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="7af61-128">Commerce değerlendirme ortamınızı sağlama</span><span class="sxs-lookup"><span data-stu-id="7af61-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="7af61-129">Bu yöntemlerde, bir Commerce değerlendirme ortamının nasıl sağlanacağı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="7af61-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="7af61-130">Bunları başarıyla tamamladıktan sonra, Commerce değerlendirme ortamı yapılandırma için hazır olacak.</span><span class="sxs-lookup"><span data-stu-id="7af61-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="7af61-131">Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="7af61-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="7af61-132">Yeni proje oluştur</span><span class="sxs-lookup"><span data-stu-id="7af61-132">Create a new project</span></span>

<span data-ttu-id="7af61-133">LCS'de bir yeni proje oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="7af61-134">LCS giriş sayfasında, bir proje oluşturmak için artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="7af61-135">Sağ bölmede aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="7af61-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="7af61-136">Bir ortaksanız **taşı, çözüm oluştur ve öğren**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="7af61-137">Müşterisiyseniz, **olası ön satışlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="7af61-138">Şablon adı, açıklama ve sektör girin.</span><span class="sxs-lookup"><span data-stu-id="7af61-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="7af61-139">**Ürün adı** alanından **Dynamics 365 Commerce** seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="7af61-140">**Ürün sürümü** alanından **Dynamics 365 Commerce** seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="7af61-141">**Metodoloji** alanında **Dynamics Retail uygulama metodoloji**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="7af61-142">İsteğe bağlı: Roller ve kullanıcılar mevcut projeden içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7af61-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="7af61-143">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-143">Select **Create**.</span></span> <span data-ttu-id="7af61-144">Proje görünümü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7af61-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="7af61-145">Azure bağlayıcısı ekle</span><span class="sxs-lookup"><span data-stu-id="7af61-145">Add the Azure Connector</span></span>

<span data-ttu-id="7af61-146">LCS projenize Azure Bağlayıcısı eklemek için, [Azure Resource Manager (ARM) ekleme işlemini tamamlama](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="7af61-147">Ortamı dağıtın</span><span class="sxs-lookup"><span data-stu-id="7af61-147">Deploy the environment</span></span>

<span data-ttu-id="7af61-148">Ortamı dağıtmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="7af61-149">Tek bir seçeneği olan sayfalar atlandığından 6., 7. ve/veya 8. adımı tamamlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="7af61-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="7af61-150">**Ortam parametreleri** görünümünde olduğunuzda, **ortam adı** alanının metin **Dynamics 365 Commerce-demo (*xx\* platform güncelleştirmesi 10.0.* x)\*\* ile doğrudan göründüğünü onaylayın.</span><span class="sxs-lookup"><span data-stu-id="7af61-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="7af61-151">Ayrıntılar için, 8. adımdan sonra görünen çizime bakın.</span><span class="sxs-lookup"><span data-stu-id="7af61-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="7af61-152">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="7af61-153">Ortam eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7af61-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="7af61-154">**Uygulama sürümü** alanında, en güncel sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="7af61-155">En güncel sürümden farklı bir uygulama sürümünü seçmeniz için özel bir gereksinim duyuyorsanız, **10.0.8** önceki bir sürümü seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="7af61-156">**Platform sürümü** alanında, seçtiğiniz uygulama sürümü için otomatik olarak seçilen platform sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="7af61-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Uygulamayı ve platform sürümünü seçme](./media/project1.png)

1. <span data-ttu-id="7af61-158">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-158">Select **Next**.</span></span>
1. <span data-ttu-id="7af61-159">Ortam topolojisi olarak **Demo**'yu seçinç</span><span class="sxs-lookup"><span data-stu-id="7af61-159">Select **Demo** as the environment topology.</span></span>

    ![Ortam topolojisini 1 seçme](./media/project2.png)

1. <span data-ttu-id="7af61-161">**Ortam dağıt** sayfasında bir ortam adı girin.</span><span class="sxs-lookup"><span data-stu-id="7af61-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="7af61-162">Gelişmiş ayarları olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="7af61-162">Leave the advanced settings as they are.</span></span>

    ![Ortamı dağıtın sayfası](./media/project4.png)

1. <span data-ttu-id="7af61-164">VM boyutunu gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7af61-164">Adjust the VM size as required.</span></span> <span data-ttu-id="7af61-165">(VM stok tutma birimi \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="7af61-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="7af61-166">Fiyat ve lisans koşullarını gözden geçirin ve kabul ettiğiniz onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="7af61-167">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-167">Select **Next**.</span></span>
1. <span data-ttu-id="7af61-168">Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="7af61-169">**Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="7af61-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="7af61-170">İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor.</span><span class="sxs-lookup"><span data-stu-id="7af61-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="7af61-171">Ortam iş akışlarının tamamlanması biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="7af61-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="7af61-172">Bu nedenle, yaklaşık altı ile dokuz saatten sonra yeniden kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="7af61-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="7af61-173">Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.</span><span class="sxs-lookup"><span data-stu-id="7af61-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="7af61-174">Commerce scale unit (bulut) Başlat</span><span class="sxs-lookup"><span data-stu-id="7af61-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="7af61-175">Bir CSU başlatmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-175">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="7af61-176">**Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="7af61-177">Sağdaki ortam görünümünde **tam ayrıntılar** 'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7af61-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="7af61-178">Ortam ayrıntıları görünümü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7af61-178">The environment details view appears.</span></span>
1. <span data-ttu-id="7af61-179">**Ortam özellikleri** altında, **Yönet**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7af61-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="7af61-180">**Commerce** sekmesinde, **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="7af61-181">CSU başlatma parametreleri görünümü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7af61-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="7af61-182">**Bölge** alanında, ortamı dağıttığınız bölgeyle aynı veya buna yakın bir bölgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="7af61-183">**Sürüm** alanını olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="7af61-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="7af61-184">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="7af61-185">Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="7af61-186">**Ticaret yönetimi** görünümü, **Commerce** sekmesinin seçildiği yerde tekrar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7af61-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="7af61-187">CSU kaynak ayırma işlemi için sıraya alındı.</span><span class="sxs-lookup"><span data-stu-id="7af61-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="7af61-188">Devam etmeden önce, CSU durumlarınız **Başarılı** olur.</span><span class="sxs-lookup"><span data-stu-id="7af61-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="7af61-189">Başlatma yaklaşık iki ile beş saat arasında sürer.</span><span class="sxs-lookup"><span data-stu-id="7af61-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="7af61-190">Ortam ayrıntıları görünümünde **Yönet** bağlantısını bulamazsanız, yardım için Microsoft ilgili kişinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="7af61-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="7af61-191">e-Ticaret başlat</span><span class="sxs-lookup"><span data-stu-id="7af61-191">Initialize e-Commerce</span></span>

<span data-ttu-id="7af61-192">Bir e-Ticaret başlatmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-192">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7af61-193">**E-ticaret** sekmesinde, değerlendirme onayını gözden geçirip **Kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-193">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="7af61-194">**E-ticaret ortamı adı** için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="7af61-194">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="7af61-195">e-Ticaret kurulumunuzu gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7af61-195">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="7af61-196">**Commerce Scale Unit adı** alanında, listesindeki CSU alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-196">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="7af61-197">(Listede yalnızca bir seçenek bulunmalıdır.)</span><span class="sxs-lookup"><span data-stu-id="7af61-197">(The list should have only one option.)</span></span>

    <span data-ttu-id="7af61-198">**E-ticaret coğrafi bölgesi** alanı otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7af61-198">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="7af61-199">Devam etmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-199">Select **Next** to continue.</span></span>
1. <span data-ttu-id="7af61-200">**Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="7af61-200">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="7af61-201">**Sistem yöneticisi için AAD güvenlik grubu** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin ve sonra arama sonuçlarını görmek için büyüteç simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-201">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="7af61-202">Listede doğru güvenlik grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-202">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="7af61-203">**Derecelendirmeler ve inceleme moderatörü için AAD güvenlik grubu** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin ve sonra arama sonuçlarını görmek için büyüteç simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-203">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="7af61-204">Listede doğru güvenlik grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-204">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="7af61-205">**Derecelendirmeler ve gözden geçirme hizmetini etkinleştir** seçeneğini **Evet**'e ayarlanmış olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="7af61-205">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="7af61-206">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7af61-206">Select **Initialize**.</span></span> <span data-ttu-id="7af61-207">**Ticaret yönetimi** görünümü, **e-Commerce** sekmesinin seçildiği yerde tekrar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7af61-207">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="7af61-208">E-ticaret başlatma işlemi başlatıldı.</span><span class="sxs-lookup"><span data-stu-id="7af61-208">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="7af61-209">Devam etmeden önce, e-ticaret başlatma durumunuz **başlatma başarılı** olana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="7af61-209">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="7af61-210">Alt sağdaki **bağlantılar** altında, aşağıdaki bağlantıların URL 'lerini not alın:</span><span class="sxs-lookup"><span data-stu-id="7af61-210">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="7af61-211">**e-ticaret sitesi** – E-ticaret sitenizin köküne olan bağlantı.</span><span class="sxs-lookup"><span data-stu-id="7af61-211">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="7af61-212">**Commerce site oluşturucu** – Site yönetimi aracına bağlantı.</span><span class="sxs-lookup"><span data-stu-id="7af61-212">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7af61-213">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7af61-213">Next steps</span></span>

<span data-ttu-id="7af61-214">Commerce değerlendirme ortamını sağlama ve yapılandırma işlemine devam etmek için bkz. [Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="7af61-214">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7af61-215">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7af61-215">Additional resources</span></span>

[<span data-ttu-id="7af61-216">Dynamics 365 Commerce değerlendirme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="7af61-216">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7af61-217">Dynamics 365 Commerce değerlendirme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7af61-217">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7af61-218">Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7af61-218">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="7af61-219">Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7af61-219">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="7af61-220">Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="7af61-220">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7af61-221">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="7af61-221">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7af61-222">Commerce Scale Unit (bulut)</span><span class="sxs-lookup"><span data-stu-id="7af61-222">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7af61-223">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="7af61-223">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7af61-224">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="7af61-224">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
