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
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920669"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="27741-103">Önceden tanımlanmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="27741-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27741-104">Bu konu, önceden tanımlanmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve bunu uygun ürün boyut gruplarına nasıl atayacağınızı açıklar.</span><span class="sxs-lookup"><span data-stu-id="27741-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="27741-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="27741-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="27741-106">Yeni ürün numara terminolojisi, Renk ve Boyut ürün boyut grubuna atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="27741-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="27741-107">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="27741-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="27741-108">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="27741-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="27741-109">**Ürün bilgi yönetimi \> Kurulum \> Ürün terminolojisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="27741-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="27741-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-110">Select **New**.</span></span>
1. <span data-ttu-id="27741-111">**Ad** alanına, örneğin `ColorSize` gibi hedef ürün boyut grubunu tanımlamaya yardımcı olacak bir terminoloji adı girin.</span><span class="sxs-lookup"><span data-stu-id="27741-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="27741-112">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="27741-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="27741-113">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-113">Select **Add**.</span></span>
1. <span data-ttu-id="27741-114">**Ürün ana numarası** seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="27741-115">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-115">Select **Add**.</span></span>
1. <span data-ttu-id="27741-116">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="27741-117">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="27741-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="27741-118">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-118">Select **Add**.</span></span>
1. <span data-ttu-id="27741-119">**Renk** seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-119">Select **Color**.</span></span>
1. <span data-ttu-id="27741-120">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-120">Select **Add**.</span></span>
1. <span data-ttu-id="27741-121">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="27741-122">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="27741-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="27741-123">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-123">Select **Add**.</span></span>
1. <span data-ttu-id="27741-124">**Boyut** seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-124">Select **Size**.</span></span>
1. <span data-ttu-id="27741-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27741-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="27741-126">Ana ürüne terminoloji atama</span><span class="sxs-lookup"><span data-stu-id="27741-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="27741-127">**Ürün boyut grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="27741-128">**SizeCol ürün boyut grubunu** seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="27741-129">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-129">Select **Edit**.</span></span>
4. <span data-ttu-id="27741-130">**Terminolojiyi kullan** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="27741-131">**Ürün çeşidi numara terminolojisi** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="27741-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="27741-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27741-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]