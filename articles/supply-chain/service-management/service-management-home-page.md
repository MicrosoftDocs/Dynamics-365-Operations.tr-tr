---
title: Servis yönetimine genel bakış
description: Servis Yönetimini servis sözleşmeleri ve servis abonelikleri ayarlamak, servis siparişlerini ve müşteri sorgularını işlemek ve servislerin müşterilere teslimini yönetmek ve incelemek için kullanın.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1d7c6960dc48bb1bb780ecbbb36a58a1bbd7352
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908220"
---
# <a name="service-management-overview"></a><span data-ttu-id="bb1fe-103">Servis yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="bb1fe-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="bb1fe-104">**Servis Yönetimini** servis sözleşmeleri ve servis abonelikleri ayarlamak, servis siparişlerini ve müşteri sorgularını işlemek ve servislerin müşterilere teslimini yönetmek ve incelemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="bb1fe-105">Servis sözleşmelerini normal servis ziyaretinde kullanılan kaynakları tanımlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="bb1fe-106">Servis sözleşmelerini bu kaynakların müşteriye nasıl faturalandığını görüntülemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="bb1fe-107">Servis sözleşmesi standart yanıt sürelerini belirten ve gerçek zamanı kaydetmek için araçlar sunan bir hizmet düzeyi sözleşmesi de içerebilir.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="bb1fe-108">Bir müşterinin tesisine servis teknisyeni tarafından yapılan zamanlanmış ve zamanlanmamış ziyaretlerle ilgili bilgileri yönetmek için servis siparişleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="bb1fe-109">Servis siparişleri aşağıdaki gibi bilgileri içerir:</span><span class="sxs-lookup"><span data-stu-id="bb1fe-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="bb1fe-110">Servis teknisyeninin gerçekleştireceği çalışma saatleri</span><span class="sxs-lookup"><span data-stu-id="bb1fe-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="bb1fe-111">Servis veya onarım türü</span><span class="sxs-lookup"><span data-stu-id="bb1fe-111">The type of service or repair</span></span>

3.  <span data-ttu-id="bb1fe-112">Belirtilen ve tanı ile ilgili bilgiler dahil olmak üzere onarılan madde</span><span class="sxs-lookup"><span data-stu-id="bb1fe-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="bb1fe-113">Onarım veya hizmet ile ilişkili tüm gider ve masraflar</span><span class="sxs-lookup"><span data-stu-id="bb1fe-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="bb1fe-114">Servis taleplerini alabilir, işleyebilir ve dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="bb1fe-115">Bir servis siparişi oluşturduktan sonra ilerlemeyi izlemek için servis aşamalarını kullanabilir ve her aşamada hangi eylemlerin etkinleştirileceğini denetleyen kurallar belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="bb1fe-116">Bir servis siparişi tamamlandıktan sonra tamamlandığından emin olmak için siparişte oturumu kapatıp fatura işlemini başlatmak üzere sipariş gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="bb1fe-117">Servis siparişi marjlarını ve abonelik hareketlerini izlemek için raporlama araçlarını kullanın ve iş açıklamaları ile iş girişlerini yazdırın.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="bb1fe-118">İş süreçleri</span><span class="sxs-lookup"><span data-stu-id="bb1fe-118">Business processes</span></span>

<span data-ttu-id="bb1fe-119">Aşağıdaki şemada **Servis yönetimi** için üst düzey iş süreçleri ve servis süreçlerinin diğer modüllerle hangi noktada tümleştirildikleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bb1fe-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules.</span></span>

<span data-ttu-id="bb1fe-120">[![Servis yönetimi iş süreci şeması](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="bb1fe-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="bb1fe-121">Bir bakışta servis yönetimi</span><span class="sxs-lookup"><span data-stu-id="bb1fe-121">Service management at a glance</span></span>

|<span data-ttu-id="bb1fe-122">Önemli görevler</span><span class="sxs-lookup"><span data-stu-id="bb1fe-122">Important tasks</span></span>           | <span data-ttu-id="bb1fe-123">Birincil sayfalar</span><span class="sxs-lookup"><span data-stu-id="bb1fe-123">Primary pages</span></span>                         |<span data-ttu-id="bb1fe-124">Sık kullanılan raporlar</span><span class="sxs-lookup"><span data-stu-id="bb1fe-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="bb1fe-125">Servis sözleşmelerini karşılama</span><span class="sxs-lookup"><span data-stu-id="bb1fe-125">Fulfill service agreements</span></span>|<span data-ttu-id="bb1fe-126">Servis sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="bb1fe-126">Service agreements</span></span>                     |<span data-ttu-id="bb1fe-127">Servis siparişi sınırı</span><span class="sxs-lookup"><span data-stu-id="bb1fe-127">Service order margin</span></span>         |
|<span data-ttu-id="bb1fe-128">Müşteri sorgularını işle</span><span class="sxs-lookup"><span data-stu-id="bb1fe-128">Handle customer inquiries</span></span> |<span data-ttu-id="bb1fe-129">Servis siparişleri</span><span class="sxs-lookup"><span data-stu-id="bb1fe-129">Service orders</span></span>                         |<span data-ttu-id="bb1fe-130">İş açıklaması</span><span class="sxs-lookup"><span data-stu-id="bb1fe-130">Work description</span></span>             |
|                          |<span data-ttu-id="bb1fe-131">Gönderme panosu</span><span class="sxs-lookup"><span data-stu-id="bb1fe-131">Dispatch board</span></span>                         |<span data-ttu-id="bb1fe-132">Hareket - abonelik</span><span class="sxs-lookup"><span data-stu-id="bb1fe-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="bb1fe-133">Abonelik ücreti hareketleri</span><span class="sxs-lookup"><span data-stu-id="bb1fe-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="bb1fe-134">Servis yönetimi tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="bb1fe-134">Integration of Service management</span></span>

<span data-ttu-id="bb1fe-135">Servis yönetimi aşağıdaki modüllerle tümleştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="bb1fe-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="bb1fe-136">Satış ve pazarlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="bb1fe-136">Sales and marketing overview</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="bb1fe-137">İnsan kaynakları</span><span class="sxs-lookup"><span data-stu-id="bb1fe-137">Human resources</span></span>](/dynamics365/unified-operations/talent/index)

  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]