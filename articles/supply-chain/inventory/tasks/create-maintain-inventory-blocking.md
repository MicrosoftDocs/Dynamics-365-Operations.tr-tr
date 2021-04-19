---
title: Stok durdurma oluştur ve sürdür
description: Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.
author: perlynne
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 319ae6da1e0e504316b2d96001d582e835cef20c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834013"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="b9ffc-103">Stok durdurma oluştur ve sürdür</span><span class="sxs-lookup"><span data-stu-id="b9ffc-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b9ffc-104">Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="b9ffc-105">Yordamı demo veri şirketi USMF kullanarak, gösterilen örnek değerlerle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="b9ffc-106">Bu yordama başlamadan önce eldeki fiziksel stoka sahip bir öğe olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="b9ffc-107">Stok durdurma oluşturun</span><span class="sxs-lookup"><span data-stu-id="b9ffc-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="b9ffc-108">**Gezinti panosu**'nda, **Modüller > Stok yönetimi > Periyodik görevler > Stok durdurma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="b9ffc-109">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-109">Click **New**.</span></span>
3. <span data-ttu-id="b9ffc-110">**Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b9ffc-111">Listede kullanmak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="b9ffc-112">Bir madde numarası ile engellemek istediğiniz eldeki fiziksel stoku seçin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="b9ffc-113">USMF kullanıyorsanız, M9201 öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="b9ffc-114">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b9ffc-115">Madde M9201 kullanıyorsanız, 200'den az seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="b9ffc-116">**Stok boyutları** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="b9ffc-117">**Ambar** alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b9ffc-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="b9ffc-119">Madde M9201 kullanıyorsanız, ambar 51'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="b9ffc-120">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="b9ffc-121">Stok durdurma koşullarını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="b9ffc-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="b9ffc-122">**Genel** hızlı sekmesinde, **Miktar** alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b9ffc-123">Stok Miktar alanını, engelleyecek miktarı yansıtacak şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="b9ffc-124">**Beklenen tarih** alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="b9ffc-125">Engellenen stokun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için, tarih atamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="b9ffc-126">Stok durdurma için Beklenen girişler seçeneği, bir durdurmayı el ile oluşturduğunuzda varsayılan olduğu şekilde, işaretliyse, bu tarih beklenen hareket üzerinde belirir.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="b9ffc-127">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="b9ffc-128">Stok durdurmayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="b9ffc-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="b9ffc-129">**Eylem Bölmesi**'nde, **Sil** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="b9ffc-130">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-130">Click **Yes**.</span></span>
3. <span data-ttu-id="b9ffc-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b9ffc-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]