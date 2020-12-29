---
title: Çağrı merkezleri için süreklilik programları kurma
description: Bu makalede, çağrı merkezi için bir süreklilik programının nasıl kurulacağı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 738841407b63ef604da092b7c8f4d0f2064d3886
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416304"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="46354-103">Çağrı merkezleri için süreklilik programları kurma</span><span class="sxs-lookup"><span data-stu-id="46354-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46354-104">Bu makalede, çağrı merkezi için bir süreklilik programının nasıl kurulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="46354-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="46354-105">Yinelenen sipariş programı olarak da bilinen olan süreklilik programında müşteriler önceden tanımlanmış bir plana uygun olarak düzenli ürün sevkiyatları alır.</span><span class="sxs-lookup"><span data-stu-id="46354-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="46354-106">Her bir sevkiyat bir 'ayın kitabı kulübünde' olduğu gibi farklı bir ürün içerebilir veya aynı ürün tekrar tekrar gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="46354-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="46354-107">Bir süreklilik programı kurmak için mutlaka aşağıdaki görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="46354-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="46354-108">**Çağrı merkezi parametreleri** sayfasından süreklilik parametrelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="46354-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="46354-109">Ödeme planı, sevkiyatların zamanlaması ve faturanın önceden düzenlenip düzenlenmeyeceği gibi ayrıntıları belirten bir süreklilik programı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46354-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="46354-110">Ayrıca, süreklilik programına dahil edilecek ürünlerin bir listesini de eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="46354-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="46354-111">Her ürün 1'den başlayarak sıralı atanan bir olay kod numarası alır.</span><span class="sxs-lookup"><span data-stu-id="46354-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="46354-112">Olay kodları, ürünlerin gönderilme sırasını belirler.</span><span class="sxs-lookup"><span data-stu-id="46354-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="46354-113">Müşteriler her sevkiyatta farklı bir ürün alıyorsa ürünler, olay kimliklerine dayalı olarak ve mevcut olaydan başlayarak ardışık olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="46354-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="46354-114">Müşteriler her sevkiyatta aynı ürünü alıyorsa liste sadece bir olaya sahip bir ürün içerir.</span><span class="sxs-lookup"><span data-stu-id="46354-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="46354-115">Aynı olay tekrar tekrar oluşur.</span><span class="sxs-lookup"><span data-stu-id="46354-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="46354-116">Her olayın kaç defa tekrarlanacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46354-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="46354-117">Görev 2'de oluşturduğunuz süreklilik programını temsil eden bir üst ürün oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46354-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="46354-118">Bu ürünü bir satış siparişine eklerseniz **Süreklilik** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="46354-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="46354-119">Ardından, fiili süreklilik siparişi oluşturmak için bu sayfayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46354-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="46354-120">Üst ürün müşterinin her sevkiyatta aldığı ürünler tek tek belirtmez.</span><span class="sxs-lookup"><span data-stu-id="46354-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="46354-121">Yukarıda açıklandığı gibi bir süreklilik programı ayarladıktan sonra müşteri için bir süreklilik siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46354-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="46354-122">Ayrıca, aşağıdaki ek idame görevlerini de gerçekleştirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="46354-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="46354-123">**Mevcut süreklilik olay dönemini güncelleştir** – Sisteme mevcut olay döneminin ne olacağını söyleyen bir toplu iş oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46354-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="46354-124">**Süreklilik alt siparişleri oluştur** – Üst süreklilik siparişinden alt siparişler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46354-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="46354-125">**Süreklilik ödemelerini işle** – Süreklilik satış siparişleriyle ilişkili ödemeler için faturalamayı ve bildirimleri işleyin.</span><span class="sxs-lookup"><span data-stu-id="46354-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="46354-126">**Süreklilik satırlarını genişlet** (gerekiyorsa) – Bir süreklilik olayının tekrarlanabileceği sayıyı girin.</span><span class="sxs-lookup"><span data-stu-id="46354-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="46354-127">Sevkiyatların tekrarlanması çağrı merkezi parametrelerindeki **Süreklilik tekrar eşiği** alanında ayarlanan sınırın ötesinde de genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="46354-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="46354-128">**Bir süreklilik güncelleştirmesi gerçekleştir** (gerekiyorsa) – Süreklilik programı ile süreklilik üst satış siparişleri arasındaki değişiklikleri eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="46354-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="46354-129">**Süreklilik üst satırlarını ve siparişlerini kapat** – Süreklilik siparişlerini kapatın.</span><span class="sxs-lookup"><span data-stu-id="46354-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>
