---
title: Bir vade farkı kodu için vade farkı oranları ayarlama
description: Vade farkı kodları, faizin nasıl belirleneceğini ve ödemesi geciken hesaplarda nasıl hesaplanacağını belirleyen ayarlar içerir.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc986ea752d1482f618401058f7a0b18f13efd5f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188722"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="85a23-103">Bir vade farkı kodu için vade farkı oranları ayarlama</span><span class="sxs-lookup"><span data-stu-id="85a23-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85a23-104">Vade farkı kodları, faizin nasıl belirleneceğini ve ödemesi geciken hesaplarda nasıl hesaplanacağını belirleyen ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="85a23-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="85a23-105">Bir tek faiz kodu ayarlayabilir ve birden fazla müşteri deftere nakil profilleri, faturalama kodları veya belirli fatura satırlarına uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="85a23-106">Faiz kodu ayrıntıları değiştiğinde, bu kodu kullanan tüm özellikler değişiklikleri yeni hareketlere otomatik olarak uygular.</span><span class="sxs-lookup"><span data-stu-id="85a23-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="85a23-107">Her faiz kodu için iki tür oran ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="85a23-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="85a23-108">Faiz gelirleri için oranlar − Bunlar faturalardaki veya vade farkı dekontlarının faizini borçlandırmadan kazanılan geliri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="85a23-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="85a23-109">Faiz ödemeleri için oranlar − Bunlar alacak dekontları üzerindeki faiz için ödenen maliyeti temsil eder.</span><span class="sxs-lookup"><span data-stu-id="85a23-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="85a23-110">Bu oran türlerinin her ikisi de aynı anda ve aynı vade farkı kodu içinde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="85a23-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="85a23-111">Faiz oranları üç hesaplama türüne bağlı olabilir:</span><span class="sxs-lookup"><span data-stu-id="85a23-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="85a23-112">Yüzdeye göre vade farkı.</span><span class="sxs-lookup"><span data-stu-id="85a23-112">Interest by percentage.</span></span>
-   <span data-ttu-id="85a23-113">Tutara göre vade farkı.</span><span class="sxs-lookup"><span data-stu-id="85a23-113">Interest by amount.</span></span>
-   <span data-ttu-id="85a23-114">Tek bir yüzde veya tutar ile sonuçlanan, aralığa göre vade farkı.</span><span class="sxs-lookup"><span data-stu-id="85a23-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="85a23-115">Bir vade farkı kodu, faizi hesaplamak için kullanıldığında, ödemenin hareket vade tarihini geçtiği süre boyunca etkin olan her vade farkı oranı için ayrı bir vade farkı dekontu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="85a23-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="85a23-116">**Vade farkı kodu** sayfası üzerindeki **Kazançlar** sekmesini kullanıp, faiz alarak edindiğiniz gelirler için vade farkı oranlarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="85a23-117">**Ödemeler** sekmesini kullanıp ödediğiniz vade farkı için vade farkı oranlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="85a23-118">Yüzdeye dayalı vade farkı oranları</span><span class="sxs-lookup"><span data-stu-id="85a23-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="85a23-119">Belirli bir yüzdeyi hesaplayan vade farkı oranlarını ayarlayabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="85a23-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="85a23-120">Vade farkı tutarı tüm para birimleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="85a23-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="85a23-121">İsteğe bağlı vade farkı tutar limitleri girilebilir.</span><span class="sxs-lookup"><span data-stu-id="85a23-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="85a23-122">**Faiz kodlarını ayarla** sayfasındaki **Faiz farklarının dayanağı** alanındaki **Yüzde** seçilidir.</span><span class="sxs-lookup"><span data-stu-id="85a23-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="85a23-123">Örneğin, fatura ödemesinin hareket vade tarihini geçtiği her iki ay için yüzde 5 vade farkı koyan vade farkı kodunu ayarlamak için **Her biri için faiz hesapla** alanına 2 girer ve **Ay**'ı seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="85a23-124">Vade farkı dekontu hesaplamasına yönelik yeni algoritma Özellik Yönetimi kullanılarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="85a23-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="85a23-125">Bu algoritmayı kullanmak için, **(GBL) yıllık yüzdenin 365'e bölündüğü günlük faizi hesaplamaya izin ver** özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="85a23-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="85a23-126">Özelliği etkinleştirme hakkında bilgi için [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın.</span><span class="sxs-lookup"><span data-stu-id="85a23-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="85a23-127">Vade farkı dekontu tutarına ait hesaplama formülü:</span><span class="sxs-lookup"><span data-stu-id="85a23-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="85a23-128">Vade farkı dekontu tutarı = Borç tutarı \* yıllık faiz % /365 \* gecikilen gün sayısı</span><span class="sxs-lookup"><span data-stu-id="85a23-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="85a23-129">Bu özellik 10.0.18 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="85a23-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="85a23-130">Tutarları temel alan faiz oranları</span><span class="sxs-lookup"><span data-stu-id="85a23-130">Interest rates based on amounts</span></span>
<span data-ttu-id="85a23-131">Belirli bir para birimine göre tutarı hesaplayan vade farkı oranlarını ayarlayabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="85a23-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="85a23-132">Vade farkı kodu içindeki her para birimi için vade farkı tutarı belirtilir.</span><span class="sxs-lookup"><span data-stu-id="85a23-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="85a23-133">İsteğe bağlı vade farkı tutar limitleri girilebilir.</span><span class="sxs-lookup"><span data-stu-id="85a23-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="85a23-134">**Vade farkı kodlarını ayarla** sayfasındaki **Vade farklarının dayanağı** alanındaki **Tutar** seçilidir.</span><span class="sxs-lookup"><span data-stu-id="85a23-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="85a23-135">Örneğin, fatura ödemesinin hareket vade tarihini geçtiği her 20 gün için yüzde 25,00 vade farkı koyan vade farkı kodunu ayarlamak için **Her biri için faiz hesapla** alanında 20 girer ve **Gün**'ü seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="85a23-136">Aralıkları temel alan faiz oranları</span><span class="sxs-lookup"><span data-stu-id="85a23-136">Interest rates based on ranges</span></span>
<span data-ttu-id="85a23-137">Geçmiş tutar, tutarın geç kaldığı gün sayısı veya tutarın geç kaldığı ay sayısına bağlı olarak değişen vade farkı oranları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="85a23-138">**Para birimine göre kazanç** sekmesini kullanarak her para birimi için belirli vade farkı ayarları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="85a23-139">Ayrıca aralığı da buradan tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="85a23-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="85a23-140">**Aralıklar** butonunu ayarlamak istediğiniz aralıkları temsil eden satırlar eklemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="85a23-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="85a23-141">**Gelen** değeri aralığın başlangıcını temsil eder ve **Vade farkı değeri** numarası **Vade farkı kodlarını ayarlamak** sayfasının **Vade farklarının dayanağı** alanındaki yüzde veya tutar seçimine bağlı olarak bir yüzdeyi veya tutarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="85a23-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="85a23-142">Örnek 1: Aralığa göre vade farkı = Tutar</span><span class="sxs-lookup"><span data-stu-id="85a23-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="85a23-143">Faturanın ödemesinin hareket vade tarihini aştığını her üç ayda bir değerlendirecek bir vade farkı kodu ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="85a23-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="85a23-144">Hesaplamayı, adımlı tutar aralıklarına göre, bir yüzde vade farkı değerine dayandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="85a23-145">Faiz değeri 1.000,00 olan faturalara kadar yüzde 1, 1.001,00'den 5.000,00 olanlara kadar yüzde 2 ve 5.000,00'den büyük olanlar için yüzde üç olacaktır.</span><span class="sxs-lookup"><span data-stu-id="85a23-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="85a23-146">Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="85a23-147">**Alan adı**</span><span class="sxs-lookup"><span data-stu-id="85a23-147">**Field name**</span></span>                  | <span data-ttu-id="85a23-148">**Alan değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="85a23-149">**Vade farkı kodu**</span><span class="sxs-lookup"><span data-stu-id="85a23-149">**Interest code**</span></span>               | <span data-ttu-id="85a23-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="85a23-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="85a23-151">**Her biri için faizi hesapla:**</span><span class="sxs-lookup"><span data-stu-id="85a23-151">**Calculate interest every**</span></span>    | <span data-ttu-id="85a23-152">3/Ay</span><span class="sxs-lookup"><span data-stu-id="85a23-152">3/Month</span></span>         |
| <span data-ttu-id="85a23-153">**Aralığa göre faiz**</span><span class="sxs-lookup"><span data-stu-id="85a23-153">**Interest by range**</span></span>           | <span data-ttu-id="85a23-154">Tutar</span><span class="sxs-lookup"><span data-stu-id="85a23-154">Amount</span></span>          |
| <span data-ttu-id="85a23-155">**Vade farkını şuna göre hesapla**</span><span class="sxs-lookup"><span data-stu-id="85a23-155">**Calculate interest based on**</span></span> | <span data-ttu-id="85a23-156">Yüzde</span><span class="sxs-lookup"><span data-stu-id="85a23-156">Percentage</span></span>      |

<span data-ttu-id="85a23-157">Aralığı bilgilerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="85a23-158">**Başlangıç değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-158">**From value**</span></span> | <span data-ttu-id="85a23-159">**Faiz değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="85a23-160">0</span><span class="sxs-lookup"><span data-stu-id="85a23-160">0</span></span>              | <span data-ttu-id="85a23-161">1</span><span class="sxs-lookup"><span data-stu-id="85a23-161">1</span></span>                  |
| <span data-ttu-id="85a23-162">1,001</span><span class="sxs-lookup"><span data-stu-id="85a23-162">1,001</span></span>          | <span data-ttu-id="85a23-163">2</span><span class="sxs-lookup"><span data-stu-id="85a23-163">2</span></span>                  |
| <span data-ttu-id="85a23-164">5,001</span><span class="sxs-lookup"><span data-stu-id="85a23-164">5,001</span></span>          | <span data-ttu-id="85a23-165">3</span><span class="sxs-lookup"><span data-stu-id="85a23-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="85a23-166">Örnek 2: Aralığa göre faiz = Gün</span><span class="sxs-lookup"><span data-stu-id="85a23-166">Example 2: Interest by range = Days</span></span>

<span data-ttu-id="85a23-167">Faturanın ödemesinin hareket vade tarihini aştığını her 15 günde bir değerlendirecek bir vade farkı kodu ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="85a23-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="85a23-168">Hesaplamayı, adımlı gün aralıklarına göre, bir tutar vade farkı değerine dayandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="85a23-169">Vade farkı değeri ilk 60 gün içinde 15 günlük 10,00, 61 ve 90. günler arasında 15 günlük 15,00 ve 91 gün ve daha fazlası için her 15 günlük 20,00 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="85a23-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="85a23-170">Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="85a23-171">**Alan adı**</span><span class="sxs-lookup"><span data-stu-id="85a23-171">**Field name**</span></span>                  | <span data-ttu-id="85a23-172">**Alan değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="85a23-173">**Vade farkı kodu**</span><span class="sxs-lookup"><span data-stu-id="85a23-173">**Interest code**</span></span>               | <span data-ttu-id="85a23-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="85a23-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="85a23-175">**Her biri için faizi hesapla:**</span><span class="sxs-lookup"><span data-stu-id="85a23-175">**Calculate interest every**</span></span>    | <span data-ttu-id="85a23-176">15/Gün</span><span class="sxs-lookup"><span data-stu-id="85a23-176">15/Day</span></span>          |
| <span data-ttu-id="85a23-177">**Aralığa göre faiz**</span><span class="sxs-lookup"><span data-stu-id="85a23-177">**Interest by range**</span></span>           | <span data-ttu-id="85a23-178">Gün</span><span class="sxs-lookup"><span data-stu-id="85a23-178">Days</span></span>            |
| <span data-ttu-id="85a23-179">**Vade farkını şuna göre hesapla**</span><span class="sxs-lookup"><span data-stu-id="85a23-179">**Calculate interest based on**</span></span> | <span data-ttu-id="85a23-180">Tutar</span><span class="sxs-lookup"><span data-stu-id="85a23-180">Amount</span></span>          |

<span data-ttu-id="85a23-181">Aralığı bilgilerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="85a23-182">**Başlangıç değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-182">**From value**</span></span> | <span data-ttu-id="85a23-183">**Faiz değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="85a23-184">0</span><span class="sxs-lookup"><span data-stu-id="85a23-184">0</span></span>              | <span data-ttu-id="85a23-185">10</span><span class="sxs-lookup"><span data-stu-id="85a23-185">10</span></span>                 |
| <span data-ttu-id="85a23-186">61</span><span class="sxs-lookup"><span data-stu-id="85a23-186">61</span></span>             | <span data-ttu-id="85a23-187">15</span><span class="sxs-lookup"><span data-stu-id="85a23-187">15</span></span>                 |
| <span data-ttu-id="85a23-188">91</span><span class="sxs-lookup"><span data-stu-id="85a23-188">91</span></span>             | <span data-ttu-id="85a23-189">20</span><span class="sxs-lookup"><span data-stu-id="85a23-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="85a23-190">Örnek 3: Aralığa göre faiz = Ay</span><span class="sxs-lookup"><span data-stu-id="85a23-190">Example 3: Interest by range = Months</span></span>

<span data-ttu-id="85a23-191">Faturanın ödemesinin hareket vade tarihini aştığını her ayda bir değerlendirecek bir vade farkı kodu ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="85a23-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="85a23-192">Hesaplamayı, adımlı aylık aralıklarına göre, bir yüzde vade farkı değerine dayandırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="85a23-193">Varde farkı değer, vadenin geçtiği ilk üç ay için her aylık yüzde 1,5, ikinci üç aylık dönem için aylık yüzde 2,0 ve ilk altı aydan sonraki her ay için yüzde 2,5 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="85a23-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="85a23-194">Vade farkı kodu alan değerlerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="85a23-195">**Alan adı**</span><span class="sxs-lookup"><span data-stu-id="85a23-195">**Field name**</span></span>                  | <span data-ttu-id="85a23-196">**Alan değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="85a23-197">**Vade farkı kodu**</span><span class="sxs-lookup"><span data-stu-id="85a23-197">**Interest code**</span></span>               | <span data-ttu-id="85a23-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="85a23-198">1M%ByMth</span></span>        |
| <span data-ttu-id="85a23-199">**Her biri için faizi hesapla:**</span><span class="sxs-lookup"><span data-stu-id="85a23-199">**Calculate interest every**</span></span>    | <span data-ttu-id="85a23-200">1/Ay</span><span class="sxs-lookup"><span data-stu-id="85a23-200">1/Month</span></span>         |
| <span data-ttu-id="85a23-201">**Aralığa göre faiz**</span><span class="sxs-lookup"><span data-stu-id="85a23-201">**Interest by range**</span></span>           | <span data-ttu-id="85a23-202">Ay</span><span class="sxs-lookup"><span data-stu-id="85a23-202">Months</span></span>          |
| <span data-ttu-id="85a23-203">**Vade farkını şuna göre hesapla**</span><span class="sxs-lookup"><span data-stu-id="85a23-203">**Calculate interest based on**</span></span> | <span data-ttu-id="85a23-204">Yüzde</span><span class="sxs-lookup"><span data-stu-id="85a23-204">Percentage</span></span>      |

<span data-ttu-id="85a23-205">Aralığı bilgilerini aşağıdaki gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85a23-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="85a23-206">**Başlangıç değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-206">**From value**</span></span> | <span data-ttu-id="85a23-207">**Faiz değeri**</span><span class="sxs-lookup"><span data-stu-id="85a23-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="85a23-208">0</span><span class="sxs-lookup"><span data-stu-id="85a23-208">0</span></span>              | <span data-ttu-id="85a23-209">1.5</span><span class="sxs-lookup"><span data-stu-id="85a23-209">1.5</span></span>                |
| <span data-ttu-id="85a23-210">4</span><span class="sxs-lookup"><span data-stu-id="85a23-210">4</span></span>              | <span data-ttu-id="85a23-211">2</span><span class="sxs-lookup"><span data-stu-id="85a23-211">2</span></span>                  |
| <span data-ttu-id="85a23-212">7</span><span class="sxs-lookup"><span data-stu-id="85a23-212">7</span></span>              | <span data-ttu-id="85a23-213">2.5</span><span class="sxs-lookup"><span data-stu-id="85a23-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="85a23-214">Yeni sürümler</span><span class="sxs-lookup"><span data-stu-id="85a23-214">New versions</span></span>
<span data-ttu-id="85a23-215">Vade farkı kodlarını yürürlülük tarihi var.</span><span class="sxs-lookup"><span data-stu-id="85a23-215">Interest codes are date effective.</span></span> <span data-ttu-id="85a23-216">Faiz oranını değiştirmek isterseniz, ileriki bir tarihte etkili olacak bir **Yeni sürüm** oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="85a23-217">Farklı sürümleri görüntülemek için, **Tarihli sürüm** menü seçeneğini kesme tarihini seçmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="85a23-218">Ayrıca sayfadaki tüm vade farkı kodlarını görüntülemek için **Tüm kayıtları görüntüle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="85a23-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
