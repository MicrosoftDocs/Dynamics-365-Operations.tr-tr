---
title: Görev ayrımındaki çakışmaları tanımlama ve çözümleme
description: Bu konu görev ayrımındaki çakışmalarının nasıl tanımlandığını ve çözümlendiğini açıklar.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ebd59c7018a50e01253697d792698664a981566
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745825"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="24602-103">Görev ayrımındaki çakışmaları tanımlama ve çözümleme</span><span class="sxs-lookup"><span data-stu-id="24602-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24602-104">Bu konu görev ayrımındaki çakışmalarının nasıl tanımlandığını ve çözümlendiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="24602-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="24602-105">Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24602-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="24602-106">Bu kavram, görev ayrımı adını taşır.</span><span class="sxs-lookup"><span data-stu-id="24602-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="24602-107">Güvenlik rolü tanımı veya bir kullanıcının rol atamaları kuralları ihlal ederse, çakışma kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="24602-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="24602-108">Tüm çakışmaların yönetici tarafından düzeltilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="24602-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="24602-109">Çakışmaları çözmek ve tanımlamak için aşağıdaki yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="24602-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="24602-110">Kural eklendikten sonra, mevcut tüm rollerin uyumlu olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="24602-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="24602-111">Mevcut rollerin ve görevlerin yeni görev ayırma kurallarıyla uyumlu olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="24602-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="24602-112">**Sistem yönetimi** > **Güvenlik** > **Görev ayrımı** > **Görev ayrımı kuralları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="24602-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="24602-113">**Görevleri ve rolleri doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="24602-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="24602-114">Herhangi bir rol kuralları ihlal ediyorsa, kuralın ve rolün - adını ve çakışan görevlerin adlarını içeren bir ileti görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="24602-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="24602-115">Çakışan roller **Güvenlik yapılandırması** kullanılarak değiştirilmeli ve çakışan görevleri içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="24602-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="24602-116">Eğer hiçbir rol seçili kuralı ihlal etmiyorsa, tüm kuralların uygun olduğunu belirten bir ileti görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="24602-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="24602-117">Doğrulama yalnızca seçili kural için gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="24602-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="24602-118">Her kural için uyumluluğu doğrulamanız önemlidir.</span><span class="sxs-lookup"><span data-stu-id="24602-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="24602-119">Bir rol oluşturduğunuzda veya değiştirdiğinizde, görev ayrımı kuralları otomatik olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="24602-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="24602-120">Çakışmaya neden olan görevleri bir role atayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="24602-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="24602-121">Daha sonra, mevcut tüm rol atamalarının uyumlu olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="24602-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="24602-122">Kullanıcı rolü atamalarının yeni görev ayırma kurallarıyla uyumlu olduğunu doğrulama</span><span class="sxs-lookup"><span data-stu-id="24602-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="24602-123">**Sistem Yönetimi > Güvenlik > Görev ayrımı > Kullanıcı rolü atamalarının uygunluğunu doğrulayın** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="24602-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="24602-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="24602-124">Select **OK**.</span></span> <span data-ttu-id="24602-125">Bir bildirim doğrulamanın sonuçlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="24602-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="24602-126">Çakışmalar, **Görev ayırma çözümlenmemiş çakışmaları** sayfasında günlüğe kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="24602-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="24602-127">Rollere kullanıcı atadığınızda, görev ayrımı kuralları otomatik olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="24602-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="24602-128">Çakışan görevler içeren rollere bir kullanıcı atamayı denerseniz hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="24602-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="24602-129">Ek rol atamasını reddederek ya da izin vererek çakışmayı çözmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="24602-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="24602-130">Atamaya izin verildiğinde ek rol atanır.</span><span class="sxs-lookup"><span data-stu-id="24602-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="24602-131">Active Directory Etki Alanı gruplarına dayalı olarak rol atanmış kullanıcılar için çakışmalar şu anda doğrulanmaz.</span><span class="sxs-lookup"><span data-stu-id="24602-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="24602-132">Çakışan kullanıcı rolü atamalarını görüntüleyin ve çözümleyin</span><span class="sxs-lookup"><span data-stu-id="24602-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="24602-133">**Sistem yönetimi** > **Güvenlik** > **Görev ayrımı** > **Görev ayırma çözümlenmemiş çakışmaları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="24602-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="24602-134">Bir çakışma seçin ve daha sonra aşağıdaki eylemlerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="24602-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="24602-135">**Atamayı reddet**: Bu eylem, kullanıcının ek güvenlik rolüne atanmasını reddeder.</span><span class="sxs-lookup"><span data-stu-id="24602-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="24602-136">Eğer otomatik rol atamayı reddederseniz, kullanıcı rolden dışarıda olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="24602-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="24602-137">Dışarıda tutulan kullanıcı, rol ile ilişkili olan erişimlere sahip olmaz ve yönetici dışarıda tutulmayı kaldırana kadar role atanamaz.</span><span class="sxs-lookup"><span data-stu-id="24602-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="24602-138">**Atamaya izin ver**: Bu işlem, çakışmayı geçersiz kılar ve kullanıcının ek güvenlik rolüne atanmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="24602-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="24602-139">Bir çakışmayı geçersiz kılarsanız, **Geçersiz kılma nedeni** için bir söz konusu alana bir sebep girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="24602-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="24602-140">Geçersiz kılınan tüm rol atamaları, **Görev ayrımı çakışmaları** sayfasında görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="24602-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="24602-141">Aynı kullanıcı için birden fazla çakışma listeleniyorsa kullanıcı kaydını seçin ve atanan rolleri **Kullanıcılar** sayfasında değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="24602-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="24602-142">Bu çakışmayı önlemek için, eklendikten veya değiştirildikten sonra her kuralı doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="24602-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]