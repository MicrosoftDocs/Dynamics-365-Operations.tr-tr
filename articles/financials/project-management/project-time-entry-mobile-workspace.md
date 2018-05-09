---
title: "Proje saati girişi mobil çalışma alanı"
description: "Bu konu, Proje zaman girişi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, kullanıcıların bir projeye karşı mobil cihazlarını kullanarak zaman girmelerini ve kaydetmelerine olanak sağlar."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e671fe6e7c99bfb6d66f3b00560c3b0c404d2343
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="1d040-104">Proje saati girişi mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="1d040-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d040-105">Bu konu, **Proje saati girişi** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1d040-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="1d040-106">Bu çalışma alanı, kullanıcıların bir projeye karşı mobil cihazlarını kullanarak zaman girmelerini ve kaydetmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="1d040-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="1d040-107">Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations mobil uygulaması ile kullanılmak üzere geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1d040-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="1d040-108">Özet</span><span class="sxs-lookup"><span data-stu-id="1d040-108">Overview</span></span>
<span data-ttu-id="1d040-109">Proje kaynakları, günlük işlerinin parçası olarak çoğu zaman tesiste veya seyahattedirler.</span><span class="sxs-lookup"><span data-stu-id="1d040-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="1d040-110">**Proje zaman girişi** mobil çalışma alanı, kullanıcıların projeye karşı faturalanabilir veya faturalanamayan zamanlarını istedikleri mobil cihazdan girmelerine izin verir.</span><span class="sxs-lookup"><span data-stu-id="1d040-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="1d040-111">Bu nedenle, proje kaynakları zaman girişlerini herhangi bir zamanda ve herhangi bir yerde yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="1d040-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="1d040-112">Daha önceden kaydettikleri zaman girişlerini de görebilirler.</span><span class="sxs-lookup"><span data-stu-id="1d040-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="1d040-113">Özellikle **Proje saati girişi** mobil çalışma alanında, kullanıcılar bu görevleri gerçekleştirebilir:</span><span class="sxs-lookup"><span data-stu-id="1d040-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="1d040-114">Seçilen herhangi bir tarih için, belirli bir göreve harcadığınız saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="1d040-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="1d040-115">Zaman girilecek projeyi bulmak için proje adı veya müşteriyi aratın.</span><span class="sxs-lookup"><span data-stu-id="1d040-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="1d040-116">Zaman harcadığınız kategori ve aktiviteyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="1d040-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="1d040-117">Zamanı faturalanabilir veya faturalanamaz olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="1d040-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="1d040-118">İsteğe bağlı olarak dahili veya harici açıklamalar girin.</span><span class="sxs-lookup"><span data-stu-id="1d040-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1d040-119">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="1d040-119">Prerequisites</span></span>
<span data-ttu-id="1d040-120">Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne dayalı olarak farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d040-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="1d040-121">Microsoft Dynamics 365 for Finance and Operations kullanıyorsanız önkoşullar</span><span class="sxs-lookup"><span data-stu-id="1d040-121">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="1d040-122">Microsoft Dynamics 365 for Finance and Operations kuruluşunuza dağıtıldıysa sistem yöneticisinin **Proje süresi girişi** mobil çalışma alanını yayımlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d040-122">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="1d040-123">Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="1d040-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="1d040-124">Microsoft Dynamics 365 for Operations sürüm 1611 platform güncelleştirmesi 3 veya daha sonraki sürüm kullanıyorsanız ön koşullar</span><span class="sxs-lookup"><span data-stu-id="1d040-124">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="1d040-125">Kuruluşunuza platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d040-125">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1d040-126">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="1d040-126">Prerequisite</span></span></th>
<th><span data-ttu-id="1d040-127">Rol</span><span class="sxs-lookup"><span data-stu-id="1d040-127">Role</span></span></th>
<th><span data-ttu-id="1d040-128">Açıklama</span><span class="sxs-lookup"><span data-stu-id="1d040-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="1d040-129">KB 4018050 uygulayın.</span><span class="sxs-lookup"><span data-stu-id="1d040-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="1d040-130">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="1d040-130">System administrator</span></span></td>
<td><span data-ttu-id="1d040-131">KB 4018050, <strong>Proje zaman girişi</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="1d040-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="1d040-132">KB 4018050 uygulamak için sistem yöneticiniz bu adımları atması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d040-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="1d040-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</span><span class="sxs-lookup"><span data-stu-id="1d040-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="1d040-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</span><span class="sxs-lookup"><span data-stu-id="1d040-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="1d040-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Dağıtılabilir bir paket oluşturun</a> <strong>ApplicationSuite</strong> ve <strong>ProjectMobile</strong> modellerini içeren ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</span><span class="sxs-lookup"><span data-stu-id="1d040-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="1d040-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</span><span class="sxs-lookup"><span data-stu-id="1d040-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1d040-137"><strong>Proje saati girişi</strong> mobil çalışma alanını yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="1d040-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="1d040-138">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="1d040-138">System administrator</span></span></td>
<td><span data-ttu-id="1d040-139">Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="1d040-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="1d040-140">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="1d040-140">Download and install the mobile app</span></span>

<span data-ttu-id="1d040-141">Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:</span><span class="sxs-lookup"><span data-stu-id="1d040-141">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="1d040-142">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="1d040-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="1d040-143">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="1d040-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="1d040-144">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="1d040-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="1d040-145">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="1d040-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="1d040-146">Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="1d040-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="1d040-147">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="1d040-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="1d040-148">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="1d040-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="1d040-149">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1d040-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="1d040-150">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1d040-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="1d040-151">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="1d040-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="1d040-152">Proje zaman girişi mobil çalışma alanını kullanarak zamanı girin</span><span class="sxs-lookup"><span data-stu-id="1d040-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="1d040-153">Mobil cihazınızda **Proje zaman girişi** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="1d040-154">**Zaman girişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-154">Select **Time entry**.</span></span> <span data-ttu-id="1d040-155">Geçerli hafta için takvim tarihleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1d040-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="1d040-156">Seçilen bir tarih için **Eylemler** &gt; **Yeni giriş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="1d040-157">Kaydedilecek saatlerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="1d040-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="1d040-158">Zaman girişi için projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-158">Select the project for the time entry.</span></span> <span data-ttu-id="1d040-159">Bir liste çevrimdışı kullanım için uygulamanıza yüklenmiş projeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d040-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="1d040-160">Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1d040-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="1d040-161">Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="1d040-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="1d040-162">Projeniz listede yoksa, **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="1d040-163">Adına göre arama yapın veya proje adı veya müşteriye göre aramaya geçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="1d040-164">Bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-164">Select a category.</span></span> <span data-ttu-id="1d040-165">Bir liste çevrimdışı kullanım için uygulamanıza yüklenmiş kategorileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d040-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="1d040-166">Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1d040-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="1d040-167">Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="1d040-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="1d040-168">Kategoriniz listede yoksa, **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="1d040-169">Kategoriye göre arama yapın veya kategori adına göre aramaya geçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="1d040-170">Bir faaliyet seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-170">Select an activity.</span></span> <span data-ttu-id="1d040-171">Bir liste çevrimdışı kullanım için uygulamanıza yüklenmiş faaliyetleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d040-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="1d040-172">Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1d040-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="1d040-173">Daha fazla bilgi için bkz. [Mobil platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="1d040-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="1d040-174">Faaliyetiniz listede yoksa, **Ara**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="1d040-175">Bir etkinlik numarasıyla arama yapın veya amaca göre aramaya geçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="1d040-176">Satır özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-176">Select the line property.</span></span>
12. <span data-ttu-id="1d040-177">İsteğe bağlı: Dahili ve harici açıklamalar girin.</span><span class="sxs-lookup"><span data-stu-id="1d040-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="1d040-178">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d040-178">Select **Done**.</span></span>

