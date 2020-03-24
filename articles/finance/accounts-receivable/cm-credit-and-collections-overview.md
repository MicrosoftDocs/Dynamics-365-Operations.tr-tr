---
title: Alacak ve tahsilatlara genel bakış
description: Bu konu, alacak ve tahsilatlar işlevselliğine genel bir bakış sağlamaktadır.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a822e5f5a6cb71a0234b1776211788578470b0bb
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124312"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="47ae8-103">Alacak ve tahsilatlara genel bakış</span><span class="sxs-lookup"><span data-stu-id="47ae8-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47ae8-104">Müşterileriniz için kredi limitlerini yönetebilir ve gerekli olduklarında, tahsilat faaliyetleri gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47ae8-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="47ae8-105">Alacak yönetimi</span><span class="sxs-lookup"><span data-stu-id="47ae8-105">Credit management</span></span>

<span data-ttu-id="47ae8-106">Müşteri kredi yönetimi, oluşturduğunuz kredi kurallarına göre kredi limitlerini yönetmenizi ve deftere nakil işlemi aracılığıyla satış siparişlerinin akışını denetlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="47ae8-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="47ae8-107">Kredi yönetimi işlemi aşağıdaki adımlardan herhangi birini içerebilir:</span><span class="sxs-lookup"><span data-stu-id="47ae8-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="47ae8-108">Müşterilerin kredi tutarı hakkında ek bilgiler sağlamak için kredi niteliklerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="47ae8-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="47ae8-109">Kredi limiti ayarlamalarını kullanarak müşteriler için kredi limitleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47ae8-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="47ae8-110">Kredi limiti ayarlamalarını kullanarak geçici kredi limitleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47ae8-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="47ae8-111">Bu şekilde, iş gereksinimlerine göre müşteri kredi limitlerini geçici olarak artırabilir veya azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47ae8-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="47ae8-112">Kredi limitini etkileyebilen bilgiler (sigorta ve garantiler hakkındaki bilgiler vb.) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="47ae8-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="47ae8-113">Müşterileri tek bir kredi limitini paylaşacak şekilde birbirine bağlayan müşteri kredi grupları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47ae8-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="47ae8-114">Müşterilere risk puanları atayın ve daha sonra kredi limiti ayarlamalarıyla bu müşteriler için otomatik olarak kredi limitleri oluşturmada bu puanları kullanın.</span><span class="sxs-lookup"><span data-stu-id="47ae8-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="47ae8-115">Risk, ödeme koşulları, kredi limitleri, vadesi geçmiş tutarlar ve kullanılmış kredi limiti yüzdesi gibi faktörlere bağlı olarak bir veya daha fazla deftere nakil işlemi sırasında siparişi beklemeye alan durdurma kuralları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="47ae8-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="47ae8-116">Beklemedeki satış siparişlerinin listesini yönetin, bekletme nedenlerini inceleyin ve sorunları çözün.</span><span class="sxs-lookup"><span data-stu-id="47ae8-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="47ae8-117">Satış siparişlerini, deftere nakil işlemi üzerinden devam edecek şekilde serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="47ae8-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="47ae8-118">Kredi limiti değişikliklerinin ve satış siparişi serbest bırakma işlemlerinin onayını yönetmek için bir iş akışı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="47ae8-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="47ae8-119">Tahsilat yönetimi</span><span class="sxs-lookup"><span data-stu-id="47ae8-119">Collections management</span></span>

<span data-ttu-id="47ae8-120">**Tahsilatlar** sayfası, alacak hesapları tahsilat bilgilerinin yönetildiği tek bir merkezi görünüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="47ae8-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="47ae8-121">Tahsilat yöneticileri, tahsilatları yönetmek için bu merkezi görünümü kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="47ae8-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="47ae8-122">Tahsilat temsilcileri, tahsilat işlemine önceden tanımlanmış tahsilat ölçütlerini kullanarak oluşturulmuş müşteri listelerinden veya **Müşteriler** sayfasından başlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="47ae8-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="47ae8-123">Tahsilatları ayarlamaya veya bunlar üzerinde çalışmaya başlamadan önce aşağıdaki kavramları anlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="47ae8-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="47ae8-124">Müşteri yaşlandırma anlık görüntüsü belirli bir zamandaki yaşlandırılmış bakiye bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="47ae8-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="47ae8-125">Tahsilat müşteri havuzları işinizi organize etmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="47ae8-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="47ae8-126">Tahsilat temsilcilerinin kendi müşteri havuzları olabilir.</span><span class="sxs-lookup"><span data-stu-id="47ae8-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="47ae8-127">Liste sayfaları tahsilat müşterilerini, etkinlikleri ve vakaları organize eder.</span><span class="sxs-lookup"><span data-stu-id="47ae8-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="47ae8-128">Bir müşteriyle ilgili tüm tahsilat bilgileri tek bir sayfada bulunur ve bu sayfadan eylem gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47ae8-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="47ae8-129">Faiz ve ücretlerden feragat etme, bunları eski durumuna getirme veya tersine çevirme işlemi tek bir adımda yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="47ae8-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="47ae8-130">Silme hareketleri tek bir adımda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="47ae8-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="47ae8-131">Yetersiz fon (NSF) ödemeleri tek adımda işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="47ae8-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="47ae8-132">Bu kavramların açıklamaları için bkz. [Tahsilat yönetimi temel kavramları](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="47ae8-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47ae8-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="47ae8-133">Additional resources</span></span>

[<span data-ttu-id="47ae8-134">Müşteri kredi yönetimi parametreleri kurulumu</span><span class="sxs-lookup"><span data-stu-id="47ae8-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="47ae8-135">Müşteri kredi yönetimi kurulum bilgileri</span><span class="sxs-lookup"><span data-stu-id="47ae8-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="47ae8-136">Müşteri için alacak yönetimi bilgileri ekleme</span><span class="sxs-lookup"><span data-stu-id="47ae8-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="47ae8-137">Müşteri alacak grupları</span><span class="sxs-lookup"><span data-stu-id="47ae8-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="47ae8-138">Müşteri kredi limiti ayarlamaları</span><span class="sxs-lookup"><span data-stu-id="47ae8-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="47ae8-139">Satış siparişleri için askıda krediler</span><span class="sxs-lookup"><span data-stu-id="47ae8-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="47ae8-140">Müşteri kredi yönetimi periyodik görevleri</span><span class="sxs-lookup"><span data-stu-id="47ae8-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
