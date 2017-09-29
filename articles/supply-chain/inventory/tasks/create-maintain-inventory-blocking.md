---
title: "Stok durdurma oluşturma ve güncelleştirme"
description: "Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir."
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: tr-tr
ms.lasthandoff: 09/12/2017

---
# <a name="create-and-maintain-inventory-blocking"></a><span data-ttu-id="bebab-103">Stok durdurma oluşturma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="bebab-103">Create and maintain inventory blocking</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bebab-104">Bu yordam, stok durdurma kullanarak eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="bebab-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="bebab-105">Yordamı demo veri şirketi USMF kullanarak, gösterilen örnek değerlerle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bebab-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="bebab-106">Bu yordama başlamadan önce eldeki fiziksel stoka sahip bir öğe olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bebab-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="bebab-107">Stok durdurma oluşturun</span><span class="sxs-lookup"><span data-stu-id="bebab-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="bebab-108">Stok yönetimi > Periyodik görevler > Stok durdurma öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="bebab-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="bebab-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bebab-109">Click New.</span></span>
3. <span data-ttu-id="bebab-110">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bebab-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bebab-111">Listede kullanmak istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="bebab-111">In the list, select the item you want to choose.</span></span>
    * <span data-ttu-id="bebab-112">Bir madde numarası ile engellemek istediğiniz eldeki fiziksel stoku seçin.</span><span class="sxs-lookup"><span data-stu-id="bebab-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="bebab-113">USMF kullanıyorsanız, M9201 öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bebab-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="bebab-114">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bebab-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bebab-115">Madde M9201 kullanıyorsanız, 200'den az seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bebab-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="bebab-116">Stok bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="bebab-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="bebab-117">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bebab-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bebab-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bebab-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bebab-119">Madde M9201 kullanıyorsanız, ambar 51'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bebab-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="bebab-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bebab-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="bebab-121">Stok durdurma koşullarını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="bebab-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="bebab-122">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bebab-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bebab-123">Stok Miktar alanını, engelleyecek miktarı yansıtacak şekilde güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bebab-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="bebab-124">Beklenen tarih alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="bebab-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="bebab-125">Engellenen stokun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için, tarih atamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bebab-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="bebab-126">Stok durdurma için Beklenen girişler seçeneği, bir durdurmayı el ile oluşturduğunuzda varsayılan olduğu şekilde, işaretliyse, bu tarih beklenen hareket üzerinde belirir.</span><span class="sxs-lookup"><span data-stu-id="bebab-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="bebab-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bebab-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="bebab-128">Stok durdurmayı kaldırın</span><span class="sxs-lookup"><span data-stu-id="bebab-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="bebab-129">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bebab-129">Click Delete.</span></span>
2. <span data-ttu-id="bebab-130">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bebab-130">Click Yes.</span></span>
3. <span data-ttu-id="bebab-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bebab-131">Close the page.</span></span>

