---
title: Ekibim mobil çalışma alanı
description: Bu konu, yöneticilerin astlarını ve genişletilmiş ekiplerini görüntülemelerini sağlayan Ekibim mobil çalışma alanı hakkında bilgi sağlar. Kullanıcılar, raporlama zincirlerindeki bireylere övgü de gönderebilirler.
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6ac3bf0a6ce20866f749b0c14030b70770e5589c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680982"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="e5226-104">Ekibim mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="e5226-104">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5226-105">Bu konu, **Ekibim** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e5226-105">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="e5226-106">Bu çalışma alanı, yöneticilerin dorudan rapor verenlerini ve genişletilmiş personellerini görüntülemelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e5226-106">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="e5226-107">Raporlama zincirlerindeki bireylere övgü de gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="e5226-107">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="e5226-108">Bu mobil çalışma alanı, Finance and Operations mobil uygulaması ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e5226-108">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="e5226-109">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="e5226-109">Overview</span></span> 
<span data-ttu-id="e5226-110">**Ekibim** mobil çalışma alanı, yöneticilerin şu görevleri yerine getirmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="e5226-110">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="e5226-111">Yöneticinin doğrudan rapor verenlerinin bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="e5226-111">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="e5226-112">Yöneticinin genişletilmiş raporlama ekibinin bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="e5226-112">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="e5226-113">Her bir takım üyesi hakkında doğum tarihi, kıdem yaşı, hizmet yılı ve ücret ve performans bilgisi gibi ayrıntılı bilgi görüntüle.</span><span class="sxs-lookup"><span data-stu-id="e5226-113">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="e5226-114">Yöneticinin genişletilmiş raporlama ekibindeki herhangi bir kişiye övgü gönder.</span><span class="sxs-lookup"><span data-stu-id="e5226-114">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e5226-115">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="e5226-115">Prerequisites</span></span>
<span data-ttu-id="e5226-116">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5226-116">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e5226-117">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="e5226-117">Prerequisite</span></span></th>
<th><span data-ttu-id="e5226-118">Rol</span><span class="sxs-lookup"><span data-stu-id="e5226-118">Role</span></span></th>
<th><span data-ttu-id="e5226-119">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e5226-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e5226-120">Aşağıdaki ürünlerden birinin kuruluşunuzda dağıtılmış olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="e5226-120">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="e5226-121">Bir Finance and Operations uygulamayı</span><span class="sxs-lookup"><span data-stu-id="e5226-121">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="e5226-122">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="e5226-122">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="e5226-123">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e5226-123">System administrator</span></span></td>
<td><span data-ttu-id="e5226-124">Kuruluşunuzda halihazırda dağıtılmış bir Finance and Operations uygulamanız yoksa bkz. <a href="../deployment/deploy-demo-environment.md">Tanıtım ortamını dağıtma</a>.</span><span class="sxs-lookup"><span data-stu-id="e5226-124">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="e5226-125">Kuruluşunuzda Human Resources dağıtılmamışsa sistem yöneticisi <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources web sayfasından</a> bir deneme sürümüne erişim sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="e5226-125">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e5226-126"><strong>Ekibim</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5226-126">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="e5226-127">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e5226-127">System administrator</span></span></td>
<td><span data-ttu-id="e5226-128">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="e5226-128">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="e5226-129">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="e5226-129">Download and install the mobile app</span></span>

<span data-ttu-id="e5226-130">Finance and Operations mobil uygulamasını indirip yükleyin:</span><span class="sxs-lookup"><span data-stu-id="e5226-130">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="e5226-131">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="e5226-131">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="e5226-132">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="e5226-132">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="e5226-133">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="e5226-133">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="e5226-134">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="e5226-134">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="e5226-135">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="e5226-135">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="e5226-136">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-136">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="e5226-137">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="e5226-137">Enter your credentials.</span></span>
4.  <span data-ttu-id="e5226-138">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e5226-138">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="e5226-139">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e5226-139">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="e5226-140">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="e5226-140">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="e5226-141">Ekibim mobil çalışma alanını kullanarak ekip üyelerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="e5226-141">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="e5226-142">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="e5226-142">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="e5226-143">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-143">A list of team members is shown.</span></span> <span data-ttu-id="e5226-144">Liste ayrıca her takım üyesinin unvanını ve üyenin sahip olduğu bağlı çalışanları gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5226-144">The list also shows each team member's title, and any direct reports that the member has.</span></span>
2.  <span data-ttu-id="e5226-145">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="e5226-145">Select a team member.</span></span> <span data-ttu-id="e5226-146">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-146">The **Team member summary** page appears.</span></span> <span data-ttu-id="e5226-147">Bu sayfadaki bilgi, takım üyesinin doğum tarihini, kıdem yaşını, hizmet süresini, geçerli pozisyonda geçirdiği yıl sayısını ve ücret bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5226-147">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="e5226-148">Ekibim mobil çalışma alanını kullanarak genişletilmiş ekip üyelerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="e5226-148">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="e5226-149">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="e5226-149">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="e5226-150">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-150">A list of team members is shown.</span></span> <span data-ttu-id="e5226-151">Liste ayrıca her takım üyesinin unvanını ve üyenin sahip olduğu bağlı çalışanları gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5226-151">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="e5226-152">**Doğrudan rapor verenler** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e5226-152">Select the **Direct reports** link.</span></span> <span data-ttu-id="e5226-153">Genişletilmiş ekibinizin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-153">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="e5226-154">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="e5226-154">Select a team member.</span></span> <span data-ttu-id="e5226-155">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-155">The **Team member summary** page appears.</span></span> <span data-ttu-id="e5226-156">Bu sayfadaki bilgi, takım üyesinin doğum tarihini, kıdem yaşını, hizmet süresini, geçerli pozisyonda geçirdiği yıl sayısını ve ücret bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5226-156">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="e5226-157">Ekibim mobil çalışma alanını kullanarak ekip üyeleri hakkında övgü gönder</span><span class="sxs-lookup"><span data-stu-id="e5226-157">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="e5226-158">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="e5226-158">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="e5226-159">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-159">A list of team members is shown.</span></span> <span data-ttu-id="e5226-160">Liste ayrıca her takım üyesinin unvanını ve üyenin sahip olduğu bağlı çalışanları gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5226-160">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="e5226-161">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="e5226-161">Select a team member.</span></span> <span data-ttu-id="e5226-162">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5226-162">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="e5226-163">**Övgü gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e5226-163">Select **Send praise**.</span></span> 
1. <span data-ttu-id="e5226-164">Göndermek istediğiniz övgü metnini girin.</span><span class="sxs-lookup"><span data-stu-id="e5226-164">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="e5226-165">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e5226-165">Select **Done**.</span></span>
