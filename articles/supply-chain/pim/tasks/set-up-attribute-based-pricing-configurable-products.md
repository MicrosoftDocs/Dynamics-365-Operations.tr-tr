---
title: Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama
description: Bu konu, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a75f3afcf4761ac6a9575eae9a620a1e9f01c8e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439147"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="5ff44-103">Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="5ff44-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ff44-104">Bu konu, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="5ff44-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="5ff44-105">Önkoşul olarak bir veya daha fazla bileşen ve özniteliğe sahip bir ürün yapılandırma modeline sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5ff44-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="5ff44-106">Bu yordam, USMF demo veri şirketindeki Son Teknoloji Hoparlör ürün modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ff44-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="5ff44-107">Genel olarak bu yordamı bir ürün yöneticisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ff44-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="5ff44-108">Yeni bir fiyat modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="5ff44-108">Create a new price model</span></span>
1. <span data-ttu-id="5ff44-109">Giriş sayfasında **Ürün çeşidi model tanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="5ff44-110">**Bağlantılar** bölümünde **Ürün yapılandırma modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="5ff44-111">Listede, **Son Teknoloji Hoparlör** satırını seçin ancak ad bağlantısını seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="5ff44-112">Eylem Bölmesinde, **Model**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="5ff44-113">**Fiyat modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-113">Select **Price models**.</span></span>
6. <span data-ttu-id="5ff44-114">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-114">Select **New**.</span></span>
7. <span data-ttu-id="5ff44-115">**Fiyat modeli adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="5ff44-116">Modelin tanımlanmasını kolaylaştıracak bir ad kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="5ff44-117">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="5ff44-118">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="5ff44-119">Fiyat öğeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="5ff44-119">Add price elements</span></span>
1. <span data-ttu-id="5ff44-120">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-120">Select **Edit**.</span></span> <span data-ttu-id="5ff44-121">Ürün modelindeki her bileşen, taban fiyat öğesine ve istenen sayıda fiyat ifade kuralına sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="5ff44-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="5ff44-122">Ayrıca farklı para birimlerinde fiyatlar da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ff44-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="5ff44-123">**Taban fiyat ifadesi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="5ff44-124">Örneğin 100 yazın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-124">For example, type 100.</span></span> <span data-ttu-id="5ff44-125">Taban fiyat ifadesi sayısal bir değer olabilir veya bir veya daha fazla özniteliği kapsayan aritmetik hesaplamadan oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="5ff44-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="5ff44-126">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-126">Select **Add**.</span></span>
4. <span data-ttu-id="5ff44-127">**Ad** alanına `Rosewood` yazın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="5ff44-128">Fiyat ifadesi adı fiyat öğesinin neyi temsil ettiğini tanımlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="5ff44-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="5ff44-129">Bu örnekte, Rosewood hoparlör kabini rengi seçeneği için bir fiyat öğesi oluşturuyoruz.</span><span class="sxs-lookup"><span data-stu-id="5ff44-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="5ff44-130">**Koşulu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-130">Select **Edit condition**.</span></span> <span data-ttu-id="5ff44-131">Fiyat koşulu, yalnızca özniteliklerin belirli bir birleşimi varsa bir fiyat ifadesinin satış fiyatına dahil edilmesini garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="5ff44-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="5ff44-132">**ConstraintBody** alanına `CabinetFinish=="Rosewood"` girin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="5ff44-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5ff44-133">Select **OK**.</span></span>
8. <span data-ttu-id="5ff44-134">**İfade** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="5ff44-135">Örneğin, `50` yazın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="5ff44-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5ff44-136">Close the page.</span></span>

