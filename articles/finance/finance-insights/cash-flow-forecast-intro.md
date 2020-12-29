---
title: Nakit akışı tahmini (önizleme)
description: Bu konuda, Nakit akışı tahmini özelliği açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645260"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="251f9-103">Nakit akışı tahmini (önizleme)</span><span class="sxs-lookup"><span data-stu-id="251f9-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="251f9-104">Nakit akışı her işletme için kritik öneme sahiptir.</span><span class="sxs-lookup"><span data-stu-id="251f9-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="251f9-105">Hatta kar elde eden şirketler bile, acil gereksinimlerini karşılamak için nakit akışını korumazsa borçlarını ödeyemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="251f9-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="251f9-106">Mali içgörülerdeki nakit akışı tahmini özelliği, şirketlerin nakit bakiyelerini etkili şekilde izlemesine ve yönetmelerine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="251f9-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="251f9-107">Bu özellik, işletmelerin nakit akışlarını geçmişe kıyasla daha doğru tahmin edebilmeleri için makine öğrenimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="251f9-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="251f9-108">Ayrıca yöneticilere, geçerli nakit pozisyonlarındaki fırsatları en iyi duruma getirecek kararlar alma konusunda yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="251f9-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="251f9-109">Birçok şirket için nakit akışını yönetme ve nakit akışı tahminlerini çalıştırma; sıkıcı, yinelenen ve el ile gerçekleştirilen bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="251f9-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="251f9-110">Pek çok şirket bunun için farklı karmaşıklık düzeylerine sahip Microsoft Excel çözümlerinden yararlanır.</span><span class="sxs-lookup"><span data-stu-id="251f9-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="251f9-111">Nakit akışını doğru şekilde tahmin etmeyle ilgili zorluklardan bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="251f9-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="251f9-112">Veriler aşağıdakiler dahil farklı yerlere dağılmış olduğundan karar mekanizmalarına sunulamaz:</span><span class="sxs-lookup"><span data-stu-id="251f9-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="251f9-113">Muhasebe veya kurumsal kaynak planlama sistemi</span><span class="sxs-lookup"><span data-stu-id="251f9-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="251f9-114">Finansal planlama yazılımı</span><span class="sxs-lookup"><span data-stu-id="251f9-114">Financial planning software</span></span>
  - <span data-ttu-id="251f9-115">Excel</span><span class="sxs-lookup"><span data-stu-id="251f9-115">Excel</span></span>
  - <span data-ttu-id="251f9-116">Ek yazılım uygulamaları</span><span class="sxs-lookup"><span data-stu-id="251f9-116">Additional software applications</span></span> 
- <span data-ttu-id="251f9-117">Tahmin, her etki alanı veya departman içinde "silolarda" içinde bulunan şirket içi bilgilere dayanır.</span><span class="sxs-lookup"><span data-stu-id="251f9-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="251f9-118">Mali öğeler gerçekleştirildikten sonra nakit akışı tahminin doğruluğunu ölçmek kesin bir sonuç sunmaz ve zordur.</span><span class="sxs-lookup"><span data-stu-id="251f9-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="251f9-119">Nakit akışı tahmini özelliğinin ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="251f9-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="251f9-120">Nakit akışı tahminleri özelliği aşağıdaki işlevleri içerir.</span><span class="sxs-lookup"><span data-stu-id="251f9-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="251f9-121">Harici sistemlerden gelen nakit akışı verilerini Dynamics 365 Finance'e tümleştirmeyi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="251f9-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="251f9-122">Nakit akışı tahminleri veri içeri-dışarı aktarma çerçevesini de kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="251f9-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="251f9-123">Bu çerçeve Excel OData ile tümleştirmeyi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="251f9-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="251f9-124">Ayrıca, kapsamlı bir nakit akışı çözümü oluşturmak için birden fazla kaynaktaki verileri birleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="251f9-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="251f9-125">Akıllı bir nakit pozisyonu sağlar.</span><span class="sxs-lookup"><span data-stu-id="251f9-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="251f9-126">Nakit pozisyonu, şirketin hesaplarına nakit gelmesini bekleyebileceği zamanı tahmin etmek için müşterinin ödeme davranışına göre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="251f9-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="251f9-127">Ayrıca, gelecekteki fatura ve siparişlerin ödenebileceği zamanı tahmin etmek için ödeme yapan satıcıların geçmiş modellerini analiz eder.</span><span class="sxs-lookup"><span data-stu-id="251f9-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="251f9-128">AI Builder ile otomatikleştirilmiş tümleştirme aracılığıyla zaman serisi tahminini kullanarak uzun süreli tahminler için akıllı nakit akışı tahmini sağlar.</span><span class="sxs-lookup"><span data-stu-id="251f9-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="251f9-129">Belirli nakit akışı pozisyonunu veya tahminlerini kaydetme, bunları düzenleme ve daha sonra tahmini gerçek mali değerlerle karşılaştırarak tahmin performansını ölçme özelliği sunar.</span><span class="sxs-lookup"><span data-stu-id="251f9-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="251f9-130">Anlık görüntü karşılaştırmasıyla durum çözümlemeleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="251f9-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="251f9-131">Örneğin, iyimser, kötümser ve nakit akışının en gerçekçi görünümlerini temsil eden birden çok anlık görüntü oluşturabilir ve farklılıkları karşılaştırabilir ve görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="251f9-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="251f9-132">Nakit akışı tahminini birden fazla para biriminde ve farklı tüzel kişilikler genelinde görüntüleme ve belirli bir banka hesabıyla ilişkili nakit akışını filtreleme ve görüntüleme özelliği sunar.</span><span class="sxs-lookup"><span data-stu-id="251f9-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="251f9-133">Mali boyutlarla ilgili banka hesaplarını filtrelemenizi ve görüntülemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="251f9-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="251f9-134">Dynamics 365 Finance'teki nakit akışı tahmini işlevi; sıkıcı, karmaşık ve yinelenen nakit akışı tahmini işlemini basit ve otomatik bir işleme dönüştürmek için kuruluşunuzu destekler.</span><span class="sxs-lookup"><span data-stu-id="251f9-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="251f9-135">Nakit akışı tahminlerinin en sıkıcı yönlerini otomatikleştirmek, istenen iş sonuçlarını elde etmek için kritik karar alma süreçlerine odaklanmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="251f9-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="251f9-136">Nakit akışı tahmini için Boyutları ayarlama</span><span class="sxs-lookup"><span data-stu-id="251f9-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="251f9-137">**Nakit akışı tahmin kurulumu** sayfasındaki yeni bir sekme, **Nakit akışı tahmini** çalışma alanında filtre uygulamak için hangi mali boyutları kullanacağınızı kontrol etmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="251f9-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="251f9-138">Bu sekme yalnızca Nakit akışı tahminleri özelliği etkinleştirildiğinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="251f9-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="251f9-139">**Boyutlar** sekmesinde, filtre için kullanılacak boyut listesinden seçim yapın ve bunları sağ sütuna taşımak için ok tuşlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="251f9-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="251f9-140">Nakit akışı tahmin verilerinin filtrelenmesi için yalnızca iki boyut seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="251f9-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="251f9-141">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="251f9-141">Privacy notice</span></span>
<span data-ttu-id="251f9-142">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="251f9-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
