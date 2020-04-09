---
title: Maliyet nesnesi denetleyicisi için erişim haklarını yapılandırma
description: Bir maliyet nesnesi denetleyicisi için erişim haklarını yapılandırmak için bu yordamı kullanın.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a931980add70ddc003d8a7c1a78f451bacbf57d4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144508"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="2e667-103">Maliyet nesnesi denetleyicisi için erişim haklarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2e667-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e667-104">Bir maliyet nesnesi denetleyicisi için erişim haklarını yapılandırmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="2e667-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="2e667-105">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2e667-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="2e667-106">Maliyet nesnesi denetçi rolünü ata</span><span class="sxs-lookup"><span data-stu-id="2e667-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="2e667-107">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="2e667-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="2e667-108">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2e667-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2e667-109">Örneğin, Kullanıcı adı alanını 'sibel' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="2e667-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="2e667-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2e667-111">Rolleri ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-111">Click Assign roles.</span></span>
5. <span data-ttu-id="2e667-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2e667-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="2e667-114">Erişim listesi güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="2e667-114">Enable access list security</span></span>
1. <span data-ttu-id="2e667-115">Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2e667-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="2e667-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e667-117">Kuruluşu seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-117">Select Organization.</span></span>  
3. <span data-ttu-id="2e667-118">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-118">Click Edit.</span></span>
4. <span data-ttu-id="2e667-119">Erişim listesi hiyerarşi alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="2e667-120">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="2e667-121">Kullanıcıya erişim haklarını ata</span><span class="sxs-lookup"><span data-stu-id="2e667-121">Assign access rights to user</span></span>
1. <span data-ttu-id="2e667-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-122">Click New.</span></span>
2. <span data-ttu-id="2e667-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2e667-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2e667-124">Kullanıcı kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="2e667-125">Yönetici seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-125">Select Admin.</span></span>  
4. <span data-ttu-id="2e667-126">Ağaçta 'Kuruluş\CEO\CFO\FIM' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="2e667-127">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-127">Click New.</span></span>
6. <span data-ttu-id="2e667-128">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2e667-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="2e667-129">Kullanıcı kimliği alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="2e667-130">Sibel'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-130">Select Alicia.</span></span>  
8. <span data-ttu-id="2e667-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="2e667-132">Maliyet muhasebesinde erişim haklarını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="2e667-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="2e667-133">Maliyet muhasebesi > Kurulum > Parametreler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="2e667-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="2e667-134">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-134">Click the General tab.</span></span>
3. <span data-ttu-id="2e667-135">Maliyet nesnesi boyut üyeleri için görüntüleme erişimini etkinleştir alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="2e667-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-136">Click Save.</span></span>
5. <span data-ttu-id="2e667-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2e667-137">Close the page.</span></span>
6. <span data-ttu-id="2e667-138">Maliyet muhasebesi > Kurulum > Maliyet denetimi çalışma alanı yapılandırması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2e667-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="2e667-139">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-139">Click Edit.</span></span>
8. <span data-ttu-id="2e667-140">Yayımlanan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2e667-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="2e667-141">Evet'i seçerseniz, aşağıdaki dört rolden birine atanmış bir kullanıcı Maliyet kontrolü çalışma alanındaki raporları görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi, maliyet muhasebe memuru ve maliyet nesnesi denetleyicisi.</span><span class="sxs-lookup"><span data-stu-id="2e667-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="2e667-142">Hayır'ı seçerseniz, yalnızca aşağıdaki rollerden birine atanmış bir kullanıcı raporları görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi ve maliyet muhasebe memuru.</span><span class="sxs-lookup"><span data-stu-id="2e667-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="2e667-143">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e667-143">Click Save.</span></span>

