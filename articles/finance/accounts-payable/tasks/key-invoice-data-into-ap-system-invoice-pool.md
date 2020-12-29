---
title: Fatura havuzu kullanarak fatura verilerini AP sistemine girme
description: Bu konu, fatura kaydının faturaları oluşturmak için nasıl kullanılacağını açıklar.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd6de42dda650d42d703e905f8d48f73b9e4afd6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448761"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="b45b5-103">Fatura havuzu kullanarak fatura verilerini AP sistemine girme</span><span class="sxs-lookup"><span data-stu-id="b45b5-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b45b5-104">Bu konu, fatura kaydının faturaları oluşturmak için nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="b45b5-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="b45b5-105">Bunun ardından, faturayı bir satınalma siparişiyle eşleştirmek ve satıcı faturası sayfasında gideri sonlandırmak için fatura havuzunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b45b5-106">Satınalma siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b45b5-106">Create a purchase order</span></span>
1. <span data-ttu-id="b45b5-107">Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Satın alma siparişleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="b45b5-108">Satınalma siparişi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="b45b5-109">**Satıcı hesabı** alanında, açılır liste için bir satıcı belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="b45b5-110">Örneğin, satıcı **1001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="b45b5-111">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-111">Select **OK**.</span></span>
5. <span data-ttu-id="b45b5-112">**Madde numarası** alanında, açılık menüde hizmet madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="b45b5-113">Örneğin, **S0001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-113">For example, select **S0001**.</span></span> <span data-ttu-id="b45b5-114">Net tutar 75,00'tir.</span><span class="sxs-lookup"><span data-stu-id="b45b5-114">The net amount is 75.00.</span></span>  <span data-ttu-id="b45b5-115">Bu, faturada olmasını beklediğimiz tutardır.</span><span class="sxs-lookup"><span data-stu-id="b45b5-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="b45b5-116">Eylem Bölmesinde, **Satınalma** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="b45b5-117">**Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="b45b5-118">Fatura oluşturun ve nakledin</span><span class="sxs-lookup"><span data-stu-id="b45b5-118">Create and post and invoice</span></span>
1. <span data-ttu-id="b45b5-119">Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura kaydı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="b45b5-120">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-120">Select **New**.</span></span>
3. <span data-ttu-id="b45b5-121">Kullanmak istediğiniz fatura kaydının adını seçmek için aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="b45b5-122">Kullanmak istediğiniz fatura kaydının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="b45b5-123">Defteri açıp gider satırlarını girmek için **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="b45b5-124">Aramada bir satıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="b45b5-125">Örneğin, satıcı **1001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="b45b5-126">**Fatura** alanına fatura numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="b45b5-127">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="b45b5-128">**Alacak** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="b45b5-129">**Satınalma siparişi** alanında, önceden oluşturduğunuz satınalma siparişini seçmek için açılır listeyi açın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="b45b5-130">**Onaylayan** alanında açılır listeden bir onaylayan seçin ve o onaylayanı seçmek için **Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="b45b5-131">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="b45b5-132">Havuzdan bir fatura açın ve bir satınalma siparişiyle eşleştirerek fatura işlemini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="b45b5-133">Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura havuzu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="b45b5-134">Havuzdaki faturadan bir satıcı faturası oluşturmak için **Satınalma siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="b45b5-135">İncelemek istediğiniz faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="b45b5-136">Eşleşmeyi tamamlamak için **Eşleştirme durumunu güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="b45b5-137">Eylem Bölmesinde, **Seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="b45b5-138">**Görünümü değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-138">Select **Change view**.</span></span>
7. <span data-ttu-id="b45b5-139">**Izgara görünümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="b45b5-140">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-140">Select **Post**.</span></span>
9. <span data-ttu-id="b45b5-141">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="b45b5-141">Close the form.</span></span>
10. <span data-ttu-id="b45b5-142">Gezinti Bölmesi'nde **Modüller > Borç hesapları > Satıcılar > Satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="b45b5-143">Satınalma siparişindeki satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="b45b5-144">Örneğin, satıcı **1001**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="b45b5-145">Eylem Bölmesinde, **Satıcılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="b45b5-146">**Hareketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="b45b5-147">Oluşturduğunuz faturayı seçin.</span><span class="sxs-lookup"><span data-stu-id="b45b5-147">Select the invoice that you created.</span></span> <span data-ttu-id="b45b5-148">Fatura kaydı tahakkuku ters kaydedilmiş ve ilgili gider hesabına nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b45b5-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

