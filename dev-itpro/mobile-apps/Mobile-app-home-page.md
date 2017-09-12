---
title: "Mobil uygulama giriş sayfası"
description: "Bu konu, Microsoft Dynamics 365 for Unified Operations mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46a77f2757bee9f688d8c0d23f15cd7eb27ebcb3
ms.contentlocale: tr-tr
ms.lasthandoff: 08/04/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="fd4ea-103">Mobil uygulama giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="fd4ea-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fd4ea-104">Bu konu, Microsoft Dynamics 365 for Unified Operations mobil uygulamasını açıklar ve kuruluşunuz içerisinde uygulamanıza yardımcı olacak kaynaklara bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="fd4ea-105">Mobil uygulamanın adı daha önce *Microsoft Dynamics 365 for Finance and Operations* idi.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="fd4ea-106">Özet</span><span class="sxs-lookup"><span data-stu-id="fd4ea-106">Overview</span></span>
--------

<span data-ttu-id="fd4ea-107">Mobil uygulama, kuruluşunuzun iş süreçlerinin mobil cihazlarda kullanılabilir olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="fd4ea-108">BT yöneticiniz mobil çalışma alanları, kuruluşunuz için etkinleştirdikten sonra, kullanıcılar uygulamaya oturum açabilir ve iş süreçlerini mobil cihazlarından yürütmeye anında başlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="fd4ea-109">Mobil uygulama, verimliliği artıracak aşağıdaki özellikleri içerir:</span><span class="sxs-lookup"><span data-stu-id="fd4ea-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="fd4ea-110">Kullanıcılar iş verilerini görebilir, düzenleyebilir ve bunlar üzerinde harekete geçebilirler, ağ bağlantıları kesintili olsa bile veya mobil cihazları tümüyle çevrimdışı olduğunda bile.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="fd4ea-111">Bir cihaz ağ bağlantısını tekrar kurduktan sonra, çevrimdışı veri işlemleri, Dynamics 365 for Finance and Operations, Enterprise edition veya Microsoft Dynamics 365 for Finance and Operations ile otomatik eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="fd4ea-112">BT yöneticileri veya geliştiricileri, kuruluşunuz için özel hazırlanmış mobil çalışma alanları hazırlayabilir ve bunları yayınlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="fd4ea-113">Uygulama, varolan kod varlıklarınızı kullanır.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-113">The app uses your existing code assets.</span></span> <span data-ttu-id="fd4ea-114">Bu nedenle, doğrulama yordamlarınızı, iş mantığınızı veya güvenlik yapılandırmanızı yeniden uygulamak zorunda kalmazsınız.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="fd4ea-115">BT yöneticileri veya geliştiricileri, web istemcisi içinde dahil olan işaretle ve tıkla çalışma alanı tasarımcısını kullanarak kolayca tasarlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="fd4ea-116">BT yöneticileri veya geliştiricileri, İş mantığı genişletilebilme çerçevesini kullanarak çalışma alanlarının kabiliyetlerini isteğe bağlı olarak optimize edebilirler.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="fd4ea-117">Cihaz çevrimdışıyken de veri işlenmeye devam ettiği için cihazlarınız sürekli internet bağlantısına sahip olmasa bile mobil senaryolarınız zengin ve akıcı kalır.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="fd4ea-118">Mobil uygulamanın öğeleri</span><span class="sxs-lookup"><span data-stu-id="fd4ea-118">Elements of the mobile app</span></span>
<span data-ttu-id="fd4ea-119">Mobil uygulamadaki gezinti, dört temel kavramdan oluşur: Pano, çalışma alanları, sayfalar ve eylemler.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="fd4ea-120">[![Mobil uygulamadaki gezinme kavramları](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="fd4ea-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="fd4ea-121">Uygulamayı başlattığınızda **pano**'ya gidersiniz.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="fd4ea-122">Panoda, yayımlanmış olan **çalışma alanlarının** bir listesini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="fd4ea-123">Her bir çalışma alanında, o çalışma alanı için kullanılabilen **sayfalar**'ın bir listesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="fd4ea-124">Sayfaya ulaştıktan sonra, bir dizi eylem gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="fd4ea-125">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="fd4ea-125">Here are some examples:</span></span>

    - <span data-ttu-id="fd4ea-126">Ayrıntılı veriyi görüntüle.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-126">View detailed data.</span></span>
    - <span data-ttu-id="fd4ea-127">ilgili veri için diğer sayfalara gezinebilirsiniz, örneğin varlık ayrıntıları veya satırlar.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="fd4ea-128">O sayfa için kullanılabilir olan **eylemlerin** bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="fd4ea-129">Eylemler veri oluşturmanıza veya mevcut veriyi düzenlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="fd4ea-130">Uygulama işlemi</span><span class="sxs-lookup"><span data-stu-id="fd4ea-130">Implementation process</span></span>
<span data-ttu-id="fd4ea-131">Aşağıdaki görsel, Microsoft tarafından sağlanan ve özel mobil çalışma alanlarının her ikisinin de uygulama işlemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Mobil uygulamalar uygulama süreci](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="fd4ea-133">Aşağıdaki tablo, Microsoft ve özel mobil çalışma alanlarından sağlanan her iki mobil çalışma alanını uygulamanıza yardımcı olacak kaynaklara bağlantılar içerir.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="fd4ea-134">İlk sütundaki sayılar, önceki görseldeki numaralandırılmış adımlara karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd4ea-135">Aşama</span><span class="sxs-lookup"><span data-stu-id="fd4ea-135">Step</span></span></th>
<th><span data-ttu-id="fd4ea-136">Rol</span><span class="sxs-lookup"><span data-stu-id="fd4ea-136">Role</span></span></th>
<th><span data-ttu-id="fd4ea-137">Eylem</span><span class="sxs-lookup"><span data-stu-id="fd4ea-137">Action</span></span></th>
<th><span data-ttu-id="fd4ea-138">Eylemi tamamlamanıza yardımcı olacak kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fd4ea-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd4ea-139">1</span><span class="sxs-lookup"><span data-stu-id="fd4ea-139">1</span></span></td>
<td><span data-ttu-id="fd4ea-140">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="fd4ea-140">System administrator</span></span></td>
<td><span data-ttu-id="fd4ea-141">Kuruluşunuzda Finance and Operations veya Finance and Operations'ı uygulayın.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="fd4ea-142">Henüz bir Microsoft Dynamics 365 sürümünü dağıtmadıysanız, bkz. <a href="../deployment/deploy-demo-environment.md">Bir gösteri sürümü dağıtmak</a>.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="fd4ea-143">Kullanılabilir mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd4ea-144">2</span><span class="sxs-lookup"><span data-stu-id="fd4ea-144">2</span></span></td>
<td><span data-ttu-id="fd4ea-145">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="fd4ea-145">System administrator</span></span></td>
<td><span data-ttu-id="fd4ea-146"><strong>Microsoft Dynamics 365 for Finance and Operations sürüm 1611 kullanıyorsanız:</strong> Microsoft tarafından sağlanan mobil çalışma alanlarını etkinleştiren KB'leri indir ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="fd4ea-147">Daha fazla bilgi için aşağıdaki konulara göz atın:</span><span class="sxs-lookup"><span data-stu-id="fd4ea-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="fd4ea-148"><a href="/dynamics365/unified-operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobil çalışma alanlarının maliyet kontrolü</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-148"><a href="/dynamics365/unified-operations/financials/cost-accounting/cost-controlling-mobile-workspace">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="fd4ea-149"><a href="/dynamics365/unified-operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Eldeki stok mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-149"><a href="/dynamics365/unified-operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="fd4ea-150"><a href="/dynamics365/unified-operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Satış siparişleri mobil çalışma alanları</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-150"><a href="/dynamics365/unified-operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="fd4ea-151"><a href="/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Satıcı işbirliği mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-151"><a href="/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="fd4ea-152"><a href="/dynamics365/unified-operations/financials/project-management/project-time-entry-mobile-workspace">Proje saati girişi mobil çalışma alanı</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-152"><a href="/dynamics365/unified-operations/financials/project-management/project-time-entry-mobile-workspace">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="fd4ea-153"><a href="/dynamics365/unified-operations/financials/expense-management/expense-management-mobile-workspace">Mobil çalışma alanında gider yönetimi</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-153"><a href="/dynamics365/unified-operations/financials/expense-management/expense-management-mobile-workspace">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd4ea-154">3</span><span class="sxs-lookup"><span data-stu-id="fd4ea-154">3</span></span></td>
<td><span data-ttu-id="fd4ea-155">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="fd4ea-155">System administrator</span></span></td>
<td><span data-ttu-id="fd4ea-156">Microsoft tarafından sağlanan mobil çalışma alanlarını yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="fd4ea-157"><a href="publish-mobile-workspace.md">Bir mobil çalışma alanı yayınlayın</a>
</span><span class="sxs-lookup"><span data-stu-id="fd4ea-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd4ea-158">4</span><span class="sxs-lookup"><span data-stu-id="fd4ea-158">4</span></span></td>
<td><span data-ttu-id="fd4ea-159">Geliştirici veya bağımsız yazılım satıcısı (ISV)</span><span class="sxs-lookup"><span data-stu-id="fd4ea-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="fd4ea-160">Mobil platformu, özel mobil çalışma alanları oluşturmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="fd4ea-161"><a href="platform/mobile-platform-home-page.md">Mobil platform</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd4ea-162">5</span><span class="sxs-lookup"><span data-stu-id="fd4ea-162">5</span></span></td>
<td><span data-ttu-id="fd4ea-163">ISV</span><span class="sxs-lookup"><span data-stu-id="fd4ea-163">ISV</span></span></td>
<td><span data-ttu-id="fd4ea-164">Özel mobil çalışma alanları içeren bir dağıtılabilir paket oluşturun ve paketi Microsoft Dynamics Lifecycle Services'a (LCS) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="fd4ea-165"><a href="../deployment/create-apply-deployable-package.md">Dağıtılabilir paket oluşturun</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd4ea-166">6</span><span class="sxs-lookup"><span data-stu-id="fd4ea-166">6</span></span></td>
<td><span data-ttu-id="fd4ea-167">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="fd4ea-167">System administrator</span></span></td>
<td><span data-ttu-id="fd4ea-168">Bağımsız yazılım satıcısı (ISV) tarafından sağlanan özel çalışma alanlarını içeren dağıtılabilir paketi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="fd4ea-169"><a href="../deployment/apply-deployable-package-system.md">Dağıtılabilir paket uygulama</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd4ea-170">7</span><span class="sxs-lookup"><span data-stu-id="fd4ea-170">7</span></span></td>
<td><span data-ttu-id="fd4ea-171">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="fd4ea-171">System administrator</span></span></td>
<td><span data-ttu-id="fd4ea-172">ISV tarafından sağlanan özel mobil çalışma alanlarını yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="fd4ea-173"><a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd4ea-174">8</span><span class="sxs-lookup"><span data-stu-id="fd4ea-174">8</span></span></td>
<td><span data-ttu-id="fd4ea-175">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="fd4ea-175">User</span></span></td>
<td><span data-ttu-id="fd4ea-176">Mobil uygulamayı indirin ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="fd4ea-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android telefonlar için</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="fd4ea-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">iPhone'lar için</a></span><span class="sxs-lookup"><span data-stu-id="fd4ea-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fd4ea-179">9</span><span class="sxs-lookup"><span data-stu-id="fd4ea-179">9</span></span></td>
<td><span data-ttu-id="fd4ea-180">Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="fd4ea-180">User</span></span></td>
<td><span data-ttu-id="fd4ea-181">Oturum açın ve mobil uygulamayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="fd4ea-182">Uygulama, sistem yöneticisi tarafından yayınlanan mobil çalışma alanlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="fd4ea-183">Microsoft tarafından sağlanan mobil çalışma alanlarının bir listesini görmek için bkz. <a href="mobile-workspaces-released.md">Yakın zamanda yayımlanmış olan mobil çalışma alanları</a>.</span><span class="sxs-lookup"><span data-stu-id="fd4ea-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

