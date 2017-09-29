--- 
title: "Maliyet kontrolü çalışma alanı parametrelerini yapılandırma"
description: "Bu yordamı Maliyet denetimi çalışma alanını yapılandırmak için kullanarak bir kuruluştaki çeşitli seviyede bulunan yöneticilerin örneğin maliyet merkezleri ve ürün grupları gibi maliyet nesnelerine dair bilgi alabilmelerini sağlayın."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8ede40951d08e159358b713fc3dde46576a1b4e3
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="ab6e6-103">Maliyet kontrolü çalışma alanı parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ab6e6-103">Configure cost control workspace parameters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab6e6-104">Bu yordamı Maliyet denetimi çalışma alanını yapılandırmak için kullanarak bir kuruluştaki çeşitli seviyede bulunan yöneticilerin örneğin maliyet merkezleri ve ürün grupları gibi maliyet nesnelerine dair bilgi alabilmelerini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="ab6e6-105">USP2 demo şirketi bu kaydı oluşturmak için kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="ab6e6-106">Maliyet muhasebesi > Kurulum > Maliyet denetimi çalışma alanı yapılandırması'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="ab6e6-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-107">Click New.</span></span>
3. <span data-ttu-id="ab6e6-108">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ab6e6-109">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ab6e6-110">Yayımlanan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="ab6e6-111">Bu seçeneği Evet olarak seçerseniz, aşağıdaki rollerden birine atanmış kullanıcılar Maliyet kontrolü çalışma alanındaki raporu görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi, maliyet muhasebe memuru veya maliyet nesnesi denetleyicisi.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="ab6e6-112">Bu seçeneği Hayır olarak seçerseniz, yalnızca aşağıdaki rollerden birine atanmış kullanıcılar Maliyet kontrolü çalışma alanındaki raporu görebilir: maliyet muhasebesi yöneticisi, maliyet muhasebecisi veya maliyet muhasebe memuru.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="ab6e6-113">Veri filtreleme bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="ab6e6-114">Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="ab6e6-115">Bütçe orijinal sürüm alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="ab6e6-116">Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="ab6e6-117">Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="ab6e6-118">Atama hesaplama kayıtları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="ab6e6-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-119">Click New.</span></span>
13. <span data-ttu-id="ab6e6-120">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ab6e6-121">Mali takvim dönemi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="ab6e6-122">Gerçek sürüm alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="ab6e6-123">Sütun başına Mali dönemleri genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="ab6e6-124">Geçerli dönem alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="ab6e6-125">Maliyet bölümlerini görüntülemek için Sütunları genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="ab6e6-126">Sabit maliyet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="ab6e6-127">Değişken maliyet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="ab6e6-128">Toplam maliyet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="ab6e6-129">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-129">Click Save.</span></span>
23. <span data-ttu-id="ab6e6-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-130">Close the page.</span></span>
24. <span data-ttu-id="ab6e6-131">Maliyet muhasebesi > Çalışma alanları > Maliyet kontrolü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="ab6e6-132">Seçili mali dönemler için sabit, değişken, toplam ve sınıflandırılmamış maliyetleri görmek için bir beyan seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="ab6e6-133">Mali takvim dönemi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="ab6e6-134">Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ab6e6-135">Bir Maliyet nesnesi boyut hiyerarşisini seçtikten sonra, istenilen maliyet değerlerini görmek için Maliyet öğesi boyut hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="ab6e6-136">Örneğin, hiyerarşiyi Üretim genel gideri'ne genişleterek değeri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab6e6-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  


