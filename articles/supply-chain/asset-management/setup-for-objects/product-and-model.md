---
title: Varlık üreticileri ve modelleri
description: Bu konu, Varlık Yönetimi'nde varlık üreticilerinin ve ilgili modellerin nasıl ayarlanacağını açıklar.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cec4f644af4a087464635d9a7ca825eb354747eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259974"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="1d98c-103">Varlık üreticileri ve modelleri</span><span class="sxs-lookup"><span data-stu-id="1d98c-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1d98c-104">Bu konu, Varlık Yönetimi'nde varlık üreticilerinin ve ilgili modellerin nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="1d98c-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="1d98c-105">Modeller, varlık türlerine bağlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="1d98c-106">Ürün model ilişkileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="1d98c-106">Set up product-model relations</span></span>

1. <span data-ttu-id="1d98c-107">**Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Üretici ve model**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="1d98c-108">Yeni ürün oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="1d98c-109">**Üretici** alanına, varlık üreticisi için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="1d98c-110">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="1d98c-111">**Modeller** hızlı sekmesinde, varlık üreticisiyle ilişkili olması gereken bir varlık modeli oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="1d98c-112">**Model** alanına, varlık modeli için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="1d98c-113">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="1d98c-114">**Varlık türü** alanında, üretici modelinin ilgili olması gereken varlık türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1d98c-115">Ayrıca varlık türleri, üreticiler ve modeller için **Varlık türleri** aramasında ilişkiler ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d98c-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="1d98c-116">Daha fazla bilgi için bkz. [Varlık türleri](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="1d98c-116">For more information, see [Asset types](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="1d98c-117">**Ayrıntılar** hızlı sekmesinde, **Modeller** alanı seçili varlık üreticisinde ayarlanan varlık modeli sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="1d98c-118">**Varlıklar** alanı seçili üreticiyi kullanan kıymet sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="1d98c-119">**Varlıklar** alanı üretici modelini kullanan nesnelerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="1d98c-120">Bir varlık türünün hiçbir varlık üreticisi modeli ilişkisi olmayabilir, bir varlık üreticisi modeliyle ilşikili olabilir veya birden çok varlık üreticisi modeliyle ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="1d98c-121">Bir varlık türü en az bir üretici modeliyle ilişkiliyse, yalnızca **Üretici modeli** aramasında ayarlanan kombinasyonlar bir varlık türü, üretici ve model kombinasyonunun bulunduğu Varlık Yönetimi sayfalarında seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="1d98c-122">Bu sayfalar **Tüm varlıklar**, **Varlık hizmet düzeyleri**, **iş türü varsayılanları** ve **Bakım bütçesi satırları**'nı içerir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="1d98c-123">Bazı varlık türleri herhangi bir üretici modeliyle ilişkili değilse, yalnızca bu varlık türleri ve varlık türleriyle hiçbir ilişkisi olmayan üretici modelleri sayfalarda gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="1d98c-124">Bir nesne üzerinde üretici ve model seçme</span><span class="sxs-lookup"><span data-stu-id="1d98c-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="1d98c-125">**Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="1d98c-126">**Varlık** sütununda, varlık için bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="1d98c-127">**Ayrıntılar** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1d98c-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="1d98c-128">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-128">Select **Edit**.</span></span>
4. <span data-ttu-id="1d98c-129">**Genel** hızlı sekmesinde, **Üretici** ve **Model** alanlarında değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="1d98c-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]