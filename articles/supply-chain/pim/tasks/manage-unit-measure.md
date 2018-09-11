--- 
title: "Ölçü birimini yönetme"
description: "Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir."
author: sorenva
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 43e645eaf6d301379182c8279dd3657a36384d5e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="f5914-103">Ölçü birimini yönetme</span><span class="sxs-lookup"><span data-stu-id="f5914-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5914-104">Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5914-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="f5914-105">Bu yordamı demo verileri veya kendi verilerinizi kullanarak adım adım yerine getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5914-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="f5914-106">Serbest bırakılan ürün bakımı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="f5914-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="f5914-107">Birimleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f5914-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="f5914-108">Bir ölçü birimi oluşturun</span><span class="sxs-lookup"><span data-stu-id="f5914-108">Create a unit of measure</span></span>
1. <span data-ttu-id="f5914-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-109">Click New.</span></span>
2. <span data-ttu-id="f5914-110">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f5914-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="f5914-111">Bir ölçü birimini referans gösterirken Kimliğini veya sembolünü girin.</span><span class="sxs-lookup"><span data-stu-id="f5914-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="f5914-112">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f5914-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f5914-113">Sistem dilinde ölçü için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="f5914-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="f5914-114">Birim sınıfı alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f5914-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="f5914-115">Birimi sınıfı, ölçü biriminin alan, hacim veya miktar gibi mantıksal bir gruplandırmalardan hangisinin parçası olduğunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f5914-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="f5914-116">Ondalık hassasiyeti alanına bir numara girmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f5914-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="f5914-117">Ölçü birimi için hesaplama tamamlandığında, çevirilen ölçü biriminin kaç ondalık basamağa yuvarlanacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f5914-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="f5914-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="f5914-119">Birim çevirilerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="f5914-119">Define unit translations</span></span>
1. <span data-ttu-id="f5914-120">Birim metinleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-120">Click Unit texts.</span></span>
2. <span data-ttu-id="f5914-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-121">Click New.</span></span>
    * <span data-ttu-id="f5914-122">Müşteri veya satıcıya özgü dillerde ölçü birimini temsil edecek bir sembol veya Kimliğin çevirisini oluştururken birim yazısı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5914-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="f5914-123">Dil alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f5914-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="f5914-124">Metin alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f5914-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="f5914-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-125">Click Save.</span></span>
6. <span data-ttu-id="f5914-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f5914-126">Close the page.</span></span>
7. <span data-ttu-id="f5914-127">Çevrilmiş birim açıklamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="f5914-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-128">Click New.</span></span>
    * <span data-ttu-id="f5914-129">Ölçü birimi için dile özgü açıklamalar tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="f5914-130">Dil alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f5914-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="f5914-131">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f5914-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f5914-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-132">Click Save.</span></span>
12. <span data-ttu-id="f5914-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f5914-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="f5914-134">Birim dönüştürme kurallarını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="f5914-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="f5914-135">Birim dönüştürmeleri'ne tıklayın</span><span class="sxs-lookup"><span data-stu-id="f5914-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="f5914-136">Ölçü birimini seçili birim sınıfında bir başka ölçü birimine dönüştürmek için kurallar tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="f5914-137">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="f5914-138">Faktör alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f5914-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="f5914-139">İlk birim ve son birim arasında dönüştürme faktörü.</span><span class="sxs-lookup"><span data-stu-id="f5914-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="f5914-140">Örneğin, bir metrede 100 santimetre olduğu için santimetreden metreye dönüştürme faktörü 100'dür.</span><span class="sxs-lookup"><span data-stu-id="f5914-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="f5914-141">Hedef birim alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f5914-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="f5914-142">Yuvarlama alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f5914-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="f5914-143">Çevrilen değerin nasıl yuvarlanması gerektiğini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="f5914-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="f5914-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5914-144">Click OK.</span></span>
7. <span data-ttu-id="f5914-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f5914-145">Close the page.</span></span>


