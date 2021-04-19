---
title: e-Ticaret kullanıcıları ve rolleri yönetme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizin geliştirme ortamına kullanıcıların erişmelerine nasıl izin verileceğini açıklamaktadır.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 44b02f262136c0d970ca9eee3e5e63ef6dc8ccb7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794295"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="0553c-103">e-Ticaret kullanıcıları ve rolleri yönetme</span><span class="sxs-lookup"><span data-stu-id="0553c-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0553c-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizin geliştirme ortamına kullanıcıların erişmelerine nasıl izin verileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0553c-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="0553c-105">Kullanıcı erişiminin denetimine yardımcı olmak ve belirli görevleri gerçekleştirmek için kullanıcılara izin vermek istiyorsanız, site geliştirme ortamı, Microsoft Azure Active Directory (Azure AD) uygulamasında oluşturduğunuz güvenlik gruplarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="0553c-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="0553c-106">İlk olarak, geliştirme ortamındaki her role Azure AD'den yeni veya varolan bir güvenlik grubu atarsınız.</span><span class="sxs-lookup"><span data-stu-id="0553c-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="0553c-107">Daha sonra, bu kullanıcıları uygun bir güvenlik grubuna ekleyerek veya bir güvenlik grubundan kaldırarak bireysel kullanıcılar için izinleri verirsiniz veya iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0553c-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="0553c-108">Geliştirme ortamındaki rollere genel bakış</span><span class="sxs-lookup"><span data-stu-id="0553c-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="0553c-109">Dynamics 365 for Commerce düzenleme ortamı aşağıdaki rolleri destekler.</span><span class="sxs-lookup"><span data-stu-id="0553c-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="0553c-110">Rol</span><span class="sxs-lookup"><span data-stu-id="0553c-110">Role</span></span>                 | <span data-ttu-id="0553c-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="0553c-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="0553c-112">Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="0553c-112">System Administrator</span></span> | <span data-ttu-id="0553c-113">Bu role sahip kullanıcıların tüm araçlar ve tüm derecelendirmeler ve incelemeler için tüm öncelikleri vardır.</span><span class="sxs-lookup"><span data-stu-id="0553c-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="0553c-114">Siteler de oluşturabilirler.</span><span class="sxs-lookup"><span data-stu-id="0553c-114">They can also create sites.</span></span> |
| <span data-ttu-id="0553c-115">Yönetici</span><span class="sxs-lookup"><span data-stu-id="0553c-115">Administrator</span></span>   | <span data-ttu-id="0553c-116">Bu role sahip kullanıcıların, belirli bir site yapısındaki tüm araçlar ve RnR ayrıcalıklarına sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0553c-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="0553c-117">Web üreticisi</span><span class="sxs-lookup"><span data-stu-id="0553c-117">Web Producer</span></span>         | <span data-ttu-id="0553c-118">Bu role sahip kullanıcılar, sayfalar, parçalar ve şablonlar oluşturabilir, varlıkları karşıya yükleyebilir ve yönetebilir, zengin ürün ve kategorileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0553c-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="0553c-119">Okuyucu</span><span class="sxs-lookup"><span data-stu-id="0553c-119">Reader</span></span>               | <span data-ttu-id="0553c-120">Bu role sahip kullanıcılar sayfaları, şablonları, varlıkları, parçaları, düzenleri ve ayarları görüntüleyebilir, ancak değişiklik yapamaz.</span><span class="sxs-lookup"><span data-stu-id="0553c-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="0553c-121">RnR Moderatörü</span><span class="sxs-lookup"><span data-stu-id="0553c-121">RnR Moderator</span></span>        | <span data-ttu-id="0553c-122">Bu role sahip kullanıcılar, ürün incelemelerinin orta olmasını içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0553c-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="0553c-123">Sistem Yöneticisi rolü</span><span class="sxs-lookup"><span data-stu-id="0553c-123">System Administrator role</span></span>

<span data-ttu-id="0553c-124">Microsoft Dynamics Lifecycle Services (LCS) ortamında Dynamics 365 Commerce sağladığınızda, **Sistem Yöneticisi** rolü için bir güvenlik grubu sağlamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="0553c-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="0553c-125">Bu rol, konfigüre ettiğiniz ortamda oluşturduğunuz tüm sitelere otomatik olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="0553c-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="0553c-126">Bu rolün güvenlik grubu yalnızca LCS'de güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0553c-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="0553c-127">Tüm sitelerin **site yönetim** sayfasında salt okunur olarak görünür ve yalnızca bilgilendirme amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="0553c-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="0553c-128">Yönetici rolü</span><span class="sxs-lookup"><span data-stu-id="0553c-128">Administrator role</span></span>

<span data-ttu-id="0553c-129">Commerce'ta yeni bir site oluşturduğunuzda, **yönetici** rolü için bir güvenlik grubu sağlamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="0553c-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="0553c-130">Bu rolün verdiği izinlere genel bakış için bu konunun yukarısındaki tabloya bakın.</span><span class="sxs-lookup"><span data-stu-id="0553c-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="0553c-131">Güvenlik grupları Ekle veya güncelleştir</span><span class="sxs-lookup"><span data-stu-id="0553c-131">Add or update security groups</span></span>

<span data-ttu-id="0553c-132">Siteniz oluşturulduktan sonra, yalnızca **Sistem Yöneticisi** ve **Yönetici** rolleriyle ilişkilendirilmiş güvenlik gruplarında olan kullanıcılar o sitenin geliştirme ortamına erişebilir.</span><span class="sxs-lookup"><span data-stu-id="0553c-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="0553c-133">**Web Üreticisi**, **RNR moderatör** ve **Okuyucu** rollerine Kullanıcı atamak için, bu rollere güvenlik grupları atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0553c-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="0553c-134">Bir role güvenlik grubu eklemek veya bir role atanmış olan bir güvenlik grubunu güncelleştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0553c-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="0553c-135">Güncelleştirmek istediğiniz siteye gidin.</span><span class="sxs-lookup"><span data-stu-id="0553c-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="0553c-136">**Site Yönetimi**'nde, **güvenlik** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="0553c-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="0553c-137">Değiştirilecek rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="0553c-137">Select the role to modify.</span></span>
1. <span data-ttu-id="0553c-138">Rollere güvenlik grupları ekleyin veya rollerden güvenlik gruplarını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0553c-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0553c-139">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0553c-139">Additional resources</span></span>

[<span data-ttu-id="0553c-140">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="0553c-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="0553c-141">Siteniz için arama motoru optimizasyonu (SEO) konuları</span><span class="sxs-lookup"><span data-stu-id="0553c-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="0553c-142">İçerik Güvenliği İlkesini (CSP) yönetme</span><span class="sxs-lookup"><span data-stu-id="0553c-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]