---
title: Müşteri ödeme öngörüleri (Önizleme)
description: Bu konu, bireysel müşterilerin tipik ödeme yöntemlerinin anlaşılmasını iyileştirmeye yardımcı olan ve başka türlü yaptığınızda tahsilat işlemlerini erken başlatmayı haklı kılan koşulları tanımlayan ödeme öngörüleri özelliğini açıklar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
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
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774066"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="56123-103">Müşteri ödeme öngörüleri (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="56123-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="56123-104">Bu konu, bireysel müşterilerin tipik ödeme yöntemlerinin anlaşılmasını iyileştirmeye yardımcı olan ve başka türlü yaptığınızda tahsilat işlemlerini erken başlatmanızı haklı kılan koşulları tanımlayan ödeme öngörüleri özelliğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="56123-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="56123-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="56123-105">Overview</span></span>

<span data-ttu-id="56123-106">Kuruluşlar genellikle müşterilerinin faturalarını ne zaman ödeyeceklerini öngörmede zorluk yaşar.</span><span class="sxs-lookup"><span data-stu-id="56123-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="56123-107">Bu bilgi eksikliği, daha az doğru nakit akışı tahminlerine, çok geç gerçekleşen tahsilat işlemlerine ve ödemelerinde temerrüde düşebilecek müşterilere gönderilen siparişlere yol açar.</span><span class="sxs-lookup"><span data-stu-id="56123-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="56123-108">Müşteri ödeme öngörüleri (Önizleme), kuruluşların bir müşteri faturasının ne zaman ödeneceğini tahmin etmesine ve kuruluşun zamanında ödeme olasılığını artıran tahsilat stratejileri oluşturmasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="56123-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="56123-109">Öngörüler</span><span class="sxs-lookup"><span data-stu-id="56123-109">Predictions</span></span>

<span data-ttu-id="56123-110">Ödeme tahminleri, kuruluşların geç ödeme olasılığı olan faturaları kolayca tespit etmelerine ve zamanında ödeme alma şanslarını artıracak uygun önlemleri almalarına yardımcı olarak iş süreçlerini iyileştirmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="56123-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="56123-111">Geçmiş faturalardan, ödemelerden ve müşteri verilerinden yararlanan bir makine öğrenimi modeli kullanan Müşteri ödeme öngörüleri (Önizleme), bir müşterinin ödeme bekleyen bir faturayı ne zaman ödeyeceğini daha doğru tahmin eder.</span><span class="sxs-lookup"><span data-stu-id="56123-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="56123-112">Her açık fatura için Müşteri ödeme bilgileri (Önizleme) üç ödeme olasılığı öngörür:</span><span class="sxs-lookup"><span data-stu-id="56123-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="56123-113">Ödemenin zamanında yapılma olasılığı</span><span class="sxs-lookup"><span data-stu-id="56123-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="56123-114">Ödemenin geç yapılma olasılığı</span><span class="sxs-lookup"><span data-stu-id="56123-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="56123-115">Ödemenin çok geç yapılma olasılığı</span><span class="sxs-lookup"><span data-stu-id="56123-115">Probability of payment being made very late</span></span>

<span data-ttu-id="56123-116">Kuruluşların bir müşteriden bekleyebilecekleri toplam ödeme tutarını üç olasılıktan birinde (Zamanında, Geç ve Çok geç) olacağını anlamalarına yardımcı olmak için Müşteri ödeme öngörüleri (Önizleme) beklenen ödemelerin toplu görünümünü de sağlar.</span><span class="sxs-lookup"><span data-stu-id="56123-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="56123-117">[![Ödeme tahminlerinin toplu görünümü](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="56123-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="56123-118">Ayrıca, her faturaya bir zamanında ödeme yapılma olasılığı da atanır.</span><span class="sxs-lookup"><span data-stu-id="56123-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="56123-119">Zamanında ödeme olasılığı %50'nin altındaysa bu faturalara tahsilat uyarısı gerekebileceğini belirtmek için faturalar kırmızı bir daire ile etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="56123-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="56123-120">[![Ödeme olasılıklarının listesi](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="56123-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="56123-121">Ayrıca Müşteri ödeme öngörüleri (Önizleme) tahminleri etkileyen en önemli faktörler, müşteriyle olan işin mevcut durumu ve geçmiş müşteri ödeme davranışı hakkında ayrıntılar gibi tahminleri açıklamak için bağlamsal bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="56123-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="56123-122">Birçok işletmede, tahsilat süreci reaktif bir faaliyettir; tahsilat süreci faturaların vadesi gelinceye kadar başlamaz.</span><span class="sxs-lookup"><span data-stu-id="56123-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="56123-123">Müşteri ödeme öngörüleri (Önizleme) ile kuruluşlar tahsilatlarda daha proaktif olabilir.</span><span class="sxs-lookup"><span data-stu-id="56123-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="56123-124">Tahsilat sürecinin başlaması için hareketlerin gerçekleşme zamanını beklemelerine gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="56123-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="56123-125">Bunun yerine, proaktif tahsilatların zamanında ödenme olasılığını artırıp artırmayacağını belirlemek için ödeme tahmini özelliğini kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="56123-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="56123-126">Ödeme tahmini, aynı zamanda işletmelere tahsilat sürecinin erken başlamasını haklı gösteren bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="56123-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="56123-127">Metodoloji</span><span class="sxs-lookup"><span data-stu-id="56123-127">Methodology</span></span>

<span data-ttu-id="56123-128">Bir yapay zeka çözümü geliştirmek ve dağıtmak zordur.</span><span class="sxs-lookup"><span data-stu-id="56123-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="56123-129">Kullanılabilir bir yapay zeka çözümünü formüle etmek, geliştirmek, dağıtmak ve korumak için uzun zamandır çalışmakta olan veri bilimcileri, konu uzmanları ve mühendislerden oluşan bir takım gerekir.</span><span class="sxs-lookup"><span data-stu-id="56123-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="56123-130">Yapay zeka çözümlerinin Finance'ta dağıtımını ve kullanılmasını kolaylaştırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="56123-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="56123-131">Finance'ta Microsoft AI Builder üzerine inşa edilen yapay zeka çözümleri hazırlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="56123-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="56123-132">Tek tıkla bir son kullanıcı, yapay zeka çözümünü dağıtabilir ve akıllı tahminlerin avantajlarından yararlanmaya başlayabilir.</span><span class="sxs-lookup"><span data-stu-id="56123-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="56123-133">Kuruluş, tahminlerin doğruluğundan memnun kalmazsa bir uzman kullanıcı yine tek tıkla AI builder uzantısı deneyimine girebilir ve ardından tahminler oluşturmak için kullanılan alanları seçebilir veya alanların seçimini kaldırabilir.</span><span class="sxs-lookup"><span data-stu-id="56123-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="56123-134">Hazır olduklarında, değişiklikler konusunda eğitim verip değişiklikleri yayımlayabilirler ve eğitimi verilmiş model, Finance'taki tahminler için otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="56123-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="56123-135">Müşteri ödeme öngörüleri (Önizleme) edinme</span><span class="sxs-lookup"><span data-stu-id="56123-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="56123-136">Müşteri ödeme öngörüleri (Önizleme) uygulamasını denemek istiyorsanız lütfen [Müşteri ödeme öngörüleri (Önizleme)](mailto:fiap@microsoft.com) adresine e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="56123-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="56123-137">Gizlilik Bildirimi</span><span class="sxs-lookup"><span data-stu-id="56123-137">Privacy Notice</span></span>

<span data-ttu-id="56123-138">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri kullanmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="56123-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


