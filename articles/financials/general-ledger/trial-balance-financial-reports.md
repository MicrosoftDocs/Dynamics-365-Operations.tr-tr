---
title: "Mizan mali raporları"
description: "Bu makalede, mizanlar için varsayılan raporlar açıklanmaktadır. Ayrıca, bu raporlarla ilgili yapı taşları ve raporların iş gereksinimlerinize uyacak şekilde nasıl değiştirileceği açıklanmaktadır."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6405599186c8d07ac5ade19d3b7d27ae83b036ff
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="a5015-104">Mizan mali raporları</span><span class="sxs-lookup"><span data-stu-id="a5015-104">Trial balance financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a5015-105">Bu makalede, mizanlar için varsayılan raporlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a5015-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="a5015-106">Ayrıca, bu raporlarla ilgili yapı taşları ve raporların iş gereksinimlerinize uyacak şekilde nasıl değiştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a5015-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="a5015-107">Varsayılan mizan raporları</span><span class="sxs-lookup"><span data-stu-id="a5015-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="a5015-108">Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümündeki Mali raporlamada üç mizan raporu bulunur.</span><span class="sxs-lookup"><span data-stu-id="a5015-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

| <span data-ttu-id="a5015-109">Varsayılan rapor</span><span class="sxs-lookup"><span data-stu-id="a5015-109">Default report</span></span>                                 | <span data-ttu-id="a5015-110">Ne yapar</span><span class="sxs-lookup"><span data-stu-id="a5015-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5015-111">Ayrıntılı Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="a5015-112">Borç ve alacak bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve hareket tarihi, fiş ve günlük açıklamasıyla birlikte bunların net değerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5015-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="a5015-113">Özet Mizan – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="a5015-114">Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve net farklarıyla birlikte borç ve alacak bakiyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5015-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="a5015-115">Özet Mizan Yıl Yıl – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="a5015-116">Açılış ve kapanış bakiyeleri olan tüm hesaplar için bakiye bilgilerini ve bu yıl ve geçen yıl için net farklarıyla birlikte borç ve alacak bakiyelerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5015-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="a5015-117">Yapı taşları</span><span class="sxs-lookup"><span data-stu-id="a5015-117">Building blocks</span></span>
<span data-ttu-id="a5015-118">Mizan mali raporları aşağıdaki yapı taşlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="a5015-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="a5015-119">Varsayılan rapor</span><span class="sxs-lookup"><span data-stu-id="a5015-119">Default report</span></span>                                 | <span data-ttu-id="a5015-120">Satır tanımı</span><span class="sxs-lookup"><span data-stu-id="a5015-120">Row definition</span></span>          | <span data-ttu-id="a5015-121">Sütun tanımı</span><span class="sxs-lookup"><span data-stu-id="a5015-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="a5015-122">Ayrıntılı Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="a5015-123">Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-123">Trial Balance - Default</span></span> | <span data-ttu-id="a5015-124">Ayrıntılı Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="a5015-125">Özet Mizan – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="a5015-126">Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-126">Trial Balance - Default</span></span> | <span data-ttu-id="a5015-127">Özet Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="a5015-128">Özet Mizan Yıl Yıl – Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="a5015-129">Mizan - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-129">Trial Balance - Default</span></span> | <span data-ttu-id="a5015-130">Özet Mizan Yıl Yıl - Varsayılan</span><span class="sxs-lookup"><span data-stu-id="a5015-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="a5015-131">Satır tanımı</span><span class="sxs-lookup"><span data-stu-id="a5015-131">Row definition</span></span>

<span data-ttu-id="a5015-132">Satır tanımı, Mizan – Varsayılan, tüm ana hesaplardan veri çeken tek bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="a5015-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="a5015-133">Bu nedenle, herhangi biri hiçbir değişiklik yapmasına gerek kalmadan rapor oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="a5015-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="a5015-134">Raporu görüntülediğinizde, her bir hesap hakkında ayrıntılı bilgileri görmek için tek bir satıra bakarsınız.</span><span class="sxs-lookup"><span data-stu-id="a5015-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="a5015-135">Satır tanımını daha fazla ayrıntı içerecek şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5015-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="a5015-136">Mizan – Varsayılan satır tanımını tüm hesaplar için satırları içerecek şekilde değiştirmek için, bu adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="a5015-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="a5015-137">**Düzenle** öğesini ve ardından **Boyutlardan Satır Ekle** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5015-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="a5015-138">**Boyutlardan Satır Ekle** komutu, satır tanımınızda olmasını istediğiniz boyutları seçmenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="a5015-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="a5015-139">Bu satır tanımı için **Ana Hesap** kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a5015-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="a5015-140">**Ana Hesabın** tüm işaretleri içerdiğinden emin olun ve ardından **Tamam** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5015-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="a5015-141">Satır tanımı şimdi varsayılan tüzel kişiliğiniz için tüm ana hesapları içermektedir.</span><span class="sxs-lookup"><span data-stu-id="a5015-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="a5015-142">Sütun tanımı</span><span class="sxs-lookup"><span data-stu-id="a5015-142">Column definition</span></span>

<span data-ttu-id="a5015-143">Her bir mizan raporunu farklı bir sütun tanımı kullanır.</span><span class="sxs-lookup"><span data-stu-id="a5015-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="a5015-144">Bu sütun tanımları, farklı ayrıntı ve mali veri düzeyleri sunmak üzere farklı türlerde sütunlar içerir.</span><span class="sxs-lookup"><span data-stu-id="a5015-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="a5015-145">**Ayrıntılı Mizan – Varsayılan sütun türleri:**</span><span class="sxs-lookup"><span data-stu-id="a5015-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="a5015-146">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="a5015-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a5015-147">**ACCT** – Hesap kodları</span><span class="sxs-lookup"><span data-stu-id="a5015-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="a5015-148">**ATTR (3)** – Öznitelikler:</span><span class="sxs-lookup"><span data-stu-id="a5015-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="a5015-149">Hareket Tarihi</span><span class="sxs-lookup"><span data-stu-id="a5015-149">Transaction Date</span></span>
        -   <span data-ttu-id="a5015-150">Fiş</span><span class="sxs-lookup"><span data-stu-id="a5015-150">Voucher</span></span>
        -   <span data-ttu-id="a5015-151">Günlük Tanımı</span><span class="sxs-lookup"><span data-stu-id="a5015-151">Journal Description</span></span>
    -   <span data-ttu-id="a5015-152">**FD** – Yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="a5015-153">**FD** – Yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="a5015-154">**CALC** – Net fark</span><span class="sxs-lookup"><span data-stu-id="a5015-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="a5015-155">**Özet Mizan – Varsayılan sütun türleri:**</span><span class="sxs-lookup"><span data-stu-id="a5015-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="a5015-156">**ACCT** – Hesap kodları</span><span class="sxs-lookup"><span data-stu-id="a5015-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="a5015-157">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="a5015-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a5015-158">**ATTR** – Öznitelik:</span><span class="sxs-lookup"><span data-stu-id="a5015-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="a5015-159">Fiş</span><span class="sxs-lookup"><span data-stu-id="a5015-159">Voucher</span></span>
    -   <span data-ttu-id="a5015-160">**FD** – Başlangıç bakiyesi mali verileri</span><span class="sxs-lookup"><span data-stu-id="a5015-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="a5015-161">**FD** – Yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="a5015-162">**FD** – Yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="a5015-163">**CALC** – Net fark</span><span class="sxs-lookup"><span data-stu-id="a5015-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="a5015-164">**CALC** – Kapanış bakiyesi</span><span class="sxs-lookup"><span data-stu-id="a5015-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="a5015-165">**Özet Mizan Yıl Yıl – Varsayılan:**</span><span class="sxs-lookup"><span data-stu-id="a5015-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="a5015-166">**ACCT** – Hesap kodları</span><span class="sxs-lookup"><span data-stu-id="a5015-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="a5015-167">**DESC** – Satır tanımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="a5015-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a5015-168">**ATTR** – Bir öznitelik</span><span class="sxs-lookup"><span data-stu-id="a5015-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="a5015-169">Fiş</span><span class="sxs-lookup"><span data-stu-id="a5015-169">Voucher</span></span>
    -   <span data-ttu-id="a5015-170">**FD** – Mevcut yıl için başlangıç bakiyesi mali verileri</span><span class="sxs-lookup"><span data-stu-id="a5015-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="a5015-171">**FD** – Geçerli yıl için yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="a5015-172">**FD** – Geçerli yıl için yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="a5015-173">**CALC** – Net fark</span><span class="sxs-lookup"><span data-stu-id="a5015-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="a5015-174">**CALC** – Kapanış bakiyesi</span><span class="sxs-lookup"><span data-stu-id="a5015-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="a5015-175">**FD** – Geçen yıl için yalnızca borçları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="a5015-176">**FD** – Geçen yıl için yalnızca alacakları içeren mali veriler</span><span class="sxs-lookup"><span data-stu-id="a5015-176">**FD** – Financial data that contains only credits for the last year</span></span>

 

<a name="see-also"></a><span data-ttu-id="a5015-177">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a5015-177">See also</span></span>
--------

[<span data-ttu-id="a5015-178">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="a5015-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="a5015-179">Mali raporları görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a5015-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="a5015-180">Dynamics Mali Raporlama Blogu</span><span class="sxs-lookup"><span data-stu-id="a5015-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




