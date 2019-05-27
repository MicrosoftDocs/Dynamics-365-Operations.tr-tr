---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558723"
---
# <a name="create-new-users"></a><span data-ttu-id="f244a-103">Yeni kullanıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="f244a-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f244a-104">Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.</span><span class="sxs-lookup"><span data-stu-id="f244a-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="f244a-105">Sistem yöneticileri bu yordamı sisteme kullanıcılar eklemek için tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="f244a-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="f244a-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="f244a-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="f244a-107">Yeni bir kullanıcı ekle</span><span class="sxs-lookup"><span data-stu-id="f244a-107">Add a new user</span></span>
1. <span data-ttu-id="f244a-108">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="f244a-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f244a-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-109">Click New.</span></span>
3. <span data-ttu-id="f244a-110">Kullanıcı kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f244a-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="f244a-111">Kullanıcı için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="f244a-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="f244a-112">Bir kullanıcı kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f244a-112">A user ID is required.</span></span>  
4. <span data-ttu-id="f244a-113">Kullanıcı adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f244a-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="f244a-114">Kullanıcının adını girin.</span><span class="sxs-lookup"><span data-stu-id="f244a-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="f244a-115">Etki alanı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f244a-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="f244a-116">Kullanıcının etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="f244a-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="f244a-117">Diğer adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f244a-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="f244a-118">Kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="f244a-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="f244a-119">Şirket alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f244a-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f244a-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f244a-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f244a-122">Kullanıcının şirketini seçin</span><span class="sxs-lookup"><span data-stu-id="f244a-122">Select the user's company</span></span>  
10. <span data-ttu-id="f244a-123">Rolleri ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-123">Click Assign roles.</span></span>
11. <span data-ttu-id="f244a-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f244a-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f244a-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-125">Click OK.</span></span>
13. <span data-ttu-id="f244a-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="f244a-127">Kullanıcıları içe aktar</span><span class="sxs-lookup"><span data-stu-id="f244a-127">Import users</span></span>
1. <span data-ttu-id="f244a-128">Kullanıcıları içe aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-128">Click Import users.</span></span>
2. <span data-ttu-id="f244a-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f244a-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f244a-130">Kullanıcıları içe aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-130">Click Import users.</span></span>
4. <span data-ttu-id="f244a-131">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f244a-131">Click Close.</span></span>

