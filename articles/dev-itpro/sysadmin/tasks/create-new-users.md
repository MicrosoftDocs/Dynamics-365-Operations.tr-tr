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
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89e492ef5030dd28020094152259b615010aa676
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851323"
---
# <a name="create-new-users"></a><span data-ttu-id="55d7e-103">Yeni kullanıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="55d7e-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55d7e-104">Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.</span><span class="sxs-lookup"><span data-stu-id="55d7e-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="55d7e-105">Sistem yöneticileri bu yordamı sisteme kullanıcılar eklemek için tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="55d7e-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="55d7e-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="55d7e-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="55d7e-107">Yeni bir kullanıcı ekle</span><span class="sxs-lookup"><span data-stu-id="55d7e-107">Add a new user</span></span>
1. <span data-ttu-id="55d7e-108">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="55d7e-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="55d7e-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-109">Click New.</span></span>
3. <span data-ttu-id="55d7e-110">Kullanıcı kimliği alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="55d7e-111">Kullanıcı için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="55d7e-112">Bir kullanıcı kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="55d7e-112">A user ID is required.</span></span>  
4. <span data-ttu-id="55d7e-113">Kullanıcı adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="55d7e-114">Kullanıcının adını girin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="55d7e-115">Etki alanı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="55d7e-116">Kullanıcının etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="55d7e-117">Diğer adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="55d7e-118">Kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="55d7e-119">Şirket alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="55d7e-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="55d7e-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55d7e-122">Kullanıcının şirketini seçin</span><span class="sxs-lookup"><span data-stu-id="55d7e-122">Select the user's company</span></span>  
10. <span data-ttu-id="55d7e-123">Rolleri ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-123">Click Assign roles.</span></span>
11. <span data-ttu-id="55d7e-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="55d7e-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-125">Click OK.</span></span>
13. <span data-ttu-id="55d7e-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="55d7e-127">Kullanıcıları içe aktar</span><span class="sxs-lookup"><span data-stu-id="55d7e-127">Import users</span></span>
1. <span data-ttu-id="55d7e-128">Kullanıcıları içe aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-128">Click Import users.</span></span>
2. <span data-ttu-id="55d7e-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="55d7e-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="55d7e-130">Kullanıcıları içe aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-130">Click Import users.</span></span>
4. <span data-ttu-id="55d7e-131">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55d7e-131">Click Close.</span></span>

