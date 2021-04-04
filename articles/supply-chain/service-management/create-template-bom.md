---
title: Şablon ürün reçetesi oluşturma
description: Çeşitli yöntemler kullanarak şablon ürün reçetesi oluşturabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470797"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="14fff-103">Şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="14fff-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="14fff-104">Aşağıdaki yöntemlerden herhangi birini kullanarak şablon ürün reçetesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14fff-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="14fff-105">Tüm yöntemlerde **Başlangıç tarihi** ve **Bitiş tarihi** alanları isteğe bağlıdır ve yalnızca bilgi verici niteliktedir.</span><span class="sxs-lookup"><span data-stu-id="14fff-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="14fff-106">El ile şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="14fff-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="14fff-107">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="14fff-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="14fff-108">**Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="14fff-109">**Ürün reçetesini satırlarını referanstan kopyala** altından **el ile** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="14fff-110">**Madde numarası** alanına **BOM** türünde bir madde girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="14fff-111">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="14fff-112">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="14fff-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-113">Select **OK**.</span></span>

<span data-ttu-id="14fff-114">Yeni, boş bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="14fff-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="14fff-115">Başka bir şablon ürün reçetesini temel alarak şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="14fff-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="14fff-116">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="14fff-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="14fff-117">**Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="14fff-118">**Ürün reçetesini satırlarını referanstan kopyala** altından **Şablon ürün reçetesi** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="14fff-119">**Referans numarası** alanında, yeni şablon ürün reçetenize kopyalanacak mevcut şablon ürün reçetesini seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="14fff-120">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="14fff-121">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="14fff-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-122">Select **OK**.</span></span>

<span data-ttu-id="14fff-123">Orijinal şablon ürün reçetesindeki satırlara karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="14fff-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="14fff-124">Bir madde ürün reçetesini temel alarak şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="14fff-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="14fff-125">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="14fff-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="14fff-126">**Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="14fff-127">**Ürün reçetesi satırlarını referanstan kopyala** altından **Ürün reçetesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="14fff-128">**Referans numarası** alanında, bir ürün reçetesi versiyonu seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="14fff-129">**Madde numarası**'na ürün reçetesi türünde bir madde kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="14fff-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="14fff-130">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="14fff-131">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="14fff-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-132">Select **OK**.</span></span>

<span data-ttu-id="14fff-133">**Üürn reçeteleri** içinde listelenen ürün reçetesinin satırlarına karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="14fff-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="14fff-134">Bir üretim ürün reçetesi temel alınarak şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="14fff-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="14fff-135">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="14fff-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="14fff-136">**Şablon ürün reçetesi oluştur** formunu açmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="14fff-137">**Ürün reçetesi satırlarını referanstan kopyala** altından **Üretim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="14fff-138">**Referans numarası** alanında, bir üretim ürün reçetesi seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="14fff-139">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="14fff-140">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="14fff-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="14fff-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="14fff-141">Select **OK**.</span></span>

<span data-ttu-id="14fff-142">**Ürün reçetesi** içinde listelenen ürün reçetesinin satırlarına karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="14fff-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="14fff-143">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="14fff-143">See also</span></span>

[<span data-ttu-id="14fff-144">Şablon ürün reçeteleri</span><span class="sxs-lookup"><span data-stu-id="14fff-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]