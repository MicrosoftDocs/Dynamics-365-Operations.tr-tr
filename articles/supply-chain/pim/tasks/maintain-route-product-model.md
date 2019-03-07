---
title: Bir ürün modeli için rotayı koruma
description: Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e793466e021671501570aed06959d684d5e9c15
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "317166"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="1d99c-103">Bir ürün modeli için rotayı koruma</span><span class="sxs-lookup"><span data-stu-id="1d99c-103">Maintain route for a product model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d99c-104">Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1d99c-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="1d99c-105">Bu yordam, işlem sırasında yol göstermek için USMF demo şirketindeki son teknoloji hoparlör modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1d99c-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="1d99c-106">Rota operasyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="1d99c-106">Add a route operation</span></span>
1. <span data-ttu-id="1d99c-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="1d99c-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="1d99c-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1d99c-110">Bu alıştırma için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="1d99c-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1d99c-112">Rota operasyonları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="1d99c-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-113">Click Add.</span></span>
7. <span data-ttu-id="1d99c-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="1d99c-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="1d99c-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="1d99c-117">Rota operasyonu ayrıntılarını girme</span><span class="sxs-lookup"><span data-stu-id="1d99c-117">Enter route operation details</span></span>
1. <span data-ttu-id="1d99c-118">Rota operasyonu ayrıntıları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-118">Click Route operation details.</span></span>
2. <span data-ttu-id="1d99c-119">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="1d99c-120">Oper.</span><span class="sxs-lookup"><span data-stu-id="1d99c-120">In the Oper.</span></span> <span data-ttu-id="1d99c-121">Hayır.</span><span class="sxs-lookup"><span data-stu-id="1d99c-121">No.</span></span> <span data-ttu-id="1d99c-122">bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-122">field, enter a number.</span></span>
    * <span data-ttu-id="1d99c-123">Operasyon numarası rota sırasını belirler.</span><span class="sxs-lookup"><span data-stu-id="1d99c-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="1d99c-124">Rota operasyonundaki her bir özellik statik bir değer alabilir veya bir öznitelik ile eşleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1d99c-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="1d99c-125">Bir öznitelik ile eşleme yapılması yapılandırmanın parçası olarak bir değer ayarlanmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="1d99c-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="1d99c-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="1d99c-127">Rota grubu; maliyetlendirme, tüketim ve ayarlar için temel davranışı belirler.</span><span class="sxs-lookup"><span data-stu-id="1d99c-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="1d99c-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="1d99c-129">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-129">Click the Times tab.</span></span>
7. <span data-ttu-id="1d99c-130">İşlem miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="1d99c-131">Tek işlem sırasında işlenecek sayıyı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="1d99c-132">Saatler/zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="1d99c-133">Zaman oranını girin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="1d99c-134">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-134">Select the Set check box.</span></span>
10. <span data-ttu-id="1d99c-135">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="1d99c-136">Belirttiğiniz miktarın işlenme süresini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="1d99c-137">Kaynak gereksinimleri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="1d99c-138">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-138">Click Add.</span></span>
13. <span data-ttu-id="1d99c-139">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="1d99c-140">Gereksinim türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="1d99c-141">Sahip olmaları gereken belirli kaynakları veya özellikleri belirtmek isteyip istemediğinize karar verin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="1d99c-142">Gerkesinim alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1d99c-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="1d99c-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1d99c-143">Click OK.</span></span>

