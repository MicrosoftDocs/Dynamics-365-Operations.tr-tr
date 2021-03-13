---
title: Satınalma siparişi onayı mobil çalışma
description: Bu konu satın alma siparişlerini görmenizi ve eylemler aracılığıyla yanıt vermenizi sağlayan Satınalma siparişi onayı mobil çalışma alanı hakkında bilgi sağlar. Örneğin, bir satınalma siparişini onaylayabilir veya reddedebilirsiniz.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7f952f3af36620a20a5c991fd9e1ccfd56119f47
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022318"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="cdddd-104">Satınalma siparişi onayı mobil çalışma</span><span class="sxs-lookup"><span data-stu-id="cdddd-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdddd-105">Bu konu, **Satınalma siparişi onayı** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cdddd-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="cdddd-106">Bu çalışma alanı, satınalma siparişlerini görüntülemenizi ve bunları eylemleri kullanarak yanıtlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="cdddd-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="cdddd-107">Örneğin, bir satınalma siparişini onaylayabilir veya reddedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdddd-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="cdddd-108">Özet</span><span class="sxs-lookup"><span data-stu-id="cdddd-108">Overview</span></span> 
<span data-ttu-id="cdddd-109">Onay gerektiren satınalma siparişleri bir onay iş akışından geçer.</span><span class="sxs-lookup"><span data-stu-id="cdddd-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="cdddd-110">İş akışı bir veya daha fazla kişinin eylem gerçekleştirmesini gerektiren çeşitli adımlar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="cdddd-111">Örneğin, bir kişinin görevi tamamlaması veya satınalma siparişini onaylaması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="cdddd-112">**Satınalma siparişi onayı** mobil çalışma alanı satınalma siparişlerini mobil cihazınızdan kolaylıkla görmenizi ve yanıtlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="cdddd-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="cdddd-113">Bu çalışma alanı, web istemcisinden alabileceğiniz aynı iş akışı eylemlerini almanıza da olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="cdddd-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cdddd-114">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="cdddd-114">Prerequisites</span></span>
<span data-ttu-id="cdddd-115">Önkoşullar, kuruluşunuza dağıtılan Supply Chain Management sürümüne göre değişiklik gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="cdddd-116">Supply Chain Management kullanıyorsanız önkoşullar</span><span class="sxs-lookup"><span data-stu-id="cdddd-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="cdddd-117">Supply Chain Management kuruluşunuza dağıtıldıysa sistem yöneticisinin **Satınalma siparişi onayı** mobil çalışma alanını yayımlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="cdddd-118">Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="cdddd-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="cdddd-119">Microsoft Dynamics 365 for Operations sürüm 1611'i Platform güncelleştirmesi 3 veya daha sonrasıyla kullanıyorsanız önkoşullar</span><span class="sxs-lookup"><span data-stu-id="cdddd-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="cdddd-120">Kuruluşunuza Platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cdddd-121">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="cdddd-121">Prerequisite</span></span></th>
<th><span data-ttu-id="cdddd-122">Rol</span><span class="sxs-lookup"><span data-stu-id="cdddd-122">Role</span></span></th>
<th><span data-ttu-id="cdddd-123">Açıklama</span><span class="sxs-lookup"><span data-stu-id="cdddd-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cdddd-124">KB 4017918 uygulayın.</span><span class="sxs-lookup"><span data-stu-id="cdddd-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="cdddd-125">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="cdddd-125">System administrator</span></span></td>
<td><span data-ttu-id="cdddd-126">KB 4017918, <strong>Satınalma siparişi onayı</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="cdddd-127">KB 4017918 uygulamak için sistem yöneticiniz bu adımları atması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="cdddd-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</span><span class="sxs-lookup"><span data-stu-id="cdddd-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="cdddd-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Meta veri düzeltmesini kurun</a>.</span><span class="sxs-lookup"><span data-stu-id="cdddd-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="cdddd-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Şunu içeren bir dağıtılabilir paket oluşturun:</a> <strong>SCMMobile</strong> modeli ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="cdddd-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Dağıtılabilir paketi uygulayın</a>.</span><span class="sxs-lookup"><span data-stu-id="cdddd-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cdddd-132"><strong>Satınalma siparişi onayı</strong> mobil çalışma alanını yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="cdddd-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="cdddd-133">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="cdddd-133">System administrator</span></span></td>
<td><span data-ttu-id="cdddd-134">Bkz. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="cdddd-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="cdddd-135">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="cdddd-135">Download and install the mobile app</span></span>
<span data-ttu-id="cdddd-136">Finance and Operations mobil uygulamasını indirip yükleyin:</span><span class="sxs-lookup"><span data-stu-id="cdddd-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="cdddd-137">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="cdddd-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="cdddd-138">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="cdddd-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="cdddd-139">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="cdddd-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="cdddd-140">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="cdddd-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="cdddd-141">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="cdddd-142">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="cdddd-143">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-143">Enter your credentials.</span></span>
4. <span data-ttu-id="cdddd-144">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="cdddd-145">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cdddd-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Kullanılabilir çalışma alanları listesindeki satınalma siparişi onayı çalışma alanı](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="cdddd-147">Size atanmış olan siparişleri görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="cdddd-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="cdddd-148">Mobil cihazınızda **Satınalma siparişi onayı** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="cdddd-149">Satınalma siparişi onayı çalışma alanında işlem yapmanız istenen tüm satınalma siparişlerini görüntülemek için **Bana atanan siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="cdddd-150">Bir sipariş seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-150">Select an order.</span></span> <span data-ttu-id="cdddd-151">**Sipariş ayrıntıları** sayfasında, sipariş başlığı bilgileri ve satırları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="cdddd-152">Ayrıca iş akışı görevinden gelen yönergeleri de bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdddd-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="cdddd-153">**Muhasebe dağılımları**'nı seçerek **Başlık muhasebe dağıtımları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="cdddd-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="cdddd-154">**Sipariş ayrıntıları** sayfasına dönün ve bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="cdddd-155">Sipariş satırı ayrıntılarından satıra özel muhasebe dağıtımlarını da keşfedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdddd-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="cdddd-156">Satınalma siparişinde bir eylemi tamamlama</span><span class="sxs-lookup"><span data-stu-id="cdddd-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="cdddd-157">Size atanan satınalma siparişini görüntüledikten ve iş akışı talimatlarını okuduktan sonra, işlem yapmaya hazır olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="cdddd-158">Mobil cihazınızda **Satınalma siparişi onayı** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="cdddd-159">Satınalma siparişi onayı çalışma alanında işlem yapmanız istenen tüm satınalma siparişlerini görüntülemek için **Bana atanan siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="cdddd-160">Bir sipariş seçin ve ayrıntılar sayfasını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="cdddd-161">Kullanılabilir eylemleri görüntülemek için **Eylemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="cdddd-162">Kullanılabilir eylemler size atanan göreve bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="cdddd-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="cdddd-163">Görev eylemi</span><span class="sxs-lookup"><span data-stu-id="cdddd-163">Task action</span></span>    | <span data-ttu-id="cdddd-164">Onay eylemi</span><span class="sxs-lookup"><span data-stu-id="cdddd-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="cdddd-165">Tam</span><span class="sxs-lookup"><span data-stu-id="cdddd-165">Complete</span></span>       | <span data-ttu-id="cdddd-166">Onayla</span><span class="sxs-lookup"><span data-stu-id="cdddd-166">Approve</span></span>          |
    | <span data-ttu-id="cdddd-167">İade</span><span class="sxs-lookup"><span data-stu-id="cdddd-167">Return</span></span>         | <span data-ttu-id="cdddd-168">Reddet</span><span class="sxs-lookup"><span data-stu-id="cdddd-168">Reject</span></span>           |
    | <span data-ttu-id="cdddd-169">İstek değişikliği</span><span class="sxs-lookup"><span data-stu-id="cdddd-169">Request change</span></span> | <span data-ttu-id="cdddd-170">İstek değişikliği</span><span class="sxs-lookup"><span data-stu-id="cdddd-170">Request change</span></span>   |
    | <span data-ttu-id="cdddd-171">Temsilci Seç</span><span class="sxs-lookup"><span data-stu-id="cdddd-171">Delegate</span></span>       | <span data-ttu-id="cdddd-172">Temsilci Seç</span><span class="sxs-lookup"><span data-stu-id="cdddd-172">Delegate</span></span>         |

5. <span data-ttu-id="cdddd-173">Uygun olan eylemi seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="cdddd-174">**Görevi tamamla** sayfasında, bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="cdddd-175">**Temsilci ata** eylemini seçerseniz, görevi atayacağınız bir temsilci seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdddd-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="cdddd-176">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cdddd-176">Select **Done**.</span></span> <span data-ttu-id="cdddd-177">Çalışma alanını yeniledikten sonra satın alma siparişi artık listenizde olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="cdddd-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 
