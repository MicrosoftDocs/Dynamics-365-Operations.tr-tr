---
title: Fatura havuzu kullanarak fatura verilerini AP sistemine girme
description: Bu görev kılavuzunda size fatura oluşturmak için fatura kaydının nasıl kullanılacağı gösterilecek.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b4e9a52a383d4acc0bf2adc669fd88c0c0f7402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "357462"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="361e1-103">Fatura havuzu kullanarak fatura verilerini AP sistemine girme</span><span class="sxs-lookup"><span data-stu-id="361e1-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="361e1-104">Bu görev kılavuzunda size fatura oluşturmak için fatura kaydının nasıl kullanılacağı gösterilecek.</span><span class="sxs-lookup"><span data-stu-id="361e1-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="361e1-105">Bunun ardından, faturayı bir satınalma siparişiyle eşleştirmek ve satıcı faturası sayfasında gideri sonlandırmak için fatura havuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="361e1-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="361e1-106">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="361e1-106">Create a purchase order</span></span>
1. <span data-ttu-id="361e1-107">Borç hesapları > Satın alma siparişleri > Satınalma siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="361e1-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="361e1-108">Satınalma siparişi oluşturmak için Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="361e1-109">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="361e1-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="361e1-110">Listeden satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-110">Select the vendor from the list.</span></span> <span data-ttu-id="361e1-111">Örneğin, satıcı 1001.</span><span class="sxs-lookup"><span data-stu-id="361e1-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="361e1-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-112">Click OK.</span></span>
6. <span data-ttu-id="361e1-113">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="361e1-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="361e1-114">Listede hizmet madde numarasını bulun.</span><span class="sxs-lookup"><span data-stu-id="361e1-114">Find the services item number in the list.</span></span> <span data-ttu-id="361e1-115">Örneğin, S0001 seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-115">For example, select S0001.</span></span>
8. <span data-ttu-id="361e1-116">Madde numarasına tıklayarak seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="361e1-117">Net tutar 75,00'tir.</span><span class="sxs-lookup"><span data-stu-id="361e1-117">The net amount is 75.00.</span></span>  <span data-ttu-id="361e1-118">Bu, faturada olmasını beklediğimiz tutardır.</span><span class="sxs-lookup"><span data-stu-id="361e1-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="361e1-119">Eylem bölmesinde, Satınalma'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="361e1-120">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="361e1-121">Fatura oluşturun ve nakledin</span><span class="sxs-lookup"><span data-stu-id="361e1-121">Create and post and invoice</span></span>
1. <span data-ttu-id="361e1-122">Borç hesapları > Faturalar > Fatura kaydı'na gidin.</span><span class="sxs-lookup"><span data-stu-id="361e1-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="361e1-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-123">Click New.</span></span>
3. <span data-ttu-id="361e1-124">Kullanmak istediğiniz fatura kaydının adını seçmek için aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="361e1-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="361e1-125">Kullanmak istediğiniz fatura kaydının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="361e1-126">Defteri açıp gider satırlarını girmek için Satırlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="361e1-127">Aramada bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="361e1-128">Örneğin, satıcı 1001'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="361e1-129">Fatura alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="361e1-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="361e1-130">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="361e1-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="361e1-131">Alacak alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="361e1-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="361e1-132">Satınalma siparişi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="361e1-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="361e1-133">Daha önce oluşturduğunuz satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="361e1-134">Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="361e1-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="361e1-135">Bir onaylayanı vurgulayın ve o onaylayanı seçmek için Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="361e1-136">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-136">Click Post.</span></span>
15. <span data-ttu-id="361e1-137">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="361e1-137">Close the form.</span></span>
16. <span data-ttu-id="361e1-138">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="361e1-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="361e1-139">Havuzdan bir fatura açın ve bir satınalma siparişiyle eşleştirerek fatura işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="361e1-140">Borç hesapları > Faturalar > Fatura havuzu'na gidin.</span><span class="sxs-lookup"><span data-stu-id="361e1-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="361e1-141">Havuzdaki faturadan bir satıcı faturası oluşturmak için Satınalma siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="361e1-142">İncelemek istediğiniz faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="361e1-143">Eşleşmeyi tamamlamak için Eşleştirme durumunu güncelleştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="361e1-144">Eylem bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="361e1-145">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-145">Click Change view.</span></span>
7. <span data-ttu-id="361e1-146">Izgara görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-146">Click Grid view.</span></span>
8. <span data-ttu-id="361e1-147">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-147">Click Post.</span></span>
9. <span data-ttu-id="361e1-148">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="361e1-148">Close the form.</span></span>
10. <span data-ttu-id="361e1-149">Borç hesapları > Satıcılar > Satıcılar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="361e1-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="361e1-150">Satınalma siparişindeki satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="361e1-151">Örneğin, satıcı 1001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="361e1-152">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="361e1-153">Eylem bölmesinde, Satıcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="361e1-154">Hareketler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361e1-154">Click Transactions.</span></span>
15. <span data-ttu-id="361e1-155">Oluşturduğunuz faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="361e1-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="361e1-156">Fatura kaydı tahakkuku ters kaydedilmiş ve ilgili gider hesabına nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="361e1-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

