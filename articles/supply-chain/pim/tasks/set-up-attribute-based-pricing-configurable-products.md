--- 
title: "Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama"
description: "Bu yordam, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a3afc9b268e9bab1b33013cc49ca372f89d8957c
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="0a7b7-103">Yapılandırılabilir ürünler için öznitelik tabanlı fiyatlandırmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="0a7b7-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a7b7-104">Bu yordam, öznitelik tabanlı fiyatlandırmanın nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="0a7b7-105">Önkoşul olarak bir veya daha fazla bileşen ve özniteliğe sahip bir ürün yapılandırma modeline sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="0a7b7-106">Bu yordam, USMF demo veri şirketindeki Son Teknoloji Hoparlör ürün modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="0a7b7-107">Genel olarak bu yordamı bir ürün yöneticisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="0a7b7-108">Yeni bir fiyat modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a7b7-108">Create a new price model</span></span>
1. <span data-ttu-id="0a7b7-109">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="0a7b7-110">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="0a7b7-111">Listede, Son Teknoloji Hoparlör satırını seçin ancak ad bağlantısına tıklamayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="0a7b7-112">Eylem Bölmesinde,Model öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="0a7b7-113">Fiyat modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-113">Click Price models.</span></span>
6. <span data-ttu-id="0a7b7-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-114">Click New.</span></span>
7. <span data-ttu-id="0a7b7-115">Fiyat modeli ad alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="0a7b7-116">Modelin tanımlanmasını kolaylaştıracak bir ad kullanın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="0a7b7-117">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="0a7b7-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="0a7b7-119">Fiyat öğeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="0a7b7-119">Add price elements</span></span>
1. <span data-ttu-id="0a7b7-120">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-120">Click Edit.</span></span>
    * <span data-ttu-id="0a7b7-121">Ürün modelindeki her bileşen, taban fiyat öğesine ve istenen sayıda fiyat ifade kuralına sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="0a7b7-122">Ayrıca farklı para birimlerinde fiyatlar da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="0a7b7-123">Taban fiyat ifadesi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="0a7b7-124">Örneğin 100 yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-124">For example, type 100.</span></span>   <span data-ttu-id="0a7b7-125">Taban fiyat ifadesi sayısal bir değer olabilir veya bir veya daha fazla özniteliği kapsayan aritmetik hesaplamadan oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="0a7b7-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-126">Click Add.</span></span>
4. <span data-ttu-id="0a7b7-127">Ad alanına "Rosewood" yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="0a7b7-128">Fiyat ifadesi adı fiyat öğesinin neyi temsil ettiğini tanımlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="0a7b7-129">Bu örnekte, Rosewood hoparlör kabini rengi seçeneği için bir fiyat öğesi oluşturuyoruz.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="0a7b7-130">Koşulu düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-130">Click Edit condition.</span></span>
    * <span data-ttu-id="0a7b7-131">Fiyat koşulu, yalnızca özniteliklerin belirli bir birleşimi varsa bir fiyat ifadesinin satış fiyatına dahil edilmesini garanti etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="0a7b7-132">ConstraintBody alanına "CabinetFinish=="Rosewood"" yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="0a7b7-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-133">Click OK.</span></span>
8. <span data-ttu-id="0a7b7-134">İfade alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="0a7b7-135">Örneğin 50 yazın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-135">For example, type 50.</span></span>  
9. <span data-ttu-id="0a7b7-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-136">Close the page.</span></span>
10. <span data-ttu-id="0a7b7-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0a7b7-137">Close the page.</span></span>


