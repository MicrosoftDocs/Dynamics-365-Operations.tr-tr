---
title: Yeni ürün oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir ürünün nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001979"
---
# <a name="create-a-new-product"></a><span data-ttu-id="a7fb8-103">Yeni ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7fb8-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a7fb8-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni bir ürünün nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a7fb8-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="a7fb8-105">Overview</span></span>

<span data-ttu-id="a7fb8-106">Ürün birincil olarak bir ürün numarası, adı ve açıklamasıyla tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="a7fb8-107">Bununla birlikte, bir ürünü veya hizmeti açıklamak için başka veriler de gereklidir:</span><span class="sxs-lookup"><span data-stu-id="a7fb8-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="a7fb8-108">Yeni ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7fb8-108">Create a new product</span></span>

1. <span data-ttu-id="a7fb8-109">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kategoriye göre ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="a7fb8-110">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a7fb8-111">**Ürün türü** açılır listesinde, **Madde** veya **Servis**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="a7fb8-112">**Ürün alt türü** açılır listesinde **Ürün**'ü (ürünün çeşitleri yoksa) veya **Ürün aslı**'nı (ürünün çeşitleri varsa) seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="a7fb8-113">**Ürün numarası** kutusuna, önceden doldurulmadıysa, bir ürün numarası girin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="a7fb8-114">**Ürün adı** kutusuna bir ürün adı girin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="a7fb8-115">**Arama adı** kutusuna bir arama adı girin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="a7fb8-116">**Perakende kategorisi** açılır listesinde uygun bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="a7fb8-117">Ürün bir set ise **Ürün seti** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="a7fb8-118">Ürün alt türü ürün aslı ise, **Ürün boyut grubunu** desteklenen çeşitleri içerecek şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="a7fb8-119">Seçenekler şunlardır: **Renk**, **Boyut**, **Stil** ve **Konfigürasyon**.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="a7fb8-120">Gerekirse ek ürün boyutu grupları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="a7fb8-121">**Yapılandırma teknolojisi** açılır listesinde uygun bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="a7fb8-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-122">Select **OK**.</span></span>

<span data-ttu-id="a7fb8-123">Aşağıdaki resimde bir eklenen ürün örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-123">The following image shows an example product being added.</span></span>

![Ürün oluşturma](media/create-new-product.png)

<span data-ttu-id="a7fb8-125">Ürün eklendikten sonra, **Ürün açıklaması**, **Çeşit grupları**, **Boyut grupları**, **Ürün öznitelikleri** ve **İlgili ürünler** gibi ek veriler ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="a7fb8-126">Aşağıdaki resimde bir ürünün ek ayrıntıları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-126">The following image shows a product's additional details.</span></span>

![Ürün ayrıntıları](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="a7fb8-128">Ürün varyantları oluştur</span><span class="sxs-lookup"><span data-stu-id="a7fb8-128">Create product variants</span></span>

<span data-ttu-id="a7fb8-129">Ürün alt türü **Ürün aslı**ise, belirli çeşitler oluşturulması gerekecektir.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="a7fb8-130">Ürün çeşitleri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="a7fb8-131">Eylem bölmesinde **Ürün çeşitleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="a7fb8-132">Eylem bölmesinde çeşit grupları seçildiyse, \**Çeşit önerileri*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="a7fb8-133">Ürün için desteklemek istediğiniz çeşitleri seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="a7fb8-134">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="a7fb8-135">Bir ürünü serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="a7fb8-135">Release a product</span></span>

<span data-ttu-id="a7fb8-136">Bir ürünü satmak için önce tüzel bir kişiliğe serbest bırakılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="a7fb8-137">Ürün sayfasından, **Ürünleri serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-137">From the product page, select **Release products**.</span></span>

    ![Ürünü serbest bırakma](media/create-new-product-3.png)

1. <span data-ttu-id="a7fb8-139">Serbest bırakılacak ürünü ve ardından **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-139">Select the product to release, and then select **Next**.</span></span>

    ![Serbest bırakılacak ürünü seçme](media/create-new-product-4.png)

1. <span data-ttu-id="a7fb8-141">Serbest bırakılacak ürün çeşitleri kümesini ve ardından **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Serbest bırakılacak çeşitleri seçme](media/create-new-product-5.png)

1. <span data-ttu-id="a7fb8-143">Tüzel kişiliği ve ardından **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-143">Select the legal entity, and then select **Next**.</span></span>

    ![Tüzel kişilik seç](media/create-new-product-6.png)

1. <span data-ttu-id="a7fb8-145">**Bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-145">Select **Finish**.</span></span>

    ![Ürün serbest bırakma işlemini bitirme](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="a7fb8-147">Serbest bırakılmış bir ürünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a7fb8-147">Configure a released product</span></span>

<span data-ttu-id="a7fb8-148">Ürün serbest bırakıldıktan sonra, ürün için fiyat eklemeyi içeren ek yapılandırma gerektirir.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="a7fb8-149">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kategoriye göre serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="a7fb8-150">Serbest bırakılan ürünle ilgili ürün kategorisi düğümünü ve ardından ürün listesinden ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="a7fb8-151">Eylem bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="a7fb8-152">**Satınalma** bölümünde, **Birim**, **Fiyat** ve **Miktar**'ı içeren tüm gerekli özellikleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="a7fb8-153">Eksik alanlar için herhangi bir hata raporlanmamasını sağlamak için, eylem bölmesinde, **Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="a7fb8-154">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a7fb8-155">Aşağıdaki resimde, serbest bırakılmış bir ürün için yapılandırma örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a7fb8-155">The following image shows an example configuration for a released product.</span></span>

![Serbest bırakılmış ürünü yapılandırma](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="a7fb8-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a7fb8-157">Additional resources</span></span>

[<span data-ttu-id="a7fb8-158">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7fb8-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="a7fb8-159">Çeşit grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7fb8-159">Create a variant group</span></span>](create-variant-group.md) 
