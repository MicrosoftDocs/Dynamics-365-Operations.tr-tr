---
title: Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma
description: Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir.
author: ChristianRytt
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f1102f5388043299e35d3e6a00d4fe203a4e696a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831811"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="2ee73-103">Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma</span><span class="sxs-lookup"><span data-stu-id="2ee73-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ee73-104">Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ee73-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="2ee73-105">Bu işlem emniyet stoku günlüğü kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="2ee73-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="2ee73-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="2ee73-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="2ee73-107">Bu görev, üretim planlamacısına minimum kapsamı korumasında yardım etmeye yönelik olarak tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2ee73-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="2ee73-108">Yeni bir emniyet stoku günlüğü adı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2ee73-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="2ee73-109">**Gezinti bölmesinde** **Master planlama > Kurulum > Emniyet stoku günlüğü adları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="2ee73-110">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-110">Click **New**.</span></span>
3. <span data-ttu-id="2ee73-111">**Ad** alanına "Malzeme" yazın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="2ee73-112">**Açıklama** alanına "Malzeme" yazın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="2ee73-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="2ee73-114">Emniyet stoku günlüğü adı oluştur</span><span class="sxs-lookup"><span data-stu-id="2ee73-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="2ee73-115">**Gezinti bölmesinde** **Master planlama > Master planlama > Çalıştır > Emniyet stoku hesaplama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="2ee73-116">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-116">Click **New**.</span></span>
3. <span data-ttu-id="2ee73-117">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="2ee73-118">Örneğin, Malzeme gibi oluşturduğunuz emniyet stoku günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="2ee73-119">**Satırlar oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="2ee73-120">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="2ee73-121">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="2ee73-122">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-122">Click **OK**.</span></span> <span data-ttu-id="2ee73-123">Bu işlem, stok işlemleri olan boyutlar için satırlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ee73-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="2ee73-124">Teklifi hesapla</span><span class="sxs-lookup"><span data-stu-id="2ee73-124">Calculate proposal</span></span>
1. <span data-ttu-id="2ee73-125">**Teklifi hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="2ee73-126">**Sağlama süresi içinde ortalama stok çıkışını kullan** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="2ee73-127">**Çarpım faktörünü** '10' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="2ee73-128">Teklifi düzenlemek için Çarpma faktörü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ee73-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="2ee73-129">Demo verilerde yalnızca birkaç işlem bulunduğundan gerçekçi bir teklif elde etmek için faktörü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2ee73-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="2ee73-130">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-130">Click **OK**.</span></span> <span data-ttu-id="2ee73-131">M0002 ve M0003'ü bulmak için aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="2ee73-132">**Hesaplanan minimum** miktar sütununu görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="2ee73-133">Minimum miktarı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="2ee73-133">Update minimum quantity</span></span>
1. <span data-ttu-id="2ee73-134">**Yeni minimum miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="2ee73-135">Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="2ee73-136">Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee73-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="2ee73-137">Örneğin, ambar 12'si olan M0002 için bu alana Hesaplanan minimum miktarı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee73-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="2ee73-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="2ee73-139">Örneğin, ambar 12'si olan M0002'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee73-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="2ee73-140">**Yeni minimum miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="2ee73-141">Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="2ee73-142">Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ee73-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="2ee73-143">Yeni minimum miktarı gönderin ve sonucu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="2ee73-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="2ee73-144">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-144">Click **Post**.</span></span>
2. <span data-ttu-id="2ee73-145">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-145">Click **OK**.</span></span>
3. <span data-ttu-id="2ee73-146">**Madde numarası** alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="2ee73-147">**Madde numarası** alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="2ee73-148">**Eylem Bölmesi**'nde Plan'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="2ee73-149">**Madde kapsamı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ee73-149">Click **Item coverage**.</span></span> <span data-ttu-id="2ee73-150">**Minimum miktarın**, emniyet stoku günlüğündeki yeni minimum miktar ile güncelleştirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2ee73-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]