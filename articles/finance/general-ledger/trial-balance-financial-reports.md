---
title: Mizan mali raporları
description: Bu makalede, mizanlar için varsayılan raporlar açıklanmaktadır. Ayrıca, bu raporlarla ilgili yapı taşları ve raporların iş gereksinimlerinize uyacak şekilde nasıl değiştirileceği açıklanmaktadır.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103670"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="057d0-104">Mizan mali raporları</span><span class="sxs-lookup"><span data-stu-id="057d0-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="057d0-105">Bu makalede, mizanlar için varsayılan raporlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="057d0-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="057d0-106">Ayrıca, bu raporlarla ilgili yapı taşları ve raporların iş gereksinimlerinize uyacak şekilde nasıl değiştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="057d0-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="057d0-107">Varsayılan mizan raporları</span><span class="sxs-lookup"><span data-stu-id="057d0-107">Default trial balance reports</span></span>

<span data-ttu-id="057d0-108">Mali raporlama için üç mizan raporu kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="057d0-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="057d0-109">Varsayılan rapor</span><span class="sxs-lookup"><span data-stu-id="057d0-109">Default report</span></span>                                 | <span data-ttu-id="057d0-110">Ne yapar</span><span class="sxs-lookup"><span data-stu-id="057d0-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="057d0-111">Ayrıntılı Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="057d0-112">Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bunların net değerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="057d0-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="057d0-113">Özet Mizan – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="057d0-114">Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="057d0-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="057d0-115">Özet Mizan Yıl Yıl – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="057d0-116">Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve bu yıl ve geçen yıl için net farklarıyla birlikte borç ve alacak bakiyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="057d0-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="057d0-117">Yapı taşları</span><span class="sxs-lookup"><span data-stu-id="057d0-117">Building blocks</span></span>
<span data-ttu-id="057d0-118">Mizan mali raporları aşağıdaki yapı taşlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="057d0-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="057d0-119">Varsayılan rapor</span><span class="sxs-lookup"><span data-stu-id="057d0-119">Default report</span></span>                                 | <span data-ttu-id="057d0-120">Satır tanımı</span><span class="sxs-lookup"><span data-stu-id="057d0-120">Row definition</span></span>          | <span data-ttu-id="057d0-121">Sütun tanımı</span><span class="sxs-lookup"><span data-stu-id="057d0-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="057d0-122">Ayrıntılı Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="057d0-123">Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-123">Trial Balance - Default</span></span> | <span data-ttu-id="057d0-124">Ayrıntılı Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="057d0-125">Özet Mizan – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="057d0-126">Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-126">Trial Balance - Default</span></span> | <span data-ttu-id="057d0-127">Özet Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="057d0-128">Özet Mizan Yıl Yıl – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="057d0-129">Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-129">Trial Balance - Default</span></span> | <span data-ttu-id="057d0-130">Özet Mizan Yıl Yıl - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="057d0-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="057d0-131">Mali raporlamada **Mizan** raporunu çalıştırırken **Tutarsız satırları görüntüle** ve **Ayarlar** sekmesinde **etkin satır olmayan raporları görüntüle** onay kutularını seçtiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="057d0-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="057d0-132">Satır tanımı</span><span class="sxs-lookup"><span data-stu-id="057d0-132">Row definition</span></span>

<span data-ttu-id="057d0-133">Satır tanımı, Mizan – Varsayılan, tüm ana hesaplardan veri çeken tek bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="057d0-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="057d0-134">Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan rapor oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="057d0-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="057d0-135">Raporu görüntülediğinizde, her bir hesap hakkında ayrıntılı bilgileri görmek için tek bir satıra bakarsınız.</span><span class="sxs-lookup"><span data-stu-id="057d0-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="057d0-136">Satır tanımını daha fazla ayrıntı içerecek şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="057d0-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="057d0-137">Mizan – Varsayılan satır tanımını tüm hesaplar için satırları içerecek şekilde değiştirmek için, bu adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="057d0-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="057d0-138">**Düzenle** öğesini ve ardından **Boyutlardan Satır Ekle** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="057d0-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="057d0-139">**Boyutlardan Satır Ekle** komutu, satır tanımınızda olmasını istediğiniz boyutları seçmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="057d0-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="057d0-140">Bu satır tanımı için **Ana Hesap** kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="057d0-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="057d0-141">**Ana Hesabın** tüm işaretleri içerdiğinden emin olun ve ardından **Tamam** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="057d0-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="057d0-142">Satır tanımı şimdi varsayılan tüzel kişiliğiniz için tüm ana hesapları içermektedir.</span><span class="sxs-lookup"><span data-stu-id="057d0-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="057d0-143">Sütun tanımı</span><span class="sxs-lookup"><span data-stu-id="057d0-143">Column definition</span></span>

<span data-ttu-id="057d0-144">Her bir mizan raporunu farklı bir sütun tanımı kullanır.</span><span class="sxs-lookup"><span data-stu-id="057d0-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="057d0-145">Bu sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.</span><span class="sxs-lookup"><span data-stu-id="057d0-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="057d0-146">**Ayrıntılı Mizan – Varsayılan sütun türleri:**</span><span class="sxs-lookup"><span data-stu-id="057d0-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="057d0-147">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="057d0-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="057d0-148">**ACCT** – Hesap kodları</span><span class="sxs-lookup"><span data-stu-id="057d0-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="057d0-149">**ATTR (3)** – Öznitelikler:</span><span class="sxs-lookup"><span data-stu-id="057d0-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="057d0-150">Hareket Tarihi</span><span class="sxs-lookup"><span data-stu-id="057d0-150">Transaction Date</span></span>
        -   <span data-ttu-id="057d0-151">Fiş</span><span class="sxs-lookup"><span data-stu-id="057d0-151">Voucher</span></span>
        -   <span data-ttu-id="057d0-152">Günlük Tanımı</span><span class="sxs-lookup"><span data-stu-id="057d0-152">Journal Description</span></span>
    -   <span data-ttu-id="057d0-153">**FD** – Yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="057d0-154">**FD** – Yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="057d0-155">**CALC** – Net fark</span><span class="sxs-lookup"><span data-stu-id="057d0-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="057d0-156">**Özet Mizan – Varsayılan sütun türleri:**</span><span class="sxs-lookup"><span data-stu-id="057d0-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="057d0-157">**ACCT** – Hesap kodları</span><span class="sxs-lookup"><span data-stu-id="057d0-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="057d0-158">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="057d0-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="057d0-159">**ATTR** – Öznitelik:</span><span class="sxs-lookup"><span data-stu-id="057d0-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="057d0-160">Fiş</span><span class="sxs-lookup"><span data-stu-id="057d0-160">Voucher</span></span>
    -   <span data-ttu-id="057d0-161">**FD** – Başlangıç bakiyesi mali verileri</span><span class="sxs-lookup"><span data-stu-id="057d0-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="057d0-162">**FD** – Yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="057d0-163">**FD** – Yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="057d0-164">**CALC** – Net fark</span><span class="sxs-lookup"><span data-stu-id="057d0-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="057d0-165">**CALC** – Kapanış bakiyesi</span><span class="sxs-lookup"><span data-stu-id="057d0-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="057d0-166">**Özet Mizan Yıl Yıl – Varsayılan:**</span><span class="sxs-lookup"><span data-stu-id="057d0-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="057d0-167">**ACCT** – Hesap kodları</span><span class="sxs-lookup"><span data-stu-id="057d0-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="057d0-168">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="057d0-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="057d0-169">**ATTR** – Bir öznitelik</span><span class="sxs-lookup"><span data-stu-id="057d0-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="057d0-170">Fiş</span><span class="sxs-lookup"><span data-stu-id="057d0-170">Voucher</span></span>
    -   <span data-ttu-id="057d0-171">**FD** – Mevcut yıl için başlangıç bakiyesi mali verileri</span><span class="sxs-lookup"><span data-stu-id="057d0-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="057d0-172">**FD** – Geçerli yıl için yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="057d0-173">**FD** – Geçerli yıl için yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="057d0-174">**CALC** – Net fark</span><span class="sxs-lookup"><span data-stu-id="057d0-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="057d0-175">**CALC** – Kapanış bakiyesi</span><span class="sxs-lookup"><span data-stu-id="057d0-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="057d0-176">**FD** – Geçen yıl için yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="057d0-177">**FD** – Geçen yıl için yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="057d0-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="057d0-178">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="057d0-178">Additional resources</span></span>

[<span data-ttu-id="057d0-179">Mali raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="057d0-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="057d0-180">Mali raporları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="057d0-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="057d0-181">Dynamics Mali Raporlama Blogu</span><span class="sxs-lookup"><span data-stu-id="057d0-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
