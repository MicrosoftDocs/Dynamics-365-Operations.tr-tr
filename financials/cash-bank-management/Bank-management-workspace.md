---
title: "Banka yönetimi çalışma alanı"
description: "Bu konu Banka yönetimi çalışma alanı hakkında bilgiler sağlar. Bu çalışma alanı, şirket banka hesaplarıyla ilgili bilgiyi gösterir ve bir Özet görünümü ve bir Analiz sayfası içerir. Bu özet görünümü, özet kutucuklarını, banka hesap bilgisini, bir bakiye grafiğini ve ilgili bilgileri gösterir. Analiz sayfası, Microsoft Power BI yeteneklerini, banka hesabı bakiyeleriyle ilgili görselleri göstermek için kullanır."
author: saraschi2
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04f2831fa8179e7273fd532cc14608886b98cd0b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="bank-management-workspace"></a><span data-ttu-id="17abc-106">Banka yönetimi çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="17abc-106">Bank management workspace</span></span>

<span data-ttu-id="17abc-107">**Banka yönetimi** çalışma alanı, şirket banka hesaplarıyla ilgili bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="17abc-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="17abc-108">Bu çalışma alanı bir **Özet** görünümü ve bir **Analiz** sayfası içerir.</span><span class="sxs-lookup"><span data-stu-id="17abc-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="17abc-109">Bu **Özet** görünümü, özet kutucuklarını, banka hesap bilgisini, bir bakiye grafiğini ve ilgili bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="17abc-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="17abc-110">**Analiz** sayfası, Microsoft Power BI yeteneklerini, banka hesabı bakiyeleriyle ilgili görselleri göstermek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="17abc-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="17abc-111">Özet görünümü</span><span class="sxs-lookup"><span data-stu-id="17abc-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="17abc-112">Özet</span><span class="sxs-lookup"><span data-stu-id="17abc-112">Summary</span></span>

<span data-ttu-id="17abc-113">**Özet** bölümündeki kutucuklar, banka hesaplarınıza bir genel bakış sunar ve en sık kullanmanız gereken sayfalara hızlı erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="17abc-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="17abc-114">Banka mutabakatı bilgisi, Gelişmiş banka mutabakatı işlevine özeldir.</span><span class="sxs-lookup"><span data-stu-id="17abc-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="17abc-115">Bilgi, yalnızca **Gelişmiş banka mutabakatı** seçeneğinin **Banka hesabı** sayfasında **Evet** olarak ayarlanmış banka hesapları için dahildir.</span><span class="sxs-lookup"><span data-stu-id="17abc-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="17abc-116">**Özet** bölümünden, elektronik banka dosyalarını, tüm tüzel varlıklar üzerindeki banka hesaplar için içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17abc-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="17abc-117">Banka hesapları</span><span class="sxs-lookup"><span data-stu-id="17abc-117">Bank accounts</span></span>

<span data-ttu-id="17abc-118">Tüzel varlıktaki her bir banka hesabı, **Banka hesapları** bölümündeki bir kart ile temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="17abc-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="17abc-119">Mevcut bakiye gösterilir ve özet bakiye tutarını oluşturan hareketlerin ayrıntısına inebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17abc-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="17abc-120">**Köprülü hareketler** tutarı, özet tutarını oluşturan hareketlerin ayrıntısına inmenize de olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="17abc-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="17abc-121">Köprülü hareketler, köprü işlevi kullanarak nakledilen, ancak henüz temizlenmemiş olan tüm bekleyen hareketlerdir.</span><span class="sxs-lookup"><span data-stu-id="17abc-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="17abc-122">**Bekleyen bakiye** tutarı, geçerli bakiye eksi köprülü veya bekleyen hareketlerdir.</span><span class="sxs-lookup"><span data-stu-id="17abc-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="17abc-123">Kart, ayrıca banka hesabında en son ne zaman mutabakat sağlandığını da gösterir</span><span class="sxs-lookup"><span data-stu-id="17abc-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="17abc-124">Bu bilgi, yalnızca banka hesabı için Gelişmiş banka mutabakatı etkinleştirilmişse gösterilir.</span><span class="sxs-lookup"><span data-stu-id="17abc-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="17abc-125">Bilanço</span><span class="sxs-lookup"><span data-stu-id="17abc-125">Balance</span></span>

<span data-ttu-id="17abc-126">**Bakiye** grafiği, **Banka hesapları** bölümünde seçili banka hesabı için tarihi bakiye bilgisini veya tüzel varlıktaki tüm banka hesapları için geçmiş bakiye bilgisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="17abc-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="17abc-127">Bu bilgiler, çeşitli dönemler için kullanılabilir: geçerli hafta, geçerli ay, geçerli yıl, son beş yıl ve tüm dönemler (banka hesabının tam geçmişi).</span><span class="sxs-lookup"><span data-stu-id="17abc-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="17abc-128">Tek bir banka hesabı için **Bakiye** grafiğini görüntülüyorsanız, tarihi bakiye banka hesabı para biriminde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="17abc-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="17abc-129">Tüzel varlıktaki tüm banka hesaplarını görüntülüyorsanız, geçmiş bakiyeler muhasebe para birimi cinsinden gösterilir.</span><span class="sxs-lookup"><span data-stu-id="17abc-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="17abc-130">Verinin en son ne zaman güncelleştirilmiş olduğu, grafiğin üstünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="17abc-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="17abc-131">Veriyi ihtiyaç duyduğunuz gibi güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17abc-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="17abc-132">İlgili bilgiler</span><span class="sxs-lookup"><span data-stu-id="17abc-132">Related information</span></span>

<span data-ttu-id="17abc-133">**İlgili bilgi** bölümünde, **Genel günlük** sayfasını banka transferlerini görüntülemek için açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17abc-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="17abc-134">**Banka hareketleri** ve **Köprülü hareketler** sayfalarını da hızlıca açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17abc-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="17abc-135">Analiz görünümü</span><span class="sxs-lookup"><span data-stu-id="17abc-135">Analytics view</span></span>

<span data-ttu-id="17abc-136">**Analizler** sayfası, geçerli şirketteki banka hesapları hakkında önemli ölçümler sağlar.</span><span class="sxs-lookup"><span data-stu-id="17abc-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="17abc-137">Aşağıdaki görselleştirmeler bir sayfada mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="17abc-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="17abc-138">Sistem para biriminden toplam banka bakiyesi</span><span class="sxs-lookup"><span data-stu-id="17abc-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="17abc-139">Tüzel kişiliğe göre bakiye</span><span class="sxs-lookup"><span data-stu-id="17abc-139">Balance by legal entity</span></span>
-   <span data-ttu-id="17abc-140">Banka hesabı para birimi cinsinden bugünün fiili ve tahmini bakiye karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="17abc-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="17abc-141">Banka hesabına göre bakiye</span><span class="sxs-lookup"><span data-stu-id="17abc-141">Balance by bank account</span></span>
-   <span data-ttu-id="17abc-142">Döviz cinsinden bakiye</span><span class="sxs-lookup"><span data-stu-id="17abc-142">Balance by currency</span></span>

<span data-ttu-id="17abc-143">Tüm şirket arasındaki banka analizlerini **Nakit genel bakışı – tüm şirketler** çalışma alanından görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17abc-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span>

