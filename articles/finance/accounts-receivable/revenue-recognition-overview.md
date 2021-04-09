---
title: Gelir kabulüne genel bakış
description: Bu konuda, Gelir kabulü özelliğiyle ilgili bilgiler verilir. Bu özellik, birden fazla öğe içeren siparişler için hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıtan esnek bir çerçeve sağlar.
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: edc0bab7287e271f1d1197d87a95709599e12b5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820557"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="ad078-104">Gelir kabulüne genel bakış</span><span class="sxs-lookup"><span data-stu-id="ad078-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad078-105">Ürünler, hizmetler, abonelikler gibi birden fazla öğe satan sektör şirketlerin çok öğeli siparişleri ayırabilmesi gerekir. Böylece, gelir şirkete özel ve sektöre özel kurallar kümesi temel alınarak kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="ad078-106">Gelir kabulü özelliği Özellik yönetiminden açılamaz.</span><span class="sxs-lookup"><span data-stu-id="ad078-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="ad078-107">Şu anda, bu özelliği etkinleştirmek için yapılandırma anahtarları kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad078-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="ad078-108">Paket işlevi dahil olmak üzere gelir kabulünün, Commerce kanallarında (e-ticaret, POS, çağrı merkezi) kullanımı desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="ad078-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="ad078-109">Gelir kabulü ile yapılandırılan maddeler, Commerce kanallarında oluşturulan siparişlere veya hareketlere eklenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="ad078-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="ad078-110">Genel olarak, gelir kabulü işlemi aşağıdaki görevleri gerçekleştirmek için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="ad078-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="ad078-111">Uygun gelir fiyatının çok öğeli siparişlerdeki bileşenlerin değerine göre kabul edilmesini sağlamaya yardımcı olmak amacıyla gelir tahsis etmek.</span><span class="sxs-lookup"><span data-stu-id="ad078-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="ad078-112">Gelirin zaman içinde kabul edilmesine yönelik sözleşmedeki zaman aralığını ve yüzdelerini temsil eden bir gelir planını temel alarak geliri ertelemek.</span><span class="sxs-lookup"><span data-stu-id="ad078-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="ad078-113">[Dynamics 365 Finance'ta gelir kabulünü kullanma](https://youtu.be/v3amIsiqvoo) videosu (yukarıda gösterilen) YouTube'daki [Finance and Operations oynatma listesine](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="ad078-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="ad078-114">Gelir kabulü özelliği, hem gelir fiyatını hem de gelir planını kabul etmeye yönelik şirkete özgü kurallar tanımlamanıza olanak tanıyan esnek bir çerçeve sağlar.</span><span class="sxs-lookup"><span data-stu-id="ad078-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="ad078-115">Serbest bırakılan ürünler, satış siparişi belgelerinde gelir kabulünü desteklemek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ad078-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="ad078-116">Serbest bırakılan ürünler, gelir fiyatını ve gelir planını belirlemek için gerekli olan ayarı içerir.</span><span class="sxs-lookup"><span data-stu-id="ad078-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="ad078-117">Satış siparişi bir Zaman ve malzeme projesinden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="ad078-118">Şirketler gelir planı işlevini, gelir fiyatı işlevini kullanmadan kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="ad078-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="ad078-119">Bu nedenle, satış siparişi satırlarındaki fiyat, gelir veya ertelenen gelir olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ad078-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="ad078-120">Satış siparişi satırında bir gelir planı varsa, satış siparişi satırındaki fiyat ertelenir.</span><span class="sxs-lookup"><span data-stu-id="ad078-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="ad078-121">Satış siparişi satırında gelir planı yoksa, satış siparişi satırındaki fiyat faturalandığında bir gelir hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="ad078-122">Gelir fiyatı satış siparişi onayladığında veya fatura deftere nakledildiğinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="ad078-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="ad078-123">Fatura deftere nakledilmeden önce gelir fiyatı önizlemesini görmek için satış siparişini onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ad078-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="ad078-124">Satış siparişi onaylandığında, herhangi bir satış siparişi satırı bir gelir planına sahipse beklenen bir gelir planı da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ad078-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="ad078-125">Satış siparişi faturalandığında, beklenen gelir planı silinir ve beklenen gelir planı gerçek gelir kabulü planıyla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="ad078-126">Gelir kabulü planının ayrıntıları her satış siparişi satırı için korunur.</span><span class="sxs-lookup"><span data-stu-id="ad078-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="ad078-127">Bu nedenle, gelir kabulü yöneticisi ayrıntıları görebilir ve sözleşme yükümlülüğü yerine getirildiğinde satırları gelir için serbest bırakabilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="ad078-128">Her dönemin sonunda, gelir kabulü yöneticisi, vadesi tanımladığı tarihte veya öncesinde olan plan satırlarını serbest bırakmak için bir gelir günlüğü oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="ad078-129">Bu gelir günlüğü hemen deftere nakledilemez.</span><span class="sxs-lookup"><span data-stu-id="ad078-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="ad078-130">Bu nedenle, gelir kabulü yöneticisi ertelenen gelirden fiili gelire doğru tutarların serbest bırakıldığını doğrulayabilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="ad078-131">Sözleşmedeki bir değişiklik var olan satış siparişine veya yeni satış siparişine yeni bir satış siparişi satırı eklenmesine neden olursa satış siparişlerindeki tüm satırlarda gelir fiyatını düzeltmek amacıyla bir yeniden tahsisat işlemi çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ad078-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]