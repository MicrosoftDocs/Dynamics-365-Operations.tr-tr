---
title: Ürün sınıflandırması için hiyerarşi oluşturma
description: Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568432"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="244fe-103">Ürün sınıflandırması için hiyerarşi oluşturma</span><span class="sxs-lookup"><span data-stu-id="244fe-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="244fe-104">Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="244fe-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="244fe-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="244fe-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="244fe-106">Bu yordam kategori yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="244fe-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="244fe-107">Yeni kategori hiyerarşisini oluştur</span><span class="sxs-lookup"><span data-stu-id="244fe-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="244fe-108">Ürün bilgi yönetimi > Kurulum > Kategoriler ve öznitelikler > Kategori hiyerarşisi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="244fe-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="244fe-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-109">Click New.</span></span>
3. <span data-ttu-id="244fe-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="244fe-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="244fe-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="244fe-112">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="244fe-113">Hiyerarşisi oluştur</span><span class="sxs-lookup"><span data-stu-id="244fe-113">Build the hierarchy</span></span>
1. <span data-ttu-id="244fe-114">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-114">Click New category node.</span></span>
2. <span data-ttu-id="244fe-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="244fe-116">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="244fe-117">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="244fe-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="244fe-118">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-118">Click New category node.</span></span>
6. <span data-ttu-id="244fe-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="244fe-120">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="244fe-121">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="244fe-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="244fe-122">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-122">Click New category node.</span></span>
10. <span data-ttu-id="244fe-123">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="244fe-124">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="244fe-125">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="244fe-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="244fe-126">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-126">Click New category node.</span></span>
14. <span data-ttu-id="244fe-127">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="244fe-128">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="244fe-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="244fe-129">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="244fe-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="244fe-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="244fe-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="244fe-131">Hiyerarşi sınıflandır</span><span class="sxs-lookup"><span data-stu-id="244fe-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="244fe-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="244fe-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="244fe-133">Eylem Bölmesinde, Kategori hiyerarşisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="244fe-134">Hiyerarşi türü ilişkilendir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="244fe-135">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-135">Click New.</span></span>
5. <span data-ttu-id="244fe-136">Kategori hiyerarşi türü alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="244fe-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="244fe-137">Ürün sınıflandırması için Emtia kodu kategori hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="244fe-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="244fe-138">Kategori hiyerarşisi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="244fe-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="244fe-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="244fe-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="244fe-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="244fe-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="244fe-141">Close the page.</span></span>

