---
title: "Fatura onayları mobil çalışma alanı"
description: "Bu konu, Fatura onayları mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı, fatura başlığı iş akışı işlemi üzerinden size atanmış olan faturaların bir listesini sağlar."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: af673f076f684500b6ca84d04c01f7f773d65cd6
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="27834-104">Fatura onayları mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="27834-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="27834-105">Bu konu, **Fatura onayları** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="27834-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="27834-106">Bu çalışma alanı, fatura başlığı iş akışı işlemi üzerinden size atanmış olan faturaların bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="27834-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="27834-107">Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations mobil uygulaması ile kullanılmak üzere geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="27834-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="27834-108">Özet</span><span class="sxs-lookup"><span data-stu-id="27834-108">Overview</span></span>

<span data-ttu-id="27834-109">**Fatura onayları** mobil çalışma alanı, Borç hesapları memurları ve yöneticilerinin, onlara atanmış olan faturalarını bir satıcı faturası başlığı iş akışı işlemi olarak görmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="27834-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="27834-110">Fatura bilgisini görüntüleyebilir ve hatta satır ve dağıtım ayrıntılarını, bilgili onay kararları vermenize yardımcı olmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27834-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="27834-111">Çalışma alanından, faturayı iş akışı işleminde taşımak için eylem alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27834-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="27834-112">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="27834-112">Prerequisites</span></span>

<span data-ttu-id="27834-113">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="27834-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="27834-114">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="27834-114">Prerequisite</span></span></th>
<th><span data-ttu-id="27834-115">Rol</span><span class="sxs-lookup"><span data-stu-id="27834-115">Role</span></span></th>
<th><span data-ttu-id="27834-116">Açıklama</span><span class="sxs-lookup"><span data-stu-id="27834-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27834-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017), kuruluşunuzda dağıtılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="27834-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="27834-118">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="27834-118">System administrator</span></span></td>
<td><span data-ttu-id="27834-119">Bkz. <a href="../deployment/deploy-demo-environment.md">Tanıtım ortamını dağıtma</a>.</span><span class="sxs-lookup"><span data-stu-id="27834-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="27834-120"><strong>Fatura onayları</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="27834-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="27834-121">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="27834-121">System administrator</span></span></td>
<td><span data-ttu-id="27834-122">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="27834-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="27834-123">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="27834-123">Download and install the mobile app</span></span>

<span data-ttu-id="27834-124">Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:</span><span class="sxs-lookup"><span data-stu-id="27834-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="27834-125">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="27834-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="27834-126">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="27834-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="27834-127">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="27834-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="27834-128">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="27834-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="27834-129">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="27834-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="27834-130">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="27834-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="27834-131">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="27834-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="27834-132">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="27834-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="27834-133">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="27834-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="27834-134">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="27834-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="27834-135">Fatura onayları mobil çalışma alanını kullanarak faturaları onaylayın</span><span class="sxs-lookup"><span data-stu-id="27834-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="27834-136">Mobil cihazınızda **Fatura onayları** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="27834-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="27834-137">Satıcı fatura başlığı iş akış işlemi tarafından size atanmış olan faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="27834-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="27834-138">**Fatura ayrıntıları** sayfasında, satıcı ve tarih bilgisi gibi fatura başlığı bilgisini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="27834-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="27834-139">Fatura üzerinde, **Fatura satırı ayrıntıları** görünümünde daha ayrıntılı bilgi görmek için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="27834-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="27834-140">**Fatura satırı ayrıntıları** görümünde, **Dağıtımlar**'ı seçerek satır dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="27834-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="27834-141">Burada fatura satırı için muhasebeyi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27834-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="27834-142">Gösterilen bilgi, mali boyutları ve ana hesabı içerir.</span><span class="sxs-lookup"><span data-stu-id="27834-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="27834-143">**Fatura satırı ayrıntıları** sayfasında , **Dağıtımlar**'ı seçerek tüm dağılımları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="27834-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="27834-144">Burada, faturanın tamamı için muhasebeyi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27834-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="27834-145">Gösterilen bilgi, mali boyutları ve ana hesapları içerir.</span><span class="sxs-lookup"><span data-stu-id="27834-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="27834-146">Faturaya eklenmiş herhangi bir notu veya dosyaları görmek için **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="27834-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="27834-147">**Fatura ayrıntıları** sayfasında, gözden geçirme işleminizi tamamlamak için ilgili iş akışı eylemini seçin.</span><span class="sxs-lookup"><span data-stu-id="27834-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="27834-148">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="27834-148">Select **Done**.</span></span>

