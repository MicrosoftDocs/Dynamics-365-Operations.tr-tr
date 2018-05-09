---
title: "Perakende hiyerarşileri"
description: "Bu makalede Microsoft Dynamics 365 for Retail'deki perakende hiyerarşileri açıklanmıştır."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 012906c0b7b718d86ccc760c0b82df14501beabe
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="retail-hierarchies"></a><span data-ttu-id="5ad19-103">Perakende hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="5ad19-103">Retail hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ad19-104">Bu makalede Microsoft Dynamics 365 for Retail'deki perakende hiyerarşileri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5ad19-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5ad19-105">Perakende kanallarınız üzerinden sattığınız ürünleri organize etmek için bir perakende kategori hiyerarşisi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="5ad19-106">Ürünleri kategorize etmek veya gruplamak için perakende ürün hiyerarşilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="5ad19-107">Daha sonra, ürün çeşitleri ve müşteri bağlılık programları oluşturmak için bu ürünleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="5ad19-108">Ayrıca, ürün öznitelikleri ve özellikler, fiyatlandırma yapısı atayabilir, ürün promosyonlarına ürün ekleyebilir ve raporlama için ürünleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="5ad19-109">Tüm ürünleri ve kuruluşunuzdaki kategorileri temsil edecek bir perakende kategori hiyerarşisi oluşturun ve sonra bu kategori hiyerarşisini birden çok amaç için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="5ad19-110">Alternatif olarak, ürün promosyonları gibi özel amaçlar için birden fazla perakende kategori hiyerarşisi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="5ad19-111">Perakende ürün hiyerarşisi oluşturduğunuzda, kategori hiyerarşisinin amacını belirlemek için bir kategori hiyerarşisi türü atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ad19-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="5ad19-112">Örneğin, ürünlere çevrimiçi veya satış noktası (POS) kategorisine göre göz atarken **Perakende gezinme hiyerarşisine** atanan tek ürün hiyerarşisi türüne başvurulur.</span><span class="sxs-lookup"><span data-stu-id="5ad19-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="5ad19-113">Perakende hiyerarşisi türleri</span><span class="sxs-lookup"><span data-stu-id="5ad19-113">Retail hierarchy types</span></span>
<span data-ttu-id="5ad19-114">Aşağıdaki tabloda kullanılabilir ve her bir türün genel amacına uygun perakende kategorisi türleri listelenir.</span><span class="sxs-lookup"><span data-stu-id="5ad19-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="5ad19-115">Kategori hiyerarşisi türü</span><span class="sxs-lookup"><span data-stu-id="5ad19-115">Category hierarchy type</span></span>       | <span data-ttu-id="5ad19-116">Amaç</span><span class="sxs-lookup"><span data-stu-id="5ad19-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad19-117">Perakende ürün hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="5ad19-117">Retail product hierarchy</span></span>      | <span data-ttu-id="5ad19-118">Kuruluşunuzun genel ürün hiyerarşisini tanımlamak için bu hiyerarşi türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ad19-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="5ad19-119">Bu hiyerarşi türünü alım satım, fiyatlandırma ve promosyonlar, raporlama ve ürün çeşidi planlaması için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="5ad19-120">Yalnızca tek bir perakende ürün hiyerarşisi bu hiyerarşi türüne atanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ad19-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="5ad19-121">Tamamlayıcı perakende hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="5ad19-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="5ad19-122">Oluşturmak istediğiniz her bir ek perakende kategori hiyerarşileri için bu hiyerarşi türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ad19-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="5ad19-123">Örneğin, ilkbaharda mayolar için bir promosyonunuz var.</span><span class="sxs-lookup"><span data-stu-id="5ad19-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="5ad19-124">O halde, mayo ürünlerini ayrı bir kategori hiyerarşisine eklersiniz ve çeşitli ürün kategorilerine promosyonlu fiyatlandırma uygularsınız.</span><span class="sxs-lookup"><span data-stu-id="5ad19-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="5ad19-125">Perakende gezinme hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="5ad19-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="5ad19-126">Ürünleri çevrimiçi olarak veya satış noktasında göz atılabilmesi amacıyla gruplamak ve kategoriler halinde düzenlemek için bu hiyerarşi türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ad19-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="5ad19-127">Ürünlerinizi yapılandırmak için bir perakende kategori hiyerarşisi kullanarak ürün özniteliklerini ve özelliklerini kategori düzeyinde ayarlayabilir ve sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="5ad19-128">Bu öznitelikler ve özellikler ürün boyutlarına ve POS ayarlarına ilişkin ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="5ad19-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="5ad19-129">Kategorilere atadığınız herhangi bir ürün, tanımladığınız öznitelikleri ve özellikleri otomatik olarak devralır.</span><span class="sxs-lookup"><span data-stu-id="5ad19-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="5ad19-130">Herhangi bir ürünün özellik ayarlarını seçilen kategorideki birden çok ürüne de aynı anda kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad19-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




