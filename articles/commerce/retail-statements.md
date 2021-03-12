---
title: Perakende ekstreleri
description: Bu konu ekstrelerin nasıl oluşturulacağını ve deftere nakledileceğini açıklar.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: e9162bb9b56432dbeb4638e0598dcbf436ab0b1b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989513"
---
# <a name="retail-statements"></a><span data-ttu-id="4024d-103">Perakende ekstreleri</span><span class="sxs-lookup"><span data-stu-id="4024d-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4024d-104">Dynamics 365 Commerce içerisinde, ekstre deftere nakletme işlemi, Bulut satış noktası (POS) veya Modern POS (MPOS) içerisinde gerçekleşen hareketlerin muhasebesini yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4024d-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="4024d-105">Beyan deftere nakil işlemi, bir POS hareket kümesini merkez (HQ) istemcisine çekmek için dağıtım planlama kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4024d-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="4024d-106">**Commerce parametreleri** ve **Mağazalar** sayfalarında tanımlanan parametreler, tek tek ekstrelere çekilecek hareketleri seçmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4024d-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="4024d-107">Aşağıdaki çizimde ekstre deftere nakletme işlemi gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4024d-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="4024d-108">Bu işlemde, POS içerisinde kaydedilen hareketler, istemciye Commerce planlayıcısı kullanılarak aktarılır.</span><span class="sxs-lookup"><span data-stu-id="4024d-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="4024d-109">İstemci hareketleri aldıktan sonra, mağaza için hareket ekstrelerinı oluşturabilir, hesaplayabilir ve deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4024d-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="4024d-110">[![Beyan deftere nakletme işlemi](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="4024d-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="4024d-111">ekstreleri oluşturmak ve deftere nakletmek</span><span class="sxs-lookup"><span data-stu-id="4024d-111">Creating and posting statements</span></span>

<span data-ttu-id="4024d-112">Bir ekstreyi el ile veya periyodik olarak gün içinde çalışmak üzere ayarlamış olduğunuz toplu iş işlemlerini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4024d-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="4024d-113">Her iki durumda da, aşağıdaki adımlar ekstreleri oluşturmak ve deftere nakletmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4024d-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="4024d-114">Ekstre oluşturma</span><span class="sxs-lookup"><span data-stu-id="4024d-114">Create the statement</span></span>

<span data-ttu-id="4024d-115">Bu adım, ekstrenin el ile oluşturulduğu mağazayı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="4024d-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="4024d-116">Bir toplu iş işlemini yapılandırırsanız, tüm bu mağazalar için otomatik olarak ekstreleri, belirlediğiniz plana uygun olarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4024d-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="4024d-117">Ekstreyi hesaplama</span><span class="sxs-lookup"><span data-stu-id="4024d-117">Calculate the statement</span></span>

<span data-ttu-id="4024d-118">Bu adımda, hareket satırları **Commerce parametreleri** ve **Mağazalar** sayfalarında tanımlanan her bir mağaza için ölçüte dayalı olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="4024d-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="4024d-119">Bu sayfalarda, hareketleri tanımlarsınız ve hareketlerin nasıl hesaplandığını belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4024d-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="4024d-120">Ekstreyi hesaplamadan önce ekstreye dahil edilmiş olan hareketlerin bir listesini görüntülemek için, **Hareketler** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="4024d-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="4024d-121">Ekstre hesaplaması, kasalardan sayımlarında sayılan tutar beyanlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="4024d-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="4024d-122">Ayrıca, düzeltilen tutarı el ile de girebilirisiniz.</span><span class="sxs-lookup"><span data-stu-id="4024d-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="4024d-123">Ekstre, tüm ödeme tiplerindeki hareket için satış tutarı ve gerçek hesaplanan tutar arasındaki farkı gösterir.</span><span class="sxs-lookup"><span data-stu-id="4024d-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="4024d-124">Ekstre, yalnızca bu fark mağaza için tanımlanan maksimum seçilen deftere nakil farkından az ise deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="4024d-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="4024d-125">Ekstre hesaplama işlemi genel numara sırasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="4024d-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="4024d-126">Bir ekstreyi hesapladığınızda, hesaplama aşağıdaki görevleri içerir:</span><span class="sxs-lookup"><span data-stu-id="4024d-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="4024d-127">Seçilen bir veri aralığı için, önceki ekstre hesaplamasına dahil edilmemiş olan hareketleri işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4024d-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="4024d-128">Seçili hareketlerde sayılan toplam tutarları hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="4024d-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="4024d-129">Sonuçlar ekstre satırlarında, ekstre yöntemine bağlı olarak gösterilir:</span><span class="sxs-lookup"><span data-stu-id="4024d-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="4024d-130">Ekstre yöntemi **Toplam** ise, seçilen hareketlerdeki her bir ödem yöntemi için bir satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="4024d-131">Ekstre yöntemi **Personel** ise, seçilen personel üyesi tarafından gerçekleştirilen hareketlerdeki her ödeme türü için bir satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="4024d-132">Ekstre yöntemi **POS Terminali** ise, seçilen kayıt üzerinde gerçekleştirilen hareketlerdeki her ödeme yöntemi için bir satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="4024d-133">Ekstre yöntemi **Vardiya** ise, vardiya sırasında gerçekleştirilen hareketlerdeki her ödeme yöntemi için bir satır oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="4024d-134">**Ekstre yöntemine göre böl** onay kutusu **Mağazalar** sayfasında seçilmişse, **Ekstre yöntemi** alanında seçilmiş olan değere dayanarak ayrı bir ekstre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="4024d-135">Mağazanızın çalışma saatleri gece yarısını geçiyorsa, ekstre deftere nakillerini, takvim gününün sonuna değil, iş gününün sonuna dayanacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4024d-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="4024d-136">**Mağazalar** sayfasında **Ekstre/kapatma** hızlı sekmesinde, **İş günü sonu** alanında, son hareketin kaydedilmesi ve iş gününü ekstresine dahil edilmesi gereken saati seçin.</span><span class="sxs-lookup"><span data-stu-id="4024d-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="4024d-137">**İş günü olarak deftere naklet** onay kutusunu, hareketleri aynı iş gününde deftere nakletmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="4024d-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="4024d-138">Ekstre deftere nakledildiğinde, aynı iş günü içerisinde kaydedilmiş olan hareketler aynı satış siparişlerine dahil edilebilir, bazı hareketler gece yarısından önce, bazıları da gece yarısından sonra gerçekleşseler bile.</span><span class="sxs-lookup"><span data-stu-id="4024d-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="4024d-139">Örnek: İki takvim gününü aşan bir iş günü için bir ekstre deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="4024d-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="4024d-140">Bir mağaza 08:00 ve 03:00 arasında açıktır, ve **İş günü olarak deftere naklet** onay kutusu, mağazanın yapılandırmasında seçilidir.</span><span class="sxs-lookup"><span data-stu-id="4024d-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="4024d-141">31 Mayıs'ta, mağaza 08:00 ve gece yarısı arasında hareketleri kaydeder.</span><span class="sxs-lookup"><span data-stu-id="4024d-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="4024d-142">Mağaza ayrıca 1 Haziran 00:01 ve 03:00 arasındaki hareketleri de kaydeder.</span><span class="sxs-lookup"><span data-stu-id="4024d-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="4024d-143">Mağaza, iş gününün kapanışı için ekstresini deftere naklettiğinde, oluşturulan satış siparişi 08:00 ve 03:00 iş saatleri arasında kaydedilen tüm hareketleri içerir; hareketler iki gün içerisinde oluşmuş olsa bile, 31 Mayıs ve 1 Haziran.</span><span class="sxs-lookup"><span data-stu-id="4024d-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="4024d-144">**Bir iş günü olarak deftere naklet** onay kutusu aynı mağaza için işaretli değilse, mağaza ekstresini iş gününün sonunda deftere naklettiğinde ayrı satış siparişleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="4024d-145">Bir satış siparişi, iş saatleri 08:00 ve 31 Mayıs gece yarısı arasında kaydedilen hareketleri içerir, diğer satış siparişi, iş saatleri 00:01 ve 03:00 1 Haziran'da kaydedilen hareketleri içerir.</span><span class="sxs-lookup"><span data-stu-id="4024d-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="4024d-146">Ekstreler oluşturabilmeden önce, ekstre dönemindeki vardiyaları kapatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4024d-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="4024d-147">Ekstreyi deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="4024d-147">Post the statement</span></span>

<span data-ttu-id="4024d-148">Bir ekstreyi deftere naklettiğinizde, satış siparişleri ve faturalar, ekstre içindeki satışlar için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4024d-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="4024d-149">Peşin alışveriş satışlar bir satış siparişinde toplanır ve mağazaya atanmış olan varsayılan kullanıcıya faturalanır.</span><span class="sxs-lookup"><span data-stu-id="4024d-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="4024d-150">POS içerisinde bir harekete bir müşterinin eklenmiş olduğu satışları, her bir benzersiz müşteri için ayrı satış siparişleri ve faturalar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4024d-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="4024d-151">Ödeme günlükleri, ekstredeki ödemeler için otomatik olarak oluşturulur ve stok, POS mağazası için güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4024d-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>
