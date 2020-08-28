---
title: Yevmiye defteri satırlarında satış vergisi hesaplaması
description: Bu konu, yevmiye defteri satırlarında farklı hesap türleri (satıcı, müşteri, genel muhasebe ve proje) için satış vergilerinin nasıl hesaplandığını açıklamaktadır.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 93c9f2bebd038723d50e64bdaa0e0992c003f88d
ms.sourcegitcommit: cec5de2dcfc7210a86a220e308f80ab204f12383
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665854"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="0a4a6-103">Yevmiye defteri satırlarında satış vergisi hesaplaması</span><span class="sxs-lookup"><span data-stu-id="0a4a6-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a4a6-104">Bu konu, yevmiye defteri satırlarında farklı hesap türleri (satıcı, müşteri, genel muhasebe ve proje) için satış vergilerinin nasıl hesaplandığını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="0a4a6-105">Bu işlem üç adıma ayrılabilir:</span><span class="sxs-lookup"><span data-stu-id="0a4a6-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="0a4a6-106">Satış vergisi yönünü belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="0a4a6-107">Geçici bir satış vergisi tablosunda depolanacak satış vergisi tutarını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="0a4a6-108">Fişteki satış vergisi tutarını ve hesabını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="0a4a6-109">Satış vergisi yönünü belirleme</span><span class="sxs-lookup"><span data-stu-id="0a4a6-109">Determine the sales tax direction</span></span>

<span data-ttu-id="0a4a6-110">Satış vergisi yönünü belirleme şekli, fişteki hesabın türüne göre değişir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="0a4a6-111">Satış vergisi yönü, hesap türü ve satış vergisi kodu bileşimine göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="0a4a6-112">Aşağıdaki bölümlerde olasılıklar daha ayrıntılı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="0a4a6-113">Hesap türü Proje'dir</span><span class="sxs-lookup"><span data-stu-id="0a4a6-113">Account type is Project</span></span>

<span data-ttu-id="0a4a6-114">Bir fişte hesap türü **Proje** olan bir günlük satırı varsa, fişteki tüm günlük satırları aynı vergi yönünü uygular.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="0a4a6-115">Aşağıdaki resimde kural gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-115">The following illustration shows the rule.</span></span> <span data-ttu-id="0a4a6-116">Aşağıdaki noktalar, proje hesapları için olası vergi yönlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="0a4a6-117">•   Satış vergisi kodu kullanım vergisi ise, satış vergisi yönü Kullanım Vergisi'dir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="0a4a6-118">•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0a4a6-119">•   Satış vergisi kodu intracom KDV'siyse, satış vergisi yönü Satış Vergisi Borcu'dur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0a4a6-120">•   Satış vergisi kodu ters gider ise, satış vergisi yönü Satış Vergisi Borcu'dur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0a4a6-121">Aksi takdirde, satış vergisi yönü Satış Vergisi Alacağı olur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0a4a6-122">Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-122">The following diagram illustrates the rule graphically.</span></span>

![Proje hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="0a4a6-124">Hesap türü Satıcı'dır</span><span class="sxs-lookup"><span data-stu-id="0a4a6-124">Account type is Vendor</span></span>

<span data-ttu-id="0a4a6-125">Bir fişte hesap türü **Satıcı** olan bir günlük satırı varsa, fişteki tüm günlük satırları aynı vergi yönünü uygular.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="0a4a6-126">Aşağıdaki noktalar, satıcı hesapları için olası vergi yönlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="0a4a6-127">•   Satış vergisi kodu kullanım vergisi ise, satış vergisi yönü Kullanım Vergisi'dir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="0a4a6-128">•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0a4a6-129">•   Satış vergisi kodu intracom KDV'siyse, satış vergisi yönü Satış Vergisi Borcu'dur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0a4a6-130">•   Satış vergisi kodu ters gider ise, satış vergisi yönü Satış Vergisi Borcu'dur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0a4a6-131">Aksi takdirde, satış vergisi yönü Satış Vergisi Alacağı olur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0a4a6-132">Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-132">The following diagram illustrates the rule graphically.</span></span>

![Satıcı hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="0a4a6-134">Hesap türü Müşteri'dir</span><span class="sxs-lookup"><span data-stu-id="0a4a6-134">Account type is Customer</span></span>

<span data-ttu-id="0a4a6-135">Bir fişte hesap türü **Müşteri** olan bir günlük satırı varsa, fişteki tüm günlük satırları aynı vergi yönünü uygular.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="0a4a6-136">Aşağıdaki noktalar, müşteri hesapları için olası vergi yönlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="0a4a6-137">•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0a4a6-138">•   Satış vergisi kodu intracom KDV'siyse, satış vergisi yönü Satış Vergisi Alacağı'dır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0a4a6-139">•   Satış vergisi kodu ters gider ise, satış vergisi yönü Satış Vergisi Alacağı'dır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="0a4a6-140">Aksi takdirde, satış vergisi yönü Satış Vergisi Borcu olur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0a4a6-141">Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-141">The following diagram illustrates the rule graphically.</span></span>

![Müşteri hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="0a4a6-143">Hesap türü Genel Muhasebe'dir</span><span class="sxs-lookup"><span data-stu-id="0a4a6-143">Account type is Ledger</span></span>

<span data-ttu-id="0a4a6-144">Aşağıdaki şekilde, bir fişte yalnızca hesap türü **Genel Muhasebe** olan günlük satırları olduğu zaman uygulanan kural gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="0a4a6-145">Aşağıdaki noktalar genel muhasebe hesapları için olası vergi yönlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="0a4a6-146">•   Satış vergisi kodu kullanım vergisi ise, satış vergisi yönü Kullanım Vergisi'dir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="0a4a6-147">•   Satış vergisi kodu vergiden muaf ise, satış vergisi yönü Vergiden Muaf Satınalma'dır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="0a4a6-148">Aksi takdirde, günlük tutarı borç (pozitif) ise satış vergisi yönü Satış Vergisi Alacağı; günlük tutarı alacak (negatif) ise, satış vergisi yönü Satış Vergisi Borcu olur.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="0a4a6-149">Aşağıdaki diyagramda kural grafik olarak gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-149">The following diagram illustrates the rule graphically.</span></span>

![Genel muhasebe hesapları için vergi yönü olasılıkları](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="0a4a6-151">Satış vergisi yönünü geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="0a4a6-151">Override the sales tax direction</span></span>

<span data-ttu-id="0a4a6-152">Fiş yalnızca hesap türünün **Genel Muhasebe** olduğu satırları içeriyorsa satış vergisi yönünün üzerine yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="0a4a6-153">**Genel muhasebe \> Hesap planı \> Hesaplar \> Ana hesaplar**'a gidin ve **Tüzel varlık geçersiz kılmaları** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="0a4a6-154">Satış vergisi tutarını belirleme</span><span class="sxs-lookup"><span data-stu-id="0a4a6-154">Determine the sales tax amount</span></span>

<span data-ttu-id="0a4a6-155">Bu bölümde, satış vergisi tutar işaretinin nasıl hesaplandığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Satış vergisi hareketleri sayfası](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="0a4a6-157">Aşağıdaki tabloda, geçici satış vergisi tablosundaki satış vergisi tutarlarının işaretini belirlemeye yönelik genel kural gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="0a4a6-158">Günlük satırı tutarı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-158">Journal line amount</span></span> | <span data-ttu-id="0a4a6-159">Satış vergisi yönü</span><span class="sxs-lookup"><span data-stu-id="0a4a6-159">Sales tax direction</span></span>  | <span data-ttu-id="0a4a6-160">Satış vergisi tutar işareti</span><span class="sxs-lookup"><span data-stu-id="0a4a6-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="0a4a6-161">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-161">Positive</span></span>            | <span data-ttu-id="0a4a6-162">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-162">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-163">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-163">Positive</span></span>              |
| <span data-ttu-id="0a4a6-164">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-164">Positive</span></span>            | <span data-ttu-id="0a4a6-165">Satış Vergisi Borcu</span><span class="sxs-lookup"><span data-stu-id="0a4a6-165">Sales Tax Payable</span></span>    | <span data-ttu-id="0a4a6-166">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-166">Negative</span></span>              |
| <span data-ttu-id="0a4a6-167">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-167">Negative</span></span>            | <span data-ttu-id="0a4a6-168">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-168">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-169">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-169">Negative</span></span>              |
| <span data-ttu-id="0a4a6-170">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-170">Negative</span></span>            | <span data-ttu-id="0a4a6-171">Satış Vergisi Borcu</span><span class="sxs-lookup"><span data-stu-id="0a4a6-171">Sales Tax Payable</span></span>    | <span data-ttu-id="0a4a6-172">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-172">Positive</span></span>              |

<span data-ttu-id="0a4a6-173">**Genel muhasebe** satırında bir satış vergisi grubu veya madde satış vergisi grubu seçildiğinde yalnızca **Proje** veya **Genel muhasebe** satırları olan fişler için özel bir kural vardır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="0a4a6-174">Bu kural, yevmiye defterleri için Bağımsız satış vergisi hesaplamasını etkinleştir özelliğiyle kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="0a4a6-175">Bu özellik kapatılınca **Genel muhasebe** satırının vergi tutarı **Proje** satırının borç/alacak yönünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="0a4a6-176">Bu özellik açılınca **Genel muhasebe** satırının vergi tutarı kendi borç/alacak yönünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="0a4a6-177">Aşağıdaki tablolarda her senaryoya ilişkin kural gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="0a4a6-178">**Özellik açıkken uygulanan kural**</span><span class="sxs-lookup"><span data-stu-id="0a4a6-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="0a4a6-179">Projenin günlük satırı tutarı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-179">Journal line amount of project</span></span> | <span data-ttu-id="0a4a6-180">Satış vergisi yönü</span><span class="sxs-lookup"><span data-stu-id="0a4a6-180">Sales tax direction</span></span>  | <span data-ttu-id="0a4a6-181">Satış vergisi tutar işareti</span><span class="sxs-lookup"><span data-stu-id="0a4a6-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="0a4a6-182">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-182">Positive</span></span>                       | <span data-ttu-id="0a4a6-183">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-183">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-184">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-184">Positive</span></span>              |
| <span data-ttu-id="0a4a6-185">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-185">Negative</span></span>                       | <span data-ttu-id="0a4a6-186">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-186">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-187">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-187">Negative</span></span>              |

<span data-ttu-id="0a4a6-188">**Özellik kapalıyken uygulanan kural**</span><span class="sxs-lookup"><span data-stu-id="0a4a6-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="0a4a6-189">Genel muhasebenin günlük satırı tutarı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="0a4a6-190">Satış vergisi yönü</span><span class="sxs-lookup"><span data-stu-id="0a4a6-190">Sales tax direction</span></span>  | <span data-ttu-id="0a4a6-191">Satış vergisi tutar işareti</span><span class="sxs-lookup"><span data-stu-id="0a4a6-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="0a4a6-192">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-192">Positive</span></span>                       | <span data-ttu-id="0a4a6-193">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-193">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-194">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-194">Positive</span></span>              |
| <span data-ttu-id="0a4a6-195">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-195">Negative</span></span>                       | <span data-ttu-id="0a4a6-196">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-196">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-197">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="0a4a6-198">Fişteki satış vergisi tutarını ve hesabını belirleme</span><span class="sxs-lookup"><span data-stu-id="0a4a6-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="0a4a6-199">Satış vergilerini deftere naklettiğinizde, ana hesap, genel muhasebe deftere nakil grubu profilinden alınır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="0a4a6-200">Satış vergileri alacak olduğu zaman, sistem profilde belirtilen Satış Vergisi Alacağı hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="0a4a6-201">Borç olan satış vergileri için, sistem profilde belirtilen Satış Vergisi Borcu hesabını kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="0a4a6-202">Aşağıdaki tabloda genel kural gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0a4a6-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="0a4a6-203">Satış vergisi yönü</span><span class="sxs-lookup"><span data-stu-id="0a4a6-203">Sales tax direction</span></span>  | <span data-ttu-id="0a4a6-204">Satış vergisi tutar işareti</span><span class="sxs-lookup"><span data-stu-id="0a4a6-204">Sales tax amount sign</span></span> | <span data-ttu-id="0a4a6-205">Satış vergisi hesabı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-205">Sales tax account</span></span>      | <span data-ttu-id="0a4a6-206">Fişteki tutar</span><span class="sxs-lookup"><span data-stu-id="0a4a6-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="0a4a6-207">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-207">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-208">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-208">Positive</span></span>              | <span data-ttu-id="0a4a6-209">Vergi Alacak Hesabı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-209">Tax Receivable Account</span></span> | <span data-ttu-id="0a4a6-210">Pozitif (Borç)</span><span class="sxs-lookup"><span data-stu-id="0a4a6-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="0a4a6-211">Satış Vergisi Alacağı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-211">Sales Tax Receivable</span></span> | <span data-ttu-id="0a4a6-212">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-212">Negative</span></span>              | <span data-ttu-id="0a4a6-213">Vergi Alacak Hesabı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-213">Tax Receivable Account</span></span> | <span data-ttu-id="0a4a6-214">Negatif (Alacak)</span><span class="sxs-lookup"><span data-stu-id="0a4a6-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="0a4a6-215">Satış Vergisi Borcu</span><span class="sxs-lookup"><span data-stu-id="0a4a6-215">Sales Tax Payable</span></span>    | <span data-ttu-id="0a4a6-216">Pozitif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-216">Positive</span></span>              | <span data-ttu-id="0a4a6-217">Vergi Borç Hesabı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-217">Tax Payable Account</span></span>    | <span data-ttu-id="0a4a6-218">Negatif (Alacak)</span><span class="sxs-lookup"><span data-stu-id="0a4a6-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="0a4a6-219">Satış Vergisi Borcu</span><span class="sxs-lookup"><span data-stu-id="0a4a6-219">Sales Tax Payable</span></span>    | <span data-ttu-id="0a4a6-220">Negatif</span><span class="sxs-lookup"><span data-stu-id="0a4a6-220">Negative</span></span>              | <span data-ttu-id="0a4a6-221">Vergi Borç Hesabı</span><span class="sxs-lookup"><span data-stu-id="0a4a6-221">Tax Payable Account</span></span>    | <span data-ttu-id="0a4a6-222">Pozitif (Borç)</span><span class="sxs-lookup"><span data-stu-id="0a4a6-222">Positive (Debit)</span></span>  |
