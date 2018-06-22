---
title: "Şablon ürün reçetesi oluşturma"
description: "Çeşitli yöntemler kullanarak şablon ürün reçetesi oluşturabilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="898c1-103">Şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="898c1-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="898c1-104">Aşağıdaki yöntemlerden herhangi birini kullanarak şablon ürün reçetesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="898c1-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="898c1-105">Tüm yöntemlerde **Başlangıç tarihi** ve **Bitiş tarihi** alanları isteğe bağlıdır ve yalnızca bilgi verici niteliktedir.</span><span class="sxs-lookup"><span data-stu-id="898c1-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="898c1-106">El ile şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="898c1-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="898c1-107">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ni tıklayın.</span><span class="sxs-lookup"><span data-stu-id="898c1-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="898c1-108">**Şablon ürün reçetesi oluştur** formunu açmak için CTRL+N tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="898c1-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="898c1-109">**Ürün reçetesini satırlarını referanstan kopyala** altından **el ile** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="898c1-110">**Madde numarası** alanına **BOM** türünde bir madde girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="898c1-111">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="898c1-112">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="898c1-113">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="898c1-113">Click **OK**.</span></span>

<span data-ttu-id="898c1-114">Yeni, boş bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="898c1-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="898c1-115">Başka bir şablon ürün reçetesini temel alarak şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="898c1-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="898c1-116">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ni tıklayın.</span><span class="sxs-lookup"><span data-stu-id="898c1-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="898c1-117">**Şablon ürün reçetesi oluştur** formunu açmak için CTRL+N tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="898c1-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="898c1-118">**Ürün reçetesini satırlarını referanstan kopyala** altından **Şablon ürün reçetesi** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="898c1-119">**Referans numarası** alanında, yeni şablon ürün reçetenize kopyalanacak mevcut şablon ürün reçetesini seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="898c1-120">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="898c1-121">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="898c1-122">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="898c1-122">Click **OK**.</span></span>

<span data-ttu-id="898c1-123">Orijinal şablon ürün reçetesindeki satırlara karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="898c1-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="898c1-124">Bir madde ürün reçetesini temel alarak şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="898c1-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="898c1-125">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ni tıklayın.</span><span class="sxs-lookup"><span data-stu-id="898c1-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="898c1-126">**Şablon ürün reçetesi oluştur** formunu açmak için CTRL+N tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="898c1-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="898c1-127">**Ürün reçetesi satırlarını referanstan kopyala** altından **Ürün reçetesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="898c1-128">**Referans numarası** alanında, bir ürün reçetesi versiyonu seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="898c1-129">**Madde numarası**'na ürün reçetesi türünde bir madde kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="898c1-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="898c1-130">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="898c1-131">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="898c1-132">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="898c1-132">Click **OK**.</span></span>

<span data-ttu-id="898c1-133">**Üürn reçeteleri** içinde listelenen ürün reçetesinin satırlarına karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="898c1-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="898c1-134">Bir üretim ürün reçetesi temel alınarak şablon ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="898c1-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="898c1-135">**Servis yönetimi** \> **Kurulum** \> **Servis nesneleri** \> **Şablon ürün reçeteleri**'ni tıklayın.</span><span class="sxs-lookup"><span data-stu-id="898c1-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="898c1-136">**Şablon ürün reçetesi oluştur** formunu açmak için CTRL+N tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="898c1-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="898c1-137">**Ürün reçetesi satırlarını referanstan kopyala** altından **Üretim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="898c1-138">**Referans numarası** alanında, bir üretim ürün reçetesi seçin.</span><span class="sxs-lookup"><span data-stu-id="898c1-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="898c1-139">**Ad** alanına, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="898c1-140">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarına, şablon ürün reçetesinin etkin olacağı tarih aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="898c1-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="898c1-141">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="898c1-141">Click **OK**.</span></span>

<span data-ttu-id="898c1-142">**Ürün reçetesi** içinde listelenen ürün reçetesinin satırlarına karşılık gelen satırlar kullanılarak yeni bir şablon ürün reçetesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="898c1-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="898c1-143">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="898c1-143">See also</span></span>

[<span data-ttu-id="898c1-144">Şablon ürün reçeteleri</span><span class="sxs-lookup"><span data-stu-id="898c1-144">Template BOMs</span></span>](template-boms.md)

  


