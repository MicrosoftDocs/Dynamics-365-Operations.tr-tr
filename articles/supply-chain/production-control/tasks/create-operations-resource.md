---
title: Operasyon kaynağı oluşturma
description: Operasyon kaynağı, bir projenin veya bir üretim işleminin etkinliklerini gerçekleştirir.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91f5498bf5a5570c9d3b3f63e0a01b788fa00f35
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838643"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="3909a-103">Operasyon kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3909a-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3909a-104">Operasyon kaynağı, bir projenin veya bir üretim işleminin etkinliklerini gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="3909a-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="3909a-105">Bu prosedürler, size bir operasyon kaynağının nasıl tanımlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3909a-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="3909a-106">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3909a-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="3909a-107">Kaynaklar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3909a-107">Go to Resources.</span></span>
2. <span data-ttu-id="3909a-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3909a-108">Click New.</span></span>
3. <span data-ttu-id="3909a-109">Kaynak alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3909a-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="3909a-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="3909a-111">Kapasite ve tüketim parametrelerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="3909a-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="3909a-112">Operasyon bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3909a-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="3909a-113">Hurda yüzdesi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="3909a-114">Kurulum kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="3909a-115">Kurulum maliyetinin nasıl açıklanacağını tanımlayan maliyet kategorisini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="3909a-116">Çalışma süresi kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="3909a-117">Çalışma zamanının nasıl açıklanacağını tanımlayan maliyet kategorisini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="3909a-118">Miktar kategorisi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="3909a-119">Çıkış miktarına göre kaynak maliyetinin nasıl açıklanacağını tanımlayan maliyet kategorisini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="3909a-120">Kapasite birimi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="3909a-121">Operasyon kaynağının kapasitesinin ifade edileceği birimi belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="3909a-122">Kapasite alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="3909a-123">Verimlilik yüzdesi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="3909a-124">Operasyon kaynağından beklediğiniz verimliliği belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="3909a-125">Verimlilik yüzdesi, operasyon kaynağının iş çıkarma yeteneğini ayarlar ve kaynağa ayrılan zamanı etkiler.</span><span class="sxs-lookup"><span data-stu-id="3909a-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="3909a-126">Operasyon planlama yüzdesi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="3909a-127">Operasyon planlamasında kullanmak istediğiniz operasyon kaynağı kapasitesinin maksimum yüzdesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="3909a-128">Sınırlı kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="3909a-129">Operasyon kaynağı, mevcut kullanılabilir kapasiteye göre planlanacaksa ve mevcut kapasite rezervasyonları değerlendirilecekse bu seçeneği Evet yapın.</span><span class="sxs-lookup"><span data-stu-id="3909a-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="3909a-130">Bu seçenek Hayır yapılırsa, operasyon kaynağının sonsuz kapasiteye sahip olduğu varsayılır ve kaynak, kapasitesinin üzerinde rezerve edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3909a-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="3909a-131">Darboğazdaki kaynak alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="3909a-132">Çalışma zamanlarını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="3909a-132">Define working times</span></span>
1. <span data-ttu-id="3909a-133">Takvimler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3909a-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="3909a-134">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3909a-134">Click Add.</span></span>
3. <span data-ttu-id="3909a-135">Takvim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="3909a-136">Kaynak kapasitesini (saat cinsinden) tanımlayan çalışma zamanı takvimini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="3909a-137">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3909a-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3909a-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="3909a-139">Kaynak yeteneklerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="3909a-139">Define resource capabilities</span></span>
1. <span data-ttu-id="3909a-140">Yetenekler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3909a-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="3909a-141">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3909a-141">Click Add.</span></span>
    * <span data-ttu-id="3909a-142">Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir.</span><span class="sxs-lookup"><span data-stu-id="3909a-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="3909a-143">Zamanlama altyapısı, kaynakları ayırmak için, her bir etkinliğin kaynak gereksinimlerini, kullanılabilecek operasyon kaynaklarının yetenekleriyle eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="3909a-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="3909a-144">Yetenekler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="3909a-145">Düzey alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="3909a-146">Kaynağın yeteneğini sergilemede kullanacağı yeterlilik düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="3909a-147">Öncelik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3909a-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="3909a-148">Yeteneğe göre operasyon kaynağı önceliğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="3909a-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="3909a-149">Önceliğe göre planlama yaparken, ilk olarak en yüksek önceliği (en düşük sayısal değerle temsil edilir) olan operasyon kaynağı seçilir.</span><span class="sxs-lookup"><span data-stu-id="3909a-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="3909a-150">Kaynak grubuna kaynak atayın</span><span class="sxs-lookup"><span data-stu-id="3909a-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="3909a-151">Kaynak grupları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3909a-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="3909a-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3909a-152">Click Add.</span></span>
    * <span data-ttu-id="3909a-153">Kaynak grubu, operasyon kaynaklarının tesis, üretim birimi ve ambar koşullarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="3909a-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="3909a-154">Kaynak grubu planlaması ancak bir kaynak grubuna atandığı zaman yapılabilir ve yalnızca kaynak grubunun bulunduğu tesiste olabilir.</span><span class="sxs-lookup"><span data-stu-id="3909a-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="3909a-155">Kaynak grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="3909a-156">Giriş konumu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3909a-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="3909a-157">Operasyon kaynağının malzemeleri alacağı ambar konumu belirtin.</span><span class="sxs-lookup"><span data-stu-id="3909a-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

