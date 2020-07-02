---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435596"
---
# <a name="create-new-users"></a><span data-ttu-id="92ed4-103">Yeni kullanıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="92ed4-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92ed4-104">Kullanıcılar, işlerini gerçekleştirmek için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.</span><span class="sxs-lookup"><span data-stu-id="92ed4-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="92ed4-105">Kullanıcıyı lisansla ilişkilendirme (yalnızca yeni lisans türleri)</span><span class="sxs-lookup"><span data-stu-id="92ed4-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="92ed4-106">2019 Ekim tarihinde eklenen yeni lisans türlerinden birinde olan müşterilerimiz için, kullanıcıların bir lisansla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="92ed4-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="92ed4-107">Bir lisans ile ilişkilendirilen kullanıcılar, ilk oturum açtıklarında otomatik olarak rolü olmayan sistem kullanıcıları olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="92ed4-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="92ed4-108">Sistem yöneticileri [Microsoft 365 yönetim merkezinden](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) [kullanıcılara lisans atayabilir](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) .</span><span class="sxs-lookup"><span data-stu-id="92ed4-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="92ed4-109">Harici kullanıcıyı lisansla ilişkilendirme (yalnızca yeni lisans türleri)</span><span class="sxs-lookup"><span data-stu-id="92ed4-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="92ed4-110">Ortamın dağıtıldığı kiracının harici kullanıcılarının lisanslara atanabilmeleri için ana bilgisayar kiracı dizininde (Azure Active Directory (Azure AD)) sunulmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="92ed4-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="92ed4-111">Bu harici kullanıcılar Azure AD'de kiracıya konuk kullanıcı olarak eklenmeli ve sonra uygun lisanslara atanmalıdırlar.</span><span class="sxs-lookup"><span data-stu-id="92ed4-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="92ed4-112">Daha fazla bilgi için bkz. [Azure portalında Azure Active Directory B2B işbirliği kullanıcıları ekleme](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="92ed4-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="92ed4-113">Yeni bir kullanıcı ekle</span><span class="sxs-lookup"><span data-stu-id="92ed4-113">Add a new user</span></span>
1. <span data-ttu-id="92ed4-114">**Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="92ed4-115">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="92ed4-116">**Kullanıcı Kimliği** alanına, kullanıcı için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="92ed4-117">Bir kullanıcı kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="92ed4-117">A user ID is required.</span></span>  
4. <span data-ttu-id="92ed4-118">**Kullanıcı adı** alanına, kullanıcının adını girin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="92ed4-119">**Etki alanı** alanına, kullanıcının etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="92ed4-120">**Diğer ad** alanına kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="92ed4-121">**Şirket** alanında, istenilen şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="92ed4-122">**Kullanıcı rolleri** hızlı sekmesinde, **Rolleri ata**'yı seçerek kullanıcıları güvenlik rollerine atayın.</span><span class="sxs-lookup"><span data-stu-id="92ed4-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="92ed4-123">Daha fazla bilgi için bkz. [Kullanıcıları güvenlik rollerine atama](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="92ed4-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="92ed4-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-124">Select **OK**.</span></span>
10. <span data-ttu-id="92ed4-125">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="92ed4-126">Kullanıcıları içe aktar</span><span class="sxs-lookup"><span data-stu-id="92ed4-126">Import users</span></span>
1. <span data-ttu-id="92ed4-127">**Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="92ed4-128">Eylem Bölmesinde, **Kullanıcıları içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="92ed4-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="92ed4-130">**Kullanıcıları içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-130">Select **Import users**.</span></span>
5. <span data-ttu-id="92ed4-131">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="92ed4-131">Select **Close**.</span></span>

