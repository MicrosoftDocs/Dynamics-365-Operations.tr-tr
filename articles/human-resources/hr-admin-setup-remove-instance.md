---
title: Örneği kaldır
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010815"
---
# <a name="remove-an-instance"></a><span data-ttu-id="ac6e0-102">Örneği kaldır</span><span class="sxs-lookup"><span data-stu-id="ac6e0-102">Remove an instance</span></span>

<span data-ttu-id="ac6e0-103">Bu konuda, Microsoft Dynamics 365 Human Resources için bir test sürüşü kaldırma yeni bir üretim ortam işlemi adım adım anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="ac6e0-104">Bir test ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ac6e0-104">Remove a test drive environment</span></span>

<span data-ttu-id="ac6e0-105">İnsan Kaynakları test ortamları 60 günlük süre sonu ilkesi ile sunulur.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="ac6e0-106">Ancak, test ortamları sahipleri aşağıdaki adımları uygulayarak denemelerini daha erken sonlandırabilir.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="ac6e0-107">[Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="ac6e0-108">**Ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-108">Select **Environments**.</span></span>
3. <span data-ttu-id="ac6e0-109">Test ortamını seçin. Test ortamı adı şuna benzer bir düzene sahiptir: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="ac6e0-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="ac6e0-110">**Sil**'i seçin ve kararı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="ac6e0-111">Var olan test ortamı kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="ac6e0-112">Kaldırıldığında, yeni bir test ortamı için kaydolabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="ac6e0-113">Bir üretim ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ac6e0-113">Remove a production environment</span></span>

<span data-ttu-id="ac6e0-114">Bu konuda, İnsan Kaynaklarını bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla aldığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="ac6e0-115">Tek bir İnsan Kaynakları ortamı tek bir Power Apps ortamı içinde "yer aldığından", dikkate alınması gereken iki seçenek vardır.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="ac6e0-116">İlk seçenek tüm Power Apps ortamını kaldırmayı, ikinci seçenek yalnızca İnsan Kaynakları'nı kaldırmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="ac6e0-117">İlk seçenek, Power Apps ortamını özellikle İnsan Kaynakları sağlamak için oluşturmuş, uygulamaya henüz başlamış veya herhangi bir tümleştirme yapmamış olmanız durumunda tercih edilir.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="ac6e0-118">İkinci seçenek Power Apps ve Power Automate'ten alınan zengin verilerle doldurulan bir Power Apps ortamınız olması durumunda uygundur.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="ac6e0-119">Power Apps ortamını kaldırmadan önce, İnsan Kaynakları kapsamı dışındaki zengin veri tümleştirmeleri için kullanılmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="ac6e0-120">Varsayılan Power Apps ortamlarının da kaldırılamayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="ac6e0-121">İnsan Kaynakları ve ilişkili uygulamalar ve akışlar dahil tüm Power Apps ortamını kaldırmak için:</span><span class="sxs-lookup"><span data-stu-id="ac6e0-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="ac6e0-122">[Power Apps Yönetim Merkezi](https://admin.businessplatform.microsoft.com/)'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="ac6e0-123">**Ortamlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-123">Select **Environments**.</span></span>
3. <span data-ttu-id="ac6e0-124">Kaldırılacak ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="ac6e0-125">**Sil**'i seçin ve kararı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="ac6e0-126">Silme işlemi tamamlanana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="ac6e0-127">İnsan Kaynakları'na abone olmak için kullandığınız hesabı kullanarak [Lifecycle Services](https://lcs.dynamics.com/Logon/Index)'da (LCS) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="ac6e0-128">Ortamı içeren İnsan Kaynakları Projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="ac6e0-129">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="ac6e0-130">Kaldırılacak örneği seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="ac6e0-131">**Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="ac6e0-132">İnsan Kaynakları ortamını mevcut bir Power Apps ortamından kaldırmak için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="ac6e0-133">Bu özellik doğrudan LCS içinden etkinleştirilene kadar, İnsan Kaynakları DevOps ekibine başvurmak ve destek almak geçicidir.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="ac6e0-134">Kaldırma isteğini başlatmak için Destek birime başvurun.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="ac6e0-135">Destek ekibi İnsan Kaynakları DevOps ekibiyle kaldırma isteğini başlatacaktır.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="ac6e0-136">Ortamın kaldırıldığı hakkında bilgi aldıktan sonra devam edin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="ac6e0-137">İnsan Kaynaklarına abone olmak için kullandığınız hesabı kullanarak LCS'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="ac6e0-138">Ortamı içeren İnsan Kaynakları Projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="ac6e0-139">LCS projenizde **İnsan Kaynakları Uygulama Yöneticisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="ac6e0-140">Kaldırmak istediğiniz örneği seçin. Bu örneğin Dağıtım durumu **Başarısız** olarak işaretlenmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="ac6e0-141">**Örneği kaldır**'ı seçin ve ardından kararınızı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="ac6e0-141">Select **Remove instance** and confirm your decision.</span></span> 
