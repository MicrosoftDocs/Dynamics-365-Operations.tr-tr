---
title: "Servis yönetimi"
description: "Servis Yönetimini servis sözleşmeleri ve servis abonelikleri ayarlamak, servis siparişlerini ve müşteri sorgularını işlemek ve servislerin müşterilere teslimini yönetmek ve incelemek için kullanın."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="c725d-103">Servis yönetimi</span><span class="sxs-lookup"><span data-stu-id="c725d-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c725d-104">**Servis Yönetimini** servis sözleşmeleri ve servis abonelikleri ayarlamak, servis siparişlerini ve müşteri sorgularını işlemek ve servislerin müşterilere teslimini yönetmek ve incelemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="c725d-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="c725d-105">Servis sözleşmelerini normal servis ziyaretinde kullanılan kaynakları tanımlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c725d-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="c725d-106">Servis sözleşmelerini bu kaynakların müşteriye nasıl faturalandığını görüntülemek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c725d-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="c725d-107">Servis sözleşmesi standart yanıt sürelerini belirten ve gerçek zamanı kaydetmek için araçlar sunan bir hizmet düzeyi sözleşmesi de içerebilir.</span><span class="sxs-lookup"><span data-stu-id="c725d-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="c725d-108">Bir müşterinin tesisine servis teknisyeni tarafından yapılan zamanlanmış ve zamanlanmamış ziyaretlerle ilgili bilgileri yönetmek için servis siparişleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c725d-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="c725d-109">Servis siparişleri aşağıdaki gibi bilgileri içerir:</span><span class="sxs-lookup"><span data-stu-id="c725d-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="c725d-110">Servis teknisyeninin gerçekleştireceği çalışma saatleri</span><span class="sxs-lookup"><span data-stu-id="c725d-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="c725d-111">Servis veya onarım türü</span><span class="sxs-lookup"><span data-stu-id="c725d-111">The type of service or repair</span></span>

3.  <span data-ttu-id="c725d-112">Belirtilen ve tanı ile ilgili bilgiler dahil olmak üzere onarılan madde</span><span class="sxs-lookup"><span data-stu-id="c725d-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="c725d-113">Onarım veya hizmet ile ilişkili tüm gider ve masraflar</span><span class="sxs-lookup"><span data-stu-id="c725d-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="c725d-114">Enterprise Portal kullanarak müşteriler internet üzerinden servis istekleri gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="c725d-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="c725d-115">Bu talepleri alabilir, işleyebilir ve dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c725d-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="c725d-116">Bir servis siparişi oluşturduktan sonra ilerlemeyi izlemek için servis aşamalarını kullanabilir ve her aşamada hangi eylemlerin etkinleştirileceğini denetleyen kurallar belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c725d-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="c725d-117">Bir servis siparişi tamamlandıktan sonra tamamlandığından emin olmak için siparişte oturumu kapatıp fatura işlemini başlatmak üzere sipariş gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c725d-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="c725d-118">Servis siparişi marjlarını ve abonelik hareketlerini izlemek için raporlama araçlarını kullanın ve iş açıklamaları ile iş girişlerini yazdırın.</span><span class="sxs-lookup"><span data-stu-id="c725d-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="c725d-119">İş süreçleri</span><span class="sxs-lookup"><span data-stu-id="c725d-119">Business processes</span></span>

<span data-ttu-id="c725d-120">Aşağıdaki şemada **Servis yönetimi** için üst düzey iş süreçleri ve servis süreçlerinin Microsoft Dynamics 365 for Finance and Operations'daki diğer modüllerle hangi noktada tümleştirildikleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c725d-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="c725d-121">[![Servis yönetimi iş süreci şeması](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="c725d-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="c725d-122">Bir bakışta servis yönetimi</span><span class="sxs-lookup"><span data-stu-id="c725d-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c725d-123">Önemli görevler</span><span class="sxs-lookup"><span data-stu-id="c725d-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="c725d-124">Birincil formlar</span><span class="sxs-lookup"><span data-stu-id="c725d-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="c725d-125">Sık kullanılan raporlar</span><span class="sxs-lookup"><span data-stu-id="c725d-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c725d-126">Servis sözleşmelerini karşılama</span><span class="sxs-lookup"><span data-stu-id="c725d-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="c725d-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Servis anlaşmaları (form)</a></span><span class="sxs-lookup"><span data-stu-id="c725d-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="c725d-128"><strong>Servis siparişi sınırı</strong></span><span class="sxs-lookup"><span data-stu-id="c725d-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c725d-129">Müşteri sorgularını işle</span><span class="sxs-lookup"><span data-stu-id="c725d-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="c725d-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Servis siparişleri (form)</a></span><span class="sxs-lookup"><span data-stu-id="c725d-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="c725d-131"><strong>İş açıklaması</strong></span><span class="sxs-lookup"><span data-stu-id="c725d-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="c725d-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Gönderme panosu (form)</a></span><span class="sxs-lookup"><span data-stu-id="c725d-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="c725d-133"><strong>Hareket - abonelik</strong></span><span class="sxs-lookup"><span data-stu-id="c725d-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c725d-134"><strong>Abonelik ücreti hareketleri</strong></span><span class="sxs-lookup"><span data-stu-id="c725d-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="c725d-135">Servis yönetimi tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="c725d-135">Integration of Service management</span></span>

<span data-ttu-id="c725d-136">Servis yönetimi Microsoft Dynamics 365 for Finance and Operations'daki şu modüllerle tümleştirilebilir:</span><span class="sxs-lookup"><span data-stu-id="c725d-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="c725d-137">Satış ve pazarlama</span><span class="sxs-lookup"><span data-stu-id="c725d-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="c725d-138">İnsan kaynakları</span><span class="sxs-lookup"><span data-stu-id="c725d-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


