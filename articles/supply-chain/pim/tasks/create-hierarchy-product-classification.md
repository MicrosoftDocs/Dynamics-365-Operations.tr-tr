---
title: Ürün sınıflandırması için hiyerarşi oluşturma
description: Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf414ca0a21ea8816eba9a5ef95c988dd31f0249
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677874"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="8607d-103">Ürün sınıflandırması için hiyerarşi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8607d-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8607d-104">Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="8607d-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="8607d-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8607d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8607d-106">Bu yordam kategori yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="8607d-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="8607d-107">Yeni kategori hiyerarşisini oluştur</span><span class="sxs-lookup"><span data-stu-id="8607d-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="8607d-108">**Gezinti bölmesi > Modüller > Ürün bilgi yönetimi > Kurulum > Kategoriler ve öznitelikler > Kategori hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8607d-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="8607d-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-109">Click **New**.</span></span>
3. <span data-ttu-id="8607d-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="8607d-111">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8607d-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8607d-112">**Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="8607d-113">Hiyerarşisi oluştur</span><span class="sxs-lookup"><span data-stu-id="8607d-113">Build the hierarchy</span></span>
1. <span data-ttu-id="8607d-114">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-114">Click **New** category node.</span></span>
2. <span data-ttu-id="8607d-115">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="8607d-116">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="8607d-117">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8607d-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="8607d-118">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-118">Click **New** category node.</span></span>
6. <span data-ttu-id="8607d-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="8607d-120">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="8607d-121">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8607d-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="8607d-122">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-122">Click **New** category node.</span></span>
10. <span data-ttu-id="8607d-123">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="8607d-124">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="8607d-125">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8607d-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="8607d-126">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-126">Click **New** category node.</span></span>
14. <span data-ttu-id="8607d-127">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="8607d-128">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8607d-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="8607d-129">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8607d-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="8607d-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8607d-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="8607d-131">Hiyerarşi sınıflandır</span><span class="sxs-lookup"><span data-stu-id="8607d-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="8607d-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8607d-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="8607d-133">**Eylem Bölmesi**'nde, **Kategori hiyerarşisi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="8607d-134">**Hiyerarşi türü ilişkilendir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="8607d-135">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-135">Click **New**.</span></span>
5. <span data-ttu-id="8607d-136">**Kategori hiyerarşi türü** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="8607d-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="8607d-137">**Ürün sınıflandırması için Emtia kodu kategori hiyerarşi türü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="8607d-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="8607d-138">**Kategori hiyerarşisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8607d-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8607d-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="8607d-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8607d-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8607d-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8607d-141">Close the page.</span></span>

