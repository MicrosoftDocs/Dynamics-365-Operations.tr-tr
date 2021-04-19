---
title: Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c69dc3f8e70c3b0a760f54d2251757ac997a432
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841635"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="30c1b-103">Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="30c1b-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30c1b-104">Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.</span><span class="sxs-lookup"><span data-stu-id="30c1b-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="30c1b-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="30c1b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="30c1b-106">Yeni ürün numara terminolojisi, Renk ve Boyut ürün boyut grubuna atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="30c1b-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="30c1b-107">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="30c1b-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="30c1b-108">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="30c1b-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="30c1b-109">**Ürün çeşidi model tanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="30c1b-110">**Ürün terminolojisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="30c1b-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-111">Select **New**.</span></span>
4. <span data-ttu-id="30c1b-112">**Ad** alanına, örneğin `ColorSize` gibi hedef ürün boyut grubunu tanımlamaya yardımcı olacak bir terminoloji adı girin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="30c1b-113">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="30c1b-114">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-114">Select **Add**.</span></span>
7. <span data-ttu-id="30c1b-115">**Ürün ana numarası** seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="30c1b-116">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-116">Select **Add**.</span></span>
9. <span data-ttu-id="30c1b-117">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="30c1b-118">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="30c1b-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="30c1b-119">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-119">Select **Add**.</span></span>
12. <span data-ttu-id="30c1b-120">**Renk** seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-120">Select **Color**.</span></span>
13. <span data-ttu-id="30c1b-121">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-121">Select **Add**.</span></span>
14. <span data-ttu-id="30c1b-122">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="30c1b-123">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="30c1b-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="30c1b-124">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-124">Select **Add**.</span></span>
17. <span data-ttu-id="30c1b-125">**Boyut** seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-125">Select **Size**.</span></span>
18. <span data-ttu-id="30c1b-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="30c1b-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="30c1b-127">Ana ürüne terminoloji atama</span><span class="sxs-lookup"><span data-stu-id="30c1b-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="30c1b-128">**Ürün boyut grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="30c1b-129">**SizeCol ürün boyut grubunu** seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="30c1b-130">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-130">Select **Edit**.</span></span>
4. <span data-ttu-id="30c1b-131">**Terminolojiyi kullan** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="30c1b-132">**Ürün çeşidi numara terminolojisi** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="30c1b-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="30c1b-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="30c1b-133">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]