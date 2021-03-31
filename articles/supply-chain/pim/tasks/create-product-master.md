---
title: Ana ürün oluşturma
description: Önceden tanımlanmış çeşitler için ana ürün oluşturun.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218501"
---
# <a name="create-a-product-master"></a><span data-ttu-id="47364-103">Ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="47364-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47364-104">Önceden tanımlanmış çeşitler için ana ürün oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47364-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="47364-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="47364-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="47364-106">Bu yordam, ürün tasarımcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="47364-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="47364-107">Yeni bir ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="47364-107">Create a new product master</span></span>
1. <span data-ttu-id="47364-108">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Ana ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="47364-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="47364-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-109">Click **New**.</span></span>
3. <span data-ttu-id="47364-110">**Ürün numarası** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="47364-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="47364-111">Numaranın benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="47364-111">The number must be unique.</span></span> <span data-ttu-id="47364-112">**Ürün numarası** alanı için bir numara serisi ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="47364-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="47364-113">Bu durumda, kullanıcı bir değer girmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="47364-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="47364-114">**Ürün adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="47364-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="47364-115">Açıklayıcı bir ürün adı girin.</span><span class="sxs-lookup"><span data-stu-id="47364-115">Enter a descriptive product name.</span></span> <span data-ttu-id="47364-116">Değer için arama adı varsayılan olarak, ancak bu kullanıcı tarafından değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="47364-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="47364-117">**Ürün boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="47364-118">Ürün boyut grubu, ürün çeşitleri oluşturmak için 4 ürün boyutundan hangisinin kullanılabileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="47364-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="47364-119">Bu örnek, renk ve boyut boyutları olan bir grup kullanır.</span><span class="sxs-lookup"><span data-stu-id="47364-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="47364-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47364-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="47364-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="47364-122">Varsayılan **Yapılandırma teknolojisi** 'Önceden tanımlanmış çeşit'tir.</span><span class="sxs-lookup"><span data-stu-id="47364-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="47364-123">Bu örnek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="47364-123">This will be used for this example.</span></span>
8. <span data-ttu-id="47364-124">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="47364-125">Ürün boyut gruplarını seçin</span><span class="sxs-lookup"><span data-stu-id="47364-125">Select product dimension groups</span></span>
1. <span data-ttu-id="47364-126">**Renk grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="47364-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47364-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="47364-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="47364-129">**Ebat grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="47364-130">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47364-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="47364-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="47364-132">Boyut grupları ekleme</span><span class="sxs-lookup"><span data-stu-id="47364-132">Add dimension groups</span></span>
1. <span data-ttu-id="47364-133">**Eylem Bölmesi**'nde, **Ürün**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="47364-134">İletişim kutusunu açmak için **Boyut grupları**'ına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="47364-135">**Depolama boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="47364-136">Depolama stok boyutları maddelerin nasıl depolandığını ve stoktan alındığını kontrol etmenize yardım eder.</span><span class="sxs-lookup"><span data-stu-id="47364-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="47364-137">Örneğin, bir depolama boyutuna tesis ve ambar dahil olabilir.</span><span class="sxs-lookup"><span data-stu-id="47364-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="47364-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47364-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="47364-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="47364-140">**İzleme boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="47364-141">İzleme boyutu grubu hangi izleme boyutlarını bir ürüne atayabileceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="47364-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="47364-142">Örneğin, toplu iş numarası ve seri numarası, stok maddelerini izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="47364-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="47364-143">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="47364-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="47364-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="47364-145">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-145">Click **OK**.</span></span>
10. <span data-ttu-id="47364-146">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="47364-146">Click **Save**.</span></span>
11. <span data-ttu-id="47364-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="47364-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]