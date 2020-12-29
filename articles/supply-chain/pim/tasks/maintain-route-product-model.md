---
title: Bir ürün modeli için rotayı koruma
description: Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc41f99085e5f30ae29edce296a5e3752cbabd33
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439155"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="55fae-103">Bir ürün modeli için rotayı koruma</span><span class="sxs-lookup"><span data-stu-id="55fae-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55fae-104">Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="55fae-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="55fae-105">Bu yordam, işlem sırasında yol göstermek için USMF demo şirketindeki son teknoloji hoparlör modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="55fae-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="55fae-106">Rota operasyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="55fae-106">Add a route operation</span></span>
1. <span data-ttu-id="55fae-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55fae-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="55fae-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55fae-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="55fae-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="55fae-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="55fae-110">Bu alıştırma için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="55fae-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="55fae-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55fae-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="55fae-112">Rota operasyonları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="55fae-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="55fae-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="55fae-113">Click Add.</span></span>
7. <span data-ttu-id="55fae-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="55fae-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="55fae-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="55fae-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="55fae-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55fae-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="55fae-117">Rota operasyonu ayrıntılarını girme</span><span class="sxs-lookup"><span data-stu-id="55fae-117">Enter route operation details</span></span>
1. <span data-ttu-id="55fae-118">Rota operasyonu ayrıntıları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="55fae-118">Click Route operation details.</span></span>
2. <span data-ttu-id="55fae-119">Operasyon alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55fae-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="55fae-120">Oper.</span><span class="sxs-lookup"><span data-stu-id="55fae-120">In the Oper.</span></span> <span data-ttu-id="55fae-121">Hayır.</span><span class="sxs-lookup"><span data-stu-id="55fae-121">No.</span></span> <span data-ttu-id="55fae-122">bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55fae-122">field, enter a number.</span></span>
    * <span data-ttu-id="55fae-123">Operasyon numarası rota sırasını belirler.</span><span class="sxs-lookup"><span data-stu-id="55fae-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="55fae-124">Rota operasyonundaki her bir özellik statik bir değer alabilir veya bir öznitelik ile eşleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="55fae-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="55fae-125">Bir öznitelik ile eşleme yapılması yapılandırmanın parçası olarak bir değer ayarlanmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="55fae-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="55fae-126">Rota grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55fae-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="55fae-127">Rota grubu; maliyetlendirme, tüketim ve ayarlar için temel davranışı belirler.</span><span class="sxs-lookup"><span data-stu-id="55fae-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="55fae-128">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55fae-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="55fae-129">Zaman sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="55fae-129">Click the Times tab.</span></span>
7. <span data-ttu-id="55fae-130">İşlem miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55fae-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="55fae-131">Tek işlem sırasında işlenecek sayıyı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="55fae-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="55fae-132">Saatler/zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55fae-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="55fae-133">Zaman oranını girin.</span><span class="sxs-lookup"><span data-stu-id="55fae-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="55fae-134">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="55fae-134">Select the Set check box.</span></span>
10. <span data-ttu-id="55fae-135">Çalışma süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="55fae-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="55fae-136">Belirttiğiniz miktarın işlenme süresini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="55fae-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="55fae-137">Kaynak gereksinimleri sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="55fae-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="55fae-138">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="55fae-138">Click Add.</span></span>
13. <span data-ttu-id="55fae-139">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="55fae-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="55fae-140">Gereksinim türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="55fae-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="55fae-141">Sahip olmaları gereken belirli kaynakları veya özellikleri belirtmek isteyip istemediğinize karar verin.</span><span class="sxs-lookup"><span data-stu-id="55fae-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="55fae-142">Gerkesinim alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="55fae-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="55fae-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="55fae-143">Click OK.</span></span>

