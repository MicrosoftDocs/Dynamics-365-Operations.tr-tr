--- 
title: "Ürün sınıflandırması için hiyerarşi oluşturma"
description: "Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="a65ef-103">Ürün sınıflandırması için hiyerarşi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a65ef-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a65ef-104">Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="a65ef-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="a65ef-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a65ef-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a65ef-106">Bu yordam kategori yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a65ef-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="a65ef-107">Yeni kategori hiyerarşisini oluştur</span><span class="sxs-lookup"><span data-stu-id="a65ef-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="a65ef-108">Ürün bilgi yönetimi > Kurulum > Kategoriler ve öznitelikler > Kategori hiyerarşisi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="a65ef-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-109">Click New.</span></span>
3. <span data-ttu-id="a65ef-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a65ef-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a65ef-112">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="a65ef-113">Hiyerarşisi oluştur</span><span class="sxs-lookup"><span data-stu-id="a65ef-113">Build the hierarchy</span></span>
1. <span data-ttu-id="a65ef-114">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-114">Click New category node.</span></span>
2. <span data-ttu-id="a65ef-115">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="a65ef-116">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="a65ef-117">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="a65ef-118">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-118">Click New category node.</span></span>
6. <span data-ttu-id="a65ef-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="a65ef-120">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="a65ef-121">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="a65ef-122">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-122">Click New category node.</span></span>
10. <span data-ttu-id="a65ef-123">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="a65ef-124">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="a65ef-125">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="a65ef-126">Yeni kategori düğümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-126">Click New category node.</span></span>
14. <span data-ttu-id="a65ef-127">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="a65ef-128">Kod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="a65ef-129">Kolay ad alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="a65ef-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="a65ef-131">Hiyerarşi sınıflandır</span><span class="sxs-lookup"><span data-stu-id="a65ef-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="a65ef-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="a65ef-133">Eylem Bölmesinde, Kategori hiyerarşisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="a65ef-134">Hiyerarşi türü ilişkilendir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="a65ef-135">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-135">Click New.</span></span>
5. <span data-ttu-id="a65ef-136">Kategori hiyerarşi türü alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="a65ef-137">Ürün sınıflandırması için Emtia kodu kategori hiyerarşi türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="a65ef-138">Kategori hiyerarşisi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a65ef-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a65ef-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a65ef-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a65ef-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a65ef-141">Close the page.</span></span>


