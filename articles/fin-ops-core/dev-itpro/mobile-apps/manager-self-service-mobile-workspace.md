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
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c2ad5f30ed0e69df1769eb0379b5da2865d4ce4f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005621"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="bca87-104">Ekibim mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="bca87-104">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bca87-105">Bu konu, **Ekibim** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="bca87-105">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="bca87-106">Bu çalışma alanı, yöneticilerin dorudan rapor verenlerini ve genişletilmiş personellerini görüntülemelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="bca87-106">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="bca87-107">Raporlama zincirlerindeki bireylere övgü de gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="bca87-107">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="bca87-108">Bu mobil çalışma alanı, Finance and Operations mobil uygulaması ile kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bca87-108">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="bca87-109">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="bca87-109">Overview</span></span> 
<span data-ttu-id="bca87-110">**Ekibim** mobil çalışma alanı, yöneticilerin şu görevleri yerine getirmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="bca87-110">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="bca87-111">Yöneticinin doğrudan rapor verenlerinin bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="bca87-111">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="bca87-112">Yöneticinin genişletilmiş raporlama ekibinin bir listesini görüntüle.</span><span class="sxs-lookup"><span data-stu-id="bca87-112">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="bca87-113">Her bir takım üyesi hakkında doğum tarihi, kıdem yaşı, hizmet yılı ve ücret ve performans bilgisi gibi ayrıntılı bilgi görüntüle.</span><span class="sxs-lookup"><span data-stu-id="bca87-113">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="bca87-114">Yöneticinin genişletilmiş raporlama ekibindeki herhangi bir kişiye övgü gönder.</span><span class="sxs-lookup"><span data-stu-id="bca87-114">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bca87-115">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="bca87-115">Prerequisites</span></span>
<span data-ttu-id="bca87-116">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bca87-116">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bca87-117">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="bca87-117">Prerequisite</span></span></th>
<th><span data-ttu-id="bca87-118">Rol</span><span class="sxs-lookup"><span data-stu-id="bca87-118">Role</span></span></th>
<th><span data-ttu-id="bca87-119">Açıklama</span><span class="sxs-lookup"><span data-stu-id="bca87-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bca87-120">Aşağıdaki ürünlerden birinin kuruluşunuzda dağıtılmış olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="bca87-120">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="bca87-121">Bir Finance and Operations uygulamayı</span><span class="sxs-lookup"><span data-stu-id="bca87-121">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="bca87-122">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="bca87-122">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="bca87-123">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="bca87-123">System administrator</span></span></td>
<td><span data-ttu-id="bca87-124">Kuruluşunuzda halihazırda dağıtılmış bir Finance and Operations uygulamanız yoksa bkz. <a href="../deployment/deploy-demo-environment.md">Tanıtım ortamını dağıtma</a>.</span><span class="sxs-lookup"><span data-stu-id="bca87-124">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="bca87-125">Kuruluşunuzda Human Resources dağıtılmamışsa sistem yöneticisi <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources web sayfasından</a> bir deneme sürümüne erişim sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="bca87-125">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bca87-126"><strong>Ekibim</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bca87-126">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="bca87-127">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="bca87-127">System administrator</span></span></td>
<td><span data-ttu-id="bca87-128">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="bca87-128">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="bca87-129">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="bca87-129">Download and install the mobile app</span></span>

<span data-ttu-id="bca87-130">Finance and Operations mobil uygulamasını indirip yükleyin:</span><span class="sxs-lookup"><span data-stu-id="bca87-130">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="bca87-131">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="bca87-131">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="bca87-132">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="bca87-132">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="bca87-133">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="bca87-133">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="bca87-134">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="bca87-134">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="bca87-135">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="bca87-135">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="bca87-136">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-136">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="bca87-137">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="bca87-137">Enter your credentials.</span></span>
4.  <span data-ttu-id="bca87-138">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bca87-138">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="bca87-139">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="bca87-139">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="bca87-140">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="bca87-140">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="bca87-141">Ekibim mobil çalışma alanını kullanarak ekip üyelerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="bca87-141">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="bca87-142">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="bca87-142">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="bca87-143">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-143">A list of team members is shown.</span></span> <span data-ttu-id="bca87-144">Liste ayrıca her bir ekip üyesinin unvanını ve sahip oldukları doğrudan rapor verenleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="bca87-144">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
2.  <span data-ttu-id="bca87-145">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="bca87-145">Select a team member.</span></span> <span data-ttu-id="bca87-146">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-146">The **Team member summary** page appears.</span></span> <span data-ttu-id="bca87-147">Bu sayfadaki bilgi, ekip üyesinin doğum tarihini, kıdem yaşını, hizmet süresini, pozisyonundaki yıllarını ve ücret bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bca87-147">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="bca87-148">Ekibim mobil çalışma alanını kullanarak genişletilmiş ekip üyelerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="bca87-148">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="bca87-149">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="bca87-149">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="bca87-150">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-150">A list of team members is shown.</span></span> <span data-ttu-id="bca87-151">Liste ayrıca her bir ekip üyesinin unvanını ve sahip oldukları doğrudan rapor verenleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="bca87-151">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="bca87-152">**Doğrudan rapor verenler** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="bca87-152">Select the **Direct reports** link.</span></span> <span data-ttu-id="bca87-153">Genişletilmiş ekibinizin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-153">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="bca87-154">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="bca87-154">Select a team member.</span></span> <span data-ttu-id="bca87-155">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-155">The **Team member summary** page appears.</span></span> <span data-ttu-id="bca87-156">Bu sayfadaki bilgi, ekip üyesinin doğum tarihini, kıdem yaşını, hizmet süresini, pozisyonundaki yıllarını ve ücret bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bca87-156">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="bca87-157">Ekibim mobil çalışma alanını kullanarak ekip üyeleri hakkında övgü gönder</span><span class="sxs-lookup"><span data-stu-id="bca87-157">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="bca87-158">Mobil uygulamada, **Ekibim** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="bca87-158">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="bca87-159">Ekip üyelerinin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-159">A list of team members is shown.</span></span> <span data-ttu-id="bca87-160">Liste ayrıca her bir ekip üyesinin unvanını ve sahip oldukları doğrudan rapor verenleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="bca87-160">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="bca87-161">Bir ekip üyesi seç.</span><span class="sxs-lookup"><span data-stu-id="bca87-161">Select a team member.</span></span> <span data-ttu-id="bca87-162">**Ekip üyesi özeti** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bca87-162">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="bca87-163">**Övgü gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bca87-163">Select **Send praise**.</span></span> 
1. <span data-ttu-id="bca87-164">Göndermek istediğiniz övgü metnini girin.</span><span class="sxs-lookup"><span data-stu-id="bca87-164">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="bca87-165">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bca87-165">Select **Done**.</span></span>
