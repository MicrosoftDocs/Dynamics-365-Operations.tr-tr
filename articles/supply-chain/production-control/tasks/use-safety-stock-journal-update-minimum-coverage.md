---
title: Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma
description: Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571439"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="1098d-103">Minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma</span><span class="sxs-lookup"><span data-stu-id="1098d-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1098d-104">Bu yordam, geçmiş işlemleri temel alarak minimum kapsam tekliflerinin nasıl hesaplanacağını ve ardından tekliflerle madde kapsamının nasıl güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1098d-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="1098d-105">Bu işlem emniyet stoku günlüğü kullanılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="1098d-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="1098d-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="1098d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="1098d-107">Bu görev, üretim planlamacısına minimum kapsamı korumasında yardım etmeye yönelik olarak tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1098d-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="1098d-108">Yeni bir emniyet stoku günlüğü adı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1098d-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="1098d-109">Emniyet stoku günlük adlarına gidin.</span><span class="sxs-lookup"><span data-stu-id="1098d-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="1098d-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-110">Click New.</span></span>
3. <span data-ttu-id="1098d-111">Ad alanına "Malzeme" yazın.</span><span class="sxs-lookup"><span data-stu-id="1098d-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="1098d-112">Açıklama alanına "Malzeme" yazın.</span><span class="sxs-lookup"><span data-stu-id="1098d-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="1098d-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1098d-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="1098d-114">Emniyet stoku günlüğü adı oluştur</span><span class="sxs-lookup"><span data-stu-id="1098d-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="1098d-115">Emniyet stoku hesaplamaya gidin.</span><span class="sxs-lookup"><span data-stu-id="1098d-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="1098d-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-116">Click New.</span></span>
3. <span data-ttu-id="1098d-117">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1098d-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="1098d-118">Örneğin, Malzeme gibi oluşturduğunuz emniyet stoku günlük adını seçin.</span><span class="sxs-lookup"><span data-stu-id="1098d-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="1098d-119">Satır oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-119">Click Create lines.</span></span>
5. <span data-ttu-id="1098d-120">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="1098d-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="1098d-121">Tarihi "02.01.2015" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="1098d-122">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="1098d-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="1098d-123">Tarihi "30.12.2015" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="1098d-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-124">Click OK.</span></span>
    * <span data-ttu-id="1098d-125">Bu işlem, stok işlemleri olan boyutlar için satırlar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1098d-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="1098d-126">Teklifi hesapla</span><span class="sxs-lookup"><span data-stu-id="1098d-126">Calculate proposal</span></span>
1. <span data-ttu-id="1098d-127">Teklifi hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="1098d-128">Sağlama süresi içinde ortalama stok çıkışını kullan seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="1098d-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="1098d-129">Çarpım faktörünü 10 olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="1098d-130">Teklifi düzenlemek için Çarpma faktörü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1098d-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="1098d-131">Demo verilerde yalnızca birkaç işlem bulunduğundan gerçekçi bir teklif elde etmek için faktörü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1098d-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="1098d-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-132">Click OK.</span></span>
    * <span data-ttu-id="1098d-133">M0002 ve M0003'ü bulmak için aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="1098d-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="1098d-134">Hesaplanan minimum miktar sütununu görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="1098d-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="1098d-135">Minimum miktarı güncelleştir</span><span class="sxs-lookup"><span data-stu-id="1098d-135">Update minimum quantity</span></span>
1. <span data-ttu-id="1098d-136">Yeni minimum miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1098d-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="1098d-137">Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1098d-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="1098d-138">Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1098d-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="1098d-139">Örneğin, ambar 12'si olan M0002 için bu alana Hesaplanan minimum miktarı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1098d-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="1098d-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="1098d-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1098d-141">Örneğin, ambar 12'si olan M0002'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1098d-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="1098d-142">Yeni minimum miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1098d-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="1098d-143">Hesaplanan minimum miktardaki değer ile eşleşmesi için Yeni minimum miktarı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="1098d-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="1098d-144">Hesaplanan minimum miktar sıfır ise istediğiniz gelecek değerini girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1098d-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="1098d-145">Yeni minimum miktarı gönderin ve sonucu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="1098d-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="1098d-146">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-146">Click Post.</span></span>
2. <span data-ttu-id="1098d-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-147">Click OK.</span></span>
3. <span data-ttu-id="1098d-148">Madde numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="1098d-149">Madde numarası alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="1098d-150">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="1098d-151">Madde kapsamı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1098d-151">Click Item coverage.</span></span>
    * <span data-ttu-id="1098d-152">Minimum miktarın, emniyet stoku günlüğündeki yeni minimum miktar ile güncelleştirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="1098d-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

