---
title: Bakım öznitelik türleri
description: Bu konuda Kıymet Yönetimi'nde öznitelik türleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b221e9168fc60b5927bb92de80bd6b9614ad591c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019816"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="5fee4-103">Bakım öznitelik türleri</span><span class="sxs-lookup"><span data-stu-id="5fee4-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5fee4-104">Bu konuda Kıymet Yönetimi'nde öznitelik türleri oluşturma işlemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5fee4-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="5fee4-105">Öznitelikler, çeşitli öğelerin özelliklerini açıklamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5fee4-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="5fee4-106">Aşağıdaki öğelerin özniteliklerini ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5fee4-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="5fee4-107">İşlem yapılacak yerleşim türleri</span><span class="sxs-lookup"><span data-stu-id="5fee4-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="5fee4-108">İşlem yapılacak yerleşimler oluşturma</span><span class="sxs-lookup"><span data-stu-id="5fee4-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="5fee4-109">Varlık türleri</span><span class="sxs-lookup"><span data-stu-id="5fee4-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="5fee4-110">Varlıklar</span><span class="sxs-lookup"><span data-stu-id="5fee4-110">Assets</span></span>

<span data-ttu-id="5fee4-111">Ayarlayabileceğiniz öznitelikler öğeye bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="5fee4-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="5fee4-112">Örneğin işlem yapılacak yerleşim için yerleşimin fiziksel boyutu ile yapılandırma özniteliklerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fee4-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="5fee4-113">Bir kıymet türü veya bir kıymet için motor hacmi, güç tüketimi ve farklı koşullarda maksimum yük kapasitesi özniteliklerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fee4-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="5fee4-114">Öznitelik türleri oluştur</span><span class="sxs-lookup"><span data-stu-id="5fee4-114">Create attribute types</span></span>

<span data-ttu-id="5fee4-115">Kendi öznitelik türlerinizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fee4-115">You can create your own attribute types.</span></span> <span data-ttu-id="5fee4-116">Ayrıca, ürün boyutlarını **Öznitelik türleri** sayfasına aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5fee4-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="5fee4-117">**Kıymet yönetimi** \> **Kurulum** \> **Öznitelik türleri** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="5fee4-118">Öznitelik türlerini ilk kez ayarladığınızda standart ürün boyutlarını otomatik olarak aktarmak için **Ürün boyutları oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="5fee4-119">Yeni bir öznitelik türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="5fee4-120">**Öznitelik türü** alanına, öznitelik türü için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="5fee4-121">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="5fee4-122">**Birim** alanında, gerektiği şekilde, ilgili öznitelik birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="5fee4-123">**Veri türü** alanında birim için bir veri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="5fee4-124">Veri türü olarak **Dize** seçtiyseniz öznitelik türü değeri oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="5fee4-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="5fee4-125">Öznitelik türünü ve ardından **Değerler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="5fee4-126">**Öznitelik değerleri** alanında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="5fee4-127">**Öznitelik türü** alanında bir öznitelik türü (boyut) seçin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="5fee4-128">**Değer** alanına ilgili değeri girin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="5fee4-129">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="5fee4-130">Kaydı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-130">Save the record.</span></span>
    7. <span data-ttu-id="5fee4-131">**Öznitelik türleri** sayfasına dönün.</span><span class="sxs-lookup"><span data-stu-id="5fee4-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="5fee4-132">Kaydı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5fee4-132">Save the record.</span></span>

    <span data-ttu-id="5fee4-133">**İşlem yapılacak yerleşim türleri** alanında öznitelik türünü kullanan işlem yapılacak yerleşimlerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fee4-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="5fee4-134">**Kıymet türleri** alanı bunu kullanan kıymet türlerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5fee4-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
