---
title: Ürün yapılandırma modeli için ürün reçetesini koruma
description: Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f663c28dfcbf6b365e3e88d3a4f6385ce2fcca9f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844405"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="c0533-103">Ürün yapılandırma modeli için ürün reçetesini koruma</span><span class="sxs-lookup"><span data-stu-id="c0533-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0533-104">Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c0533-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="c0533-105">Bu yordamı oluşturmak için USMF demo şirketindeki son teknoloji hoparlör modeli kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c0533-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="c0533-106">Bir ürün reçetesi satırı ekleme</span><span class="sxs-lookup"><span data-stu-id="c0533-106">Add a BOM line</span></span>
1. <span data-ttu-id="c0533-107">Ürün varyantı model tanımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="c0533-108">Ürün yapılandırma modelleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="c0533-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c0533-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c0533-110">Bu yordam için son teknoloji hoparlörü seçin.</span><span class="sxs-lookup"><span data-stu-id="c0533-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="c0533-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c0533-112">Ürün reçetesi satırları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c0533-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="c0533-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c0533-113">Click Add.</span></span>
7. <span data-ttu-id="c0533-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c0533-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c0533-115">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c0533-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="c0533-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="c0533-117">Ürün reçetesi satırı ayrıntılarını ekleme</span><span class="sxs-lookup"><span data-stu-id="c0533-117">Add BOM line details</span></span>
1. <span data-ttu-id="c0533-118">Ürün reçetesi satır ayrıntılarını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c0533-118">Click BOM line details.</span></span>
2. <span data-ttu-id="c0533-119">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c0533-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c0533-120">Örneğin, ürün M0055'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0533-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="c0533-121">Her ürün reçetesi satırı özelliği için sabit bir değer mi alacağını yoksa bir özniteliğe mi eşleneceğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0533-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="c0533-122">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c0533-122">Select the Set check box.</span></span>
4. <span data-ttu-id="c0533-123">Hesaplama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c0533-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="c0533-124">Hesaplama özelliğini Evet olarak ayarladığınızda, ürün reçetesi satırının maliyet hesaplamalarına dahil edildiğinden emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="c0533-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="c0533-125">Kurulum sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="c0533-126">Ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c0533-126">Select the Set check box.</span></span>
7. <span data-ttu-id="c0533-127">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c0533-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c0533-128">Miktar alanı, ürünün ne kadarının ürün reçetesine dahil edileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="c0533-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="c0533-129">Bu, özellik eşleme için kullanılabilecek kesin bir seçenek olabilir.</span><span class="sxs-lookup"><span data-stu-id="c0533-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="c0533-130">Boyut sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c0533-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="c0533-131">Ürün boyutlarından herhangi birinin etkin olup olmadığını ve ardından bir değerin eklenmiş veya özniteliğin atanmış olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="c0533-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0533-132">Click OK.</span></span>

