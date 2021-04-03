---
title: Mobil uygulama giriş sayfası
description: Bu konu, Finance and Operations (Dynamics 365) Mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar.
author: ChrisGarty
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 925d1fff51317b592a7af61ebd797fa70ab5b6f4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567200"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="6cefb-103">Mobil uygulama giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="6cefb-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cefb-104">Bu konu, **Finance and Operations (Dynamics 365)** mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="6cefb-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="6cefb-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="6cefb-105">Overview</span></span>
--------

<span data-ttu-id="6cefb-106">Mobil uygulama, kuruluşunuzun iş süreçlerinin mobil cihazlarda kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="6cefb-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="6cefb-107">BT yöneticiniz mobil çalışma alanları, kuruluşunuz için etkinleştirdikten sonra, kullanıcılar uygulamaya oturum açabilir ve iş süreçlerini mobil cihazlarından yürütmeye anında başlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="6cefb-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="6cefb-108">Mobil uygulama, verimliliği artıracak aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="6cefb-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="6cefb-109">Kullanıcılar iş verilerini görebilir, düzenleyebilir ve bunlar üzerinde harekete geçebilirler, ağ bağlantıları kesintili olsa bile veya mobil cihazları tümüyle çevrimdışı olduğunda bile.</span><span class="sxs-lookup"><span data-stu-id="6cefb-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="6cefb-110">Bir cihaz, ağ bağlantısını yeniden kurduğunda çevrimdışı veri operasyonları otomatik olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="6cefb-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="6cefb-111">BT yöneticileri veya geliştiricileri, kuruluşunuz için özel hazırlanmış mobil çalışma alanları hazırlayabilir ve bunları yayınlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="6cefb-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="6cefb-112">Uygulama, var olan kod varlıklarınızı kullanır.</span><span class="sxs-lookup"><span data-stu-id="6cefb-112">The app uses your existing code assets.</span></span> <span data-ttu-id="6cefb-113">Bu nedenle, doğrulama yordamlarınızı, iş mantığınızı veya güvenlik yapılandırmanızı yeniden uygulamak zorunda kalmazsınız.</span><span class="sxs-lookup"><span data-stu-id="6cefb-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="6cefb-114">BT yöneticileri veya geliştiricileri, web istemcisi içinde dahil olan işaretle ve tıkla çalışma alanı tasarımcısını kullanarak kolayca tasarlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="6cefb-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="6cefb-115">BT yöneticileri veya geliştiricileri, İş mantığı genişletilebilme çerçevesini kullanarak çalışma alanlarının kabiliyetlerini isteğe bağlı olarak optimize edebilirler.</span><span class="sxs-lookup"><span data-stu-id="6cefb-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="6cefb-116">Cihaz çevrimdışıyken de veri işlenmeye devam ettiği için cihazlarınız sürekli internet bağlantısına sahip olmasa bile mobil senaryolarınız zengin ve akıcı kalır.</span><span class="sxs-lookup"><span data-stu-id="6cefb-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="6cefb-117">Mobil uygulamanın öğeleri</span><span class="sxs-lookup"><span data-stu-id="6cefb-117">Elements of the mobile app</span></span>
<span data-ttu-id="6cefb-118">Mobil uygulamadaki gezinti, dört temel kavramdan oluşur: Pano, çalışma alanları, sayfalar ve eylemler.</span><span class="sxs-lookup"><span data-stu-id="6cefb-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="6cefb-119">[![Mobil uygulamadaki gezinme kavramları](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="6cefb-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="6cefb-120">Uygulamayı başlattığınızda **pano**'ya gidersiniz.</span><span class="sxs-lookup"><span data-stu-id="6cefb-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="6cefb-121">Panoda, yayımlanmış olan **çalışma alanlarının** bir listesini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cefb-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="6cefb-122">Her bir çalışma alanında, o çalışma alanı için kullanılabilen **sayfalar**'ın bir listesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="6cefb-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="6cefb-123">Sayfaya ulaştıktan sonra, bir dizi eylem gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6cefb-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="6cefb-124">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="6cefb-124">Here are some examples:</span></span>

    - <span data-ttu-id="6cefb-125">Ayrıntılı veriyi görüntüle.</span><span class="sxs-lookup"><span data-stu-id="6cefb-125">View detailed data.</span></span>
    - <span data-ttu-id="6cefb-126">ilgili veri için diğer sayfalara gezinebilirsiniz, örneğin varlık ayrıntıları veya satırlar.</span><span class="sxs-lookup"><span data-stu-id="6cefb-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="6cefb-127">O sayfa için kullanılabilir olan **eylemlerin** bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="6cefb-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="6cefb-128">Eylemler veri oluşturmanıza veya mevcut veriyi düzenlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="6cefb-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="6cefb-129">Uygulama işlemi</span><span class="sxs-lookup"><span data-stu-id="6cefb-129">Implementation process</span></span>
<span data-ttu-id="6cefb-130">Aşağıdaki görsel, Microsoft tarafından sağlanan ve özel mobil çalışma alanlarının her ikisinin de uygulama işlemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6cefb-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="6cefb-131">[![Mobil uygulamalar uygulama süreci](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="6cefb-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="6cefb-132">Aşağıdaki tablo, Microsoft ve özel mobil çalışma alanlarından sağlanan her iki mobil çalışma alanını uygulamanıza yardımcı olacak kaynaklara bağlantılar içerir.</span><span class="sxs-lookup"><span data-stu-id="6cefb-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="6cefb-133">İlk sütundaki sayılar, önceki görseldeki numaralandırılmış adımlara karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="6cefb-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cefb-134">Aşama</span><span class="sxs-lookup"><span data-stu-id="6cefb-134">Step</span></span></th>
<th><span data-ttu-id="6cefb-135">Rol</span><span class="sxs-lookup"><span data-stu-id="6cefb-135">Role</span></span></th>
<th><span data-ttu-id="6cefb-136">Eylem</span><span class="sxs-lookup"><span data-stu-id="6cefb-136">Action</span></span></th>
<th><span data-ttu-id="6cefb-137">Eylemi tamamlamanıza yardımcı olacak kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6cefb-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6cefb-138">1</span><span class="sxs-lookup"><span data-stu-id="6cefb-138">1</span></span></td>
<td><span data-ttu-id="6cefb-139">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="6cefb-139">System administrator</span></span></td>
<td><span data-ttu-id="6cefb-140">Finance and Operations uygulamasını kuruluşunuzda uygulayın.</span><span class="sxs-lookup"><span data-stu-id="6cefb-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="6cefb-141">Henüz bir Microsoft Dynamics 365 sürümünü dağıtmadıysanız, bkz. <a href="../deployment/deploy-demo-environment.md">Bir gösteri sürümü dağıtmak</a>.</span><span class="sxs-lookup"><span data-stu-id="6cefb-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="6cefb-142">Kullanılabilir mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.</span><span class="sxs-lookup"><span data-stu-id="6cefb-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cefb-143">2</span><span class="sxs-lookup"><span data-stu-id="6cefb-143">2</span></span></td>
<td><span data-ttu-id="6cefb-144">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="6cefb-144">System administrator</span></span></td>
<td><span data-ttu-id="6cefb-145"><strong>Microsoft Dynamics 365 for Operations sürüm 1611 kullanıyorsanız:</strong> Microsoft tarafından sağlanan mobil çalışma alanlarını etkinleştiren KB'leri indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="6cefb-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="6cefb-146">Daha fazla bilgi için aşağıdaki konulara göz atın:</span><span class="sxs-lookup"><span data-stu-id="6cefb-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="6cefb-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobil çalışma alanlarının maliyet kontrolü</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="6cefb-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Eldeki stok mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="6cefb-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Satış siparişleri mobil çalışma alanları</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="6cefb-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Satıcı iş birliği mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="6cefb-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Proje saati girişi mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="6cefb-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Gider yönetimi mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cefb-153">3</span><span class="sxs-lookup"><span data-stu-id="6cefb-153">3</span></span></td>
<td><span data-ttu-id="6cefb-154">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="6cefb-154">System administrator</span></span></td>
<td><span data-ttu-id="6cefb-155">Microsoft tarafından sağlanan mobil çalışma alanlarını yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="6cefb-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="6cefb-156"><a href="publish-mobile-workspace.md">Bir mobil çalışma alanı yayınlayın</a>
</span><span class="sxs-lookup"><span data-stu-id="6cefb-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cefb-157">4</span><span class="sxs-lookup"><span data-stu-id="6cefb-157">4</span></span></td>
<td><span data-ttu-id="6cefb-158">Geliştirici veya bağımsız yazılım satıcısı (ISV)</span><span class="sxs-lookup"><span data-stu-id="6cefb-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="6cefb-159">Mobil platformu, özel mobil çalışma alanları oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="6cefb-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="6cefb-160"><a href="platform/mobile-platform-home-page.md">Mobil platform</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cefb-161">5</span><span class="sxs-lookup"><span data-stu-id="6cefb-161">5</span></span></td>
<td><span data-ttu-id="6cefb-162">ISV</span><span class="sxs-lookup"><span data-stu-id="6cefb-162">ISV</span></span></td>
<td><span data-ttu-id="6cefb-163">Özel mobil çalışma alanları içeren bir dağıtılabilir paket oluşturun ve paketi Microsoft Dynamics Lifecycle Services'a (LCS) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="6cefb-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="6cefb-164"><a href="../deployment/create-apply-deployable-package.md">Dağıtılabilir paket oluşturma</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cefb-165">6</span><span class="sxs-lookup"><span data-stu-id="6cefb-165">6</span></span></td>
<td><span data-ttu-id="6cefb-166">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="6cefb-166">System administrator</span></span></td>
<td><span data-ttu-id="6cefb-167">Bağımsız yazılım satıcısı (ISV) tarafından sağlanan özel çalışma alanlarını içeren dağıtılabilir paketi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="6cefb-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="6cefb-168"><a href="../deployment/apply-deployable-package-system.md">Dağıtılabilir paket uygulama</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cefb-169">7</span><span class="sxs-lookup"><span data-stu-id="6cefb-169">7</span></span></td>
<td><span data-ttu-id="6cefb-170">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="6cefb-170">System administrator</span></span></td>
<td><span data-ttu-id="6cefb-171">ISV tarafından sağlanan özel mobil çalışma alanlarını yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="6cefb-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="6cefb-172"><a href="publish-mobile-workspace.md">Mobil çalışma alanı yayımlama</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cefb-173">8</span><span class="sxs-lookup"><span data-stu-id="6cefb-173">8</span></span></td>
<td><span data-ttu-id="6cefb-174">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="6cefb-174">User</span></span></td>
<td><span data-ttu-id="6cefb-175">Mobil uygulamayı indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="6cefb-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="6cefb-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Android için Finance and Operations uygulaması</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="6cefb-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">iOS için Finance and Operations uygulaması</a></span><span class="sxs-lookup"><span data-stu-id="6cefb-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="6cefb-178">(Windows Phone desteklenmemektedir)</span><span class="sxs-lookup"><span data-stu-id="6cefb-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cefb-179">9</span><span class="sxs-lookup"><span data-stu-id="6cefb-179">9</span></span></td>
<td><span data-ttu-id="6cefb-180">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="6cefb-180">User</span></span></td>
<td><span data-ttu-id="6cefb-181">Oturum açın ve mobil uygulamayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="6cefb-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="6cefb-182">Uygulama, sistem yöneticisi tarafından yayınlanan mobil çalışma alanlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="6cefb-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="6cefb-183">Microsoft tarafından sağlanan mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.</span><span class="sxs-lookup"><span data-stu-id="6cefb-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="6cefb-184">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="6cefb-184">Troubleshooting</span></span>
[<span data-ttu-id="6cefb-185">Mobil platform kaynakları</span><span class="sxs-lookup"><span data-stu-id="6cefb-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]