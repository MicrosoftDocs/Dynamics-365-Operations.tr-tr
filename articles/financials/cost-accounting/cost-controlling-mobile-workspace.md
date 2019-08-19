---
title: Mobil çalışma alanının maliyet denetimi
description: Bu konu, Maliyet denetleme mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, maliyet merkezi yöneticilerinin maliyet merkezi performansı hakkındaki bilgileri her zaman ve her yerde görebilmelerini sağlar.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 82cabe93844cc27ae3c8470e3eecb902a3e5d089
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841645"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="a1d9c-104">Mobil çalışma alanının maliyet denetimi</span><span class="sxs-lookup"><span data-stu-id="a1d9c-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1d9c-105">Bu konu, **Maliyet denetleme** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="a1d9c-106">Bu çalışma alanı, maliyet merkezi yöneticilerinin maliyet merkezi performansı hakkındaki bilgileri her zaman ve her yerde görebilmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="a1d9c-107">Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations Mobile uygulaması ile kullanılmak üzere geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="a1d9c-108">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="a1d9c-108">Overview</span></span>
<span data-ttu-id="a1d9c-109">**Maliyet denetleme** mobil çalışma alanı, maliyet merkezlerinin mevcut performansı hakkında anında bilgiyi, ffili maliyetleri, bütçelendirilmiş maliyete kıyaslayarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="a1d9c-110">Tekil maliyet öğelerinin durumunun detayına inebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="a1d9c-111">Örneğin, bir personel uluslararası bir konferansa davetiye almıştır ancak kuruluşun tüm seyahat masraflarını üstlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="a1d9c-112">Personel, yöneticisi kendi konferansa katılıp katılamayacağını sorar.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="a1d9c-113">Yönetici, personelin konferansa katılması için bütçeye sahip olup olmadığını görmek için mobil cihazında **Maliyet denetimi** mobil çalışma alanını açar.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="a1d9c-114">Veri güvenliği</span><span class="sxs-lookup"><span data-stu-id="a1d9c-114">Data security</span></span>
<span data-ttu-id="a1d9c-115">**Maliyet denetimi** mobil çalışma alanındaki veriler, kullanıcı kimlik bilgileriyle güvenlik altına alınır.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="a1d9c-116">Maliyet merkezi yöneticilerinin yalnızca kendi maliyet merkezleri için verileri görmelerine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="a1d9c-117">Erişim düzeyi güvenliği **Maliyet muhasebesi** modülünde yönetilir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="a1d9c-118">Maliyet muhasebecileri, **Maliyet muhasebesi** modülünde **Maliyet denetimi** mobil çalışma alanının yapılandırmasını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="a1d9c-119">Çalışma alanı mobil uygulamada yayımlandıktan sonra, uygulamada kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="a1d9c-120">Bu sayede, kuruluşunuzdaki tüm maliyet merkezi yöneticilerinin aynı biçimdeki veriyi görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="a1d9c-121">Eylemler, görünümler ve bağlantılar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-121">Actions, views, and links</span></span>
<span data-ttu-id="a1d9c-122">**Maliyet denetleme** mobil çalışma alanı aşağıdaki eylemleri, görünümleri ve bağlantıları sağlar:</span><span class="sxs-lookup"><span data-stu-id="a1d9c-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="a1d9c-123">**Eylemler:**</span><span class="sxs-lookup"><span data-stu-id="a1d9c-123">**Actions:**</span></span>

    -   <span data-ttu-id="a1d9c-124">Düzeni seçmek için **Yapılandırmayı seç**'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="a1d9c-125">**Maliyet nesnesini seç**'i, verinin filtreleneceği maliyet merkezini seçmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="a1d9c-126">Listede görünen maliyet merkezleri, **Maliyet muhasebesi** modülünde verilmiş olan erişime bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="a1d9c-127">**Görünümler:** **Maliyet muhasebesi** modülünün yapılandırmasında seçilen eylemlere dayanarak, kartlarda aşağıdaki bilgileri görüntüleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a1d9c-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="a1d9c-128">Gerçek tutar ile bütçe karşılaştırması (geçerli dönem)</span><span class="sxs-lookup"><span data-stu-id="a1d9c-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="a1d9c-129">Gerçek tutar ile düzeltilmiş bütçe karşılaştırması (geçerli dönem)</span><span class="sxs-lookup"><span data-stu-id="a1d9c-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="a1d9c-130">Fiili - bütçe (önceki dönem) karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="a1d9c-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="a1d9c-131">Fiili - revize edilmiş bütçe (önceki dönem) karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="a1d9c-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="a1d9c-132">Fiili - bütçe (günümüze kadar yıl) karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="a1d9c-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="a1d9c-133">Fiili - revize edilmiş bütçe (günümüze kadar yıl) karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="a1d9c-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="a1d9c-134">Aşağıda tutarlar tüm kartlar üzerinde gösterilir: Fiili, Bütçe, Fark ve Fark %'si.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="a1d9c-135">**Bağlantılar:**</span><span class="sxs-lookup"><span data-stu-id="a1d9c-135">**Links:**</span></span>

    -   <span data-ttu-id="a1d9c-136">Geçerli dönem için ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-136">Details for current period</span></span>
    -   <span data-ttu-id="a1d9c-137">Önceki dönem için ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-137">Details for previous period</span></span>
    -   <span data-ttu-id="a1d9c-138">Yıl başından bu güne için ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-138">Details for year to date</span></span>

    <span data-ttu-id="a1d9c-139">Bir bağlantıyı seçtiğinizde, her bir maliyet öğesi için bir kart gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="a1d9c-140">Her kart için aşağıdaki tutarlar gösterilir: Fiili, Bütçe, Bütçe farkı, Bütçe farkı %'si, Revize edilmiş bütçe, Revize edilmiş farkı ve Revize edilmiş farkı %'si.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="a1d9c-141">[![Bir maliyet öğesi için kart ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="a1d9c-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a1d9c-142">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-142">Prerequisites</span></span>
<span data-ttu-id="a1d9c-143">Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne dayalı olarak farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="a1d9c-144">Microsoft Dynamics 365 for Finance and Operations kullanıyorsanız önkoşullar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="a1d9c-145">Microsoft Dynamics 365 for Finance and Operations kuruluşunuza dağıtıldıysa sistem yöneticisinin **Maliyet kontrolü** mobil çalışma alanını yayımlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-145">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="a1d9c-146">Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="a1d9c-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="a1d9c-147">Microsoft Dynamics 365 for Operations sürüm 1611'i platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar</span><span class="sxs-lookup"><span data-stu-id="a1d9c-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="a1d9c-148">Kuruluşunuza platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a1d9c-149">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="a1d9c-149">Prerequisite</span></span></th>
<th><span data-ttu-id="a1d9c-150">Rol</span><span class="sxs-lookup"><span data-stu-id="a1d9c-150">Role</span></span></th>
<th><span data-ttu-id="a1d9c-151">Açıklama</span><span class="sxs-lookup"><span data-stu-id="a1d9c-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1d9c-152">KB 4013633 uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="a1d9c-153">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="a1d9c-153">System administrator</span></span></td>

<td><span data-ttu-id="a1d9c-154">KB 4013633, <strong>Maliyet denetleme</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="a1d9c-155">KB 4013633 uygulamak için sistem yöneticiniz bu adımları atması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="a1d9c-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="a1d9c-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="a1d9c-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="a1d9c-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1d9c-160"><strong>Maliyet denetleme</strong> mobil çalışma alanını yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="a1d9c-161">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="a1d9c-161">System administrator</span></span></td>
<td><span data-ttu-id="a1d9c-162">Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="a1d9c-163">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="a1d9c-163">Download and install the mobile app</span></span>
<span data-ttu-id="a1d9c-164">Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:</span><span class="sxs-lookup"><span data-stu-id="a1d9c-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="a1d9c-165">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="a1d9c-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="a1d9c-166">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="a1d9c-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="a1d9c-167">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="a1d9c-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="a1d9c-168">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="a1d9c-169">Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="a1d9c-170">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="a1d9c-171">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="a1d9c-172">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="a1d9c-173">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="a1d9c-174">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="a1d9c-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="a1d9c-175">Maliyet merkezinizin performansını Maliyet denetimi mobil çalışma alanını kullanarak görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="a1d9c-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="a1d9c-176">Mobil cihazınızda **Maliyet denetleme** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="a1d9c-177">**Maliyet nesnesi denetleme** seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="a1d9c-178">**Eylemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="a1d9c-179">**Yapılandırma seç**'i seçerek bir maliyet denetleme biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="a1d9c-180">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-180">Select **Done**.</span></span>
6.  <span data-ttu-id="a1d9c-181">**Eylemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="a1d9c-182">**Maliyet nesnesi seç**'i seçerek erişiminizin sağlandığı maliyet merkezlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="a1d9c-183">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-183">Select **Done**.</span></span>
9.  <span data-ttu-id="a1d9c-184">Maliyet merkezinizin toplam performansını görün.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="a1d9c-185">**Geçerli dönem için ayrıntılar** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="a1d9c-186">Bireysel maliyet öğelerinin performansını görün.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="a1d9c-187">Belirli maliyet öğeleri için de arama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a1d9c-187">You can also search for specific cost elements.</span></span>

