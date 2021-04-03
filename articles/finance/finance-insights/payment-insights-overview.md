---
title: Müşteriye ödeme tahminleri (önizleme)
description: Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamanıza yardımcı olan ödeme tahmini özelliği açıklanmıştır. Bu özellik, tahsilat işlemlerini normalde yaptığınızdan daha erken başlatmanızı gerektiren durumları belirlemenize de yardımcı olabilir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 398320726a5749f80584ba281095a5dbd668ae87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241350"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="536ca-104">Müşteriye ödeme tahminleri (önizleme)</span><span class="sxs-lookup"><span data-stu-id="536ca-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="536ca-105">Bu konuda, müşterilerin tipik ödeme uygulamalarını daha iyi anlamanıza yardımcı olan ödeme tahmini özelliği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="536ca-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="536ca-106">Bu özellik, tahsilatları normalde yaptığınızdan daha erken başlatmanızı gerektiren durumları belirlemenize de yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="536ca-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="536ca-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="536ca-107">Overview</span></span>

<span data-ttu-id="536ca-108">Kuruluşlar genellikle müşterilerinin faturalarını ne zaman ödeyeceklerini öngörmede zorluk yaşar.</span><span class="sxs-lookup"><span data-stu-id="536ca-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="536ca-109">Bu içgörü eksikliği, aşağıdaki sorunlara neden olabilir:</span><span class="sxs-lookup"><span data-stu-id="536ca-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="536ca-110">Daha az doğru nakit akışı tahminleri</span><span class="sxs-lookup"><span data-stu-id="536ca-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="536ca-111">Çok geç başlayan tahsilat işlemleri</span><span class="sxs-lookup"><span data-stu-id="536ca-111">Collections processes that start too late</span></span>
- <span data-ttu-id="536ca-112">Borcunu ödeyemeyecek müşterilere gönderilen siparişler</span><span class="sxs-lookup"><span data-stu-id="536ca-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="536ca-113">Müşteri ödeme tahminleri (önizleme), müşteri faturasının ne zaman ödeneceğini tahmin etme konusunda kuruluşlara yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="536ca-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="536ca-114">Böylece, kuruluşlar zamanında ödeme alma olasılığı artırmaya yardımcı olan tahsilat stratejileri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="536ca-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="536ca-115">Öngörüler</span><span class="sxs-lookup"><span data-stu-id="536ca-115">Predictions</span></span>

<span data-ttu-id="536ca-116">Ödeme tahminleri, kuruluşların, geç ödenme olasılığı yüksek olan faturaları tanımlamasına yardımcı olacak iş süreçlerini geliştirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="536ca-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="536ca-117">Kuruluş, faturanın zamanından ödenmesi olasılığını artırmaya yardımcı olan önlemler almak için bu bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="536ca-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="536ca-118">Müşteri ödeme tahminleri özelliği, bir müşterinin bekleyen bir faturayı ne zaman ödeyeceğini daha doğru tahmin için bir makine öğrenimi modeli kullanır.</span><span class="sxs-lookup"><span data-stu-id="536ca-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="536ca-119">Bu makine öğrenimi modeli geçmiş faturaları, ödemeleri ve müşteri verilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="536ca-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="536ca-120">Her açık fatura için özellik, üç ödeme olasılığından birini atar:</span><span class="sxs-lookup"><span data-stu-id="536ca-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="536ca-121">Ödemenin zamanında yapılması olasılığı</span><span class="sxs-lookup"><span data-stu-id="536ca-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="536ca-122">Ödemenin geç yapılması olasılığı</span><span class="sxs-lookup"><span data-stu-id="536ca-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="536ca-123">Ödemenin çok geç yapılması olasılığı</span><span class="sxs-lookup"><span data-stu-id="536ca-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="536ca-124">Bu özellik ayrıca beklenen ödemelerin toplu görünümünü de sağlar.</span><span class="sxs-lookup"><span data-stu-id="536ca-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="536ca-125">[![Ödeme tahminlerinin toplu görünümü](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="536ca-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="536ca-126">Her faturaya, zamanında ödeme yapılma olasılığı atanır.</span><span class="sxs-lookup"><span data-stu-id="536ca-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="536ca-127">Zamanında ödeme olasılığı yüzde 50'nin altında olan faturalar, tahsilat temsilcisinin ilgilenmesinin gerekebileceğini belirtmek için kırmızı bir daireyle işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="536ca-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="536ca-128">[![Ödeme olasılıklarının listesi](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="536ca-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="536ca-129">Müşteri ödeme tahminleri özelliği, tahmini açıklamak için bağlam hakkında bilgiler de sağlar.</span><span class="sxs-lookup"><span data-stu-id="536ca-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="536ca-130">Bu bilgiler arasında tahmini etkileyen başlıca etmenler, müşteriyle işin geçerli durumu ve müşterinin geçmiş ödeme davranışıyla ilgili ayrıntılar yer alır.</span><span class="sxs-lookup"><span data-stu-id="536ca-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="536ca-131">Birçok işletmede tahsilat işlemi reaktif bir faaliyettir.</span><span class="sxs-lookup"><span data-stu-id="536ca-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="536ca-132">Diğer bir ifadeyle tahsilat işlemi, faturaların vadesi gelene kadar başlamaz.</span><span class="sxs-lookup"><span data-stu-id="536ca-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="536ca-133">Müşteri ödeme tahminleri, kuruluşların tahsilatlar konusunda daha proaktif olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="536ca-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="536ca-134">Kuruluşun tahsilat sürecini başlatmak için hareketin gerçekleşme zamanını beklemesine gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="536ca-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="536ca-135">Bunun yerine, proaktif tahsilatların zamanında ödenme olasılığını artırıp artırmayacağını belirlemek için ödeme tahminleri özelliğini kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="536ca-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="536ca-136">Metodoloji</span><span class="sxs-lookup"><span data-stu-id="536ca-136">Methodology</span></span>

<span data-ttu-id="536ca-137">Geçmişte, yapay zeka (AI) çözümü geliştirmek ve dağıtmak genellikle zordu.</span><span class="sxs-lookup"><span data-stu-id="536ca-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="536ca-138">Kullanılabilir bir AI çözümünü formüle etmek, geliştirmek, dağıtmak ve korumak için uzun zamandır çalışmakta olan veri bilimcileri, konu uzmanları (SME'ler) ve mühendislerden oluşan bir takım gerekliydi.</span><span class="sxs-lookup"><span data-stu-id="536ca-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="536ca-139">Müşteri ödeme tahminleri, Microsoft Dynamics 365 Finance'te bir AI çözümünü dağıtmayı ve kullanmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="536ca-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="536ca-140">Microsoft, Microsoft AI Builder üzerine inşa edilen AI çözümlerini önceden hazırlayıp sunuyor.</span><span class="sxs-lookup"><span data-stu-id="536ca-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="536ca-141">Böylece kullanıcılar, akıllı tahminlerin avantajlarından yararlanmak için tek bir fare tıklamasıyla AI çözümünü dağıtabiliyor.</span><span class="sxs-lookup"><span data-stu-id="536ca-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="536ca-142">Tahminlerin doğruluğundan memnun kalmazsanız bir uzman kullanıcı yine tek tıkla AI builder uzantısı deneyimine girebilir ve ardından tahminler oluşturmak için kullanılan alanları seçebilir veya alanların seçimini kaldırabilir.</span><span class="sxs-lookup"><span data-stu-id="536ca-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="536ca-143">Hazır olduğunuzda modeli "eğitebilirsiniz" ve değişiklikleri yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="536ca-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="536ca-144">Yeni eğitilen model, Dynamics 365 Finance'te tahmin oluşturmak için otomatik olarak seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="536ca-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="536ca-145">Serbest bırakma ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="536ca-145">Release details</span></span>

<span data-ttu-id="536ca-146">Mali İçgörüler genel önizleme, Amerika Birleşik Devletleri, Avrupa ve Birleşik Krallık'ta deneme için sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="536ca-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="536ca-147">Microsoft, destek sunduğu bölgeleri kademeli olarak artırmaktadır.</span><span class="sxs-lookup"><span data-stu-id="536ca-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="536ca-148">Genel önizleme özellikleri, yalnızca Katman 2 korumalı alan ortamlarında açılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="536ca-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="536ca-149">Korumalı alan ortamında oluşturulan kurulum ve AI modelleri, üretim ortamına geçirilemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="536ca-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="536ca-150">Daha fazla bilgi için bkz. [Microsoft Dynamics 365 Önizlemeleri için Ek Kullanım Koşulları](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="536ca-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="536ca-151">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="536ca-151">Privacy notice</span></span>

<span data-ttu-id="536ca-152">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="536ca-152">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]