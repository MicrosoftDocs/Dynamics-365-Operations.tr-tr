---
title: Ürün yapılandırma modeli için ürün reçetesini koruma
description: Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921329"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="138fc-103">Ürün yapılandırma modeli için ürün reçetesini koruma</span><span class="sxs-lookup"><span data-stu-id="138fc-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="138fc-104">Bu yordamın çalıştırılması için mevcut bir ürün yapılandırma modeli olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="138fc-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="138fc-105">Bu yordamı oluşturmak için USMF demo şirketindeki son teknoloji hoparlör modeli kullanılır.</span><span class="sxs-lookup"><span data-stu-id="138fc-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="138fc-106">Bir ürün reçetesi satırı ekleme</span><span class="sxs-lookup"><span data-stu-id="138fc-106">Add a BOM line</span></span>

1. <span data-ttu-id="138fc-107">**Ürün bilgileri yönetimi \> Ürünler \> Ürün yapılandırma modelleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="138fc-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="138fc-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="138fc-109">Bu yordam için son teknoloji hoparlörü seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="138fc-110">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="138fc-111">**Ürün reçetesi satırları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="138fc-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="138fc-112">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-112">Select **Add**.</span></span>
1. <span data-ttu-id="138fc-113">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="138fc-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="138fc-114">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="138fc-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="138fc-115">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="138fc-116">Ürün reçetesi satırı ayrıntılarını ekleme</span><span class="sxs-lookup"><span data-stu-id="138fc-116">Add BOM line details</span></span>

1. <span data-ttu-id="138fc-117">**Ürün reçetesi satırı ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="138fc-118">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="138fc-119">Örneğin, ürün M0055'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="138fc-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="138fc-120">Her ürün reçetesi satırı özelliği için sabit bir değer mi alacağını yoksa bir özniteliğe mi eşleneceğini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="138fc-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="138fc-121">**Ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="138fc-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="138fc-122">**Hesaplama** alanında *Evet*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="138fc-123">**Hesaplama** özelliğini *Evet* olarak ayarladığınızda, ürün reçetesi satırının maliyet hesaplamalarına dahil edildiğinden emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="138fc-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="138fc-124">**Kurulum** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="138fc-125">**Ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="138fc-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="138fc-126">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="138fc-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="138fc-127">Miktar alanı, ürünün ne kadarının ürün reçetesine dahil edileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="138fc-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="138fc-128">Bu, özellik eşleme için kullanılabilecek kesin bir seçenek olabilir.</span><span class="sxs-lookup"><span data-stu-id="138fc-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="138fc-129">**Boyut** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="138fc-130">Ürün boyutlarından herhangi birinin etkin olup olmadığını ve ardından bir değerin eklenmiş veya özniteliğin atanmış olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="138fc-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="138fc-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="138fc-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]