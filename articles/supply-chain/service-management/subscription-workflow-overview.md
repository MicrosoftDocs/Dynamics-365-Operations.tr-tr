---
title: Abonelik iş akışı özeti
description: Bu konu, abonelik iş akışına genel bir bakış sağlar.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5cff6910dcb273fc081443546676426387f6625
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566422"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="fdb4a-103">Abonelik iş akışı özeti</span><span class="sxs-lookup"><span data-stu-id="fdb4a-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fdb4a-104">Aydınlatma donanımı bakımı için abonelikler sunan bir aydınlatma şirketi için abonelik yöneticisisiniz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="fdb4a-105">Bir müşteriniz, aydınlatma donanımı bakımı için yıllık bir abonelik satın almak amacıyla şirketinize başvuruyor.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="fdb4a-106">Abonelikler ayarlama</span><span class="sxs-lookup"><span data-stu-id="fdb4a-106">Setting up subscriptions</span></span>

<span data-ttu-id="fdb4a-107">Bir abonelik ayarlamak için öncelikler yeni hizmet sözleşmesi için bir abonelik grubu oluşturmanız veya bir abonelik grubu bulunduğunu doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="fdb4a-108">Bir abonelik grubu zaten varsa, bunu müşteriyi yıllık olarak faturalandırmak ve satış gelirini yılın her ayı tahakkuk edecek şekilde ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="fdb4a-109">Aboneliklerin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Abonelik grupları ayarlama](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="fdb4a-110">Abonelik grubu oluşturulduktan sonra aboneliği oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="fdb4a-111">Servis abonelikleri oluşturma hakkında daha fazla bilgi için bkz. [Abonelik grubundan servis abonelikleri oluşturma](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="fdb4a-112">Abonelik hareketleri oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="fdb4a-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="fdb4a-113">Abonelik ayarladıktan sonra bir yıl olan ilk faturalama dönemine yönelik abonelik ücreti hareketi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="fdb4a-114">Hareketler **Normal** türünde olur.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="fdb4a-115">Bu nedenle, yalnızca başlangıç tarihi ve bitiş tarihi **Dönem türleri** formunda önceden oluşturulmuş döneme karşılık gelen abonelik hareketleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="fdb4a-116">Ücret hareketleriyle ilgili daha fazla bilgi için bkz. [Abonelik ücreti hareketleri oluşturma](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="fdb4a-117">Müşteriniz için abonelik ayarladıktan sonra servis teklifleri için tüm fiyat listesi üzerinden yüzde 10 indirim anlaşması yapmış olduğunuzu hatırlarsınız.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="fdb4a-118">Bu nedenle, oluşturduğunuz hareket ücretinin fiyatını indirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="fdb4a-119">Günün ilerleyen bölümünde, müşteriniz sizi arayacak aydınlatma donanımı için servis sözleşmesini hala istediklerini ancak yıl içinde yeni bir aydınlatma donanımı edineceklerini bildirir.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="fdb4a-120">Bu nedenle, yalnızca Ekim 2013'e kadar bakım hizmetine gereksinim duymaktadırlar.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="fdb4a-121">Müşteri aboneliğinden ay sayısını indirmek için **Azaltma günleri** türünde yeni bir abonelik ücreti hareketi oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="fdb4a-122">Gün azaltma hakkında daha fazla bilgi için bkz. [Abonelik ücretlerinde günleri azaltma](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="fdb4a-123">Abonelik hareketlerini faturalandırma ve tahakkuk ettirme</span><span class="sxs-lookup"><span data-stu-id="fdb4a-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="fdb4a-124">Abonelik ayarlamayı tamamladınız ve müşterinizi bunun için faturalandırmaya hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="fdb4a-125">Aboneliklerin nasıl faturalandırılacağı hakkında daha fazla bilgi için bkz. [Abonelik hareketlerini faturalandırma](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="fdb4a-126">İki gün sonra, müşteriniz sizi arayarak aboneliğin Euro değil ABD doları olarak faturalandırılması gerektiğini söyler.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="fdb4a-127">Bu nedenle, bir alacak dekontu ve doğru para birimi cinsinde yeni bir abonelik hareketi oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="fdb4a-128">Abonelik hareketlerini alacaklandırma hakkında daha fazla bilgi için bkz. [Abonelik hareketlerini alacaklandırma](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="fdb4a-129">Her ayın sonunda, müşterinin aboneliğinden gelen bir aylık geliri kar-zarar hesabına ve süren iş hesaplarına tahakkuk ettirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdb4a-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="fdb4a-130">Abonelikler için gelir tahakkuk ettirme hakkında daha fazla bilgi için, bkz. [Abonelik geliri tahakkuku](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="fdb4a-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


