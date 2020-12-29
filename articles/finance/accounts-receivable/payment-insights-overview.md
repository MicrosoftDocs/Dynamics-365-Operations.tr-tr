---
title: Müşteri ödeme öngörüleri (Önizleme)
description: Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamaya yardımcı olan ödeme içgörüleri özelliği açıklanmıştır. Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanıza gerekçe olabilecek durumları belirlemenize yardımcı olabilir.
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
ms.openlocfilehash: f151942555ac503338f0fd44aa8779e3c2970fb1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644645"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="670a3-104">Müşteri ödeme öngörüleri (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="670a3-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="670a3-105">Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamaya yardımcı olan ödeme içgörüleri özelliği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="670a3-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="670a3-106">Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanıza gerekçe olabilecek durumları belirlemenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="670a3-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="670a3-107">Overview</span></span>

<span data-ttu-id="670a3-108">Müşterilerinin faturalarını ne zaman ödeyeceklerini tahmin etmek zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="670a3-109">Bu bilgi eksikliği, daha az doğru nakit akışı tahminlerine, çok geç gerçekleşen tahsilat işlemlerine ve ödemelerinde temerrüde düşebilecek müşterilere gönderilen siparişlere yol açar.</span><span class="sxs-lookup"><span data-stu-id="670a3-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="670a3-110">Müşteri ödeme içgörüleri (Önizleme), müşteri faturasının ne zaman ödeneceğini tahmin etme konusunda kuruluşlara yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="670a3-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="670a3-111">Bu bilgiler kuruluşların, zamanında ödeme olasılığını artıran tahsilat stratejileri oluşturmalarına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="670a3-112">Öngörüler</span><span class="sxs-lookup"><span data-stu-id="670a3-112">Predictions</span></span>

<span data-ttu-id="670a3-113">Ödeme tahminleri, kuruluşların geç ödeme olasılığı olan faturaları kolayca tespit etmelerine ve zamanında ödeme alma şanslarını artıracak uygun önlemleri almalarına yardımcı olarak iş süreçlerini iyileştirmelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="670a3-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="670a3-114">Geçmiş faturalardan, ödemelerden ve müşteri verilerinden yararlanan bir makine öğrenimi modeli kullanan Müşteri ödeme öngörüleri (Önizleme), bir müşterinin ödeme bekleyen bir faturayı ne zaman ödeyeceğini daha doğru tahmin eder.</span><span class="sxs-lookup"><span data-stu-id="670a3-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="670a3-115">Her açık fatura için Müşteri ödeme içgörüleri (Önizleme) üç ödeme olasılığı tahmin edebilir:</span><span class="sxs-lookup"><span data-stu-id="670a3-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="670a3-116">Ödemenin zamanında yapılma olasılığı</span><span class="sxs-lookup"><span data-stu-id="670a3-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="670a3-117">Ödemenin geç yapılma olasılığı</span><span class="sxs-lookup"><span data-stu-id="670a3-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="670a3-118">Ödemenin çok geç yapılma olasılığı</span><span class="sxs-lookup"><span data-stu-id="670a3-118">Probability of payment being made very late</span></span>

<span data-ttu-id="670a3-119">Müşteri ödeme içgörüleri (Önizleme), beklenen ödemelerin toplu görünümünü de sunar. Bu da kuruluşların üç olasılıktan birinde (Zamanında, Geç ve Çok geç) müşteriden bekleyebilecekleri toplam ödeme tutarını anlamalarına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="670a3-120">[![Ödeme tahminlerinin toplu görünümü](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="670a3-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="670a3-121">Ayrıca, her faturaya bir zamanında ödeme yapılma olasılığı da atanır.</span><span class="sxs-lookup"><span data-stu-id="670a3-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="670a3-122">Zamanında ödeme olasılığı %50'nin altındaysa bu faturalara tahsilat uyarısı gerekebileceğini belirtmek için faturalar kırmızı bir daire ile etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="670a3-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="670a3-123">[![Ödeme olasılıklarının listesi](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="670a3-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="670a3-124">Ayrıca Müşteri ödeme öngörüleri (Önizleme) tahminleri etkileyen en önemli faktörler, müşteriyle olan işin mevcut durumu ve geçmiş müşteri ödeme davranışı hakkında ayrıntılar gibi tahminleri açıklamak için bağlamsal bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="670a3-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="670a3-125">Birçok işletmede, tahsilat süreci reaktif bir faaliyettir; tahsilat süreci faturaların vadesi gelinceye kadar başlamaz.</span><span class="sxs-lookup"><span data-stu-id="670a3-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="670a3-126">Müşteri ödeme öngörüleri (Önizleme) ile kuruluşlar tahsilatlarda daha proaktif olabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="670a3-127">Tahsilat sürecinin başlaması için hareketlerin gerçekleşme zamanını beklemelerine gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="670a3-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="670a3-128">Bunun yerine, proaktif tahsilatların zamanında ödenme olasılığını artırıp artırmayacağını belirlemek için ödeme tahmini özelliğini kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="670a3-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="670a3-129">Ödeme tahmini, aynı zamanda işletmelere tahsilat sürecinin erken başlamasını haklı gösteren bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="670a3-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="670a3-130">Metodoloji</span><span class="sxs-lookup"><span data-stu-id="670a3-130">Methodology</span></span>

<span data-ttu-id="670a3-131">Bir yapay zeka çözümü geliştirmek ve dağıtmak zordur.</span><span class="sxs-lookup"><span data-stu-id="670a3-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="670a3-132">Kullanılabilir bir yapay zeka çözümünü formüle etmek, geliştirmek, dağıtmak ve korumak için uzun zamandır çalışmakta olan veri bilimcileri, konu uzmanları ve mühendislerden oluşan bir takım gereklidir.</span><span class="sxs-lookup"><span data-stu-id="670a3-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="670a3-133">Yapay zeka çözümlerinin Finance'ta dağıtımını ve kullanılmasını kolaylaştırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="670a3-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="670a3-134">Finance'ta Microsoft AI Builder üzerine inşa edilen yapay zeka çözümleri hazırlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="670a3-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="670a3-135">Tek tıkla bir son kullanıcı, yapay zeka çözümünü dağıtabilir ve akıllı tahminlerin avantajlarından yararlanmaya başlayabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="670a3-136">Kuruluş, tahminlerin doğruluğundan memnun kalmazsa bir uzman kullanıcı yine tek tıkla AI builder uzantısı deneyimine girebilir ve ardından tahminler oluşturmak için kullanılan alanları seçebilir veya alanların seçimini kaldırabilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="670a3-137">Hazır olduklarında, değişiklikler konusunda eğitim verip değişiklikleri yayımlayabilirler ve eğitimi verilmiş model, Finance'taki tahminler için otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="670a3-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="670a3-138">Müşteri ödeme öngörüleri (Önizleme) edinme</span><span class="sxs-lookup"><span data-stu-id="670a3-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="670a3-139">Müşteri ödeme içgörüleri (Önizleme) uygulamasını denemek istiyorsanız lütfen [Müşteri ödeme içgörüleri (Önizleme)](mailto:fiap@microsoft.com) adresine e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="670a3-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="670a3-140">Gizlilik Bildirimi</span><span class="sxs-lookup"><span data-stu-id="670a3-140">Privacy Notice</span></span>

<span data-ttu-id="670a3-141">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri kullanmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="670a3-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


