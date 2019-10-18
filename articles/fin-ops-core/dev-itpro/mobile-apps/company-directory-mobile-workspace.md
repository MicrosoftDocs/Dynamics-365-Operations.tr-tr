---
title: Şirket dizini mobil çalışma alanı
description: Bu konuda, kullanıcıların kuruluşları içindeki diğer personeli görmesini ve iletişim kurmasını sağlayan Şirket dizini mobil çalışma alanı hakkında bilgi verilmektedir.
author: jcart1106
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5a96955b72fcc5b0e2975f4bb1e619062be33e20
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248769"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="ddd15-103">Şirket dizini mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="ddd15-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddd15-104">Bu konu, **Şirket dizini** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ddd15-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="ddd15-105">Bu çalışma alanı, kullanıcıların kuruluşlarındaki diğer personelleri görmelerine ve onlarla iletişim kurmalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="ddd15-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="ddd15-106">Bu mobil çalışma alanı, Finance and Operations mobil uygulaması ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-106">This mobile workspace can be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="ddd15-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="ddd15-107">Overview</span></span>
<span data-ttu-id="ddd15-108">**Şirket dizini** mobil çalışma alanı, kullanıcıların şu görevleri yerine getirmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="ddd15-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="ddd15-109">Kuruluştaki personellerin bir listesini görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="ddd15-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="ddd15-110">Kuruluşta personel aramak.</span><span class="sxs-lookup"><span data-stu-id="ddd15-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="ddd15-111">Personeller için iletişim bilgilerini görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="ddd15-111">View contact information for employees.</span></span>
- <span data-ttu-id="ddd15-112">Personellerle, profil bilgisinden iletişim kurmak.</span><span class="sxs-lookup"><span data-stu-id="ddd15-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ddd15-113">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="ddd15-113">Prerequisites</span></span>
<span data-ttu-id="ddd15-114">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ddd15-115">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="ddd15-115">Prerequisite</span></span></th>
<th><span data-ttu-id="ddd15-116">Rol</span><span class="sxs-lookup"><span data-stu-id="ddd15-116">Role</span></span></th>
<th><span data-ttu-id="ddd15-117">Açıklama</span><span class="sxs-lookup"><span data-stu-id="ddd15-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ddd15-118">Aşağıdaki ürünlerden birinin kuruluşunuzda dağıtılmış olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="ddd15-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="ddd15-119">Bir Finance and Operations uygulaması</span><span class="sxs-lookup"><span data-stu-id="ddd15-119">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="ddd15-120">Microsoft Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="ddd15-120">Microsoft Dynamics 365 Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="ddd15-121">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="ddd15-121">System administrator</span></span></td>
<td><span data-ttu-id="ddd15-122">Kuruluşunuzda halihazırda dağıtılmış bir Finance and Operations uygulamanız yoksa <a href="../deployment/deploy-demo-environment.md">Bir tanıtım ortamı dağıtma</a> başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="ddd15-122">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="ddd15-123">Kuruluşunuzda Talent dağıtılmamışsa sistem yöneticisi <a href="https://www.microsoft.com/dynamics365/talent">Talent web sayfasından</a> bir deneme sürümüne erişim sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-123">If you don&#39;t already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ddd15-124"><strong>Şirket dizini</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="ddd15-125">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="ddd15-125">System administrator</span></span></td>
<td><span data-ttu-id="ddd15-126">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="ddd15-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="ddd15-127">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="ddd15-127">Download and install the mobile app</span></span>
<span data-ttu-id="ddd15-128">Finance and Operations mobil uygulamasını indirip yükleyin:</span><span class="sxs-lookup"><span data-stu-id="ddd15-128">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="ddd15-129">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="ddd15-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="ddd15-130">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="ddd15-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="ddd15-131">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="ddd15-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="ddd15-132">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="ddd15-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="ddd15-133">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="ddd15-134">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="ddd15-135">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="ddd15-136">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="ddd15-137">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ddd15-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="ddd15-138">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="ddd15-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="ddd15-139">Şirket dizinini mobil çalışma alanı kullanarak görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="ddd15-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="ddd15-140">Mobil uygulamada, **Şirket dizini** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="ddd15-141">Personellerin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="ddd15-142">Bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-142">Select an employee.</span></span> <span data-ttu-id="ddd15-143">**Personel profili** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="ddd15-144">Bu sayfadaki bilgiler arasında personelin adı, soyadı, unvanı ve bölümü bulunur.</span><span class="sxs-lookup"><span data-stu-id="ddd15-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="ddd15-145">Şirket dizinini mobil çalışma alanı kullanarak arayın</span><span class="sxs-lookup"><span data-stu-id="ddd15-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="ddd15-146">Mobil uygulamada, **Şirket dizini** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="ddd15-147">**Arama** alanında, bir personelin adını, soyadını, unvanını veya bölümünü, aramayı başlatmak için girin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="ddd15-148">Bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="ddd15-148">Select an employee.</span></span> <span data-ttu-id="ddd15-149">**Personel profili** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ddd15-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="ddd15-150">Bu sayfadaki bilgiler arasında personelin adı, soyadı, unvanı ve bölümü bulunur.</span><span class="sxs-lookup"><span data-stu-id="ddd15-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
