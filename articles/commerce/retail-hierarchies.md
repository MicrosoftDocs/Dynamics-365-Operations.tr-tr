---
title: Commerce hiyerarşileri
description: Bu konu, Dynamics 365 Commerce içinde hiyerarşilerini açıklar.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 94b391ab5028f76debb75d25ac9469e25361cb12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979628"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="ba971-103">Commerce hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="ba971-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ba971-104">Bu konu, Dynamics 365 Commerce içinde hiyerarşilerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ba971-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ba971-105">Kanallarınız üzerinden sattığınız ürünleri organize etmek için bir kategori hiyerarşisi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="ba971-106">Ürünleri kategorize etmek veya gruplamak için ürün hiyerarşilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="ba971-107">Daha sonra, ürün çeşitleri ve müşteri bağlılık programları oluşturmak için bu ürünleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="ba971-108">Ayrıca, ürün öznitelikleri ve özellikler, fiyatlandırma yapısı atayabilir, ürün promosyonlarına ürün ekleyebilir ve raporlama için ürünleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="ba971-109">Tüm ürünleri ve kuruluşunuzdaki kategorileri temsil edecek bir kategori hiyerarşisi oluşturun ve sonra bu kategori hiyerarşisini birden çok amaç için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="ba971-110">Alternatif olarak, ürün promosyonları gibi özel amaçlar için birden fazla kategori hiyerarşisi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="ba971-111">Ürün hiyerarşisi oluşturduğunuzda, kategori hiyerarşisinin amacını belirlemek için bir kategori hiyerarşisi türü atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba971-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="ba971-112">Örneğin, ürünlere çevrimiçi veya satış noktası (POS) kategorisine göre göz atarken **Commerce gezinme hiyerarşisine** atanan tek ürün hiyerarşisi türüne başvurulur.</span><span class="sxs-lookup"><span data-stu-id="ba971-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="ba971-113">Hiyerarşi türü</span><span class="sxs-lookup"><span data-stu-id="ba971-113">Hierarchy types</span></span>

<span data-ttu-id="ba971-114">Aşağıdaki tabloda kullanılabilir ve her bir türün genel amacına uygun kategorisi türleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="ba971-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="ba971-115">Kategori hiyerarşisi türü</span><span class="sxs-lookup"><span data-stu-id="ba971-115">Category hierarchy type</span></span>       | <span data-ttu-id="ba971-116">Amaç</span><span class="sxs-lookup"><span data-stu-id="ba971-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="ba971-117">Ürün hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="ba971-117">Product hierarchy</span></span>      | <span data-ttu-id="ba971-118">Kuruluşunuzun genel ürün hiyerarşisini tanımlamak için bu hiyerarşi türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba971-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="ba971-119">Bu hiyerarşi türünü alım satım, fiyatlandırma ve promosyonlar, raporlama ve ürün çeşidi planlaması için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="ba971-120">Yalnızca tek bir ürün hiyerarşisi bu hiyerarşi türüne atanabilir.</span><span class="sxs-lookup"><span data-stu-id="ba971-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="ba971-121">Tamamlayıcı hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="ba971-121">Supplemental hierarchy</span></span> | <span data-ttu-id="ba971-122">Oluşturmak istediğiniz her bir ek kategori hiyerarşileri için bu hiyerarşi türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba971-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="ba971-123">Örneğin, ilkbaharda mayolar için bir promosyonunuz var.</span><span class="sxs-lookup"><span data-stu-id="ba971-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="ba971-124">O halde, mayo ürünlerini ayrı bir kategori hiyerarşisine eklersiniz ve çeşitli ürün kategorilerine promosyonlu fiyatlandırma uygularsınız.</span><span class="sxs-lookup"><span data-stu-id="ba971-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="ba971-125">Gezinme hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="ba971-125">Navigation hierarchy</span></span>   | <span data-ttu-id="ba971-126">Ürünleri çevrimiçi olarak veya satış noktasında göz atılabilmesi amacıyla gruplamak ve kategoriler halinde düzenlemek için bu hiyerarşi türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="ba971-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="ba971-127">Ürünlerinizi yapılandırmak için bir kategori hiyerarşisi kullanarak ürün özniteliklerini ve özelliklerini kategori düzeyinde ayarlayabilir ve sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="ba971-128">Bu öznitelikler ve özellikler ürün boyutlarına ve POS ayarlarına ilişkin ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="ba971-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="ba971-129">Kategorilere atadığınız herhangi bir ürün, tanımladığınız öznitelikleri ve özellikleri otomatik olarak devralır.</span><span class="sxs-lookup"><span data-stu-id="ba971-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="ba971-130">Herhangi bir ürünün özellik ayarlarını seçilen kategorideki birden çok ürüne de aynı anda kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba971-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
