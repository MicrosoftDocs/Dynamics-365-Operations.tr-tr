---
title: "Satınalma siparişi onayı mobil çalışma"
description: "Bu konu satın alma siparişlerini görmenizi ve eylemler aracılığıyla yanıt vermenizi sağlayan Satınalma siparişi onayı mobil çalışma alanı hakkında bilgi sağlar. Örneğin, bir satınalma siparişini onaylayabilir veya reddedebilirsiniz."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2108f7fd7ba7c24b172befc8d294faeeae4c101f
ms.contentlocale: tr-tr
ms.lasthandoff: 12/01/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="231b0-104">Satınalma siparişi onayı mobil çalışma</span><span class="sxs-lookup"><span data-stu-id="231b0-104">Purchase order approval mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

<span data-ttu-id="231b0-105">Bu konu, **Satınalma siparişi onayı** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="231b0-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="231b0-106">Bu çalışma alanı, satınalma siparişlerini görüntülemenizi ve bunları eylemleri kullanarak yanıtlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="231b0-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="231b0-107">Örneğin, bir satınalma siparişini onaylayabilir veya reddedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="231b0-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="231b0-108">Özet</span><span class="sxs-lookup"><span data-stu-id="231b0-108">Overview</span></span> 
<span data-ttu-id="231b0-109">Onay gerektiren satınalma siparişleri bir onay iş akışından geçer.</span><span class="sxs-lookup"><span data-stu-id="231b0-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="231b0-110">İş akışı bir veya daha fazla kişinin eylem gerçekleştirmesini gerektiren çeşitli adımlar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="231b0-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="231b0-111">Örneğin, bir kişinin görevi tamamlaması veya satınalma siparişini onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="231b0-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="231b0-112">**Satınalma siparişi onayı** mobil çalışma alanı satınalma siparişlerini mobil cihazınızdan kolaylıkla görmenizi ve yanıtlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="231b0-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="231b0-113">Bu çalışma alanı, Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition web istemcisinden alabileceğiniz aynı iş akışı eylemlerini almanıza da olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="231b0-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="231b0-114">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="231b0-114">Prerequisites</span></span>
<span data-ttu-id="231b0-115">Önkoşullar, kuruluşunuza dağıtılan Finance and Operations sürümüne göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="231b0-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="231b0-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kullanıyorsanız önkoşullar</span><span class="sxs-lookup"><span data-stu-id="231b0-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span></span> 
<span data-ttu-id="231b0-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kuruluşunuza dağıtıldıysa, sistem yöneticisinin **Satınalma siparişi onayı** mobil çalışma alanını yayımlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="231b0-117">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="231b0-118">Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="231b0-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="231b0-119">Microsoft Dynamics 365 for Operations sürüm 1611 Platform güncelleştirmesi 3 veya daha sonraki sürüm kullanıyorsanız ön koşullar</span><span class="sxs-lookup"><span data-stu-id="231b0-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="231b0-120">Kuruluşunuza Platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="231b0-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="231b0-121">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="231b0-121">Prerequisite</span></span></th>
<th><span data-ttu-id="231b0-122">Rol</span><span class="sxs-lookup"><span data-stu-id="231b0-122">Role</span></span></th>
<th><span data-ttu-id="231b0-123">Açıklama</span><span class="sxs-lookup"><span data-stu-id="231b0-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="231b0-124">KB 4017918 uygulayın.</span><span class="sxs-lookup"><span data-stu-id="231b0-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="231b0-125">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="231b0-125">System administrator</span></span></td>
<td><span data-ttu-id="231b0-126">KB 4017918, <strong>Satınalma siparişi onayı</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="231b0-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="231b0-127">KB 4017918 uygulamak için sistem yöneticiniz bu adımları atması gerekir.</span><span class="sxs-lookup"><span data-stu-id="231b0-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="231b0-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</span><span class="sxs-lookup"><span data-stu-id="231b0-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="231b0-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</span><span class="sxs-lookup"><span data-stu-id="231b0-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="231b0-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</span><span class="sxs-lookup"><span data-stu-id="231b0-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="231b0-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</span><span class="sxs-lookup"><span data-stu-id="231b0-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="231b0-132"><strong>Satınalma siparişi onayı</strong> mobil çalışma alanını yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="231b0-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="231b0-133">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="231b0-133">System administrator</span></span></td>
<td><span data-ttu-id="231b0-134">Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="231b0-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="231b0-135">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="231b0-135">Download and install the mobile app</span></span>
<span data-ttu-id="231b0-136">Microsoft Dynamics 365 for Operations mobil uygulamasını yükleyin ve kurun:</span><span class="sxs-lookup"><span data-stu-id="231b0-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="231b0-137">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="231b0-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="231b0-138">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="231b0-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="231b0-139">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="231b0-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="231b0-140">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="231b0-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="231b0-141">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="231b0-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="231b0-142">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="231b0-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="231b0-143">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="231b0-143">Enter your credentials.</span></span>
4. <span data-ttu-id="231b0-144">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="231b0-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="231b0-145">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="231b0-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Kullanılabilir çalışma alanları listesindeki satınalma siparişi onayı çalışma alanı](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="231b0-147">Size atanmış olan siparişleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="231b0-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="231b0-148">Mobil cihazınızda **Satınalma siparişi onayı** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="231b0-149">Satınalma siparişi onayı çalışma alanında işlem yapmanız istenen tüm satınalma siparişlerini görüntülemek için **Bana atanan siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="231b0-150">Bir sipariş seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-150">Select an order.</span></span> <span data-ttu-id="231b0-151">**Sipariş ayrıntıları** sayfasında, sipariş başlığı bilgileri ve satırları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="231b0-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="231b0-152">Ayrıca iş akışı görevinden gelen yönergeleri de bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="231b0-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="231b0-153">**Muhasebe dağılımları**'nı seçerek **Başlık muhasebe dağıtımları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="231b0-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="231b0-154">**Sipariş ayrıntıları** sayfasına dönün ve bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="231b0-155">Sipariş satırı ayrıntılarından satıra özel muhasebe dağıtımlarını da keşfedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="231b0-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="231b0-156">Satınalma siparişinde bir eylemi tamamlama</span><span class="sxs-lookup"><span data-stu-id="231b0-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="231b0-157">Size atanan satınalma siparişini görüntüledikten ve iş akışı talimatlarını okuduktan sonra, işlem yapmaya hazır olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="231b0-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="231b0-158">Mobil cihazınızda **Satınalma siparişi onayı** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="231b0-159">Satınalma siparişi onayı çalışma alanında işlem yapmanız istenen tüm satınalma siparişlerini görüntülemek için **Bana atanan siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="231b0-160">Bir sipariş seçin ve ayrıntılar sayfasını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="231b0-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="231b0-161">Kullanılabilir eylemleri görüntülemek için **Eylemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="231b0-162">Kullanılabilir eylemler size atanan göreve bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="231b0-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="231b0-163">Görev eylemi</span><span class="sxs-lookup"><span data-stu-id="231b0-163">Task action</span></span>    | <span data-ttu-id="231b0-164">Onay eylemi</span><span class="sxs-lookup"><span data-stu-id="231b0-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="231b0-165">Tam</span><span class="sxs-lookup"><span data-stu-id="231b0-165">Complete</span></span>       | <span data-ttu-id="231b0-166">Onayla</span><span class="sxs-lookup"><span data-stu-id="231b0-166">Approve</span></span>          |
    | <span data-ttu-id="231b0-167">İade</span><span class="sxs-lookup"><span data-stu-id="231b0-167">Return</span></span>         | <span data-ttu-id="231b0-168">Reddet</span><span class="sxs-lookup"><span data-stu-id="231b0-168">Reject</span></span>           |
    | <span data-ttu-id="231b0-169">İstek değişikliği</span><span class="sxs-lookup"><span data-stu-id="231b0-169">Request change</span></span> | <span data-ttu-id="231b0-170">İstek değişikliği</span><span class="sxs-lookup"><span data-stu-id="231b0-170">Request change</span></span>   |
    | <span data-ttu-id="231b0-171">Temsilci Seç</span><span class="sxs-lookup"><span data-stu-id="231b0-171">Delegate</span></span>       | <span data-ttu-id="231b0-172">Temsilci Seç</span><span class="sxs-lookup"><span data-stu-id="231b0-172">Delegate</span></span>         |

5. <span data-ttu-id="231b0-173">Uygun olan eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="231b0-174">**Görevi tamamla** sayfasında, bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="231b0-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="231b0-175">**Temsilci ata** eylemini seçerseniz, görevi atayacağınız bir temsilci seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="231b0-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="231b0-176">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="231b0-176">Select **Done**.</span></span> <span data-ttu-id="231b0-177">Çalışma alanını yeniledikten sonra satın alma siparişi artık listenizde olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="231b0-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 

