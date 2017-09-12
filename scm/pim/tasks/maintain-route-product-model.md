--- 
title: "Ürün modeli için rotayı koruma"
description: "Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="74883-103">Ürün modeli için rotayı koruma</span><span class="sxs-lookup"><span data-stu-id="74883-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74883-104">Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="74883-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="74883-105">Bu yordam, işlem sırasında yol göstermek için USMF demo şirketindeki son teknoloji hoparlör modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="74883-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="74883-106">Rota operasyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="74883-106">Add a route operation</span></span>
1. <span data-ttu-id="74883-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74883-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="74883-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74883-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="74883-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="74883-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="74883-110">Bu alıştırma için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="74883-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="74883-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74883-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="74883-112">Rota operasyonları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="74883-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="74883-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="74883-113">Click Add.</span></span>
7. <span data-ttu-id="74883-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="74883-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="74883-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="74883-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="74883-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74883-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="74883-117">Rota operasyonu ayrıntılarını girme</span><span class="sxs-lookup"><span data-stu-id="74883-117">Enter route operation details</span></span>
1. <span data-ttu-id="74883-118">Rota operasyonu ayrıntıları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="74883-118">Click Route operation details.</span></span>
2. <span data-ttu-id="74883-119">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="74883-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="74883-120">Oper.</span><span class="sxs-lookup"><span data-stu-id="74883-120">In the Oper.</span></span> <span data-ttu-id="74883-121">Hayır.</span><span class="sxs-lookup"><span data-stu-id="74883-121">No.</span></span> <span data-ttu-id="74883-122">bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="74883-122">field, enter a number.</span></span>
    * <span data-ttu-id="74883-123">Operasyon numarası rota sırasını belirler.</span><span class="sxs-lookup"><span data-stu-id="74883-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="74883-124">Rota operasyonundaki her bir özellik statik bir değer alabilir veya bir öznitelik ile eşleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="74883-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="74883-125">Bir öznitelik ile eşleme yapılması yapılandırmanın parçası olarak bir değer ayarlanmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="74883-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="74883-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="74883-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="74883-127">Rota grubu; maliyetlendirme, tüketim ve ayarlar için temel davranışı belirler.</span><span class="sxs-lookup"><span data-stu-id="74883-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="74883-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74883-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="74883-129">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="74883-129">Click the Times tab.</span></span>
7. <span data-ttu-id="74883-130">İşlem miktarında.</span><span class="sxs-lookup"><span data-stu-id="74883-130">In the Process qty.</span></span> <span data-ttu-id="74883-131">bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="74883-131">field, enter a number.</span></span>
    * <span data-ttu-id="74883-132">Tek işlem sırasında işlenecek sayıyı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="74883-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="74883-133">Saatler/zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="74883-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="74883-134">Zaman oranını girin.</span><span class="sxs-lookup"><span data-stu-id="74883-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="74883-135">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="74883-135">Select the Set check box.</span></span>
10. <span data-ttu-id="74883-136">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="74883-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="74883-137">Belirttiğiniz miktarın işlenme süresini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="74883-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="74883-138">Kaynak gereksinimleri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="74883-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="74883-139">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="74883-139">Click Add.</span></span>
13. <span data-ttu-id="74883-140">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="74883-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="74883-141">Gereksinim türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="74883-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="74883-142">Sahip olmaları gereken belirli kaynakları veya özellikleri belirtmek isteyip istemediğinize karar verin.</span><span class="sxs-lookup"><span data-stu-id="74883-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="74883-143">Gerkesinim alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="74883-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="74883-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="74883-144">Click OK.</span></span>


