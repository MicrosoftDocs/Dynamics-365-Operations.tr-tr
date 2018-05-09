--- 
title: "Ana ürün oluşturma"
description: "Önceden tanımlanmış çeşitler için ana ürün oluşturun."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fa2ea0f36f059b582b5e8658ffacde527425fcba
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-product-master"></a><span data-ttu-id="9a32a-103">Ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a32a-103">Create a product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a32a-104">Önceden tanımlanmış çeşitler için ana ürün oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9a32a-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="9a32a-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9a32a-106">Bu yordam, ürün tasarımcılarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="9a32a-107">Yeni bir ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a32a-107">Create a new product master</span></span>
1. <span data-ttu-id="9a32a-108">Ürün bilgi yönetimi > Ürünler > Ana ürünler'e git.</span><span class="sxs-lookup"><span data-stu-id="9a32a-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="9a32a-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-109">Click New.</span></span>
3. <span data-ttu-id="9a32a-110">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="9a32a-111">Numaranın benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-111">The number must be unique.</span></span> <span data-ttu-id="9a32a-112">Ürün numarası alanı için bir numara serisi girilebilir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="9a32a-113">Bu durumda, kullanıcı bir değer girmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="9a32a-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="9a32a-114">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="9a32a-115">Açıklayıcı bir ürün adı girin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-115">Enter a descriptive product name.</span></span> <span data-ttu-id="9a32a-116">Değer için arama adı varsayılan olarak, ancak bu kullanıcı tarafından değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="9a32a-117">Ürün boyutu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9a32a-118">Ürün boyut grubu, ürün çeşitleri oluşturmak için 4 ürün boyutundan hangisinin kullanılabileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="9a32a-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="9a32a-119">Bu örnek, renk ve boyut boyutları olan bir grup kullanır.</span><span class="sxs-lookup"><span data-stu-id="9a32a-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="9a32a-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9a32a-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9a32a-122">Varsayılan yapılandırma teknolojisi Önceden tanımlanmış çeşididir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="9a32a-123">Bu örnek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="9a32a-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="9a32a-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="9a32a-125">Ürün boyut gruplarını seçin</span><span class="sxs-lookup"><span data-stu-id="9a32a-125">Select product dimension groups</span></span>
1. <span data-ttu-id="9a32a-126">Renk grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="9a32a-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9a32a-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9a32a-129">Ebat grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9a32a-130">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9a32a-131">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="9a32a-132">Boyut grupları ekleme</span><span class="sxs-lookup"><span data-stu-id="9a32a-132">Add dimension groups</span></span>
1. <span data-ttu-id="9a32a-133">Eylem Bölmesinde, Ürün'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="9a32a-134">İletişim kutusunu açmak için Boyut grupları'ına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="9a32a-135">Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9a32a-136">Depolama stok boyutları maddelerin nasıl depolandığını ve stoktan alındığını kontrol etmenize yardım eder.</span><span class="sxs-lookup"><span data-stu-id="9a32a-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="9a32a-137">Örneğin, bir depolama boyutuna tesis ve ambar dahil olabilir.</span><span class="sxs-lookup"><span data-stu-id="9a32a-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="9a32a-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9a32a-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9a32a-140">İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9a32a-141">İzleme boyutu grubu hangi izleme boyutlarını bir ürüne atayabileceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="9a32a-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="9a32a-142">Örneğin, toplu iş numarası ve seri numarası, stok maddelerini izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9a32a-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="9a32a-143">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9a32a-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9a32a-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9a32a-145">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-145">Click OK.</span></span>
10. <span data-ttu-id="9a32a-146">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-146">Click Save.</span></span>
11. <span data-ttu-id="9a32a-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9a32a-147">Close the page.</span></span>


