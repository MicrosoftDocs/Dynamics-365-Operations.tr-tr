---
title: Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma
description: Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921023"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="3395a-103">Yapılandırılmış ürün çeşitleri için ürün numarası terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3395a-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3395a-104">Bu yordam, yapılandırılmış ürün çeşitleri için bir ürün numara terminolojisinin nasıl ayarlanacağını ve yapılandırılabilir bir ana ürüne nasıl eklenebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3395a-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="3395a-105">Bu yordam ayrıca bir ürün yapılandırma model bileşeni için bir yapılandırma terminolojisini nasıl oluşturabileceğinizi de gösterir.</span><span class="sxs-lookup"><span data-stu-id="3395a-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="3395a-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="3395a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3395a-107">Yeni ürün numarası terminolojisi D0004 ana ürününe atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3395a-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="3395a-108">Bu görev genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3395a-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="3395a-109">Ürün numara terminolojisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3395a-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="3395a-110">**Ürün bilgi yönetimi \> Kurulum \> Ürün terminolojisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3395a-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="3395a-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-111">Select **New**.</span></span>
1. <span data-ttu-id="3395a-112">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3395a-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="3395a-113">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3395a-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="3395a-114">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-114">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-115">**Ürün ana numarası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="3395a-116">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-116">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-117">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="3395a-118">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-119">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3395a-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="3395a-120">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-120">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-121">**Yapılandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="3395a-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3395a-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="3395a-123">Ana ürüne, ürün numara terminolojisi atama</span><span class="sxs-lookup"><span data-stu-id="3395a-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="3395a-124">**Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3395a-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="3395a-125">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="3395a-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3395a-126">Örneğin, **Ürün numarası** alanında "D" değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="3395a-127">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="3395a-128">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-128">Select **Edit**.</span></span>
1. <span data-ttu-id="3395a-129">*Terminolojiyi kullan* alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="3395a-130">**Ürün çeşidi numara terminolojisi** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="3395a-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3395a-131">Close the page.</span></span>
1. <span data-ttu-id="3395a-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3395a-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="3395a-133">Ürün yapılandırma model bileşeni için terminoloji oluşturma</span><span class="sxs-lookup"><span data-stu-id="3395a-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="3395a-134">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3395a-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="3395a-135">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="3395a-136">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="3395a-137">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-137">Select **Edit**.</span></span>
1. <span data-ttu-id="3395a-138">**Yapılandırma terminolojisini kullan** alanında *Evet*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="3395a-139">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-139">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-140">**Öznitelik değeri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="3395a-141">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-142">**Öznitelik** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="3395a-143">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-143">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-144">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="3395a-145">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-146">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3395a-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="3395a-147">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-147">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-148">**Öznitelik değeri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="3395a-149">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-150">**Öznitelik** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="3395a-151">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-151">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-152">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="3395a-153">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-154">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3395a-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="3395a-155">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-155">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-156">**Öznitelik değeri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="3395a-157">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-158">**Öznitelik** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="3395a-159">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-159">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-160">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="3395a-161">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-162">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3395a-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="3395a-163">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-163">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-164">**Öznitelik değeri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="3395a-165">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-166">**Öznitelik** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="3395a-167">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-167">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-168">**Metin sabiti** seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="3395a-169">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-170">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3395a-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="3395a-171">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-171">Select **Add**.</span></span>
1. <span data-ttu-id="3395a-172">**Numara serisi değeri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="3395a-173">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3395a-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="3395a-174">**Numara sırası** alanında, bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3395a-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="3395a-175">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3395a-175">Close the page.</span></span>
1. <span data-ttu-id="3395a-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3395a-176">Close the page.</span></span>
1. <span data-ttu-id="3395a-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3395a-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]