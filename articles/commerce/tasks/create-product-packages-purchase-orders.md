---
title: " Satınalma siparişleri için ürün paketleri oluşturma"
description: Bu yordam, bir ürün paketi oluşturma ve bunu bir satınalma siparişinde kullanmayla ilgili süreci açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964682"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="aadc1-103"> Satınalma siparişleri için ürün paketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="aadc1-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aadc1-104">Bu yordam, bir ürün paketi oluşturma ve bunu bir satınalma siparişinde kullanmayla ilgili süreci açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="aadc1-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="aadc1-105">Satınalma siparişi, önceden tanımlanmış bir ürün kümesi için sipariş oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aadc1-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="aadc1-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="aadc1-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="aadc1-107">Ürün paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="aadc1-107">Create a product package</span></span>
1. <span data-ttu-id="aadc1-108">Retail and Commerce > Stok yönetimi > Stok yenileme > Ürün paketleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="aadc1-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-109">Click New.</span></span>
3. <span data-ttu-id="aadc1-110">Paket numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="aadc1-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="aadc1-112">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="aadc1-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="aadc1-114">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-114">Click Add.</span></span>
8. <span data-ttu-id="aadc1-115">Madde numarası alanına '0160' yazın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="aadc1-116">Boyut alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="aadc1-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="aadc1-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="aadc1-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-119">Click Add.</span></span>
13. <span data-ttu-id="aadc1-120">Madde numarası alanına '0160' yazın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="aadc1-121">Varyant numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="aadc1-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="aadc1-123">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="aadc1-124">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-124">Click Add.</span></span>
18. <span data-ttu-id="aadc1-125">Madde numarası alanına '0175' yazın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="aadc1-126">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="aadc1-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-127">Click Save.</span></span>
21. <span data-ttu-id="aadc1-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="aadc1-129">Paketi satınalma siparişine ekleme</span><span class="sxs-lookup"><span data-stu-id="aadc1-129">Add package to purchase order</span></span>
1. <span data-ttu-id="aadc1-130">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="aadc1-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-131">Click New.</span></span>
3. <span data-ttu-id="aadc1-132">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aadc1-133">Ürün paketi oluşturulurken bir satıcı seçildiyse, listeden aynı satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="aadc1-134">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="aadc1-135">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aadc1-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="aadc1-137">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="aadc1-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="aadc1-139">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-139">Click OK.</span></span>
11. <span data-ttu-id="aadc1-140">Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="aadc1-141">Ürün paketleri sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="aadc1-142">Satınalma siparişi satırına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="aadc1-143">Paketten satırlar oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="aadc1-144">Listede, önceki adımda oluşturduğunuz ürün paketi bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="aadc1-145">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aadc1-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="aadc1-146">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-146">Click Create.</span></span>
18. <span data-ttu-id="aadc1-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadc1-147">Click Save.</span></span>

