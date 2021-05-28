---
title: Yıl sonu kapanışında eksik açılış bakiyeleri
description: Bu konuda, bir yılı kapatırken açılış bakiyelerin neden eksik olabileceği ve eksik olduklarında bu bakiyelerin nasıl yeniden oluşturulacağı açıklanmaktadır.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028591"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="bc3f4-103">Yıl sonu kapanışında eksik açılış bakiyeleri</span><span class="sxs-lookup"><span data-stu-id="bc3f4-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc3f4-104">Bu konuda, bir yılı kapatırken açılış bakiyelerin neden eksik olabileceği ve eksik olduklarında bu bakiyelerin nasıl yeniden oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="bc3f4-105">Belirti</span><span class="sxs-lookup"><span data-stu-id="bc3f4-105">Symptom</span></span>

<span data-ttu-id="bc3f4-106">Genel muhasebe yıl sonu kapanışını çalıştırdıktan sonra neden hiç başlangıç bakiyesi yok?</span><span class="sxs-lookup"><span data-stu-id="bc3f4-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="bc3f4-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="bc3f4-107">Resolution</span></span>

<span data-ttu-id="bc3f4-108">Genel muhasebede bir yılı kapattıysanız ve ardından sonraki mali yıl için açılış bakiyelerini görüntülemeyen bir mizan oluşturduysanız denetleyeceğiniz şeyler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bc3f4-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="bc3f4-109">**Önceki kapanış geri al** alanı **Evet** olarak ayarlanırsa aynı mali yıl için önceki yıl sonu kapanışı tersine çevrilir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="bc3f4-110">Yıl sonu kapanışını tersine çevirme işlemi çalıştırılırken yıl hiç kapatılmamış gibi kapanış ve açılış bakiyeleri için tüm girişler silinir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="bc3f4-111">Ayrıca fişler de silinir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-111">The vouchers are also deleted.</span></span> <span data-ttu-id="bc3f4-112">Yıl sonu kapanışı işlemi otomatik olarak yeniden çalıştırılmaz.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="bc3f4-113">İşlemi yeniden başlatmanız gerekir, bu kez **Önceki kapanışı geri al** seçeneğini **Hayır** olarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="bc3f4-114">Bu senaryo, yıl sonu kapanışıyla ilgili SSS konusunda kapsanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="bc3f4-115">Daha fazla bilgi için bkz. [Yıl sonu faaliyetleriyle ilgili SSS](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="bc3f4-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="bc3f4-116">Belirti</span><span class="sxs-lookup"><span data-stu-id="bc3f4-116">Symptom</span></span>

<span data-ttu-id="bc3f4-117">Yıl sonu kapanışını **Önceki kapanışı geri al** seçeneğini **Hayır** olarak ayarlayarak çalıştırdım ve yine de mali yılım için açılış bakiyelerim yok.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="bc3f4-118">Çözüm</span><span class="sxs-lookup"><span data-stu-id="bc3f4-118">Resolution</span></span>

<span data-ttu-id="bc3f4-119">Öncelikle toplu işin durumunu denetleyin.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-119">First check the status of the batch job.</span></span> <span data-ttu-id="bc3f4-120">Bir yılı kapatmak bir dizi ayrı görev içerir ancak en önemli adım, görev açıklaması **Adım 5.0.0** olan toplu görevdir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="bc3f4-121">Genel muhasebe için açılış işlemlerini ve isteğe bağlı olarak kapanış işlemlerini deftere nakletme bu adım sırasında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="bc3f4-122">[![Toplu iş geçmişi listesi](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="bc3f4-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="bc3f4-123">Bu adım başarıyla sonlandıysa ancak **Mizan sorgusu** sayfasında (**Genel muhasebe > Sorgular ve raporlar > Mizan**) açılış bakiyelerini göremiyorsanız Bakiyeleri yeniden oluşturma adımının başarıyla tamamlanıp tamamlanmadığını görmek için yıl sonu kapanışı toplu işinin sonuçlarını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="bc3f4-124">[![Yıl sonu kapanışı toplu işinin sonuçları](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="bc3f4-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="bc3f4-125">Bu adım bir nedenle başarısız olursa açılış (ve isteğe bağlı olarak kapanış) işlemleri büyük olasılıkla başarılı şekilde deftere nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="bc3f4-126">Fiş numarasını belirterek **Fiş hareketleri sorgusu** sayfasını ve kapattığınız yıl için yıl sonu kapanışı iletişim kutusunda sağlanan tarihi kullanarak (**Genel Muhasebe > Sorgular ve raporlar > Fiş hareketleri**) Genel muhasebe işlemlerinin başarıyla deftere nakledildiğini doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="bc3f4-127">[![Fiş hareketleri sorgusu](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="bc3f4-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="bc3f4-128">Açılış (ve isteğe bağlı olarak kapanış) fişleri varsa yıl sonu kapanışını yeniden çalıştırmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="bc3f4-129">Bunun yerine, nasıl ilerleyeceğiniz hakkında bilgi için sonraki bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="bc3f4-130">Belirti</span><span class="sxs-lookup"><span data-stu-id="bc3f4-130">Symptom</span></span>

<span data-ttu-id="bc3f4-131">Yıl sonu kapanışında "Bakiyeleri yeniden oluşturma" adımı başarısız olduysa tüm yıl sonu kapanışı işlemini yeniden çalıştırmam gerekir mi?</span><span class="sxs-lookup"><span data-stu-id="bc3f4-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="bc3f4-132">Çözüm</span><span class="sxs-lookup"><span data-stu-id="bc3f4-132">Resolution</span></span>

<span data-ttu-id="bc3f4-133">Bakiyeleri yeniden oluşturma adımında, Mizan sorgusu oluşturulduğunda kullanılan Genel muhasebe bakiyeleri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="bc3f4-134">Bu, yıl sonu kapanışı işlemindeki son adımdır.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="bc3f4-135">Bu başarısız olan tek adım ise Genel muhasebe işlemleri başarıyla deftere nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="bc3f4-136">Yıl sonu kapanışını yeniden çalıştırmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="bc3f4-137">**Mali boyut kümeleri** sayfasını (**Genel muhasebe > Hesap planı > Boyutlar > Mali boyut kümeleri**) kullanarak bakiyeleri el ile yeniden oluşturma işlemini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="bc3f4-138">[![Mali boyut kümeleri sayfasında bakiyeleri yeniden oluşturma düğmesi](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="bc3f4-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="bc3f4-139">Bu adımın işlenmesi uzun sürerse [Mali boyut kümelerini güncelleştirmek için en iyi uygulamalar](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets) bölümünde açıklandığı gibi mali boyut kümeleri için en iyi uygulamaları incelemeyi öneririz.</span><span class="sxs-lookup"><span data-stu-id="bc3f4-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

