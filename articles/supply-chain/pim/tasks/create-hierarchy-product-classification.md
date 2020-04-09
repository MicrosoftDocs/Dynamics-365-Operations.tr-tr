---
title: Ürün sınıflandırması için hiyerarşi oluşturma
description: Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ac87356f46edc118a592acd393823603815917a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150136"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="ecbea-103">Ürün sınıflandırması için hiyerarşi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ecbea-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ecbea-104">Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="ecbea-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="ecbea-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ecbea-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ecbea-106">Bu yordam kategori yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ecbea-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="ecbea-107">Yeni kategori hiyerarşisini oluştur</span><span class="sxs-lookup"><span data-stu-id="ecbea-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="ecbea-108">**Gezinti bölmesi > Modüller > Ürün bilgi yönetimi > Kurulum > Kategoriler ve öznitelikler > Kategori hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="ecbea-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-109">Click **New**.</span></span>
3. <span data-ttu-id="ecbea-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="ecbea-111">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ecbea-112">**Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="ecbea-113">Hiyerarşisi oluştur</span><span class="sxs-lookup"><span data-stu-id="ecbea-113">Build the hierarchy</span></span>
1. <span data-ttu-id="ecbea-114">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-114">Click **New** category node.</span></span>
2. <span data-ttu-id="ecbea-115">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="ecbea-116">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="ecbea-117">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="ecbea-118">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-118">Click **New** category node.</span></span>
6. <span data-ttu-id="ecbea-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="ecbea-120">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="ecbea-121">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="ecbea-122">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-122">Click **New** category node.</span></span>
10. <span data-ttu-id="ecbea-123">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="ecbea-124">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="ecbea-125">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="ecbea-126">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-126">Click **New** category node.</span></span>
14. <span data-ttu-id="ecbea-127">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="ecbea-128">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="ecbea-129">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="ecbea-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="ecbea-131">Hiyerarşi sınıflandır</span><span class="sxs-lookup"><span data-stu-id="ecbea-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="ecbea-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="ecbea-133">**Eylem Bölmesi**'nde, **Kategori hiyerarşisi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="ecbea-134">**Hiyerarşi türü ilişkilendir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="ecbea-135">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-135">Click **New**.</span></span>
5. <span data-ttu-id="ecbea-136">**Kategori hiyerarşi türü** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="ecbea-137">**Ürün sınıflandırması için Emtia kodu kategori hiyerarşi türü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="ecbea-138">**Kategori hiyerarşisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ecbea-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ecbea-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ecbea-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ecbea-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ecbea-141">Close the page.</span></span>

