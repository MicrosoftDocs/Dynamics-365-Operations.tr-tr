---
title: Kullanıcıları güvenlik rollerine atama
description: Finance and Operations uygulamalarına erişim sağlamak için kullanıcıların güvenlik rollerine atanmış olmaları gerekir.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808008"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="e53dd-103">Kullanıcıları güvenlik rollerine atama</span><span class="sxs-lookup"><span data-stu-id="e53dd-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e53dd-104">Ortak yetenekler dışında herhangi bir şey kullanmak için, kullanıcıların güvenlik rollerine atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e53dd-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="e53dd-105">Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e53dd-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="e53dd-106">Kullanıcıları rollere otomatik olarak ata</span><span class="sxs-lookup"><span data-stu-id="e53dd-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="e53dd-107">**Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="e53dd-108">Ağaçta, 'Muhasebe yöneticisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="e53dd-109">Kuralı yapılandırmak istediğiniz rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="e53dd-110">Bu örnekte, Muhasebe yöneticisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="e53dd-111">İletişim kutusunu açmak için **Kural ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="e53dd-112">**Sorgu seçin**listesinde, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="e53dd-113">Bu kuralda kullanılacak sorguyu seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="e53dd-114">**Üyelik kuralı adı** listesinde, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e53dd-115">**Sorguyu düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-115">Click **Edit query**.</span></span> <span data-ttu-id="e53dd-116">Sorguyu gerektiği gibi düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="e53dd-117">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-117">Click **OK**.</span></span>
8. <span data-ttu-id="e53dd-118">**Otomatik rol atamayı çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="e53dd-119">**Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin (ideal olarak ayrı bir tarayıcı sekmesinde).</span><span class="sxs-lookup"><span data-stu-id="e53dd-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="e53dd-120">Rol atama sorgusunun doğru olduğunu onaylamak için çeşitli kullanıcılara atanan rolleri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="e53dd-121">Gerekirse ayarlayın ve yeniden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="e53dd-122">Kullanıcıları otomatik rol atamasının dışında bırakmak</span><span class="sxs-lookup"><span data-stu-id="e53dd-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="e53dd-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-123">Close the page.</span></span>
2. <span data-ttu-id="e53dd-124">**Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="e53dd-125">Ağaçta, 'Muhasebe yöneticisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="e53dd-126">Bir rol seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-126">Select a role.</span></span> <span data-ttu-id="e53dd-127">Bu örnek için, Muhasebe yöneticisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="e53dd-128">**Role atanmış kullanıcılar** menüsünde, **Kullanıcıları el ile ata/dışarıda tut**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="e53dd-129">**Kullanıcıları role atayın veya rol dışında bırakın** listesinde, seçili satırları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="e53dd-130">Bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-130">Select a user.</span></span>  
6. <span data-ttu-id="e53dd-131">**Eylem bölmesi**'nde, **Rol dışında bırakın**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="e53dd-132">Seçili kullanıcıları rolün dışında bırakmak için **Rol dışında bırakın**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e53dd-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="e53dd-133">Dışarıda bırakmaları kaldırmak için, hariç tutulma durumunu kaldırmak istediğiniz kullanıcıları seçin ve sonra **Durumu sıfırla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e53dd-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="e53dd-134">Bir kullanıcının durumunu sıfırlayarak bir hariç tutmayı kaldırdığınızda, kullanıcının rolü otomatik olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="e53dd-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="e53dd-135">Ancak, durumunu sıfırladığınızda, kullanıcı hemen role atanmaz veya rolden hariç tutulmaz.</span><span class="sxs-lookup"><span data-stu-id="e53dd-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="e53dd-136">Bunun yerine kullanıcı otomatik rol atama bir sonraki çalıştığında rolüne eklenir veya çıkartılır.</span><span class="sxs-lookup"><span data-stu-id="e53dd-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
