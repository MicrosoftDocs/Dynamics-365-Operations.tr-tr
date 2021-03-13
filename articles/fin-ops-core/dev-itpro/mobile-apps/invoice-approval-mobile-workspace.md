---
title: Fatura onayları mobil çalışma alanı
description: Bu konu, Fatura onayları mobil çalışma alanı hakkında bilgi sağlar.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 1a7aa1a03791b8ccb7050389097d1272f5930a49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127581"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="3d93c-103">Fatura onayları mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="3d93c-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d93c-104">Bu konu, **Fatura onayları** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d93c-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="3d93c-105">Bu çalışma alanı, fatura başlığı iş akışı işlemi üzerinden size atanmış olan faturaların bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d93c-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="3d93c-106">Bu mobil çalışma alanı, Finance and Operations mobil uygulaması ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3d93c-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="3d93c-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="3d93c-107">Overview</span></span>

<span data-ttu-id="3d93c-108">**Fatura onayları** mobil çalışma alanı, Borç hesapları memurları ve yöneticilerinin, onlara atanmış olan faturalarını bir satıcı faturası başlığı iş akışı işlemi olarak görmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d93c-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="3d93c-109">Fatura bilgisini görüntüleyebilir ve hatta satır ve dağıtım ayrıntılarını, bilgili onay kararları vermenize yardımcı olmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d93c-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="3d93c-110">Çalışma alanından, faturayı iş akışı işleminde taşımak için eylem alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d93c-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3d93c-111">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="3d93c-111">Prerequisites</span></span>

<span data-ttu-id="3d93c-112">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d93c-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3d93c-113">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="3d93c-113">Prerequisite</span></span></th>
<th><span data-ttu-id="3d93c-114">Rol</span><span class="sxs-lookup"><span data-stu-id="3d93c-114">Role</span></span></th>
<th><span data-ttu-id="3d93c-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d93c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d93c-116">Microsoft Dynamics 365 Finance kuruluşunuzda dağıtılmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3d93c-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="3d93c-117">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="3d93c-117">System administrator</span></span></td>
<td><span data-ttu-id="3d93c-118">Bkz. <a href="../deployment/deploy-demo-environment.md">Tanıtım ortamını dağıtma</a>.</span><span class="sxs-lookup"><span data-stu-id="3d93c-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d93c-119"><strong>Fatura onayları</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d93c-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="3d93c-120">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="3d93c-120">System administrator</span></span></td>
<td><span data-ttu-id="3d93c-121">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="3d93c-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="3d93c-122">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="3d93c-122">Download and install the mobile app</span></span>

<span data-ttu-id="3d93c-123">Finance and Operations mobil uygulamasını indirip yükleyin:</span><span class="sxs-lookup"><span data-stu-id="3d93c-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="3d93c-124">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="3d93c-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="3d93c-125">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="3d93c-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="3d93c-126">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="3d93c-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="3d93c-127">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="3d93c-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="3d93c-128">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="3d93c-129">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="3d93c-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="3d93c-130">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="3d93c-131">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3d93c-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="3d93c-132">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3d93c-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="3d93c-133">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="3d93c-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="3d93c-134">Fatura onayları mobil çalışma alanını kullanarak faturaları onaylayın</span><span class="sxs-lookup"><span data-stu-id="3d93c-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="3d93c-135">Mobil cihazınızda **Fatura onayları** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="3d93c-136">Satıcı fatura başlığı iş akış işlemi tarafından size atanmış olan faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="3d93c-137">**Fatura ayrıntıları** sayfasında, satıcı ve tarih bilgisi gibi fatura başlığı bilgisini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="3d93c-138">Fatura üzerinde, **Fatura satırı ayrıntıları** görünümünde daha ayrıntılı bilgi görmek için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="3d93c-139">**Fatura satırı ayrıntıları** görümünde, **Dağıtımlar**'ı seçerek satır dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="3d93c-140">Burada fatura satırı için muhasebeyi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d93c-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="3d93c-141">Gösterilen bilgi, mali boyutları ve ana hesabı içerir.</span><span class="sxs-lookup"><span data-stu-id="3d93c-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="3d93c-142">**Fatura satırı ayrıntıları** sayfasında , **Dağıtımlar**'ı seçerek tüm dağılımları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="3d93c-143">Burada, faturanın tamamı için muhasebeyi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d93c-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="3d93c-144">Gösterilen bilgi, mali boyutları ve ana hesapları içerir.</span><span class="sxs-lookup"><span data-stu-id="3d93c-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="3d93c-145">Faturaya eklenmiş herhangi bir notu veya dosyaları görmek için **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="3d93c-146">**Fatura ayrıntıları** sayfasında, gözden geçirme işleminizi tamamlamak için ilgili iş akışı eylemini seçin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="3d93c-147">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d93c-147">Select **Done**.</span></span>
