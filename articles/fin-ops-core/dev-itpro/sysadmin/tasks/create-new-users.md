---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570533"
---
# <a name="create-new-users"></a><span data-ttu-id="bf3d9-103">Yeni kullanıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="bf3d9-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf3d9-104">Kullanıcılar, işlerini gerçekleştirmek için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="bf3d9-105">Kullanıcıyı lisansla ilişkilendirme (yalnızca yeni lisans türleri)</span><span class="sxs-lookup"><span data-stu-id="bf3d9-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="bf3d9-106">2019 Ekim tarihinde eklenen yeni lisans türlerinden birinde olan müşterilerimiz için, kullanıcıların bir lisansla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="bf3d9-107">Bir lisans ile ilişkilendirilen kullanıcılar, ilk oturum açtıklarında otomatik olarak rolü olmayan sistem kullanıcıları olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="bf3d9-108">Bir lisans ile ilişkili olmayan kullanıcılar bir uyarı iletisi alır.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="bf3d9-109">Sistem yöneticileri [Microsoft 365 yönetim merkezinden](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) [kullanıcılara lisans atayabilir](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) .</span><span class="sxs-lookup"><span data-stu-id="bf3d9-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="bf3d9-110">Yeni bir kullanıcı ekle</span><span class="sxs-lookup"><span data-stu-id="bf3d9-110">Add a new user</span></span>
1. <span data-ttu-id="bf3d9-111">**Sistem yönetimi \> Kullanıcılar \> Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="bf3d9-112">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="bf3d9-113">**Kullanıcı Kimliği** alanına, kullanıcı için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="bf3d9-114">Bir kullanıcı kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-114">A user ID is required.</span></span>  
4. <span data-ttu-id="bf3d9-115">**Kullanıcı adı** alanına, kullanıcının adını girin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="bf3d9-116">**Etki alanı** alanına, kullanıcının etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="bf3d9-117">**Diğer ad** alanına kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="bf3d9-118">**Şirket** alanında, istenilen şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="bf3d9-119">**Kullanıcı rolleri** hızlı sekmesinde, **Rol ata**'yı seçerek [kullanıcılara güvenlik rolleri atayın](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="bf3d9-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="bf3d9-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-120">Select **OK**.</span></span>
10. <span data-ttu-id="bf3d9-121">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="bf3d9-122">Kullanıcıları içe aktar</span><span class="sxs-lookup"><span data-stu-id="bf3d9-122">Import users</span></span>
1. <span data-ttu-id="bf3d9-123">Eylem Bölmesinde, **Kullanıcıları içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="bf3d9-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bf3d9-125">**Kullanıcıları içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-125">Select **Import users**.</span></span>
4. <span data-ttu-id="bf3d9-126">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bf3d9-126">Select **Close**.</span></span>

