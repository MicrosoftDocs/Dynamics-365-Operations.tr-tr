---
title: Satış vergisi ödemeleri ve yuvarlama kuralları
description: Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edbe92d009c77702a21d32afb5aebe93bc5e2ee0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815392"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="3049d-103">Satış vergisi ödemeleri ve yuvarlama kuralları</span><span class="sxs-lookup"><span data-stu-id="3049d-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3049d-104">Bu makalede, Satış vergisi makamlarında yuvarlama kuralı ayarlarının nasıl çalıştığı ve Satış vergilerini kapatma ve deftere nakletme işi sırasında satış vergisi bilançosunun yuvarlanması açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3049d-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="3049d-105">Satış vergilerinin düzenli olarak vergi dairelerine bildirilmesi ve ödenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3049d-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="3049d-106">Bu, Satış vergisi sayfasındaki satış vergisi kapatma ve nakletme işlemi çalıştırılarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="3049d-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="3049d-107">Bir döneme ait satış vergisi, satış vergisi hesaplarına karşı kapatılır ve satış vergisi bakiyesi Satış vergisi kapatma hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3049d-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="3049d-108">Satış verghisi kapatma hesabına nakledilen satış vergisi bakiyesi, Satş vergisi sayfasında bir yuvarlama kuralı ayarlanarak vergi kurumlarının gerektirdiği şekilde yuvarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="3049d-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="3049d-109">Yuvarlama farkı, Genel muhasebenin Otomatik hareketler için hesaplar alanında seçilen Satış vergisi yuvarlama hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3049d-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="3049d-110">Aşağıdaki örnekte, Satış vergisi dairesinde yuvarlama kuralının nasıl işlediği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3049d-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="3049d-111">Örnekler</span><span class="sxs-lookup"><span data-stu-id="3049d-111">Examples</span></span>

<span data-ttu-id="3049d-112">Bir döneme ilişkin toplam satış vergisi alacak bakiyesi -98.765,43 olarak görünmektedir.</span><span class="sxs-lookup"><span data-stu-id="3049d-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="3049d-113">Tüzel kişilik ödediğinden daha fazla satış vergisi tahsil etmiştir.</span><span class="sxs-lookup"><span data-stu-id="3049d-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="3049d-114">Bu nedenle, tüzel kişiliğin vergi dairesine ödeme yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3049d-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="3049d-115">Tüzel kişilik bakiyeyi en yakın 1,00 değerine yuvarlayan bir yuvarlama yöntemi kullanmak istemektedir.</span><span class="sxs-lookup"><span data-stu-id="3049d-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="3049d-116">Satış vergisi muhasebesinden sorumlu kullanıcı aşağıdaki adımlardan birini gerçekleştirmelidir:</span><span class="sxs-lookup"><span data-stu-id="3049d-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="3049d-117">**Vergi** >  **Dolaylı vergiler** > **Satış vergisi** > **Satış vergisi dairesi** öğelerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3049d-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="3049d-118">**Genel** hızlı sekmesinde, **Yuvarlama formu** alanından **Normal** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3049d-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="3049d-119">**Yuvarlama** alanına 1,00 girin.</span><span class="sxs-lookup"><span data-stu-id="3049d-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="3049d-120">Satış vergisini vergi dairesine ödeme zamanı geldiğinde, **Veri** > **Beyannameler** > **Satış vergisi** > **Satış vergisini kapat ve deftere naklet**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3049d-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="3049d-121">Satış vergisi kapatma hesabındaki **98.765,43** tutarındaki vergi borcunun **98.765**'e yuvarlandığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3049d-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="3049d-122">Aşağıdaki tabloda, 98.765,43 tutarının **Satış vergisi dairesi** sayfasındaki **Yuvarlama formu** alanında bulunan her yuvarlama yöntemi kullanılarak nasıl yuvarlandığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3049d-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="3049d-123">Yuvarlama değeri 0,00 olarak ayarlanmışsa,:</span><span class="sxs-lookup"><span data-stu-id="3049d-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="3049d-124">Normal yuvarlama için, yuvarlama davranışı **Yuvarla = 0,01** ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="3049d-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="3049d-125">**Yuvarlama formu seçenekleri** **Aşağı doğru**, **Yukarı yuvarlama** ve **Kendi avantajı** için, davranış **Yuvarla = 1,00** ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="3049d-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="3049d-126">Yuvarlama formu seçeneği</span><span class="sxs-lookup"><span data-stu-id="3049d-126">Rounding form option</span></span>                | <span data-ttu-id="3049d-127">Yuvarlama değeri = 0,01</span><span class="sxs-lookup"><span data-stu-id="3049d-127">Round-off value = 0.01</span></span> | <span data-ttu-id="3049d-128">Yuvarlama değeri = 0,10</span><span class="sxs-lookup"><span data-stu-id="3049d-128">Round-off value = 0.10</span></span> | <span data-ttu-id="3049d-129">Yuvarlama değeri = 1,00</span><span class="sxs-lookup"><span data-stu-id="3049d-129">Round-off value = 1.00</span></span> | <span data-ttu-id="3049d-130">Yuvarlama değeri = 100,00</span><span class="sxs-lookup"><span data-stu-id="3049d-130">Round-off value = 100.00</span></span> | <span data-ttu-id="3049d-131">Yuvarlama değeri = 0,00</span><span class="sxs-lookup"><span data-stu-id="3049d-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="3049d-132">Normal</span><span class="sxs-lookup"><span data-stu-id="3049d-132">Normal</span></span>                              | <span data-ttu-id="3049d-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="3049d-133">98,765.43</span></span>              | <span data-ttu-id="3049d-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="3049d-134">98,765.40</span></span>              | <span data-ttu-id="3049d-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="3049d-135">98,765.00</span></span>              | <span data-ttu-id="3049d-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="3049d-136">98,800.00</span></span>                | <span data-ttu-id="3049d-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="3049d-137">98,765.43</span></span>                |
| <span data-ttu-id="3049d-138">Aşağı yuvarlama</span><span class="sxs-lookup"><span data-stu-id="3049d-138">Downward</span></span>                            | <span data-ttu-id="3049d-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="3049d-139">98,765.43</span></span>              | <span data-ttu-id="3049d-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="3049d-140">98,765.40</span></span>              | <span data-ttu-id="3049d-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="3049d-141">98,765.00</span></span>              | <span data-ttu-id="3049d-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="3049d-142">98,700.00</span></span>                | <span data-ttu-id="3049d-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="3049d-143">98,765.00</span></span>                |
| <span data-ttu-id="3049d-144">Yukarı yuvarlama</span><span class="sxs-lookup"><span data-stu-id="3049d-144">Rounding-up</span></span>                         | <span data-ttu-id="3049d-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="3049d-145">98,765.43</span></span>              | <span data-ttu-id="3049d-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="3049d-146">98,765.50</span></span>              | <span data-ttu-id="3049d-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="3049d-147">98,766.00</span></span>              | <span data-ttu-id="3049d-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="3049d-148">98,800.00</span></span>                | <span data-ttu-id="3049d-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="3049d-149">98,766.00</span></span>                |
| <span data-ttu-id="3049d-150">Kendi avantajı, alacak bakiyesi için</span><span class="sxs-lookup"><span data-stu-id="3049d-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="3049d-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="3049d-151">98,765.43</span></span>              | <span data-ttu-id="3049d-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="3049d-152">98,765.40</span></span>              | <span data-ttu-id="3049d-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="3049d-153">98,765.00</span></span>              | <span data-ttu-id="3049d-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="3049d-154">98,700.00</span></span>                | <span data-ttu-id="3049d-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="3049d-155">98,765.00</span></span>                |
| <span data-ttu-id="3049d-156">Kendi avantajı, borç bakiyesi için</span><span class="sxs-lookup"><span data-stu-id="3049d-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="3049d-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="3049d-157">98,765.43</span></span>              | <span data-ttu-id="3049d-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="3049d-158">98,765.50</span></span>              | <span data-ttu-id="3049d-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="3049d-159">98,766.00</span></span>              | <span data-ttu-id="3049d-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="3049d-160">98,800.00</span></span>                | <span data-ttu-id="3049d-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="3049d-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="3049d-162">Normal yuvarlama, yuvarlama hassasiyeti 0,01'dir</span><span class="sxs-lookup"><span data-stu-id="3049d-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="3049d-163">Yuvarlama</span><span class="sxs-lookup"><span data-stu-id="3049d-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="3049d-164">Hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="3049d-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="3049d-165">yuvarla(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="3049d-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="3049d-166">yuvarla(1,015 / 0,01, 0) = yuvarla(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="3049d-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="3049d-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="3049d-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="3049d-168">yuvarla(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="3049d-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="3049d-169">yuvarla(1,014 / 0,01, 0) = yuvarla(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="3049d-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="3049d-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="3049d-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="3049d-171">yuvarla(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="3049d-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="3049d-172">yuvarla(1,011 / 0,02, 0) = yuvarla(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="3049d-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="3049d-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="3049d-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="3049d-174">yuvarla(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="3049d-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="3049d-175">yuvarla(1,009 / 0,02, 0) = yuvarla(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="3049d-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="3049d-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="3049d-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="3049d-177">Kendi avantajı seçeneğini seçerseniz, yuvarlama daima tüzel kişiliğin yararına yapılır.</span><span class="sxs-lookup"><span data-stu-id="3049d-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="3049d-178">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="3049d-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="3049d-179">Satış vergisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="3049d-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="3049d-180">Satış vergisi ödemesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3049d-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="3049d-181">Belgelerde satış vergisi hareketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="3049d-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="3049d-182">Deftere nakledilen satış vergisi hareketlerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="3049d-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="3049d-183">yuvarla işlevi</span><span class="sxs-lookup"><span data-stu-id="3049d-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]