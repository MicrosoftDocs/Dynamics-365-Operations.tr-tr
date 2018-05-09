--- 
title: Fatura havuzu kullanarak fatura verilerini AP sistemine girme
description: "Bu görev kılavuzunda size fatura oluşturmak için fatura kaydının nasıl kullanılacağı gösterilecek."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a1273593f221963064c15a6404d4d92453f69d40
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="be6a3-103">Fatura havuzu kullanarak fatura verilerini AP sistemine girme</span><span class="sxs-lookup"><span data-stu-id="be6a3-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be6a3-104">Bu görev kılavuzunda size fatura oluşturmak için fatura kaydının nasıl kullanılacağı gösterilecek.</span><span class="sxs-lookup"><span data-stu-id="be6a3-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="be6a3-105">Bunun ardından, faturayı bir satınalma siparişiyle eşleştirmek ve satıcı faturası sayfasında gideri sonlandırmak için fatura havuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="be6a3-106">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="be6a3-106">Create a purchase order</span></span>
1. <span data-ttu-id="be6a3-107">Borç hesapları > Satın alma siparişleri > Satınalma siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="be6a3-108">Satınalma siparişi oluşturmak için Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="be6a3-109">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="be6a3-110">Listeden satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-110">Select the vendor from the list.</span></span> <span data-ttu-id="be6a3-111">Örneğin, satıcı 1001.</span><span class="sxs-lookup"><span data-stu-id="be6a3-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="be6a3-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-112">Click OK.</span></span>
6. <span data-ttu-id="be6a3-113">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="be6a3-114">Listede hizmet madde numarasını bulun.</span><span class="sxs-lookup"><span data-stu-id="be6a3-114">Find the services item number in the list.</span></span> <span data-ttu-id="be6a3-115">Örneğin, S0001 seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-115">For example, select S0001.</span></span>
8. <span data-ttu-id="be6a3-116">Madde numarasına tıklayarak seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="be6a3-117">Net tutar 75,00'tir.</span><span class="sxs-lookup"><span data-stu-id="be6a3-117">The net amount is 75.00.</span></span>  <span data-ttu-id="be6a3-118">Bu, faturada olmasını beklediğimiz tutardır.</span><span class="sxs-lookup"><span data-stu-id="be6a3-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="be6a3-119">Eylem bölmesinde, Satınalma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="be6a3-120">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="be6a3-121">Fatura oluşturun ve nakledin</span><span class="sxs-lookup"><span data-stu-id="be6a3-121">Create and post and invoice</span></span>
1. <span data-ttu-id="be6a3-122">Borç hesapları > Faturalar > Fatura kaydı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="be6a3-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-123">Click New.</span></span>
3. <span data-ttu-id="be6a3-124">Kullanmak istediğiniz fatura kaydının adını seçmek için aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="be6a3-125">Kullanmak istediğiniz fatura kaydının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="be6a3-126">Defteri açıp gider satırlarını girmek için Satırlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="be6a3-127">Aramada bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="be6a3-128">Örneğin, satıcı 1001'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="be6a3-129">Fatura alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="be6a3-130">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="be6a3-131">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="be6a3-132">Satınalma siparişi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="be6a3-133">Daha önce oluşturduğunuz satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="be6a3-134">Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="be6a3-135">Bir onaylayanı vurgulayın ve o onaylayanı seçmek için Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="be6a3-136">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-136">Click Post.</span></span>
15. <span data-ttu-id="be6a3-137">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-137">Close the form.</span></span>
16. <span data-ttu-id="be6a3-138">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="be6a3-139">Havuzdan bir fatura açın ve bir satınalma siparişiyle eşleştirerek fatura işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="be6a3-140">Borç hesapları > Faturalar > Fatura havuzu'na gidin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="be6a3-141">Havuzdaki faturadan bir satıcı faturası oluşturmak için Satınalma siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="be6a3-142">İncelemek istediğiniz faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="be6a3-143">Eşleşmeyi tamamlamak için Eşleştirme durumunu güncelleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="be6a3-144">Eylem bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="be6a3-145">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-145">Click Change view.</span></span>
7. <span data-ttu-id="be6a3-146">Izgara görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-146">Click Grid view.</span></span>
8. <span data-ttu-id="be6a3-147">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-147">Click Post.</span></span>
9. <span data-ttu-id="be6a3-148">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-148">Close the form.</span></span>
10. <span data-ttu-id="be6a3-149">Borç hesapları > Satıcılar > Satıcılar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="be6a3-150">Satınalma siparişindeki satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="be6a3-151">Örneğin, satıcı 1001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="be6a3-152">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="be6a3-153">Eylem bölmesinde, Satıcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="be6a3-154">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="be6a3-154">Click Transactions.</span></span>
15. <span data-ttu-id="be6a3-155">Oluşturduğunuz faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="be6a3-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="be6a3-156">Fatura kaydı tahakkuku ters kaydedilmiş ve ilgili gider hesabına nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="be6a3-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


