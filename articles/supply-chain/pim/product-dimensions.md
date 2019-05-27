---
title: Ürün boyutları
description: Dört ürün boyutu bulunur - Renk, Yapılandırma, Boyut ve Stil. Ürün boyutlarını boyut gruplarında birleştirebilirsiniz ve ürün master öğelerine boyut grupları atayabilirsiniz. Ürün boyutlarının kombinasyonları, ürün çeşitlerinin nasıl tanımlanacağını belirler.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb9d47bf6f081dbcc9590bddd4516cf7385ec23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563586"
---
# <a name="product-dimensions"></a><span data-ttu-id="3d334-105">Ürün boyutları</span><span class="sxs-lookup"><span data-stu-id="3d334-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="3d334-106">Dört ürün boyutu bulunur - Renk, Yapılandırma, Boyut ve Stil.</span><span class="sxs-lookup"><span data-stu-id="3d334-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="3d334-107">Ürün boyutlarını boyut gruplarında birleştirebilirsiniz ve ürün master öğelerine boyut grupları atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d334-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="3d334-108">Ürün boyutlarının kombinasyonları, ürün çeşitlerinin nasıl tanımlanacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="3d334-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="3d334-109">Ürün boyutları, ürün varyantı tanımlamaya hizmet eden özelliklerdir.</span><span class="sxs-lookup"><span data-stu-id="3d334-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="3d334-110">Ürün boyutlarının birleşimleri, ürün varyantları tanımlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d334-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="3d334-111">Bir ürün varyantı oluşturmak için bir ana ürüne en az bir ürün boyutu tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d334-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="3d334-112">Ürün çeşitleri</span><span class="sxs-lookup"><span data-stu-id="3d334-112">Product variants</span></span>
----------------

<span data-ttu-id="3d334-113">Ürün varyantlarına maddeler de denilir.</span><span class="sxs-lookup"><span data-stu-id="3d334-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="3d334-114">Bir madde bir hizmetten farklı olarak somut bir üründür.</span><span class="sxs-lookup"><span data-stu-id="3d334-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="3d334-115">Hizmet türüyle bir ana ürün tanımlamak da mümkündür.</span><span class="sxs-lookup"><span data-stu-id="3d334-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="3d334-116">Hizmet türü kullanarak hizmetleri içerecek ürün varyantları belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d334-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="3d334-117">Örneğin, Danışmanlık işi için bir ana ürün ve üst düzey danışmanlar ve alt düzey danışmanlar tarafından gerçekleştirilen iş için ürün varyantları belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d334-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="3d334-118">Ürün boyutları</span><span class="sxs-lookup"><span data-stu-id="3d334-118">Product dimensions</span></span>
<span data-ttu-id="3d334-119">Aşağıdaki ürün boyutları mevcuttur: Yapılandırma, Renk, Boyut ve Stil.</span><span class="sxs-lookup"><span data-stu-id="3d334-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="3d334-120">Ürün boyut değerlerini temel alan bir ürün çeşidi oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="3d334-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="3d334-121">Boyut, Renk ve Stil gibi ürün boyutu değerleri **Boyut**, **Renk** ve **Stil** sayfalarında oluşturulabilir ve bu sayfalara şu konumlardan erişilebilir: **Ürün bilgileri yönetimi** &gt; **Kurulum** &gt; **Boyut ve çeşit Grupları** &gt; **Boyutlar/Renkler/Stiller**.</span><span class="sxs-lookup"><span data-stu-id="3d334-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="3d334-122">Yapılandırma boyutuna yönelik ürün boyutu genellikle ya Ürün yapılandırıcısı ya da Boyut bazlı yapılandırıcı kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3d334-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="3d334-123">Ürün boyutları, aşağıdaki konumlardan erişilebilecek **Ürün boyutları** sayfasında da oluşturulup muhafaza edilebilir:</span><span class="sxs-lookup"><span data-stu-id="3d334-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="3d334-124">**Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Ana ürünler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="3d334-125">**Eylem Bölmesi**'nde **Ürün boyutları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3d334-126">**Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Tüm ürünler ve ana ürünler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="3d334-127">Bir ana ürün seçin.</span><span class="sxs-lookup"><span data-stu-id="3d334-127">Select a product master.</span></span> <span data-ttu-id="3d334-128">**Eylem Bölmesi**'nde **Ürün boyutları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3d334-129">**Ürün bilgileri yönetimi** &gt; **Serbest bırakılan ürünler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="3d334-130">Bir ana ürün seçin.</span><span class="sxs-lookup"><span data-stu-id="3d334-130">Select a product master.</span></span> <span data-ttu-id="3d334-131">**Eylem Bölmesi**'nde, **Ürün**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="3d334-132">**Ana ürün** grubunda **Ürün boyutları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d334-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="3d334-133">Maddeler için oluşturabileceğiniz varyant sayısı, olası ürün boyutu kombinasyonlarının sayısı ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="3d334-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="3d334-134">**İpucu**</span><span class="sxs-lookup"><span data-stu-id="3d334-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d334-135">Bir ürünü örneğin bir emir satırında kullanırken, birlikle çalışmak istediğiniz ürün varyantını tanımlamak için ürün boyutlarını seçerseniz.</span><span class="sxs-lookup"><span data-stu-id="3d334-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="3d334-136">Örnek</span><span class="sxs-lookup"><span data-stu-id="3d334-136">Example</span></span>
<span data-ttu-id="3d334-137">Bir şirket kot kumaşından ürünler satıyor.</span><span class="sxs-lookup"><span data-stu-id="3d334-137">A company sells denim jeans.</span></span> <span data-ttu-id="3d334-138">Kot kumaşı maddesi Renk ve Ebat boyutlarını kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="3d334-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="3d334-139">Kot kumaşları üç farklı renk ve altı farklı ebatta satılıyor.</span><span class="sxs-lookup"><span data-stu-id="3d334-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="3d334-140">Renkler: Mavi, Siyah, Kahverengi Boyutlar: XS, S, M, L, XL, XXL Tüm rengin tümünde tüm ebatlar yoktur.</span><span class="sxs-lookup"><span data-stu-id="3d334-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="3d334-141">Kombinasyonların tümü mevcut olsaydı, 18 farklı kot türü oluşturacaktı.</span><span class="sxs-lookup"><span data-stu-id="3d334-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="3d334-142">Bu örnekte, yalnızca aşağıdaki dokuz ürün varyantı kombinasyonu üretilir.</span><span class="sxs-lookup"><span data-stu-id="3d334-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="3d334-143">Renk</span><span class="sxs-lookup"><span data-stu-id="3d334-143">Color</span></span> | <span data-ttu-id="3d334-144">Ebat</span><span class="sxs-lookup"><span data-stu-id="3d334-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="3d334-145">Mavi</span><span class="sxs-lookup"><span data-stu-id="3d334-145">Blue</span></span>  | <span data-ttu-id="3d334-146">XS</span><span class="sxs-lookup"><span data-stu-id="3d334-146">XS</span></span>   |
| <span data-ttu-id="3d334-147">Mavi</span><span class="sxs-lookup"><span data-stu-id="3d334-147">Blue</span></span>  | <span data-ttu-id="3d334-148">S</span><span class="sxs-lookup"><span data-stu-id="3d334-148">S</span></span>    |
| <span data-ttu-id="3d334-149">Mavi</span><span class="sxs-lookup"><span data-stu-id="3d334-149">Blue</span></span>  | <span data-ttu-id="3d334-150">P</span><span class="sxs-lookup"><span data-stu-id="3d334-150">M</span></span>    |
| <span data-ttu-id="3d334-151">Siyah</span><span class="sxs-lookup"><span data-stu-id="3d334-151">Black</span></span> | <span data-ttu-id="3d334-152">P</span><span class="sxs-lookup"><span data-stu-id="3d334-152">M</span></span>    |
| <span data-ttu-id="3d334-153">Siyah</span><span class="sxs-lookup"><span data-stu-id="3d334-153">Black</span></span> | <span data-ttu-id="3d334-154">L</span><span class="sxs-lookup"><span data-stu-id="3d334-154">L</span></span>    |
| <span data-ttu-id="3d334-155">Siyah</span><span class="sxs-lookup"><span data-stu-id="3d334-155">Black</span></span> | <span data-ttu-id="3d334-156">XL</span><span class="sxs-lookup"><span data-stu-id="3d334-156">XL</span></span>   |
| <span data-ttu-id="3d334-157">Kahverengi</span><span class="sxs-lookup"><span data-stu-id="3d334-157">Brown</span></span> | <span data-ttu-id="3d334-158">L</span><span class="sxs-lookup"><span data-stu-id="3d334-158">L</span></span>    |
| <span data-ttu-id="3d334-159">Kahverengi</span><span class="sxs-lookup"><span data-stu-id="3d334-159">Brown</span></span> | <span data-ttu-id="3d334-160">XL</span><span class="sxs-lookup"><span data-stu-id="3d334-160">XL</span></span>   |
| <span data-ttu-id="3d334-161">Kahverengi</span><span class="sxs-lookup"><span data-stu-id="3d334-161">Brown</span></span> | <span data-ttu-id="3d334-162">XXL</span><span class="sxs-lookup"><span data-stu-id="3d334-162">XXL</span></span>  |





