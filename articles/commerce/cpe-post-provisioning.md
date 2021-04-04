---
title: Dynamics 365 Commerce değerlendirme ortamı yapılandırma
description: Bu konu, sağlandıktan sonra Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9b11ab600bb2aa17cf330947304f5b22dd522081
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477985"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="b1872-103">Dynamics 365 Commerce değerlendirme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b1872-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1872-104">Bu konu, sağlandıktan sonra Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b1872-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="b1872-105">Bu konudaki yordamları yalnızca Commerce değerlendirme ortamınızı sağlandıktan sonra tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b1872-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="b1872-106">Commerce değerlendirme ortamını sağlamak hakkında bilgi için bkz. [Commerce değerlendirme ortamı sağlama](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="b1872-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="b1872-107">Commerce değerlendirme ortamınız sona kadar sağlanmış olduktan sonra, ortamı değerlendirmeye başlamadan önce ek sağlama sonrası yapılandırma adımlarının tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b1872-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="b1872-108">Bu adımları tamamlamak için, Microsoft Dynamics Lifecycle Services'i (LCS) ve Dynamics 365 Commerce öğesini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="b1872-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="b1872-109">Başlamadan önce</span><span class="sxs-lookup"><span data-stu-id="b1872-109">Before you start</span></span>

1. <span data-ttu-id="b1872-110">[LCS portalda](https://lcs.dynamics.com) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b1872-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="b1872-111">Projenize gidin.</span><span class="sxs-lookup"><span data-stu-id="b1872-111">Go to your project.</span></span>
1. <span data-ttu-id="b1872-112">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b1872-113">Listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="b1872-114">Sağdaki ortam bilgilerinde **Ortamda oturum aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1872-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="b1872-115">Commerce Headquarters'a gönderilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1872-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="b1872-116">Sağ üst köşede **USRT** hukuk varlığının seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b1872-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="b1872-117">Commerce Headquarters'daki sağlama sonrası etkinlikler sırasında, **USRT** yasal varlığının her zaman seçili olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b1872-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="b1872-118">Satış noktası yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b1872-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="b1872-119">Çalışanı kimlikle ilişkilendir</span><span class="sxs-lookup"><span data-stu-id="b1872-119">Associate a worker with your identity</span></span>

<span data-ttu-id="b1872-120">Bir çalışanı kimliğinizle ilişkilendirmek için, Commerce Headquarters'daki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1872-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="b1872-121">Soldaki menüyü kullanarak, **Modüller \> perakende ve ticaret \> çalışanlar \> İşçiler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b1872-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="b1872-122">Listede, **000713 - Andrew Collette** kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="b1872-123">Eylem Bölmesinde **Commerce** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="b1872-124">**Var olan kimliği ilişkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="b1872-125">**E-posta** alanında (**E-posta kullanarak arama**'nın sağındaki) e-posta adresinizi yazın.</span><span class="sxs-lookup"><span data-stu-id="b1872-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="b1872-126">**Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-126">Select **Search**.</span></span>
1. <span data-ttu-id="b1872-127">Adınızı taşıyan kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="b1872-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-128">Select **OK**.</span></span>
1. <span data-ttu-id="b1872-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="b1872-130">Bulut POS'u etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b1872-130">Activate Cloud POS</span></span>

<span data-ttu-id="b1872-131">Bulut POS'u etkinleştirmek için LCS'deki şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1872-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="b1872-132">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b1872-133">Listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="b1872-134">Sağdaki ortam bilgilerinde **Bulut Satış Noktasında oturum aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="b1872-135">**Başlamadan önce** iletişim kutusunu açmak için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="b1872-136">**Sunucu URL'si** alanını olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="b1872-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="b1872-137">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-137">Select **Next**.</span></span>
1. <span data-ttu-id="b1872-138">Microsoft Azure Active Directory (Azure AD) hesabınızı kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b1872-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="b1872-139">**Mağaza adı** altında, **San Francisco**'yu ve ardından **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="b1872-140">**Kayıt ve aygıt** altında, **SANFRAN-1** seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="b1872-141">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-141">Select **Activate**.</span></span> <span data-ttu-id="b1872-142">Oturumunuz kapalı ve POS oturum açma sayfasına götürülüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b1872-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="b1872-143">Şimdi operatör Kodu **000713** ve parola **123** kullanarak Cloud POS deneyimlerinde oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1872-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="b1872-144">Commerce'te sitenizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="b1872-144">Set up your site in Commerce</span></span>

<span data-ttu-id="b1872-145">Commerce'te değerlendirme sitenizi ayarlamaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1872-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b1872-146">Sağlama sırasında e-Ticareti başlattığınız zaman not ettiğiniz URL'yi kullanarak site oluşturucu aracında oturum açın (bkz. [e-Ticareti başlatma](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="b1872-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="b1872-147">Site kurulum iletişim kutusunu açmak için **Fabrikam** sitesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1872-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="b1872-148">E-ticaret'i başlattığınızda girdiğiniz etki alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="b1872-149">Varsayılan kanal için **Fabrikam genişletilmiş çevrimiçi mağaza**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="b1872-150">(**Genişletilmiş** çevrimiçi mağazayı seçtiğinizden emin olun)</span><span class="sxs-lookup"><span data-stu-id="b1872-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="b1872-151">Varsayılan dil için **tr-tr** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b1872-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="b1872-152">**Yol** alanının değerini olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="b1872-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="b1872-153">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-153">Select **OK**.</span></span> <span data-ttu-id="b1872-154">Sitedeki Sayfalar listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b1872-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="b1872-155">İşleri etkinleştir</span><span class="sxs-lookup"><span data-stu-id="b1872-155">Enable jobs</span></span>

<span data-ttu-id="b1872-156">Commerce'de işleri etkinleştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b1872-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b1872-157">Ortama oturum açın (HQ).</span><span class="sxs-lookup"><span data-stu-id="b1872-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="b1872-158">Soldaki menüyü kullanarak **perakende ve ticaret \> Sorgulamalar ve raporlar \> toplu işler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b1872-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="b1872-159">Bu yordamın geri kalan adımlarının aşağıdaki işlerin her biri için tamamlanması gerekir:</span><span class="sxs-lookup"><span data-stu-id="b1872-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="b1872-160">Perakende siparişi e-posta bildirimini işle</span><span class="sxs-lookup"><span data-stu-id="b1872-160">Process retail order email notification</span></span>
    * <span data-ttu-id="b1872-161">Ürün bulunabilirliği</span><span class="sxs-lookup"><span data-stu-id="b1872-161">Product availability</span></span>
    * <span data-ttu-id="b1872-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="b1872-162">P-0001</span></span>
    * <span data-ttu-id="b1872-163">Sipariş işlerini eşitle</span><span class="sxs-lookup"><span data-stu-id="b1872-163">Synchronize orders job</span></span>

1. <span data-ttu-id="b1872-164">Yukarıdaki adı kullanarak işi aramak için hızlı filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1872-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="b1872-165">İşin durumu **Yürütülüyor** ise, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b1872-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="b1872-166">Etkin kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-166">Select the record.</span></span>
    1. <span data-ttu-id="b1872-167">Eylem Bölmesi'nde **Toplu iş**'te **Durumu değiştir**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1872-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="b1872-168">**İptal ediliyor**'u ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="b1872-169">İsteğe bağlı olarak, yineleme aralığını aşağıdaki işler için bir (1) dakikaya ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b1872-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="b1872-170">Perakende siparişi e-posta bildirimini işleme işi</span><span class="sxs-lookup"><span data-stu-id="b1872-170">Process retail order email notification job</span></span>
* <span data-ttu-id="b1872-171">P-0001 iş</span><span class="sxs-lookup"><span data-stu-id="b1872-171">P-0001 job</span></span>
* <span data-ttu-id="b1872-172">Sipariş işlerini eşitle</span><span class="sxs-lookup"><span data-stu-id="b1872-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="b1872-173">Tam veri eşitlemeyi çalıştır</span><span class="sxs-lookup"><span data-stu-id="b1872-173">Run full data synchronization</span></span>

<span data-ttu-id="b1872-174">Commerce'de tam veri eşitlemesini çalıştırmak için Commerce Headquarters'da aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1872-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="b1872-175">Soldaki menüyü kullanarak, **Modüller \> Perakende ve ticaret \> Genel merkez ayarı \> Ticaret planlayıcısı \> Kanal veritabanı** gidin.</span><span class="sxs-lookup"><span data-stu-id="b1872-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="b1872-176">**scXXXXXXXXX** adlı kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="b1872-177">Eylem bölmesinde **tam veri eşitleme**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b1872-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="b1872-178">Dağıtım planı olarak **9999**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="b1872-179">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-179">Select **OK**.</span></span>
1. <span data-ttu-id="b1872-180">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1872-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="b1872-181">Test satın almaları gerçekleştirmek için kredi kartı bilgilerini sına</span><span class="sxs-lookup"><span data-stu-id="b1872-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="b1872-182">Sitede test hareketleri gerçekleştirmek için, aşağıdaki test kredi kartı bilgilerini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b1872-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="b1872-183">**Kart numarası:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="b1872-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="b1872-184">**Son kullanma tarihi:** 10/20</span><span class="sxs-lookup"><span data-stu-id="b1872-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="b1872-185">**Kart doğrulama değeri (CVV) kod:** 737</span><span class="sxs-lookup"><span data-stu-id="b1872-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1872-186">Herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!</span><span class="sxs-lookup"><span data-stu-id="b1872-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b1872-187">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="b1872-187">Next steps</span></span>

<span data-ttu-id="b1872-188">Sağlama ve yapılandırma adımları tamamlandıktan sonra, değerlendirme ortamınızı kullanmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1872-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="b1872-189">Yazma deneyimine gitmek için Commerce site oluşturucu URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1872-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="b1872-190">Perakende müşteri site deneyimine gitmek için Commerce sitesi URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1872-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="b1872-191">Commerce değerlendirme ortamınızla ilgili isteğe bağlı özellikleri yapılandırmak için bkz. [Commerce değerlendirme ortamınız için isteğe bağlı özellikler yapılandırma](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="b1872-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1872-192">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b1872-192">Additional resources</span></span>

[<span data-ttu-id="b1872-193">Dynamics 365 Commerce değerlendirme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="b1872-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b1872-194">Dynamics 365 Commerce değerlendirme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="b1872-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b1872-195">Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b1872-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b1872-196">Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b1872-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="b1872-197">Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="b1872-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b1872-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b1872-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b1872-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b1872-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b1872-200">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="b1872-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b1872-201">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="b1872-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
