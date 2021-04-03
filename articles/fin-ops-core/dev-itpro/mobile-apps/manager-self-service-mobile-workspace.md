---
title: Ekibim mobil çalışma alanı
description: Bu konu, yöneticilerin astlarını ve genişletilmiş ekiplerini görüntülemelerini sağlayan Ekibim mobil çalışma alanı hakkında bilgi sağlar.
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dc2f8b5195fb5210ca6399cbf744f210671f475
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570104"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="cf6bc-103">Takımım mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="cf6bc-103">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf6bc-104">Bu konu, **Ekibim** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-104">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="cf6bc-105">Bu çalışma alanı, yöneticilerin dorudan rapor verenlerini ve genişletilmiş personellerini görüntülemelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-105">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="cf6bc-106">Raporlama zincirlerindeki bireylere övgü de gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-106">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="cf6bc-107">Bu mobil çalışma alanı, Finance and Operations mobil uygulaması ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="cf6bc-108">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="cf6bc-108">Overview</span></span> 
<span data-ttu-id="cf6bc-109">**Ekibim** mobil çalışma alanı, yöneticilerin şu görevleri yerine getirmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="cf6bc-109">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="cf6bc-110">Yöneticinin doğrudan rapor verenlerinin bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-110">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="cf6bc-111">Yöneticinin genişletilmiş raporlama ekibinin bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-111">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="cf6bc-112">Her bir takım üyesi hakkında doğum tarihi, kıdem yaşı, hizmet yılı ve ücret ve performans bilgisi gibi ayrıntılı bilgi görüntüle.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-112">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="cf6bc-113">Yöneticinin genişletilmiş raporlama ekibindeki herhangi bir kişiye övgü gönder.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-113">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cf6bc-114">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="cf6bc-114">Prerequisites</span></span>
<span data-ttu-id="cf6bc-115">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-115">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf6bc-116">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="cf6bc-116">Prerequisite</span></span></th>
<th><span data-ttu-id="cf6bc-117">Rol</span><span class="sxs-lookup"><span data-stu-id="cf6bc-117">Role</span></span></th>
<th><span data-ttu-id="cf6bc-118">Açıklama</span><span class="sxs-lookup"><span data-stu-id="cf6bc-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf6bc-119">Aşağıdaki ürünlerden birinin kuruluşunuzda dağıtılmış olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="cf6bc-119">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="cf6bc-120">Bir Finance and Operations uygulamayı</span><span class="sxs-lookup"><span data-stu-id="cf6bc-120">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="cf6bc-121">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="cf6bc-121">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="cf6bc-122">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="cf6bc-122">System administrator</span></span></td>
<td><span data-ttu-id="cf6bc-123">Kuruluşunuzda halihazırda dağıtılmış bir Finance and Operations uygulamanız yoksa bkz. <a href="../deployment/deploy-demo-environment.md">Tanıtım ortamını dağıtma</a>.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-123">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="cf6bc-124">Kuruluşunuzda Human Resources dağıtılmamışsa sistem yöneticisi <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources web sayfasından</a> bir deneme sürümüne erişim sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-124">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf6bc-125"><strong>Ekibim</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-125">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="cf6bc-126">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="cf6bc-126">System administrator</span></span></td>
<td><span data-ttu-id="cf6bc-127">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-127">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="cf6bc-128">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="cf6bc-128">Download and install the mobile app</span></span>

<span data-ttu-id="cf6bc-129">Finance and Operations mobil uygulamasını indirip yükleyin:</span><span class="sxs-lookup"><span data-stu-id="cf6bc-129">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="cf6bc-130">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="cf6bc-130">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="cf6bc-131">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="cf6bc-131">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="cf6bc-132">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="cf6bc-132">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="cf6bc-133">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-133">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="cf6bc-134">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-134">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="cf6bc-135">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-135">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="cf6bc-136">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-136">Enter your credentials.</span></span>
4.  <span data-ttu-id="cf6bc-137">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-137">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="cf6bc-138">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-138">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="cf6bc-139">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="cf6bc-139">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="cf6bc-140">Ekibim mobil çalışma alanını kullanarak ekip üyelerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="cf6bc-140">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="cf6bc-141">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-141">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="cf6bc-142">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-142">A list of team members is shown.</span></span> <span data-ttu-id="cf6bc-143">Liste ayrıca her takım üyesinin unvanını ve üyenin sahip olduğu bağlı çalışanları gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-143">The list also shows each team member's title, and any direct reports that the member has.</span></span>
2.  <span data-ttu-id="cf6bc-144">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-144">Select a team member.</span></span> <span data-ttu-id="cf6bc-145">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-145">The **Team member summary** page appears.</span></span> <span data-ttu-id="cf6bc-146">Bu sayfadaki bilgi, takım üyesinin doğum tarihini, kıdem yaşını, hizmet süresini, geçerli pozisyonda geçirdiği yıl sayısını ve ücret bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-146">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="cf6bc-147">Ekibim mobil çalışma alanını kullanarak genişletilmiş ekip üyelerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="cf6bc-147">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="cf6bc-148">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-148">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="cf6bc-149">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-149">A list of team members is shown.</span></span> <span data-ttu-id="cf6bc-150">Liste ayrıca her takım üyesinin unvanını ve üyenin sahip olduğu bağlı çalışanları gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-150">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="cf6bc-151">**Doğrudan rapor verenler** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-151">Select the **Direct reports** link.</span></span> <span data-ttu-id="cf6bc-152">Genişletilmiş ekibinizin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-152">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="cf6bc-153">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-153">Select a team member.</span></span> <span data-ttu-id="cf6bc-154">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-154">The **Team member summary** page appears.</span></span> <span data-ttu-id="cf6bc-155">Bu sayfadaki bilgi, takım üyesinin doğum tarihini, kıdem yaşını, hizmet süresini, geçerli pozisyonda geçirdiği yıl sayısını ve ücret bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-155">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="cf6bc-156">Ekibim mobil çalışma alanını kullanarak ekip üyeleri hakkında övgü gönder</span><span class="sxs-lookup"><span data-stu-id="cf6bc-156">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="cf6bc-157">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-157">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="cf6bc-158">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-158">A list of team members is shown.</span></span> <span data-ttu-id="cf6bc-159">Liste ayrıca her takım üyesinin unvanını ve üyenin sahip olduğu bağlı çalışanları gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-159">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="cf6bc-160">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-160">Select a team member.</span></span> <span data-ttu-id="cf6bc-161">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-161">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="cf6bc-162">**Övgü gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-162">Select **Send praise**.</span></span> 
1. <span data-ttu-id="cf6bc-163">Göndermek istediğiniz övgü metnini girin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-163">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="cf6bc-164">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf6bc-164">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]