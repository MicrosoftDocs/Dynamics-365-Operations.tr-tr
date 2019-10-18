---
title: Kullanıcıları güvenlik rollerine atama
description: Finance and Operations uygulamalarına erişim sağlamak için kullanıcıların güvenlik rollerine atanmış olmaları gerekir.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180979"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="0411b-103">Kullanıcıları güvenlik rollerine atama</span><span class="sxs-lookup"><span data-stu-id="0411b-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0411b-104">Ortak yetenekler dışında herhangi bir şey kullanmak için, kullanıcıların güvenlik rollerine atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0411b-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="0411b-105">Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="0411b-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="0411b-106">Kullanıcıları rollere otomatik olarak ata</span><span class="sxs-lookup"><span data-stu-id="0411b-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="0411b-107">**Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0411b-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="0411b-108">Ağaçta, 'Muhasebe yöneticisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="0411b-109">Kuralı yapılandırmak istediğiniz rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="0411b-110">Bu örnekte, Muhasebe yöneticisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="0411b-111">İletişim kutusunu açmak için **Kural ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0411b-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="0411b-112">**Sorgu seçin**listesinde, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="0411b-113">Bu kuralda kullanılacak sorguyu seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="0411b-114">**Üyelik kuralı adı** listesinde, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0411b-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0411b-115">**Sorguyu düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0411b-115">Click **Edit query**.</span></span> <span data-ttu-id="0411b-116">Sorguyu gerektiği gibi düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="0411b-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="0411b-117">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0411b-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="0411b-118">Kullanıcıları otomatik rol atamasının dışında bırakmak</span><span class="sxs-lookup"><span data-stu-id="0411b-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="0411b-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0411b-119">Close the page.</span></span>
2. <span data-ttu-id="0411b-120">**Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Kullanıcılara roller atayın**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="0411b-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="0411b-121">Ağaçta, 'Muhasebe yöneticisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="0411b-122">Bir rol seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-122">Select a role.</span></span> <span data-ttu-id="0411b-123">Bu örnek için, Muhasebe yöneticisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="0411b-124">**Role atanmış kullanıcılar** menüsünde, **Kullanıcıları el ile ata/dışarıda tut**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="0411b-125">**Kullanıcıları role atayın veya rol dışında bırakın** listesinde, seçili satırları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0411b-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="0411b-126">Bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-126">Select a user.</span></span>  
6. <span data-ttu-id="0411b-127">**Eylem bölmesi**'nde, **Rol dışında bırakın**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="0411b-128">Seçili kullanıcıları rolün dışında bırakmak için **Rol dışında bırakın**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0411b-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="0411b-129">Dışarıda bırakmaları kaldırmak için, hariç tutulma durumunu kaldırmak istediğiniz kullanıcıları seçin ve sonra **Durumu sıfırla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0411b-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="0411b-130">Bir kullanıcının durumunu sıfırlayarak bir hariç tutmayı kaldırdığınızda, kullanıcının rolü otomatik olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="0411b-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="0411b-131">Ancak, durumunu sıfırladığınızda, kullanıcı hemen role atanmaz veya rolden hariç tutulmaz.</span><span class="sxs-lookup"><span data-stu-id="0411b-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="0411b-132">Bunun yerine kullanıcı otomatik rol atama bir sonraki çalıştığında rolüne eklenir veya çıkartılır.</span><span class="sxs-lookup"><span data-stu-id="0411b-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
