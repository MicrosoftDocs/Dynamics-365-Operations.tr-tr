--- 
title: " Satınalma siparişleri için ürün paketleri oluşturma"
description: "Bu yordam, bir ürün paketi oluşturma ve bunu bir satınalma siparişinde kullanmayla ilgili süreci açıklamaktadır."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="89fb6-103"> Satınalma siparişleri için ürün paketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="89fb6-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="89fb6-104">Bu yordam, bir ürün paketi oluşturma ve bunu bir satınalma siparişinde kullanmayla ilgili süreci açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="89fb6-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="89fb6-105">Satınalma siparişi, önceden tanımlanmış bir ürün kümesi için sipariş oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="89fb6-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="89fb6-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="89fb6-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="89fb6-107">Ürün paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="89fb6-107">Create a product package</span></span>
1. <span data-ttu-id="89fb6-108">Retail and commerce > Inventory management > Replenishment > Product packages (Perakende ve ticaret > Stok yönetimi > Stok yenileme > Ürün paketleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="89fb6-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-109">Click New.</span></span>
3. <span data-ttu-id="89fb6-110">Paket numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="89fb6-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="89fb6-112">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="89fb6-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="89fb6-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-114">Click Add.</span></span>
8. <span data-ttu-id="89fb6-115">Madde numarası alanına '0160' yazın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="89fb6-116">Boyut alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="89fb6-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="89fb6-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="89fb6-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-119">Click Add.</span></span>
13. <span data-ttu-id="89fb6-120">Madde numarası alanına '0160' yazın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="89fb6-121">Varyant numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="89fb6-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="89fb6-123">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="89fb6-124">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-124">Click Add.</span></span>
18. <span data-ttu-id="89fb6-125">Madde numarası alanına '0175' yazın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="89fb6-126">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="89fb6-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-127">Click Save.</span></span>
21. <span data-ttu-id="89fb6-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="89fb6-129">Paketi satınalma siparişine ekleme</span><span class="sxs-lookup"><span data-stu-id="89fb6-129">Add package to puchase order</span></span>
1. <span data-ttu-id="89fb6-130">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="89fb6-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-131">Click New.</span></span>
3. <span data-ttu-id="89fb6-132">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="89fb6-133">Ürün paketi oluşturulurken bir satıcı seçildiyse, listeden aynı satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="89fb6-134">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="89fb6-135">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="89fb6-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="89fb6-137">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="89fb6-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="89fb6-139">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-139">Click OK.</span></span>
11. <span data-ttu-id="89fb6-140">Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="89fb6-141">Ürün paketleri sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="89fb6-142">Satınalma siparişi satırına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="89fb6-143">Paketten satırlar oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="89fb6-144">Listede, önceki adımda oluşturduğunuz ürün paketi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="89fb6-145">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="89fb6-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="89fb6-146">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-146">Click Create.</span></span>
18. <span data-ttu-id="89fb6-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fb6-147">Click Save.</span></span>


