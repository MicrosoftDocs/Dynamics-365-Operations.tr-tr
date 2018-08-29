---
title: "Çağrı merkezleri için süreklilik programları kurma"
description: "Bu makalede, çağrı merkezi için bir süreklilik programının nasıl kurulacağı açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 9952785afd8e5d1877e96239ee23f9de1c332bcf
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="e1cdf-103">Çağrı merkezleri için süreklilik programları kurma</span><span class="sxs-lookup"><span data-stu-id="e1cdf-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1cdf-104">Bu makalede, çağrı merkezi için bir süreklilik programının nasıl kurulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="e1cdf-105">Yinelenen sipariş programı olarak da bilinen olan süreklilik programında müşteriler önceden tanımlanmış bir plana uygun olarak düzenli ürün sevkiyatları alır.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="e1cdf-106">Her bir sevkiyat bir 'ayın kitabı kulübünde' olduğu gibi farklı bir ürün içerebilir veya aynı ürün tekrar tekrar gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="e1cdf-107">Bir süreklilik programı kurmak için mutlaka aşağıdaki görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="e1cdf-108">**Çağrı merkezi parametreleri** sayfasından süreklilik parametrelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="e1cdf-109">Ödeme planı, sevkiyatların zamanlaması ve faturanın önceden düzenlenip düzenlenmeyeceği gibi ayrıntıları belirten bir süreklilik programı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="e1cdf-110">Ayrıca, süreklilik programına dahil edilecek ürünlerin bir listesini de eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="e1cdf-111">Her ürün 1'den başlayarak sıralı atanan bir olay kod numarası alır.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="e1cdf-112">Olay kodları, ürünlerin gönderilme sırasını belirler.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="e1cdf-113">Müşteriler her sevkiyatta farklı bir ürün alıyorsa ürünler, olay kimliklerine dayalı olarak ve mevcut olaydan başlayarak ardışık olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="e1cdf-114">Müşteriler her sevkiyatta aynı ürünü alıyorsa liste sadece bir olaya sahip bir ürün içerir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="e1cdf-115">Aynı olay tekrar tekrar oluşur.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="e1cdf-116">Her olayın kaç defa tekrarlanacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="e1cdf-117">Görev 2'de oluşturduğunuz süreklilik programını temsil eden bir üst ürün oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="e1cdf-118">Bu ürünü bir satış siparişine eklerseniz **Süreklilik** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="e1cdf-119">Ardından, fiili süreklilik siparişi oluşturmak için bu sayfayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="e1cdf-120">Üst ürün müşterinin her sevkiyatta aldığı ürünler tek tek belirtmez.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="e1cdf-121">Yukarıda açıklandığı gibi bir süreklilik programı ayarladıktan sonra müşteri için bir süreklilik siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="e1cdf-122">Ayrıca, aşağıdaki ek idame görevlerini de gerçekleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="e1cdf-123">**Mevcut süreklilik olay dönemini güncelleştir** – Sisteme mevcut olay döneminin ne olacağını söyleyen bir toplu iş oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="e1cdf-124">**Süreklilik alt siparişleri oluştur** – Üst süreklilik siparişinden alt siparişler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="e1cdf-125">**Süreklilik ödemelerini işle** – Süreklilik satış siparişleriyle ilişkili ödemeler için faturalamayı ve bildirimleri işleyin.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="e1cdf-126">**Süreklilik satırlarını genişlet** (gerekiyorsa) – Bir süreklilik olayının tekrarlanabileceği sayıyı girin.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="e1cdf-127">Sevkiyatların tekrarlanması çağrı merkezi parametrelerindeki **Süreklilik tekrar eşiği** alanında ayarlanan sınırın ötesinde de genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="e1cdf-128">**Bir süreklilik güncelleştirmesi gerçekleştir** (gerekiyorsa) – Süreklilik programı ile süreklilik üst satış siparişleri arasındaki değişiklikleri eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="e1cdf-129">**Süreklilik üst satırlarını ve siparişlerini kapat** – Süreklilik siparişlerini kapatın.</span><span class="sxs-lookup"><span data-stu-id="e1cdf-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





