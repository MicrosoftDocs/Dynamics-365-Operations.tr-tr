---
title: "Satış vergisi ödemeleri ve yuvarlama kuralları"
description: "Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 8de01b77fcbeb65321e60614b6a11d264460208f
ms.contentlocale: tr-tr
ms.lasthandoff: 08/01/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="7bc1e-103">Satış vergisi ödemeleri ve yuvarlama kuralları</span><span class="sxs-lookup"><span data-stu-id="7bc1e-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7bc1e-104">Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="7bc1e-105">Satış vergilerinin düzenli olarak vergi dairelerine bildirilmesi ve ödenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="7bc1e-106">Bu, Satış vergisi sayfasındaki satış vergisi kapatma ve nakletme işlemi çalıştırılarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="7bc1e-107">Bir döneme ait satış vergisi, satış vergisi hesaplarına karşı kapatılır ve satış vergisi bakiyesi Satış vergisi kapatma hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="7bc1e-108">Satış verghisi kapatma hesabına nakledilen satış vergisi bakiyesi, Satş vergisi sayfasında bir yuvarlama kuralı ayarlanarak vergi kurumlarının gerektirdiği şekilde yuvarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="7bc1e-109">Yuvarlama farkı, Genel muhasebenin Otomatik hareketler için hesaplar alanında seçilen Satış vergisi yuvarlama hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="7bc1e-110">Aşağıdaki örnekte, Satış vergisi dairesinde yuvarlama kuralının nasıl işlediği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="7bc1e-111">Örnek:</span><span class="sxs-lookup"><span data-stu-id="7bc1e-111">Example:</span></span>

<span data-ttu-id="7bc1e-112">Bir döneme ilişkin toplam satış vergisi alacak bakiyesi -98.765,43 olarak görünmektedir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="7bc1e-113">Tüzel kişilik ödediğinden daha fazla satış vergisi tahsil etmiştir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="7bc1e-114">Bu nedenle, tüzel kişiliğin vergi dairesine ödeme yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="7bc1e-115">Tüzel kişilik bakiyeyi en yakın 1,00 değerine yuvarlayan bir yuvarlama yöntemi kullanmak istemektedir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="7bc1e-116">Satış vergisi muhasebesinden sorumlu kullanıcı aşağıdaki adımlardan birini gerçekleştirmelidir:</span><span class="sxs-lookup"><span data-stu-id="7bc1e-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="7bc1e-117">Vergi &gt; Dolaylı vergiler &gt; Satış vergisi &gt; Satış vergisi dairesi öğelerine tıklayın</span><span class="sxs-lookup"><span data-stu-id="7bc1e-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="7bc1e-118">Genel hızlı sekmesinde, Yuvarlama formu alanından Normal seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="7bc1e-119">Yuvarlama alanına 1,00 girin.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="7bc1e-120">Satış vergisini vergi dairesine ödeme zamanı geldiğinde, Satış vergisini kapat ve naklet sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="7bc1e-121">(Vergi &gt; Beyannameler &gt; Satış vergisi &gt; Satış vergisini kapat ve naklet'e tıklayın.)</span><span class="sxs-lookup"><span data-stu-id="7bc1e-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="7bc1e-122">Satış vergisi kapatma hesabındaki 98.765,43 tutarındaki vergi borcu 98.765'e yuvarlanır.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="7bc1e-123">Aşağıdaki tabloda, 98.765,43 tutarının Satış vergisi dairesi sayfasındaki Yuvarlama formu alanında bulunan her yuvarlama yöntemi kullanılarak nasıl yuvarlandığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="7bc1e-124">Yuvarlama formu seçeneği</span><span class="sxs-lookup"><span data-stu-id="7bc1e-124">Rounding form option</span></span>                | <span data-ttu-id="7bc1e-125">Yuvarlama değeri = 0,01</span><span class="sxs-lookup"><span data-stu-id="7bc1e-125">Round-off value = 0.01</span></span> | <span data-ttu-id="7bc1e-126">Yuvarlama değeri = 0,10</span><span class="sxs-lookup"><span data-stu-id="7bc1e-126">Round-off value = 0.10</span></span> | <span data-ttu-id="7bc1e-127">Yuvarlama değeri = 1,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-127">Round-off value = 1.00</span></span> | <span data-ttu-id="7bc1e-128">Yuvarlama değeri = 100,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="7bc1e-129">Normal</span><span class="sxs-lookup"><span data-stu-id="7bc1e-129">Normal</span></span>                              | <span data-ttu-id="7bc1e-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="7bc1e-130">98,765.43</span></span>              | <span data-ttu-id="7bc1e-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="7bc1e-131">98,765.40</span></span>              | <span data-ttu-id="7bc1e-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-132">98,765.00</span></span>              | <span data-ttu-id="7bc1e-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-133">98,800.00</span></span>                |
| <span data-ttu-id="7bc1e-134">Aşağı yuvarlama</span><span class="sxs-lookup"><span data-stu-id="7bc1e-134">Downward</span></span>                            | <span data-ttu-id="7bc1e-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="7bc1e-135">98,765.43</span></span>              | <span data-ttu-id="7bc1e-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="7bc1e-136">98,765.40</span></span>              | <span data-ttu-id="7bc1e-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-137">98,765.00</span></span>              | <span data-ttu-id="7bc1e-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-138">98,700.00</span></span>                |
| <span data-ttu-id="7bc1e-139">Yukarı yuvarlama</span><span class="sxs-lookup"><span data-stu-id="7bc1e-139">Rounding-up</span></span>                         | <span data-ttu-id="7bc1e-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="7bc1e-140">98,765.43</span></span>              | <span data-ttu-id="7bc1e-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="7bc1e-141">98,765.50</span></span>              | <span data-ttu-id="7bc1e-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-142">98,766.00</span></span>              | <span data-ttu-id="7bc1e-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-143">98,800.00</span></span>                |
| <span data-ttu-id="7bc1e-144">Kendi avantajı, alacak bakiyesi için</span><span class="sxs-lookup"><span data-stu-id="7bc1e-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="7bc1e-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="7bc1e-145">98,765.43</span></span>              | <span data-ttu-id="7bc1e-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="7bc1e-146">98,765.40</span></span>              | <span data-ttu-id="7bc1e-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-147">98,765.00</span></span>              | <span data-ttu-id="7bc1e-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-148">98,700.00</span></span>                |
| <span data-ttu-id="7bc1e-149">Kendi avantajı, borç bakiyesi için</span><span class="sxs-lookup"><span data-stu-id="7bc1e-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="7bc1e-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="7bc1e-150">98,765.43</span></span>              | <span data-ttu-id="7bc1e-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="7bc1e-151">98,765.50</span></span>              | <span data-ttu-id="7bc1e-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-152">98,766.00</span></span>              | <span data-ttu-id="7bc1e-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="7bc1e-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="7bc1e-154">Kendi avantajı seçeneğini seçerseniz, yuvarlama daima tüzel kişiliğin yararına yapılır.</span><span class="sxs-lookup"><span data-stu-id="7bc1e-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="7bc1e-155">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="7bc1e-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="7bc1e-156">Satış vergisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7bc1e-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="7bc1e-157">Satış vergisi ödemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bc1e-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="7bc1e-158">Belgelerde satış hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bc1e-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="7bc1e-159">Deftere nakledilen satış vergisi hareketlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7bc1e-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



