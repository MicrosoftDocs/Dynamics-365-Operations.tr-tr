---
title: "Şirket dizini mobil çalışma alanı"
description: "Bu konu, kullanıcıların kuruluşları içindeki diğer personelleri görmelerine ve iletişim kurmalarına sağlayan Şirket dizini mobil çalışma alanı hakkında bilgi sağlar."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Talent, Operations
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73062587a2cfed3af212f618df48a26df574ee87
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="d543e-103">Şirket dizini mobil çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="d543e-103">Company directory mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d543e-104">Bu konu, **Şirket dizini** mobil çalışma alanı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d543e-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="d543e-105">Bu çalışma alanı, kullanıcıların kuruluşlarındaki diğer personelleri görmelerine ve onlarla iletişim kurmalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="d543e-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="d543e-106">Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations mobil uygulaması ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d543e-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="d543e-107">Özet</span><span class="sxs-lookup"><span data-stu-id="d543e-107">Overview</span></span>
<span data-ttu-id="d543e-108">**Şirket dizini** mobil çalışma alanı, kullanıcıların şu görevleri yerine getirmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="d543e-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="d543e-109">Kuruluştaki personellerin bir listesini görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="d543e-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="d543e-110">Kuruluşta personel aramak.</span><span class="sxs-lookup"><span data-stu-id="d543e-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="d543e-111">Personeller için iletişim bilgilerini görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="d543e-111">View contact information for employees.</span></span>
- <span data-ttu-id="d543e-112">Personellerle, profil bilgisinden iletişim kurmak.</span><span class="sxs-lookup"><span data-stu-id="d543e-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d543e-113">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="d543e-113">Prerequisites</span></span>
<span data-ttu-id="d543e-114">Bu mobil çalışma alanını kullanmadan önce, aşağıdaki gereksinimleri karşılamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d543e-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d543e-115">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="d543e-115">Prerequisite</span></span></th>
<th><span data-ttu-id="d543e-116">Rol</span><span class="sxs-lookup"><span data-stu-id="d543e-116">Role</span></span></th>
<th><span data-ttu-id="d543e-117">Açıklama</span><span class="sxs-lookup"><span data-stu-id="d543e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d543e-118">Aşağıdaki ürünlerden birinin kuruluşunuzda dağıtılmış olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="d543e-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="d543e-119">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017)</span><span class="sxs-lookup"><span data-stu-id="d543e-119">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span></li>
<li><span data-ttu-id="d543e-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="d543e-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="d543e-121">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="d543e-121">System administrator</span></span></td>
<td><span data-ttu-id="d543e-122">Kuruluşunuzda Finance and Operations zaten mevcut değilse, bkz. <a href="../deployment/deploy-demo-environment.md">Bir gösteri ortamı dağıtmak</a>.</span><span class="sxs-lookup"><span data-stu-id="d543e-122">If you don't already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="d543e-123">Kuruluşunuzda Talent dağıtılmış değilse, sistem yöneticisi bir deneme sürümüne <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent web sitesi</a> üzerinden erişebilir.</span><span class="sxs-lookup"><span data-stu-id="d543e-123">If you don't already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d543e-124"><strong>Şirket dizini</strong> mobil çalışma alanını yayımlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d543e-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="d543e-125">Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="d543e-125">System administrator</span></span></td>
<td><span data-ttu-id="d543e-126">Bkz. <a href="publish-mobile-workspace.md">Mobil çalışma alanı yayınlama</a>.</span><span class="sxs-lookup"><span data-stu-id="d543e-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d543e-127">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="d543e-127">Download and install the mobile app</span></span>
<span data-ttu-id="d543e-128">Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:</span><span class="sxs-lookup"><span data-stu-id="d543e-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="d543e-129">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="d543e-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d543e-130">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="d543e-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d543e-131">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="d543e-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="d543e-132">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="d543e-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d543e-133">Microsoft Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="d543e-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d543e-134">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="d543e-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d543e-135">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="d543e-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="d543e-136">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="d543e-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d543e-137">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d543e-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="d543e-138">[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d543e-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="d543e-139">Şirket dizinini mobil çalışma alanı kullanarak görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="d543e-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="d543e-140">Mobil uygulamada, **Şirket dizini** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="d543e-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="d543e-141">Personellerin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d543e-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="d543e-142">Bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="d543e-142">Select an employee.</span></span> <span data-ttu-id="d543e-143">**Personel profili** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d543e-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="d543e-144">Bu sayfadaki bilgiler arasında personelin adı, soyadı, unvanı ve bölümü bulunur.</span><span class="sxs-lookup"><span data-stu-id="d543e-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="d543e-145">Şirket dizinini mobil çalışma alanı kullanarak arayın</span><span class="sxs-lookup"><span data-stu-id="d543e-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="d543e-146">Mobil uygulamada, **Şirket dizini** çalışma alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="d543e-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="d543e-147">**Arama** alanında, bir personelin adını, soyadını, unvanını veya bölümünü, aramayı başlatmak için girin.</span><span class="sxs-lookup"><span data-stu-id="d543e-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="d543e-148">Bir çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="d543e-148">Select an employee.</span></span> <span data-ttu-id="d543e-149">**Personel profili** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d543e-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="d543e-150">Bu sayfadaki bilgiler arasında personelin adı, soyadı, unvanı ve bölümü bulunur.</span><span class="sxs-lookup"><span data-stu-id="d543e-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
