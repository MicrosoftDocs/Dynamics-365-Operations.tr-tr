---
title: Bakım öznitelik türleri
description: Bu konuda Kıymet Yönetimi'nde öznitelik türleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c07f303b72f286c33979181fca1592b47efa1303
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571243"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="f7f32-103">Bakım öznitelik türleri</span><span class="sxs-lookup"><span data-stu-id="f7f32-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f7f32-104">Bu konuda Kıymet Yönetimi'nde öznitelik türleri oluşturma işlemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f7f32-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="f7f32-105">Öznitelikler, çeşitli öğelerin özelliklerini açıklamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7f32-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="f7f32-106">Aşağıdaki öğelerin özniteliklerini ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f7f32-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="f7f32-107">İşlem yapılacak yerleşim türleri</span><span class="sxs-lookup"><span data-stu-id="f7f32-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="f7f32-108">İşlem yapılacak yerleşimler</span><span class="sxs-lookup"><span data-stu-id="f7f32-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="f7f32-109">Kıymet türleri</span><span class="sxs-lookup"><span data-stu-id="f7f32-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="f7f32-110">Varlıklar</span><span class="sxs-lookup"><span data-stu-id="f7f32-110">Assets</span></span>

<span data-ttu-id="f7f32-111">Ayarlayabileceğiniz öznitelikler öğeye bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="f7f32-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="f7f32-112">Örneğin işlem yapılacak yerleşim için yerleşimin fiziksel boyutu ile yapılandırma özniteliklerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7f32-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="f7f32-113">Bir kıymet türü veya bir kıymet için motor hacmi, güç tüketimi ve farklı koşullarda maksimum yük kapasitesi özniteliklerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7f32-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="f7f32-114">Öznitelik türleri oluştur</span><span class="sxs-lookup"><span data-stu-id="f7f32-114">Create attribute types</span></span>

<span data-ttu-id="f7f32-115">Kendi öznitelik türlerinizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7f32-115">You can create your own attribute types.</span></span> <span data-ttu-id="f7f32-116">Ayrıca, ürün boyutlarını **Öznitelik türleri** sayfasına aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7f32-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="f7f32-117">**Kıymet yönetimi** \> **Kurulum** \> **Öznitelik türleri** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="f7f32-118">Öznitelik türlerini ilk kez ayarladığınızda standart ürün boyutlarını otomatik olarak aktarmak için **Ürün boyutları oluştur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="f7f32-119">Yeni bir öznitelik türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="f7f32-120">**Öznitelik türü** alanına, öznitelik türü için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="f7f32-121">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="f7f32-122">**Birim** alanında, gerektiği şekilde, ilgili öznitelik birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="f7f32-123">**Veri türü** alanında birim için bir veri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="f7f32-124">Veri türü olarak **Dize** seçtiyseniz öznitelik türü değeri oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="f7f32-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="f7f32-125">Öznitelik türünü ve ardından **Değerler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="f7f32-126">**Öznitelik değerleri** alanında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="f7f32-127">**Öznitelik türü** alanında bir öznitelik türü (boyut) seçin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="f7f32-128">**Değer** alanına ilgili değeri girin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="f7f32-129">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="f7f32-130">Kaydı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-130">Save the record.</span></span>
    7. <span data-ttu-id="f7f32-131">**Öznitelik türleri** sayfasına dönün.</span><span class="sxs-lookup"><span data-stu-id="f7f32-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="f7f32-132">Kaydı kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f7f32-132">Save the record.</span></span>

    <span data-ttu-id="f7f32-133">**İşlem yapılacak yerleşim türleri** alanında öznitelik türünü kullanan işlem yapılacak yerleşimlerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7f32-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="f7f32-134">**Kıymet türleri** alanı bunu kullanan kıymet türlerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7f32-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
