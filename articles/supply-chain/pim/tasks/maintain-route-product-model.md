---
title: Bir ürün modeli için rotayı koruma
description: Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921277"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="275fe-103">Bir ürün modeli için rotayı koruma</span><span class="sxs-lookup"><span data-stu-id="275fe-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="275fe-104">Bu yordamın çalıştırılması için bir ürün yapılandırma modeli bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="275fe-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="275fe-105">Bu yordam, işlem sırasında yol göstermek için USMF demo şirketindeki son teknoloji hoparlör modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="275fe-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="275fe-106">Rota operasyonu ekleme</span><span class="sxs-lookup"><span data-stu-id="275fe-106">Add a route operation</span></span>

1. <span data-ttu-id="275fe-107">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="275fe-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="275fe-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="275fe-109">Bu alıştırma için son teknoloji hoparlör modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="275fe-110">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="275fe-111">**Rota operasyonları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="275fe-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="275fe-112">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-112">Select **Add**.</span></span>
1. <span data-ttu-id="275fe-113">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="275fe-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="275fe-114">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="275fe-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="275fe-115">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="275fe-116">Rota operasyonu ayrıntılarını girme</span><span class="sxs-lookup"><span data-stu-id="275fe-116">Enter route operation details</span></span>

1. <span data-ttu-id="275fe-117">**Rota operasyon ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="275fe-118">**Operasyon** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="275fe-119">**Operasyon Numarası** içerisinde</span><span class="sxs-lookup"><span data-stu-id="275fe-119">In the **Oper. No.**</span></span> <span data-ttu-id="275fe-120">bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="275fe-120">field, enter a number.</span></span>
    * <span data-ttu-id="275fe-121">Operasyon numarası rota sırasını belirler.</span><span class="sxs-lookup"><span data-stu-id="275fe-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="275fe-122">Rota operasyonundaki her bir özellik statik bir değer alabilir veya bir öznitelik ile eşleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="275fe-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="275fe-123">Bir öznitelik ile eşleme yapılması yapılandırmanın parçası olarak bir değer ayarlanmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="275fe-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="275fe-124">**Rota grubu** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="275fe-125">Rota grubu; maliyetlendirme, tüketim ve ayarlar için temel davranışı belirler.</span><span class="sxs-lookup"><span data-stu-id="275fe-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="275fe-126">**Kurulum** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="275fe-127">**Zamanlar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="275fe-128">**İşlem miktarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="275fe-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="275fe-129">Tek işlem sırasında işlenecek sayıyı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="275fe-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="275fe-130">**Saatler/zaman** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="275fe-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="275fe-131">Zaman oranını girin.</span><span class="sxs-lookup"><span data-stu-id="275fe-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="275fe-132">**Ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="275fe-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="275fe-133">**Çalışma süresi** alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="275fe-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="275fe-134">Belirttiğiniz miktarın işlenme süresini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="275fe-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="275fe-135">**Kaynak gereksinimleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="275fe-136">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-136">Select **Add**.</span></span>
1. <span data-ttu-id="275fe-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="275fe-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="275fe-138">**Gereksinim türü** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="275fe-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="275fe-139">Sahip olmaları gereken belirli kaynakları veya özellikleri belirtmek isteyip istemediğinize karar verin.</span><span class="sxs-lookup"><span data-stu-id="275fe-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="275fe-140">**Gerkesinim** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="275fe-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="275fe-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]