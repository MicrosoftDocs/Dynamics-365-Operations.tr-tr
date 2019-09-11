---
title: Yeni kullanıcılar oluşturma
description: Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916496"
---
# <a name="create-new-users"></a><span data-ttu-id="b839d-103">Yeni kullanıcılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="b839d-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b839d-104">Kullanıcılar, işlerini yapmak için sistem erişimine sahip olmaları gereken, kendi kuruluşunuzun dahili personelleri veya harici müşteriler veya satıcılardır.</span><span class="sxs-lookup"><span data-stu-id="b839d-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="b839d-105">Sistem yöneticileri bu yordamı sisteme kullanıcılar eklemek için tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="b839d-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="b839d-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="b839d-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="b839d-107">Yeni bir kullanıcı ekle</span><span class="sxs-lookup"><span data-stu-id="b839d-107">Add a new user</span></span>
1. <span data-ttu-id="b839d-108">**Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="b839d-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="b839d-109">**Eylem bölmesinde** **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="b839d-110">**Kullanıcı kimliği** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b839d-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="b839d-111">Kullanıcı için benzersiz bir tanımlayıcı girin.</span><span class="sxs-lookup"><span data-stu-id="b839d-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="b839d-112">Bir kullanıcı kimliği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b839d-112">A user ID is required.</span></span>  
4. <span data-ttu-id="b839d-113">**Kullanıcı adı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b839d-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="b839d-114">Kullanıcının adını girin.</span><span class="sxs-lookup"><span data-stu-id="b839d-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="b839d-115">**Etki alanı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b839d-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="b839d-116">Kullanıcının etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="b839d-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="b839d-117">**Diğer adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b839d-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="b839d-118">Kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="b839d-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="b839d-119">**Şirket** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b839d-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b839d-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="b839d-121">**Kullanıcının rolleri** bölümünde, **Rol ata**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="b839d-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b839d-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="b839d-123">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-123">Click **OK**.</span></span>
12. <span data-ttu-id="b839d-124">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="b839d-125">Kullanıcıları içe aktar</span><span class="sxs-lookup"><span data-stu-id="b839d-125">Import users</span></span>
1. <span data-ttu-id="b839d-126">**Eylem Bölmesi**'nde, **Kullanıcıları içe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="b839d-127">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b839d-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b839d-128">**Kullanıcıları içe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-128">Click **Import users**.</span></span>
4. <span data-ttu-id="b839d-129">**Kapat**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b839d-129">Click **Close**.</span></span>

