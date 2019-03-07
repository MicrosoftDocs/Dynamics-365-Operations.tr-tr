---
title: Müşteri ödeme bilgileri (önizleme)
description: Bu konuda, Müşteri ödeme bilgilerinin, bir faturanın ne zaman ödeneceğini öngörmeye ve kuruluşlara zamanında ödeme yapma olasılığını artıran optimizasyon stratejileri oluşturmada nasıl yardımcı olabileceği açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "344674"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="52fde-103">Müşteri ödeme bilgileri (önizleme)</span><span class="sxs-lookup"><span data-stu-id="52fde-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="52fde-104">Bu özellik, hedeflenen sürümün bir parçasıdır ve yalnızca Özel Önizleme'ye katılmayı seçen kullanıcılar tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="52fde-105">Bu özellik, gelecekteki bir genel kullanım sürümüne eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="52fde-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="52fde-106">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="52fde-106">Overview</span></span>

<span data-ttu-id="52fde-107">Kuruluşlar genellikle bir müşterinin faturalarını ne zaman ödeyeceğini öngörmede zorluk yaşar.</span><span class="sxs-lookup"><span data-stu-id="52fde-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="52fde-108">Bu bilgi eksikliği, yanlış nakit akışı tahminlerine, verimsiz tahsilat işlemlerine ve siparişlerin kredi riski yaratabilecek müşterilere gönderilmesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="52fde-109">Müşteri ödeme bilgileri (önizleme), bir faturanın ne zaman ödeneceğini öngörmek için makine öğrenimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="52fde-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="52fde-110">Ayrıca müşterilerin zamanında ödeme yapma olasılığını en üst düzeye çıkarmak için uyarlanabilecek optimizasyon stratejileri de sunar.</span><span class="sxs-lookup"><span data-stu-id="52fde-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="52fde-111">Öngörüler</span><span class="sxs-lookup"><span data-stu-id="52fde-111">Predictions</span></span>

<span data-ttu-id="52fde-112">Ödeme öngörüleri, aşağıdakilere yardımcı olarak kuruluşların iş süreçlerini iyileştirmelerine olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="52fde-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="52fde-113">Geç ödeneceği öngörülen faturaları kolayca belirleyin.</span><span class="sxs-lookup"><span data-stu-id="52fde-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="52fde-114">Zamanında ödeme alma olasılığını artırmak için uygun önlemler alın.</span><span class="sxs-lookup"><span data-stu-id="52fde-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="52fde-115">Müşteri ödeme bilgileri (önizleme), bir faturanın ne zaman ödeneceğini öngörmek için makine öğrenimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="52fde-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="52fde-116">Bir faturanın ne zaman ödeneceğini öngörmek için kullanılan makine öğrenimi modelini oluşturmak için geçmiş fatura, ödeme ve müşteri verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="52fde-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="52fde-117">Her açık fatura için Müşteri ödeme bilgileri (önizleme) üç ödeme olasılığı öngörür:</span><span class="sxs-lookup"><span data-stu-id="52fde-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="52fde-118">Ödemenin zamanında yapılma olasılığı (fatura vade tarihi içinde).</span><span class="sxs-lookup"><span data-stu-id="52fde-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="52fde-119">Ödemenin fatura vade tarihinden itibaren 30 gün içinde yapılma olasılığı.</span><span class="sxs-lookup"><span data-stu-id="52fde-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="52fde-120">Ödemenin fatura vade tarihinden sonraki 30 günden daha geç yapılma olasılığı.</span><span class="sxs-lookup"><span data-stu-id="52fde-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="52fde-121">Ödeme olasılığı öngörü bölümünde görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="52fde-122">[![Ödeme öngörüleri](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="52fde-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="52fde-123">Her faturaya, yukarıda tanımlanan üç öngörülen ödeme olasılığı senaryosundan biri kullanılarak ödemeyi kazanma olasılığı da atanır.</span><span class="sxs-lookup"><span data-stu-id="52fde-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="52fde-124">En yüksek ödeme olasılığına sahip senaryo, kazanan senaryodur.</span><span class="sxs-lookup"><span data-stu-id="52fde-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="52fde-125">Örneğin, bir faturada öngörünün, faturanın zamanında ödenmesi olasılığını yüzde 71, faturanın vade tarihinden itibaren 30 gün içinde ödenmesi olasılığını yüzde 13 ve faturanın vade tarihinden sonraki 30 günden daha geç ödenme olasılığını yüzde 16 olarak gösterdiğini varsayalım.</span><span class="sxs-lookup"><span data-stu-id="52fde-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="52fde-126">En yüksek olasılık, faturanın zamanında ödeneceği senaryoda gösterilir bu nedenle fatura, zamanında ödenme olasılığıyla etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="52fde-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="52fde-127">[![Ödeme öngörüleri](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="52fde-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="52fde-128">Optimizasyon stratejileri</span><span class="sxs-lookup"><span data-stu-id="52fde-128">Optimization strategies</span></span>

<span data-ttu-id="52fde-129">Müşteri Ödeme Bilgileri (önizleme), ödeme öngörülerine ek olarak zamanında ödeme alma şansını artırmak için optimizasyon stratejileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="52fde-130">Bu şekilde kuruluşlar, kullanıcıların fatura ve müşteri parametrelerini ayarlamasına ve ardından faturaların zamanında ödenme olasılığına karşılık gelen etkiyi karşılaştırmasına izin vererek "Ya ise" analizi yapabilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="52fde-131">Örneğin, bir kuruluş ödemeyi zamanında alma olasılığına faturalardaki nakit iskontosu güncelleştirmesinin etkisini değerlendirmek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="52fde-132">Faturalar yeni iskontoyu kullanmak üzere optimize edildiğinde, kullanıcılar bu faturalar için zamanında ödeme alma olasılığına yapılan iskontonun etkisini inceleyebilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="52fde-133">İskontoyu uygulamanın maliyeti, ödemenin zamanında tahsil edilmesiyle karşılaştırıldığında daha düşükse kuruluş seçilen iskontoyu gelecekteki tüm açık siparişlere uygulamayı tercih edebilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="52fde-134">Şu anda Müşteri ödeme bilgileri (önizleme) için optimizasyon stratejisi olarak yalnızca iskonto kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="52fde-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="52fde-135">[![Optimize edilmiş öngörüler](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="52fde-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="52fde-136">Müşteri ödeme bilgilerini (önizleme) edinme</span><span class="sxs-lookup"><span data-stu-id="52fde-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="52fde-137">Müşteri ödeme bilgilerini (önizleme) denemekle ilgileniyorsanız lütfen [Mali Bilgiler Önizleme ekibine](mailto:fiap@microsoft.com) e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="52fde-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="52fde-138">Gizlilik Bildirimi</span><span class="sxs-lookup"><span data-stu-id="52fde-138">Privacy Statement</span></span>

<span data-ttu-id="52fde-139">Önizlemeler, müşteri verilerini Amerika Birleşik Devletleri’nde saklar.</span><span class="sxs-lookup"><span data-stu-id="52fde-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="52fde-140">Ayrıca önizlemeler (1), Dynamics 365 for Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri kullanmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="52fde-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>
