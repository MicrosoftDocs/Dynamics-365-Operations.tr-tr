---
title: Örneği kaldırma
description: Bu konuda, Microsoft Dynamics 365 Human Resources için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17f299f81d1326dfb06c11a6125acc54b8ef2a6e
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431211"
---
# <a name="remove-an-instance"></a><span data-ttu-id="6750d-103">Örneği kaldırma</span><span class="sxs-lookup"><span data-stu-id="6750d-103">Remove an instance</span></span>

<span data-ttu-id="6750d-104">Bu konuda, Microsoft Dynamics 365 Human Resources için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6750d-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="6750d-105">Bir test ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6750d-105">Remove a test drive environment</span></span>

<span data-ttu-id="6750d-106">İnsan Kaynakları test ortamları 60 günlük süre sonu ilkesi ile sunulur.</span><span class="sxs-lookup"><span data-stu-id="6750d-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="6750d-107">Ancak, test ortamları sahipleri aşağıdaki adımları uygulayarak denemelerini daha erken sonlandırabilir.</span><span class="sxs-lookup"><span data-stu-id="6750d-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="6750d-108">[Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6750d-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="6750d-109">**Ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-109">Select **Environments**.</span></span>
3. <span data-ttu-id="6750d-110">Test ortamını seçin. Test ortamı adı şuna benzer bir düzene sahiptir: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="6750d-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="6750d-111">**Sil**'i seçin ve kararı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="6750d-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="6750d-112">Var olan test ortamı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="6750d-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="6750d-113">Kaldırıldığında, yeni bir test ortamı için kaydolabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6750d-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="6750d-114">Bir üretim ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="6750d-114">Remove a production environment</span></span>

<span data-ttu-id="6750d-115">Bu konuda, İnsan Kaynaklarını bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="6750d-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="6750d-116">Tek bir İnsan Kaynakları ortamı tek bir Power Apps ortamı içinde "yer aldığından", dikkate alınması gereken iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="6750d-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="6750d-117">İlk seçenek tüm Power Apps ortamını kaldırmayı, ikinci seçenek yalnızca İnsan Kaynakları'nı kaldırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="6750d-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="6750d-118">İlk seçenek, Power Apps ortamını özellikle İnsan Kaynakları sağlamak için oluşturmuş, uygulamaya henüz başlamış veya herhangi bir tümleştirme yapmamış olmanız durumunda tercih edilir.</span><span class="sxs-lookup"><span data-stu-id="6750d-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="6750d-119">İkinci seçenek Power Apps ve Power Automate'ten alınan zengin verilerle doldurulan bir Power Apps ortamınız olması durumunda uygundur.</span><span class="sxs-lookup"><span data-stu-id="6750d-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="6750d-120">Power Apps ortamını kaldırmadan önce, İnsan Kaynakları kapsamı dışındaki zengin veri tümleştirmeleri için kullanılmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6750d-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="6750d-121">Varsayılan Power Apps ortamlarının da kaldırılamayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6750d-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="6750d-122">İnsan Kaynakları ve ilişkili uygulamalar ve akışlar dahil tüm Power Apps ortamını kaldırmak için:</span><span class="sxs-lookup"><span data-stu-id="6750d-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="6750d-123">[Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6750d-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="6750d-124">**Ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-124">Select **Environments**.</span></span>
3. <span data-ttu-id="6750d-125">Kaldırılacak ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="6750d-126">**Sil**'i seçin ve kararı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="6750d-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="6750d-127">Silme işlemi tamamlanana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="6750d-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="6750d-128">İnsan Kaynakları'na abone olmak için kullandığınız hesabı kullanarak [Lifecycle Services](https://lcs.dynamics.com/Logon/Index)'da (LCS) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6750d-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="6750d-129">Ortamı içeren İnsan Kaynakları Projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="6750d-130">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="6750d-131">Kaldırılacak örneği seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="6750d-132">**Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="6750d-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="6750d-133">İnsan Kaynakları ortamını mevcut bir Power Apps ortamından kaldırmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="6750d-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="6750d-134">Bu özellik doğrudan LCS içinden etkinleştirilene kadar, İnsan Kaynakları DevOps ekibine başvurmak ve destek almak geçicidir.</span><span class="sxs-lookup"><span data-stu-id="6750d-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="6750d-135">Kaldırma isteğini başlatmak için Destek birime başvurun.</span><span class="sxs-lookup"><span data-stu-id="6750d-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="6750d-136">Destek ekibi İnsan Kaynakları DevOps ekibiyle kaldırma isteğini başlatacaktır.</span><span class="sxs-lookup"><span data-stu-id="6750d-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="6750d-137">Ortamın kaldırıldığı hakkında bilgi aldıktan sonra devam edin.</span><span class="sxs-lookup"><span data-stu-id="6750d-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="6750d-138">İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak LCS'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6750d-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="6750d-139">Ortamı içeren İnsan Kaynakları Projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="6750d-140">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6750d-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="6750d-141">Kaldırmak istediğiniz örneği seçin. Bu örneğin Dağıtım durumu **Başarısız** olarak işaretlenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6750d-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="6750d-142">**Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="6750d-142">Select **Remove instance** and confirm your decision.</span></span> 
