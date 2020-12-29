---
title: Bir vade farkı kodu için vade farkı oranları ayarlama
description: Vade farkı kodları, faizin nasıl belirleneceğini ve ödemesi geciken hesaplarda nasıl hesaplanacağını belirleyen ayarlar içerir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448713"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="d72e8-103">Bir vade farkı kodu için vade farkı oranları ayarlama</span><span class="sxs-lookup"><span data-stu-id="d72e8-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d72e8-104">Vade farkı kodları, faizin nasıl belirleneceğini ve ödemesi geciken hesaplarda nasıl hesaplanacağını belirleyen ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="d72e8-105">Bir tek faiz kodu ayarlayabilir ve birden fazla müşteri deftere nakil profilleri, faturalama kodları veya belirli fatura satırlarına uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="d72e8-106">Faiz kodu ayrıntıları değiştiğinde, bu kodu kullanan tüm özellikler değişiklikleri yeni hareketlere otomatik olarak uygular.</span><span class="sxs-lookup"><span data-stu-id="d72e8-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="d72e8-107">Her faiz kodu için iki tür oran ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d72e8-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="d72e8-108">Faiz gelirleri için oranlar − Bunlar faturalardaki veya vade farkı dekontlarının faizini borçlandırmadan kazanılan geliri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d72e8-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="d72e8-109">Faiz ödemeleri için oranlar − Bunlar alacak dekontları üzerindeki faiz için ödenen maliyeti temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d72e8-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="d72e8-110">Bu oran türlerinin her ikisi de aynı anda ve aynı vade farkı kodu içinde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="d72e8-111">Faiz oranları üç hesaplama türüne bağlı olabilir:</span><span class="sxs-lookup"><span data-stu-id="d72e8-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="d72e8-112">Yüzdeye göre vade farkı.</span><span class="sxs-lookup"><span data-stu-id="d72e8-112">Interest by percentage.</span></span>
-   <span data-ttu-id="d72e8-113">Tutara göre vade farkı.</span><span class="sxs-lookup"><span data-stu-id="d72e8-113">Interest by amount.</span></span>
-   <span data-ttu-id="d72e8-114">Tek bir yüzde veya tutar ile sonuçlanan, aralığa göre vade farkı.</span><span class="sxs-lookup"><span data-stu-id="d72e8-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="d72e8-115">Bir vade farkı kodu, faizi hesaplamak için kullanıldığında, ödemenin hareket vade tarihini geçtiği süre boyunca etkin olan her vade farkı oranı için ayrı bir vade farkı dekontu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d72e8-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="d72e8-116">**Vade farkı kodu** sayfası üzerindeki **Kazançlar** sekmesini kullanıp, faiz alarak edindiğiniz gelirler için vade farkı oranlarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="d72e8-117">**Ödemeler** sekmesini kullanıp ödediğiniz vade farkı için vade farkı oranlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="d72e8-118">Yüzdeye dayalı vade farkı oranları</span><span class="sxs-lookup"><span data-stu-id="d72e8-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="d72e8-119">Belirli bir yüzdeyi hesaplayan vade farkı oranlarını ayarlayabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d72e8-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="d72e8-120">Vade farkı tutarı tüm para birimleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="d72e8-121">İsteğe bağlı vade farkı tutar limitleri girilebilir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="d72e8-122"><strong>Faiz kodlarını ayarla</strong> sayfasındaki <strong>**Faiz farklarının dayanağı</strong> alanındaki <strong>Yüzde</strong> seçilidir**.</span><span class="sxs-lookup"><span data-stu-id="d72e8-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="d72e8-123">Örneğin, fatura ödemesinin hareket vade tarihini geçtiği her iki ay için yüzde 5 vade farkı koyan vade farkı kodunu ayarlamak için **Her biri için faiz hesapla** alanına 2 girer ve **Ay**'ı seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="d72e8-124">Tutarları temel alan faiz oranları</span><span class="sxs-lookup"><span data-stu-id="d72e8-124">Interest rates based on amounts</span></span>
<span data-ttu-id="d72e8-125">Belirli bir para birimine göre tutarı hesaplayan vade farkı oranlarını ayarlayabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d72e8-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="d72e8-126">Vade farkı kodu içindeki her para birimi için vade farkı tutarı belirtilir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="d72e8-127">İsteğe bağlı vade farkı tutar limitleri girilebilir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="d72e8-128">**Vade farkı kodlarını ayarla** sayfasındaki **Vade farklarının dayanağı** alanındaki **Tutar** seçilidir.</span><span class="sxs-lookup"><span data-stu-id="d72e8-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="d72e8-129">Örneğin, fatura ödemesinin hareket vade tarihini geçtiği her 20 gün için yüzde 25,00 vade farkı koyan vade farkı kodunu ayarlamak için **Her biri için faiz hesapla** alanında 20 girer ve **Gün**'ü seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="d72e8-130">Aralıkları temel alan faiz oranları</span><span class="sxs-lookup"><span data-stu-id="d72e8-130">Interest rates based on ranges</span></span>
<span data-ttu-id="d72e8-131">Geçmiş tutar, tutarın geç kaldığı gün sayısı veya tutarın geç kaldığı ay sayısına bağlı olarak değişen vade farkı oranları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="d72e8-132">**Para birimine göre kazanç** sekmesini kullanarak her para birimi için belirli vade farkı ayarları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="d72e8-133">Ayrıca aralığı da buradan tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="d72e8-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="d72e8-134">**Aralıklar** butonunu ayarlamak istediğiniz aralıkları temsil eden satırlar eklemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="d72e8-135">**Gelen** değeri aralığın başlangıcını temsil eder ve **Vade farkı değeri** numarası **Vade farkı kodlarını ayarlamak** sayfasının **Vade farklarının dayanağı** alanındaki yüzde veya tutar seçimine bağlı olarak bir yüzdeyi veya tutarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d72e8-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="d72e8-136">Örnek 1: Aralığa göre vade farkı = Tutar</span><span class="sxs-lookup"><span data-stu-id="d72e8-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="d72e8-137">Faturanın ödemesinin hareket vade tarihini aştığını her üç ayda bir değerlendirecek bir vade farkı kodu ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="d72e8-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="d72e8-138">Hesaplamayı, adımlı tutar aralıklarına göre, bir yüzde vade farkı değerine dayandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="d72e8-139">Faiz değeri 1.000,00 olan faturalara kadar yüzde 1, 1.001,00'den 5.000,00 olanlara kadar yüzde 2 ve 5.000,00'den büyük olanlar için yüzde üç olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d72e8-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="d72e8-140">Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="d72e8-141">**Alan adı**</span><span class="sxs-lookup"><span data-stu-id="d72e8-141">**Field name**</span></span>                  | <span data-ttu-id="d72e8-142">**Alan değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="d72e8-143">**Vade farkı kodu**</span><span class="sxs-lookup"><span data-stu-id="d72e8-143">**Interest code**</span></span>               | <span data-ttu-id="d72e8-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="d72e8-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="d72e8-145">**Her biri için faizi hesapla:**</span><span class="sxs-lookup"><span data-stu-id="d72e8-145">**Calculate interest every**</span></span>    | <span data-ttu-id="d72e8-146">3/Ay</span><span class="sxs-lookup"><span data-stu-id="d72e8-146">3/Month</span></span>         |
| <span data-ttu-id="d72e8-147">**Aralığa göre faiz**</span><span class="sxs-lookup"><span data-stu-id="d72e8-147">**Interest by range**</span></span>           | <span data-ttu-id="d72e8-148">Tutar</span><span class="sxs-lookup"><span data-stu-id="d72e8-148">Amount</span></span>          |
| <span data-ttu-id="d72e8-149">**Vade farkını şuna göre hesapla**</span><span class="sxs-lookup"><span data-stu-id="d72e8-149">**Calculate interest based on**</span></span> | <span data-ttu-id="d72e8-150">Yüzde</span><span class="sxs-lookup"><span data-stu-id="d72e8-150">Percentage</span></span>      |

<span data-ttu-id="d72e8-151">Aralığı bilgilerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="d72e8-152">**Başlangıç değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-152">**From value**</span></span> | <span data-ttu-id="d72e8-153">**Faiz değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="d72e8-154">0</span><span class="sxs-lookup"><span data-stu-id="d72e8-154">0</span></span>              | <span data-ttu-id="d72e8-155">1</span><span class="sxs-lookup"><span data-stu-id="d72e8-155">1</span></span>                  |
| <span data-ttu-id="d72e8-156">1,001</span><span class="sxs-lookup"><span data-stu-id="d72e8-156">1,001</span></span>          | <span data-ttu-id="d72e8-157">2</span><span class="sxs-lookup"><span data-stu-id="d72e8-157">2</span></span>                  |
| <span data-ttu-id="d72e8-158">5,001</span><span class="sxs-lookup"><span data-stu-id="d72e8-158">5,001</span></span>          | <span data-ttu-id="d72e8-159">3</span><span class="sxs-lookup"><span data-stu-id="d72e8-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="d72e8-160">Örnek 2: Aralığa göre faiz = Gün</span><span class="sxs-lookup"><span data-stu-id="d72e8-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="d72e8-161">Faturanın ödemesinin hareket vade tarihini aştığını her 15 günde bir değerlendirecek bir vade farkı kodu ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="d72e8-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="d72e8-162">Hesaplamayı, adımlı gün aralıklarına göre, bir tutar vade farkı değerine dayandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="d72e8-163">Vade farkı değeri ilk 60 gün içinde 15 günlük 10,00, 61 ve 90. günler arasında 15 günlük 15,00 ve 91 gün ve daha fazlası için her 15 günlük 20,00 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d72e8-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="d72e8-164">Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="d72e8-165">**Alan adı**</span><span class="sxs-lookup"><span data-stu-id="d72e8-165">**Field name**</span></span>                  | <span data-ttu-id="d72e8-166">**Alan değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="d72e8-167">**Vade farkı kodu**</span><span class="sxs-lookup"><span data-stu-id="d72e8-167">**Interest code**</span></span>               | <span data-ttu-id="d72e8-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="d72e8-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="d72e8-169">**Her biri için faizi hesapla:**</span><span class="sxs-lookup"><span data-stu-id="d72e8-169">**Calculate interest every**</span></span>    | <span data-ttu-id="d72e8-170">15/Gün</span><span class="sxs-lookup"><span data-stu-id="d72e8-170">15/Day</span></span>          |
| <span data-ttu-id="d72e8-171">**Aralığa göre faiz**</span><span class="sxs-lookup"><span data-stu-id="d72e8-171">**Interest by range**</span></span>           | <span data-ttu-id="d72e8-172">Gün</span><span class="sxs-lookup"><span data-stu-id="d72e8-172">Days</span></span>            |
| <span data-ttu-id="d72e8-173">**Vade farkını şuna göre hesapla**</span><span class="sxs-lookup"><span data-stu-id="d72e8-173">**Calculate interest based on**</span></span> | <span data-ttu-id="d72e8-174">Tutar</span><span class="sxs-lookup"><span data-stu-id="d72e8-174">Amount</span></span>          |

<span data-ttu-id="d72e8-175">Aralığı bilgilerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="d72e8-176">**Başlangıç değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-176">**From value**</span></span> | <span data-ttu-id="d72e8-177">**Faiz değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="d72e8-178">0</span><span class="sxs-lookup"><span data-stu-id="d72e8-178">0</span></span>              | <span data-ttu-id="d72e8-179">10</span><span class="sxs-lookup"><span data-stu-id="d72e8-179">10</span></span>                 |
| <span data-ttu-id="d72e8-180">61</span><span class="sxs-lookup"><span data-stu-id="d72e8-180">61</span></span>             | <span data-ttu-id="d72e8-181">15</span><span class="sxs-lookup"><span data-stu-id="d72e8-181">15</span></span>                 |
| <span data-ttu-id="d72e8-182">91</span><span class="sxs-lookup"><span data-stu-id="d72e8-182">91</span></span>             | <span data-ttu-id="d72e8-183">20</span><span class="sxs-lookup"><span data-stu-id="d72e8-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="d72e8-184">Örnek 3: Aralığa göre faiz = Ay</span><span class="sxs-lookup"><span data-stu-id="d72e8-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="d72e8-185">Faturanın ödemesinin hareket vade tarihini aştığını her ayda bir değerlendirecek bir vade farkı kodu ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="d72e8-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="d72e8-186">Hesaplamayı, adımlı aylık aralıklarına göre, bir yüzde vade farkı değerine dayandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="d72e8-187">Varde farkı değer, vadenin geçtiği ilk üç ay için her aylık yüzde 1,5, ikinci üç aylık dönem için aylık yüzde 2,0 ve ilk altı aydan sonraki her ay için yüzde 2,5 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d72e8-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="d72e8-188">Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="d72e8-189">**Alan adı**</span><span class="sxs-lookup"><span data-stu-id="d72e8-189">**Field name**</span></span>                  | <span data-ttu-id="d72e8-190">**Alan değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="d72e8-191">**Vade farkı kodu**</span><span class="sxs-lookup"><span data-stu-id="d72e8-191">**Interest code**</span></span>               | <span data-ttu-id="d72e8-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="d72e8-192">1M%ByMth</span></span>        |
| <span data-ttu-id="d72e8-193">**Her biri için faizi hesapla:**</span><span class="sxs-lookup"><span data-stu-id="d72e8-193">**Calculate interest every**</span></span>    | <span data-ttu-id="d72e8-194">1/Ay</span><span class="sxs-lookup"><span data-stu-id="d72e8-194">1/Month</span></span>         |
| <span data-ttu-id="d72e8-195">**Aralığa göre faiz**</span><span class="sxs-lookup"><span data-stu-id="d72e8-195">**Interest by range**</span></span>           | <span data-ttu-id="d72e8-196">Ay</span><span class="sxs-lookup"><span data-stu-id="d72e8-196">Months</span></span>          |
| <span data-ttu-id="d72e8-197">**Vade farkını şuna göre hesapla**</span><span class="sxs-lookup"><span data-stu-id="d72e8-197">**Calculate interest based on**</span></span> | <span data-ttu-id="d72e8-198">Yüzde</span><span class="sxs-lookup"><span data-stu-id="d72e8-198">Percentage</span></span>      |

<span data-ttu-id="d72e8-199">Aralığı bilgilerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d72e8-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="d72e8-200">**Başlangıç değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-200">**From value**</span></span> | <span data-ttu-id="d72e8-201">**Faiz değeri**</span><span class="sxs-lookup"><span data-stu-id="d72e8-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="d72e8-202">0</span><span class="sxs-lookup"><span data-stu-id="d72e8-202">0</span></span>              | <span data-ttu-id="d72e8-203">1.5</span><span class="sxs-lookup"><span data-stu-id="d72e8-203">1.5</span></span>                |
| <span data-ttu-id="d72e8-204">4</span><span class="sxs-lookup"><span data-stu-id="d72e8-204">4</span></span>              | <span data-ttu-id="d72e8-205">2</span><span class="sxs-lookup"><span data-stu-id="d72e8-205">2</span></span>                  |
| <span data-ttu-id="d72e8-206">7</span><span class="sxs-lookup"><span data-stu-id="d72e8-206">7</span></span>              | <span data-ttu-id="d72e8-207">2.5</span><span class="sxs-lookup"><span data-stu-id="d72e8-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="d72e8-208">Yeni sürümler</span><span class="sxs-lookup"><span data-stu-id="d72e8-208">New versions</span></span>
<span data-ttu-id="d72e8-209">Vade farkı kodlarını yürürlülük tarihi var.</span><span class="sxs-lookup"><span data-stu-id="d72e8-209">Interest codes are date effective.</span></span> <span data-ttu-id="d72e8-210">Faiz oranını değiştirmek isterseniz, ileriki bir tarihte etkili olacak bir **Yeni sürüm** oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="d72e8-211">Farklı sürümleri görüntülemek için, **Tarihli sürüm** menü seçeneğini kesme tarihini seçmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="d72e8-212">Ayrıca sayfadaki tüm vade farkı kodlarını görüntülemek için **Tüm kayıtları görüntüle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d72e8-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



