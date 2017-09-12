--- 
title: "Önceden tanımlanmış ürün çeşitleri için ürün numarası oluşturma"
description: "Bu kılavuz, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı gösterir."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
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
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="1353d-103">Önceden tanımlanmış ürün çeşitleri için ürün numarası oluşturma</span><span class="sxs-lookup"><span data-stu-id="1353d-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1353d-104">Bu kılavuz, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="1353d-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="1353d-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="1353d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1353d-106">Yeni ürün numara terminolojisi, Renk ve Boyut ürün boyut grubuna atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1353d-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="1353d-107">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1353d-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="1353d-108">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1353d-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="1353d-109">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="1353d-110">Ürün terminolojisi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="1353d-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-111">Click New.</span></span>
4. <span data-ttu-id="1353d-112">Ad alanına, örneğin ColorSize gibi hedef ürün boyut grubunu tanımlamaya yardımcı olacak bir terminoloji adı girin.</span><span class="sxs-lookup"><span data-stu-id="1353d-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="1353d-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1353d-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="1353d-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-114">Click Add.</span></span>
7. <span data-ttu-id="1353d-115">Ana ürün numarası'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-115">Click Product master number.</span></span>
8. <span data-ttu-id="1353d-116">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-116">Click Add.</span></span>
9. <span data-ttu-id="1353d-117">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-117">Click Text constant.</span></span>
10. <span data-ttu-id="1353d-118">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1353d-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="1353d-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-119">Click Add.</span></span>
12. <span data-ttu-id="1353d-120">Renk'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-120">Click Color.</span></span>
13. <span data-ttu-id="1353d-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-121">Click Add.</span></span>
14. <span data-ttu-id="1353d-122">Metin sabiti'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-122">Click Text constant.</span></span>
15. <span data-ttu-id="1353d-123">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1353d-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="1353d-124">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-124">Click Add.</span></span>
17. <span data-ttu-id="1353d-125">Boyut'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-125">Click Size.</span></span>
18. <span data-ttu-id="1353d-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="1353d-127">Ana ürüne terminoloji atama</span><span class="sxs-lookup"><span data-stu-id="1353d-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="1353d-128">Ürün boyut grupları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="1353d-129">SizeCol ürün boyut grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1353d-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="1353d-130">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1353d-130">Click Edit.</span></span>
4. <span data-ttu-id="1353d-131">Terminoloji kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1353d-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="1353d-132">Ürün çeşidi numara terminolojisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="1353d-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="1353d-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1353d-133">Close the page.</span></span>


