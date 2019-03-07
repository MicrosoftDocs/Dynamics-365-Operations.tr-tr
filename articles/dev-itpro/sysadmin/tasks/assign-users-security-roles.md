---
title: Kullanıcıları güvenlik rollerine atama
description: Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a erişmek için kullanıcıların güvenlik rolleri atanmış olmalıdır.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "349964"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="49ec3-103">Kullanıcıları güvenlik rollerine atama</span><span class="sxs-lookup"><span data-stu-id="49ec3-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49ec3-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a erişmek için kullanıcıların güvenlik rolleri atanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49ec3-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="49ec3-105">Bu yordam sistem yöneticilerinin kullanıcıları iş verilerine dayalı olarak rollere otomatik olarak nasıl atayabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="49ec3-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="49ec3-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="49ec3-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="49ec3-107">Kullanıcıları rollere otomatik olarak ata</span><span class="sxs-lookup"><span data-stu-id="49ec3-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="49ec3-108">Sistem Yönetimi > Güvenlik > Kullanıcılara roller atayın'a gidin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="49ec3-109">Ağaçta, 'Muhasebe yöneticisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="49ec3-110">Kuralı yapılandırmak istediğiniz rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="49ec3-111">Bu örnekte, Muhasebe yöneticisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="49ec3-112">İletişim kutusunu açmak için Kural ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="49ec3-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="49ec3-114">Bu kuralda kullanılacak sorguyu seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="49ec3-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="49ec3-116">Sorguyu düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-116">Click Edit query.</span></span>
    * <span data-ttu-id="49ec3-117">Sorguyu gerektiği gibi düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="49ec3-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="49ec3-119">Kullanıcıları otomatik rol atamasının dışında bırakmak</span><span class="sxs-lookup"><span data-stu-id="49ec3-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="49ec3-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-120">Close the page.</span></span>
2. <span data-ttu-id="49ec3-121">Sistem Yönetimi > Güvenlik > Kullanıcılara roller atayın'a gidin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="49ec3-122">Ağaçta, 'Muhasebe yöneticisi' seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="49ec3-123">Bir rol seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-123">Select a role.</span></span> <span data-ttu-id="49ec3-124">Bu örnek için, Muhasebe yöneticisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="49ec3-125">Kullanıcıları el ile ata / dışarıda tut seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="49ec3-126">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="49ec3-127">Bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="49ec3-127">Select a user.</span></span>  
6. <span data-ttu-id="49ec3-128">Rol dışında tut seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="49ec3-129">Seçili kullanıcıları, rolün dışında bırakmak için, Rolün dışında bırak'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="49ec3-130">Dışarıda bırakmaları kaldırmak için, hariç tutulma durumunu kaldırmak istediğiniz kullanıcıları seçin ve sonra Durum sıfırla'ya basın.</span><span class="sxs-lookup"><span data-stu-id="49ec3-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="49ec3-131">Bir kullanıcının durumunu sıfırlayarak bir hariç tutmayı kaldırdığınızda, kullanıcının rolü otomatik olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="49ec3-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="49ec3-132">Ancak, durumunu sıfırladığınızda, kullanıcı hemen role atanmaz veya rolden hariç tutulmaz.</span><span class="sxs-lookup"><span data-stu-id="49ec3-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="49ec3-133">Bunun yerine kullanıcı otomatik rol atama bir sonraki çalıştığında rolüne eklenir veya çıkartılır.</span><span class="sxs-lookup"><span data-stu-id="49ec3-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

