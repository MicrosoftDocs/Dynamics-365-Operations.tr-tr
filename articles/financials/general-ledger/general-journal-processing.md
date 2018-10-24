---
title: "Genel günlük işleme"
description: "Bu konu, yevmiye işlemlerini daha kolay yapmaya yardımcı olabilecek Microsoft Dynamics 365 for Finance and Operations yeteneklerini açıklar. Bunlar ayrıca doğru verilerin kaydedildiğini ve dahili kontrolün hatasız olduğunu da sağlamaya yardımcı olur."
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf744bc41ffcca6d029da5dd2031ada607a0109b
ms.openlocfilehash: e77aafafed5c972a6ad8c064107306d3ebde0b79
ms.contentlocale: tr-tr
ms.lasthandoff: 09/24/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="6fdb0-103">Genel günlük işleme</span><span class="sxs-lookup"><span data-stu-id="6fdb0-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fdb0-104">Bu konu, yevmiye işlemlerini daha kolay yapmaya yardımcı olabilecek Microsoft Dynamics 365 for Finance and Operations yeteneklerini açıklar. Bunlar ayrıca doğru verilerin kaydedildiğini ve dahili kontrolün hatasız olduğunu da sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-104">This topic describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="6fdb0-105">Günlük adları</span><span class="sxs-lookup"><span data-stu-id="6fdb0-105">Journal names</span></span>

<span data-ttu-id="6fdb0-106">Ayarlanması gereken en önemli alanlardan biri günlük adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="6fdb0-107">Her amaç için belirli günlük adlarını tanımlamak iyi bir fikirdir; örneğin şirketlerarası, tahakkuk ayarlaması ve hata düzeltme gibi.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="6fdb0-108">Her günlük adını, her bir amaç için bir veri girişi yapmak için güvenle ve kolayca özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="6fdb0-109">**Günlük adları** sayfasında aşağıdaki öğeleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="6fdb0-110">**İş akışı onayı** – İç denetim artırmak için toplam borç tutarı gibi ölçütlere göre gözden geçirme ve onay adımları için maddesellik sınırları kuran günlük iş akışları tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="6fdb0-111">Genel günlükler için iş akışlarını **Genel muhasebe iş akışları** sayfası üzerinde ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="6fdb0-112">**Varsayılan değerler** – Mahsup hesaplar, para ve mali boyutlar için varsayılan değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="6fdb0-113">**Günlük kontrolü** – Şirket ve hesap türü ve ayrıca segment değerleri üzerindeki kısıtlamaları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="6fdb0-114">**Örnekler**</span><span class="sxs-lookup"><span data-stu-id="6fdb0-114">**Examples**</span></span>

<span data-ttu-id="6fdb0-115">Günlük adı sadece ayarlamalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="6fdb0-116">Bu durumda, yalnızca **defter** hesap türünün tüm şirketler arasında geçerli olduğunu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="6fdb0-117">[![Günlük kontrol hesap tipleri](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="6fdb0-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="6fdb0-118">Günlük adı yalnızca belirli bir kesim veya ana hesap aralığı için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="6fdb0-119">[![Günlük kontrol segmenti](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="6fdb0-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="6fdb0-120">**Otomatik ters** seçeneği genel günlüklerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="6fdb0-121">Örneğin, aşağıdaki çizimde gösterildiği gibi gerçek belgenin henüz işlenmemiş olduğu tahakkuk ayarlamanız vardır.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="6fdb0-122">[![Yevmiye günlüğü tersine çevirme](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="6fdb0-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="6fdb0-123">Günlük girdisi için Microsoft Excel eklentisi, otomasyon ek düzeyi sağlar ve veri girişini kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="6fdb0-124">**Satırları Excel'de açma** eylemi **yevmiye defteri** ve **günlük fişi** sayfalarında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="6fdb0-125">**Periyodik günlüklere** sayfası üzerinde, günlük işlemini otomatikleştirmek için yinelenen günlükler ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="6fdb0-126">Herhangi bir anda fiş şablonları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="6fdb0-127">**Yevmiye defterleri** sayfası üzerinde, **Kaydet** ve **Fiş şablonu seç** eylemleri **Günlük fişi** sayfası üzerinde **İşlevler** altında fiş satırları için bulunur.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="6fdb0-128">İlgili kurulum</span><span class="sxs-lookup"><span data-stu-id="6fdb0-128">Related setup</span></span>
<span data-ttu-id="6fdb0-129">Aşağıdaki kurulum genel günlüklere özgü değildir, ancak veri girişinin doğru veri olduğunu ve kolay olduğunu sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="6fdb0-130">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="6fdb0-130">Main account</span></span>

<span data-ttu-id="6fdb0-131">Ana hesap kurulumu yevmiye defterine işlemek için birçok seçenek sağlar:</span><span class="sxs-lookup"><span data-stu-id="6fdb0-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="6fdb0-132">**DC/CR gereksinimi** – Bir ana hesap borç veya alacak hareketleriyle sınırlandırılmışsa, bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="6fdb0-133">Kurulum, bir günlük doğrulandığında veya deftere nakledildiğinde doğrulanır.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="6fdb0-134">**Varsayılan mahsup hesap**</span><span class="sxs-lookup"><span data-stu-id="6fdb0-134">**Default offset account**</span></span>
-   <span data-ttu-id="6fdb0-135">**Askıya alınmış** – Tüm şirketler arasında veya belirli şirket/yasal varlık için bir ana hesap veri girişini askıya alma.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="6fdb0-136">**El ile girişe izin verme** – Kullanıcıların hesap günlükleri için el ile bir değer girmesini engellemek.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="6fdb0-137">**Varsayılan/Para birimi doğrula**</span><span class="sxs-lookup"><span data-stu-id="6fdb0-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="6fdb0-138">**Tüzel kişilik geçersizleştir** – Bu kurulum tanımlanan şirket/yasal varlığa özeldir:</span><span class="sxs-lookup"><span data-stu-id="6fdb0-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="6fdb0-139">**Varsayılan/Satış vergisini doğrula**</span><span class="sxs-lookup"><span data-stu-id="6fdb0-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="6fdb0-140">**Varsayılan boyut** – **Sabit olmayan** veya **Sabit değer**.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="6fdb0-141">**Sabit değer** bu ana hesap için tüm nakillerin **Sabit** olarak ayarladığınız herhangi bir boyut değeri her zaman kullanmasını sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="6fdb0-142">**Deftere nakli doğrulama**</span><span class="sxs-lookup"><span data-stu-id="6fdb0-142">**Posting validation**</span></span>
    -   <span data-ttu-id="6fdb0-143">**Kullanıcı doğrulama** – Bu seçenek, bir ana hesap için deftere nakletmek için hangi kullanıcıların izinli olacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="6fdb0-144">**Deftere gönderme türü doğrulama** – Bu seçenek, bir ana hesap için hangi deftere nakletme türlerinin izinli olacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="6fdb0-145">Hesap yapıları ve gelişmiş kurallar yapıları</span><span class="sxs-lookup"><span data-stu-id="6fdb0-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="6fdb0-146">Hesap yapıları ve Gelişmiş kurallar yapıları finansal raporlama ve performans izleme için gerekli olan verilerin yevmiye işleme ve belgeleri sırasında yakalandığını sağlamak için büyük önem taşımaktadır.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="6fdb0-147">Hesap yapıları ve gelişmiş kurallar yapıları veri girişi deneyimini uyarlamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="6fdb0-148">Veri girişini sadece her durumda ilgili olan mali boyutları için izin verebilirsiniz ve gerekli ve doğru verileri her zaman yakalanmasını gereksinimini de zorlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="6fdb0-149">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="6fdb0-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="6fdb0-150">[Planlama: Hesap planı](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="6fdb0-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="6fdb0-151">Günlükler için gelişmiş kurallar oluşturma</span><span class="sxs-lookup"><span data-stu-id="6fdb0-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="6fdb0-152">Şablon kullanarak yevmiye defteri girişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6fdb0-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="6fdb0-153">Günlükler oluşturma ve doğrulama</span><span class="sxs-lookup"><span data-stu-id="6fdb0-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="6fdb0-154">Periyodik günlükleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="6fdb0-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="6fdb0-155">Genel muhasebe tahsisat günlüğünü işleme</span><span class="sxs-lookup"><span data-stu-id="6fdb0-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="6fdb0-156">Deftere nakil benzetimi gerçekleştir</span><span class="sxs-lookup"><span data-stu-id="6fdb0-156">Simulate posting</span></span>
<span data-ttu-id="6fdb0-157">**Deftere nakletmeyi simüle et**'i çoğu günlük için **Doğrula** menüsünde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="6fdb0-158">Bir günlüğü **Doğrula** işlevini kullanarak doğruladığınızda, sistem günlüğü belirli hata koşullarına karşı test eder.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="6fdb0-159">**Deftere nakletmeyi simüle et** işlevini kullanırsanız, sistem, deftere nakil sırasında çalıştırılacak tüm işlemleri günlüğü deftere gerçekte nakletmeden yapar.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="6fdb0-160">Daha sonra görüntülenen deftere nakil mesajlarını gözden geçirebilir, bulduğunuz hataları düzeltebilir ve daha sonra günlüğü deftere nakletmek için **Deftere naklet** menüsünü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-160">You can then review the posting messages that are displayed, fix any errors that you find, and then click the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="6fdb0-161">**Deftere nakletmeyi simüle et**, toplu işlem için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="6fdb0-162">Ancak, deftere nakli toplu iş için simüle etme kodu mevcuttur ve geliştiriciler bu kodu bu özelliğe eklemek üzere genişletebilir.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

