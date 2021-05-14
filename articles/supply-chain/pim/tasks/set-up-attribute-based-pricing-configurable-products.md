---
title: Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama
description: Bu konu, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını açıklar.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921253"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="befb3-103">Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="befb3-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="befb3-104">Bu konu, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="befb3-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="befb3-105">Önkoşul olarak bir veya daha fazla bileşen ve özniteliğe sahip bir ürün yapılandırma modeline sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="befb3-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="befb3-106">Bu yordam, USMF demo veri şirketindeki Son Teknoloji Hoparlör ürün modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="befb3-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="befb3-107">Genel olarak bu yordamı bir ürün yöneticisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="befb3-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="befb3-108">Yeni bir fiyat modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="befb3-108">Create a new price model</span></span>

1. <span data-ttu-id="befb3-109">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="befb3-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="befb3-110">Listede, **Son Teknoloji Hoparlör** satırını seçin ancak ad bağlantısını seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="befb3-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="befb3-111">Eylem Bölmesinde, **Model**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="befb3-112">**Fiyat modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-112">Select **Price models**.</span></span>
1. <span data-ttu-id="befb3-113">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-113">Select **New**.</span></span>
1. <span data-ttu-id="befb3-114">**Fiyat modeli adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="befb3-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="befb3-115">Modelin tanımlanmasını kolaylaştıracak bir ad kullanın.</span><span class="sxs-lookup"><span data-stu-id="befb3-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="befb3-116">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="befb3-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="befb3-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="befb3-118">Fiyat öğeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="befb3-118">Add price elements</span></span>

1. <span data-ttu-id="befb3-119">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-119">Select **Edit**.</span></span> <span data-ttu-id="befb3-120">Ürün modelindeki her bileşen, taban fiyat öğesine ve istenen sayıda fiyat ifade kuralına sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="befb3-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="befb3-121">Ayrıca farklı para birimlerinde fiyatlar da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="befb3-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="befb3-122">**Taban fiyat ifadesi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="befb3-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="befb3-123">Örneğin 100 yazın.</span><span class="sxs-lookup"><span data-stu-id="befb3-123">For example, type 100.</span></span> <span data-ttu-id="befb3-124">Taban fiyat ifadesi sayısal bir değer olabilir veya bir veya daha fazla özniteliği kapsayan aritmetik hesaplamadan oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="befb3-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="befb3-125">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-125">Select **Add**.</span></span>
4. <span data-ttu-id="befb3-126">**Ad** alanına `Rosewood` yazın.</span><span class="sxs-lookup"><span data-stu-id="befb3-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="befb3-127">Fiyat ifadesi adı fiyat öğesinin neyi temsil ettiğini tanımlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="befb3-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="befb3-128">Bu örnekte, Rosewood hoparlör kabini rengi seçeneği için bir fiyat öğesi oluşturuyoruz.</span><span class="sxs-lookup"><span data-stu-id="befb3-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="befb3-129">**Koşulu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-129">Select **Edit condition**.</span></span> <span data-ttu-id="befb3-130">Fiyat koşulu, yalnızca özniteliklerin belirli bir birleşimi varsa bir fiyat ifadesinin satış fiyatına dahil edilmesini garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="befb3-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="befb3-131">**ConstraintBody** alanına `CabinetFinish=="Rosewood"` girin.</span><span class="sxs-lookup"><span data-stu-id="befb3-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="befb3-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="befb3-132">Select **OK**.</span></span>
8. <span data-ttu-id="befb3-133">**İfade** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="befb3-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="befb3-134">Örneğin, `50` yazın.</span><span class="sxs-lookup"><span data-stu-id="befb3-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="befb3-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="befb3-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]