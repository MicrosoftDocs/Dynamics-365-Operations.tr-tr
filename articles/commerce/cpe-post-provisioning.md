---
title: Commerce önizleme ortamı yapılandırma
description: Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f19d03f3f2f5a9f6f7ba08b682277e4e3b764d10
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906151"
---
# <a name="configure-a-commerce-preview-environment"></a><span data-ttu-id="d6757-103">Commerce önizleme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d6757-103">Configure a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d6757-104">Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d6757-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="d6757-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="d6757-105">Overview</span></span>

<span data-ttu-id="d6757-106">Bu konudaki yordamları yalnızca Commerce Preview ortamınızı sağlandıktan sonra tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d6757-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="d6757-107">Commerce önizleme ortamını sağlamak hakkında bilgi için bkz. [Commerce önizleme ortamı sağlama](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="d6757-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="d6757-108">Commerce Preview ortamınız sona kadar sağlanmış olduktan sonra, ortamı değerlendirmeye başlamadan önce ek sağlama sonrası konfigürasyon adımlarının tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d6757-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="d6757-109">Bu adımları tamamlamak için, Microsoft Dynamics Lifecycle Services'i (LCS), Dynamics 365 Commerce ve Dynamics 365 Retail öğesini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d6757-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="d6757-110">Başlamadan önce</span><span class="sxs-lookup"><span data-stu-id="d6757-110">Before you start</span></span>

1. <span data-ttu-id="d6757-111">[LCS portalda](https://lcs.dynamics.com) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="d6757-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="d6757-112">Projenize gidin.</span><span class="sxs-lookup"><span data-stu-id="d6757-112">Go to your project.</span></span>
1. <span data-ttu-id="d6757-113">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d6757-114">Listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="d6757-115">Sağdaki ortam bilgilerinde **tam ayrıntılar** 'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d6757-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="d6757-116">**Oturum aç**'ı tıklatın bir menü açmak için **ortamda oturum aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="d6757-117">Sağ üst köşede **USRT** hukuk varlığının seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="d6757-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="d6757-118">LCS'de satış noktasını konfigüre et</span><span class="sxs-lookup"><span data-stu-id="d6757-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="d6757-119">Çalışanı kimlikle ilişkilendir</span><span class="sxs-lookup"><span data-stu-id="d6757-119">Associate a worker with your identity</span></span>

<span data-ttu-id="d6757-120">Bir çalışanı LCS ile sizin kimlik ile ilişkilendirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6757-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="d6757-121">Soldaki menüyü kullanarak, **Modüller \> perakende \> çalışanlar \> İşçiler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d6757-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="d6757-122">Listede, **000713 - Andrew Collette** kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="d6757-123">Eylem Bölmesinde, **Perakende**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="d6757-124">**Var olan kimliği ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="d6757-125">**E-posta** alanında (**E-posta kullanarak arama**'nın sağındaki) e-posta adresinizi yazın.</span><span class="sxs-lookup"><span data-stu-id="d6757-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="d6757-126">**Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-126">Select **Search**.</span></span>
1. <span data-ttu-id="d6757-127">Adınızı taşıyan kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="d6757-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-128">Select **OK**.</span></span>
1. <span data-ttu-id="d6757-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="d6757-130">Bulut POS'u etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="d6757-130">Activate Cloud POS</span></span>

<span data-ttu-id="d6757-131">LCS içindeki POS'u etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6757-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="d6757-132">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d6757-133">Listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="d6757-134">Sağdaki ortam bilgilerinde **tam ayrıntılar** 'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d6757-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="d6757-135">Bir menüyü açmak için **oturum aç**'ı seçin ve sonra satış noktasını açmak için **bulut satış noktasında oturum aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="d6757-136">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-136">Select **Next**.</span></span>
1. <span data-ttu-id="d6757-137">Microsoft Azure Active Directory (Azure AD) hesabınızı kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="d6757-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="d6757-138">**Mağaza adı** altında, **San Francisco**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="d6757-139">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-139">Select **Next**.</span></span>
1. <span data-ttu-id="d6757-140">**Kayıt ve aygıt** altında, **SANFRAN-1** seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="d6757-141">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-141">Select **Activate**.</span></span> <span data-ttu-id="d6757-142">Oturumunuz kapalı ve POS oturum açma sayfasına götürülüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="d6757-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="d6757-143">Şimdi operatör Kodu **000713** ve parola **123** kullanarak Cloud POS deneyimlerinde oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d6757-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="d6757-144">Commerce'te sitenizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="d6757-144">Set up your site in Commerce</span></span>

<span data-ttu-id="d6757-145">Commerce'te önizleme sitenizi ayarlamaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6757-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d6757-146">Sağlama sırasında e-ticareti başlattığınızda oluşan bir not oluşturduğunuz URL'yi kullanarak Commerce site yönetimi aracında oturum açın (bkz. [e-Ticareti başlat](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="d6757-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="d6757-147">Site kurulum iletişim kutusunu açmak için **Fabrikam** sitesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6757-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="d6757-148">E-ticaret'i başlattığınızda girdiğiniz etki alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="d6757-149">Varsayılan kanal için **Fabrikam genişletilmiş çevrimiçi mağaza**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="d6757-150">(**Genişletilmiş** çevrimiçi mağazayı seçtiğinizden emin olun)</span><span class="sxs-lookup"><span data-stu-id="d6757-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="d6757-151">Varsayılan dil için **tr-tr** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d6757-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="d6757-152">**Yol** alanının değerini olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="d6757-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="d6757-153">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-153">Select **OK**.</span></span> <span data-ttu-id="d6757-154">Sitedeki Sayfalar listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d6757-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="d6757-155">Perakendede işleri etkinleştir</span><span class="sxs-lookup"><span data-stu-id="d6757-155">Enable jobs in Retail</span></span>

<span data-ttu-id="d6757-156">Perakendede işleri etkinleştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="d6757-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="d6757-157">Ortama oturum açın (HQ).</span><span class="sxs-lookup"><span data-stu-id="d6757-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="d6757-158">Soldaki menüyü kullanarak **perakende \> Sorgulamalar ve raporlar \> toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d6757-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="d6757-159">Bu yordamın geri kalan adımlarının aşağıdaki işlerin her biri için tamamlanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="d6757-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="d6757-160">Perakende siparişi e-posta bildirimini işle</span><span class="sxs-lookup"><span data-stu-id="d6757-160">Process retail order email notification</span></span>
    * <span data-ttu-id="d6757-161">Ürün bulunabilirliği</span><span class="sxs-lookup"><span data-stu-id="d6757-161">Product availability</span></span>
    * <span data-ttu-id="d6757-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="d6757-162">P-0001</span></span>
    * <span data-ttu-id="d6757-163">Sipariş işlerini eşitle</span><span class="sxs-lookup"><span data-stu-id="d6757-163">Synchronize orders job</span></span>

1. <span data-ttu-id="d6757-164">Yukarıdaki adı kullanarak işi aramak için hızlı filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6757-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="d6757-165">İşin durumu **stopaj** ise, aşağıdaki adımları gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="d6757-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="d6757-166">Etkin kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-166">Select the record.</span></span>
    1. <span data-ttu-id="d6757-167">Eylem Bölmesi'nde **Toplu iş**'te **Durumu değiştir**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d6757-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="d6757-168">**Bekliyor**'u seçin ve sonra **Tamam**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="d6757-169">Tam veri eşitlemesini perakende olarak çalıştır</span><span class="sxs-lookup"><span data-stu-id="d6757-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="d6757-170">Tam veri eşitlemesini perakende olarak çalıştırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d6757-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="d6757-171">Soldaki menüyü kullanarak, **Modüller \> Perakende \> Genel merkez ayarı \> Perakende planlayıcısı \> Kanal veritabanı** gidin.</span><span class="sxs-lookup"><span data-stu-id="d6757-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="d6757-172">**Varsayılan** kanal, soldaki listeden seçilir.</span><span class="sxs-lookup"><span data-stu-id="d6757-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="d6757-173">Diğer kullanılabilir kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-173">Select the other available channel.</span></span> <span data-ttu-id="d6757-174">Bu kanala, **scXXXXXXXXX** adı verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d6757-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="d6757-175">Eylem bölmesinde **tam veri eşitleme**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d6757-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="d6757-176">Dağıtım planı olarak **9999**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="d6757-177">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-177">Select **OK**.</span></span>
1. <span data-ttu-id="d6757-178">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d6757-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="d6757-179">Test satın almaları gerçekleştirmek için kredi kartı bilgilerini sına</span><span class="sxs-lookup"><span data-stu-id="d6757-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="d6757-180">Sitede test hareketleri gerçekleştirmek için, aşağıdaki test kredi kartı bilgilerini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d6757-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="d6757-181">**Kart numarası:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="d6757-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="d6757-182">**Son kullanma tarihi:** 10/20</span><span class="sxs-lookup"><span data-stu-id="d6757-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="d6757-183">**Kart doğrulama değeri (CVV) kod:** 737</span><span class="sxs-lookup"><span data-stu-id="d6757-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6757-184">Herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!</span><span class="sxs-lookup"><span data-stu-id="d6757-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d6757-185">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="d6757-185">Next steps</span></span>

<span data-ttu-id="d6757-186">Sağlama ve yapılandırma adımları tamamlandıktan sonra, önizleme ortamınızı değerlendirmeye hazırsınız demektir.</span><span class="sxs-lookup"><span data-stu-id="d6757-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="d6757-187">Geliştirme deneyimine gitmek için Commerce site Management aracının URL 'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6757-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="d6757-188">Perakende müşteri sitesi deneyimine gitmek için Commerce sitesi URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d6757-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="d6757-189">Commerce Preview ortamınızla ilgili isteğe bağlı özellikleri konfigüre etmek için, bkz. [Commerce önizleme ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="d6757-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6757-190">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d6757-190">Additional resources</span></span>

[<span data-ttu-id="d6757-191">Ticaret önizleme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="d6757-191">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d6757-192">Ticaret önizleme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="d6757-192">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="d6757-193">Bir Commerce Preview ortamı için isteğe bağlı özellikleri konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="d6757-193">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d6757-194">Ticaret önizleme ortamı SSS</span><span class="sxs-lookup"><span data-stu-id="d6757-194">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d6757-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d6757-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d6757-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="d6757-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d6757-197">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="d6757-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d6757-198">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="d6757-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="d6757-199">Dynamics 365 Retail için yardım kaynakları</span><span class="sxs-lookup"><span data-stu-id="d6757-199">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
