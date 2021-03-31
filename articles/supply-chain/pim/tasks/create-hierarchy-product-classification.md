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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59631148dbd2ad27ce2bb5c268d78e625daef6bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224463"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="99b7b-103">Ürün sınıflandırması için hiyerarşi oluşturma</span><span class="sxs-lookup"><span data-stu-id="99b7b-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99b7b-104">Bu yordam yeni bir kategori hiyerarşisi oluşturmayı ve emtia kodu hiyerarşi türü atamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="99b7b-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="99b7b-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="99b7b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="99b7b-106">Bu yordam kategori yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="99b7b-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="99b7b-107">Yeni kategori hiyerarşisini oluştur</span><span class="sxs-lookup"><span data-stu-id="99b7b-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="99b7b-108">**Gezinti bölmesi > Modüller > Ürün bilgi yönetimi > Kurulum > Kategoriler ve öznitelikler > Kategori hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="99b7b-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-109">Click **New**.</span></span>
3. <span data-ttu-id="99b7b-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="99b7b-111">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="99b7b-112">**Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="99b7b-113">Hiyerarşisi oluştur</span><span class="sxs-lookup"><span data-stu-id="99b7b-113">Build the hierarchy</span></span>
1. <span data-ttu-id="99b7b-114">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-114">Click **New** category node.</span></span>
2. <span data-ttu-id="99b7b-115">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="99b7b-116">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="99b7b-117">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="99b7b-118">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-118">Click **New** category node.</span></span>
6. <span data-ttu-id="99b7b-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="99b7b-120">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="99b7b-121">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="99b7b-122">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-122">Click **New** category node.</span></span>
10. <span data-ttu-id="99b7b-123">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="99b7b-124">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="99b7b-125">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="99b7b-126">**Yeni** kategori düğümüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-126">Click **New** category node.</span></span>
14. <span data-ttu-id="99b7b-127">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="99b7b-128">**Kod** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="99b7b-129">**Kolay ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="99b7b-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="99b7b-131">Hiyerarşi sınıflandır</span><span class="sxs-lookup"><span data-stu-id="99b7b-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="99b7b-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="99b7b-133">**Eylem Bölmesi**'nde, **Kategori hiyerarşisi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="99b7b-134">**Hiyerarşi türü ilişkilendir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="99b7b-135">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-135">Click **New**.</span></span>
5. <span data-ttu-id="99b7b-136">**Kategori hiyerarşi türü** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="99b7b-137">**Ürün sınıflandırması için Emtia kodu kategori hiyerarşi türü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="99b7b-138">**Kategori hiyerarşisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="99b7b-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="99b7b-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="99b7b-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="99b7b-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99b7b-141">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]