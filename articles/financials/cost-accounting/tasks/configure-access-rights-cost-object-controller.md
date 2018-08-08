--- 
title: "Maliyet nesnesi denetleyicisi için erişim haklarını yapılandırma"
description: "Bir maliyet nesnesi denetleyicisi için erişim haklarını yapılandırmak için bu yordamı kullanın."
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="54c5e-103">Maliyet nesnesi denetleyicisi için erişim haklarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="54c5e-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54c5e-104">Bir maliyet nesnesi denetleyicisi için erişim haklarını yapılandırmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="54c5e-105">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="54c5e-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="54c5e-106">Maliyet nesnesi denetçi rolünü ata</span><span class="sxs-lookup"><span data-stu-id="54c5e-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="54c5e-107">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="54c5e-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="54c5e-108">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="54c5e-109">Örneğin, Kullanıcı adı alanını 'sibel' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="54c5e-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="54c5e-111">Rolleri ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-111">Click Assign roles.</span></span>
5. <span data-ttu-id="54c5e-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="54c5e-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="54c5e-114">Erişim listesi güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="54c5e-114">Enable access list security</span></span>
1. <span data-ttu-id="54c5e-115">Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="54c5e-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="54c5e-117">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-117">Select Organization.</span></span>  
3. <span data-ttu-id="54c5e-118">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-118">Click Edit.</span></span>
4. <span data-ttu-id="54c5e-119">Erişim listesi hiyerarşi alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="54c5e-120">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="54c5e-121">Kullanıcıya erişim haklarını ata</span><span class="sxs-lookup"><span data-stu-id="54c5e-121">Assign access rights to user</span></span>
1. <span data-ttu-id="54c5e-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-122">Click New.</span></span>
2. <span data-ttu-id="54c5e-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="54c5e-124">Kullanıcı kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="54c5e-125">Yönetici seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-125">Select Admin.</span></span>  
4. <span data-ttu-id="54c5e-126">Ağaçta 'Kuruluş\CEO\CFO\FIM' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="54c5e-127">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-127">Click New.</span></span>
6. <span data-ttu-id="54c5e-128">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="54c5e-129">Kullanıcı kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="54c5e-130">Sibel'i seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-130">Select Alicia.</span></span>  
8. <span data-ttu-id="54c5e-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="54c5e-132">Maliyet muhasebesinde erişim haklarını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="54c5e-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="54c5e-133">Maliyet muhasebesi > Kurulum > Parametreler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="54c5e-134">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-134">Click the General tab.</span></span>
3. <span data-ttu-id="54c5e-135">Maliyet nesnesi boyut üyeleri için görüntüleme erişimini etkinleştir alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="54c5e-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-136">Click Save.</span></span>
5. <span data-ttu-id="54c5e-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-137">Close the page.</span></span>
6. <span data-ttu-id="54c5e-138">Maliyet muhasebesi > Kurulum > Maliyet denetimi çalışma alanı yapılandırması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="54c5e-139">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-139">Click Edit.</span></span>
8. <span data-ttu-id="54c5e-140">Yayımlanan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="54c5e-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="54c5e-141">Evet'i seçerseniz, aşağıdaki dört rolden birine atanmış bir kullanıcı Maliyet kontrolü çalışma alanındaki raporları görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi, maliyet muhasebe memuru ve maliyet nesnesi denetleyicisi.</span><span class="sxs-lookup"><span data-stu-id="54c5e-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="54c5e-142">Hayır'ı seçerseniz, yalnızca aşağıdaki rollerden birine atanmış bir kullanıcı raporları görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi ve maliyet muhasebe memuru.</span><span class="sxs-lookup"><span data-stu-id="54c5e-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="54c5e-143">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="54c5e-143">Click Save.</span></span>


