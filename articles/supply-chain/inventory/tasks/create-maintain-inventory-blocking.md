---
title: Stok durdurma oluştur ve sürdür
description: Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 845d517ad10245df3b208874df61e235c199c7fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836420"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="8277f-103">Stok durdurma oluştur ve sürdür</span><span class="sxs-lookup"><span data-stu-id="8277f-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8277f-104">Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="8277f-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="8277f-105">Yordamı demo veri şirketi USMF kullanarak, gösterilen örnek değerlerle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8277f-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="8277f-106">Bu yordama başlamadan önce eldeki fiziksel stoka sahip bir öğe olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8277f-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="8277f-107">Stok durdurma oluşturun</span><span class="sxs-lookup"><span data-stu-id="8277f-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="8277f-108">Stok yönetimi > Periyodik görevler > Stok durdurma öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="8277f-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="8277f-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8277f-109">Click New.</span></span>
3. <span data-ttu-id="8277f-110">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="8277f-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8277f-111">Listede kullanmak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="8277f-111">In the list, select the item you want to choose.</span></span> 
    * <span data-ttu-id="8277f-112">Bir madde numarası ile engellemek istediğiniz eldeki fiziksel stoku seçin.</span><span class="sxs-lookup"><span data-stu-id="8277f-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="8277f-113">USMF kullanıyorsanız, M9201 öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8277f-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="8277f-114">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8277f-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8277f-115">Madde M9201 kullanıyorsanız, 200'den az seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8277f-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="8277f-116">Stok bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8277f-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="8277f-117">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="8277f-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8277f-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8277f-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8277f-119">Madde M9201 kullanıyorsanız, ambar 51'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8277f-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="8277f-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8277f-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="8277f-121">Stok durdurma koşullarını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="8277f-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="8277f-122">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8277f-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8277f-123">Stok Miktar alanını, engelleyecek miktarı yansıtacak şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8277f-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="8277f-124">Beklenen tarih alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8277f-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="8277f-125">Engellenen stokun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için, tarih atamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8277f-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="8277f-126">Stok durdurma için Beklenen girişler seçeneği, bir durdurmayı el ile oluşturduğunuzda varsayılan olduğu şekilde, işaretliyse, bu tarih beklenen hareket üzerinde belirir.</span><span class="sxs-lookup"><span data-stu-id="8277f-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="8277f-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8277f-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="8277f-128">Stok durdurmayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="8277f-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="8277f-129">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8277f-129">Click Delete.</span></span>
2. <span data-ttu-id="8277f-130">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8277f-130">Click Yes.</span></span>
3. <span data-ttu-id="8277f-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8277f-131">Close the page.</span></span>

