---
title: Talent ortamlarını kaldırma
description: Bu konuda, Dynamics 365 Talent için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: bbc65a77b7c3df6545dfd7aa2109aba5c4e1b57b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773047"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="c1ec7-103">Talent ortamlarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1ec7-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1ec7-104">Bu konuda, Dynamics 365 Talent için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="c1ec7-105">Bir test ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1ec7-105">Removing a test drive environment</span></span>

<span data-ttu-id="c1ec7-106">Talent test ortamları 60 günlük süre sonu ilkesi ile sunulur.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="c1ec7-107">Ancak, test ortamları sahipleri aşağıdaki adımları uygulayarak denemelerini daha erken sonlandırabilir.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="c1ec7-108">[Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="c1ec7-109">**Ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-109">Select **Environments**.</span></span>
3. <span data-ttu-id="c1ec7-110">Test ortamını seçin. Test ortamı adı şuna benzer bir düzene sahiptir: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="c1ec7-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="c1ec7-111">**Sil**'i seçin ve kararı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="c1ec7-112">Var olan test ortamı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="c1ec7-113">Kaldırıldığında, yeni bir test ortamı için kaydolabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="c1ec7-114">Bir üretim ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c1ec7-114">Removing a production environment</span></span>

<span data-ttu-id="c1ec7-115">Bu konuda, Talent'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="c1ec7-116">Tek bir Talent ortamı tek bir Power Apps ortamı içinde "yer aldığından", dikkate alınması gereken iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-116">Since a single Talent environment is “contained” within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="c1ec7-117">İlk seçenek tüm Power Apps ortamını kaldırmayı, ikinci seçenek yalnızca Talent'ı kaldırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="c1ec7-118">İlk seçenek, Power Apps ortamını özellikle Talent sağlamak için oluşturmuş, uygulamaya henüz başlamış veya herhangi bir tümleştirme yapmamış olmanız durumunda tercih edilir.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="c1ec7-119">İkinci seçenek Power Apps ve Power Automate'ten alınan zengin verilerle doldurulan bir Power Apps ortamınız olması durumunda uygundur.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="c1ec7-120">Power Apps ortamını kaldırmadan önce, Talent kapsamı dışındaki zengin veri tümleştirmeleri için kullanılmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="c1ec7-121">Varsayılan Power Apps ortamlarının da kaldırılamayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="c1ec7-122">Talent ve ilişkili uygulamalar ve akışlar dahil tüm Power Apps ortamını kaldırmak için:</span><span class="sxs-lookup"><span data-stu-id="c1ec7-122">To remove the entire Power Apps environment, including Talent and the associated apps and flows:</span></span>

1. <span data-ttu-id="c1ec7-123">[Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="c1ec7-124">**Ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-124">Select **Environments**.</span></span>
3. <span data-ttu-id="c1ec7-125">Kaldırılacak ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="c1ec7-126">**Sil**'i seçin ve kararı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="c1ec7-127">Silme işlemi tamamlanana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="c1ec7-128">Talent'a abone olmak için kullandığınız hesabı kullanarak [Lifecycle Services](https://lcs.dynamics.com/Logon/Index)'da (LCS) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="c1ec7-129">Ortamı içeren Talent Projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="c1ec7-130">LCS projenizde **Talent Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="c1ec7-131">Kaldırılacak örneği seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="c1ec7-132">**Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="c1ec7-133">Talent ortamını mevcut bir Power Apps ortamından kaldırmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-133">To remove a Talent environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="c1ec7-134">Bu özellik doğrudan LCS içinden etkinleştirilene kadar, Talent DevOps ekibine başvurmak ve destek almak geçicidir.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="c1ec7-135">Kaldırma isteğini başlatmak için Destek birime başvurun.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="c1ec7-136">Destek ekibi Talent DevOps ekibiyle kaldırma isteğini başlatacaktır.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="c1ec7-137">Ortamın kaldırıldığı hakkında bilgi aldıktan sonra devam edin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="c1ec7-138">Talent'a abone olmak için kullandığınız hesabı kullanarak LCS'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="c1ec7-139">Ortamı içeren Talent projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="c1ec7-140">LCS projenizde **Talent Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="c1ec7-141">Kaldırmak istediğiniz örneği seçin. Bu örneğin Dağıtım durumu **Başarısız** olarak işaretlenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="c1ec7-142">**Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c1ec7-142">Select **Remove instance** and confirm your decision.</span></span> 

