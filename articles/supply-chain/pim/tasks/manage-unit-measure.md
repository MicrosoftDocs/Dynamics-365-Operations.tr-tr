---
title: Ölçü birimini yönetme
description: Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.
author: sorenva
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 966e189e7395bec15d2c62735c6df3df2ab34b8a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817977"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="aaf7e-103">Ölçü birimini yönetme</span><span class="sxs-lookup"><span data-stu-id="aaf7e-103">Manage unit of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aaf7e-104">Bu yordam, bir ölçü birimi tanımlamayı, bu birim ve açıklaması için çeviriler oluşturmayı ve ilgili birimler için dönüştürme kuralları tanımlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="aaf7e-105">Bu yordamı demo verileri veya kendi verilerinizi kullanarak adım adım yerine getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="aaf7e-106">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürün bakımı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-106">Go to **Navigation pane > Modules > Product information management > Released product maintenance**.</span></span>
2. <span data-ttu-id="aaf7e-107">**Birimler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-107">Click **Units**.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="aaf7e-108">Bir ölçü birimi oluşturun</span><span class="sxs-lookup"><span data-stu-id="aaf7e-108">Create a unit of measure</span></span>
1. <span data-ttu-id="aaf7e-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-109">Click **New**.</span></span>
2. <span data-ttu-id="aaf7e-110">**Birim** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-110">In the **Unit** field, type a value.</span></span> <span data-ttu-id="aaf7e-111">Bir ölçü birimini referans gösterirken Kimliğini veya sembolünü girin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="aaf7e-112">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-112">In the **Description** field, type a value.</span></span> <span data-ttu-id="aaf7e-113">Sistem dilinde ölçü için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="aaf7e-114">**Birim sınıfı** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-114">In the **Unit class** field, select an option.</span></span> <span data-ttu-id="aaf7e-115">Birimi sınıfı, ölçü biriminin alan, hacim veya miktar gibi mantıksal bir gruplandırmalardan hangisinin parçası olduğunu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="aaf7e-116">**Ondalık hassasiyeti** alanına bir numara girmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-116">In the **Decimal precision** field, enter a number.</span></span> <span data-ttu-id="aaf7e-117">Ölçü birimi için hesaplama tamamlandığında, çevirilen ölçü biriminin kaç ondalık basamağa yuvarlanacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="aaf7e-118">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-118">Click **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="aaf7e-119">Birim çevirilerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="aaf7e-119">Define unit translations</span></span>
1. <span data-ttu-id="aaf7e-120">**Eylem Bölmesi**'nde, **Birim metinleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-120">On the **Action Pane**, click **Unit texts**.</span></span>
2. <span data-ttu-id="aaf7e-121">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-121">Click **New**.</span></span> <span data-ttu-id="aaf7e-122">Müşteri veya satıcıya özgü dillerde ölçü birimini temsil edecek bir sembol veya Kimliğin çevirisini oluştururken birim yazısı kullanın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="aaf7e-123">**Dil** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-123">In the **Language** field, enter or select a value.</span></span>
4. <span data-ttu-id="aaf7e-124">**Metin** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-124">In the **Text** field, type a value.</span></span>
5. <span data-ttu-id="aaf7e-125">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-125">Click **Save**.</span></span>
6. <span data-ttu-id="aaf7e-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-126">Close the page.</span></span>
7. <span data-ttu-id="aaf7e-127">**Eylem Bölmesi**'nde, **Çevrilmiş birim açıklamaları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-127">On the **Action Pane**, click **Translated unit descriptions**.</span></span>
8. <span data-ttu-id="aaf7e-128">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-128">Click **New**.</span></span> <span data-ttu-id="aaf7e-129">Ölçü birimi için dile özgü açıklamalar tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="aaf7e-130">**Dil** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-130">In the **Language** field, enter or select a value.</span></span>
10. <span data-ttu-id="aaf7e-131">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-131">In the **Description** field, type a value.</span></span>
11. <span data-ttu-id="aaf7e-132">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-132">Click **Save**.</span></span>
12. <span data-ttu-id="aaf7e-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="aaf7e-134">Birim dönüştürme kurallarını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="aaf7e-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="aaf7e-135">**Eylem Bölmesi**'nde, **Birim dönüştürmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-135">On the **Action Pane**, click **Unit conversions**.</span></span> <span data-ttu-id="aaf7e-136">Ölçü birimini seçili birim sınıfında bir başka ölçü birimine dönüştürmek için kurallar tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="aaf7e-137">Açılır iletişim kutusunu açmak için **Yeni** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-137">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="aaf7e-138">**Faktör** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-138">In the **Factor** field, enter a number.</span></span> <span data-ttu-id="aaf7e-139">İlk birim ve son birim arasında dönüştürme faktörü.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="aaf7e-140">Örneğin, bir metrede 100 santimetre olduğu için santimetreden metreye dönüştürme faktörü 100'dür.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="aaf7e-141">**Hedef birim** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-141">In the **To unit** field, enter or select a value.</span></span>
5. <span data-ttu-id="aaf7e-142">**Yuvarlama** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-142">In the **Rounding** field, select an option.</span></span> <span data-ttu-id="aaf7e-143">Çevrilen değerin nasıl yuvarlanması gerektiğini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="aaf7e-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="aaf7e-144">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-144">Click **OK**.</span></span>
7. <span data-ttu-id="aaf7e-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aaf7e-145">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]