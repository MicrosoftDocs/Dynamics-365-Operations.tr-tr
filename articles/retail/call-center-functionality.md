---
title: "Çağrı merkezi işlevi"
description: "Bu makale Microsoft Dynamics 365 for Retail içerisindeki çağrı merkezi satış özelliği hakkında genel bakış sağlar."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 00d24e9933d087f150ec5270da94ad911423824d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="call-center-functionality"></a><span data-ttu-id="097c7-103">Çağrı merkezi işlevi</span><span class="sxs-lookup"><span data-stu-id="097c7-103">Call center functionality</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="097c7-104">Bu makale Microsoft Dynamics 365 for Retail içerisindeki çağrı merkezi satış özelliği hakkında genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="097c7-104">This article provides an overview of the call center sales functionality in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="097c7-105">Dynamics for Retal'daki perakende, çağrı merkezlerini bir perakende kanalı türü olarak destekler.</span><span class="sxs-lookup"><span data-stu-id="097c7-105">Dynamics 365 for Retail supports call centers as a type of retail channel.</span></span> <span data-ttu-id="097c7-106">Çağrı merkezinde, çalışanlar müşterilerin siparişlerini telefonda alır ve satış siparişleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="097c7-106">In a call center, workers take orders from customers over the phone and create sales orders.</span></span> <span data-ttu-id="097c7-107">Çağrı merkezi işlevselliği, telefon siparişleri almayı ve karşılama işlevi boyunca müşteri hizmetlerini yönetmeyi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="097c7-107">Call center functionality includes features that are designed to make it easier to take phone orders and handle customer service throughout the order fulfillment process.</span></span> <span data-ttu-id="097c7-108">Örneğin, çağrı merkezi çalışanları, ödeme bilgisini doğrudan satış siparişine girebilir ve ücretler ve ödemelerin detaylı özetini, siparişi göndermeden önce görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="097c7-108">For example, call center workers can enter payment information directly into the sales order, and can view a detailed summary of charges and payments before they submit the order.</span></span> <span data-ttu-id="097c7-109">Çalışanların ayrıca fiyatlandırma denetlemek için seçeneği vardır ve **satış sipariş** sayfasından müşteriler, ürünler ve fiyatları ile ilgili çeşitli verilere erişebilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-109">Workers also have options for controlling pricing, and can access various data about customers, products, and prices from the **Sales order** page.</span></span> <span data-ttu-id="097c7-110">Ayrıca, çağrı merkezleri Gelişmiş müşteri geçmişi ve sipariş durumunu izlemek için işlevlere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="097c7-110">Additionally, call centers have enhanced functionality for tracking customer history and order status.</span></span> <span data-ttu-id="097c7-111">Her bir çağrı merkezinin kendi kullanıcıları, ödeme yöntemleri, fiyat grupları, mali boyutları ve teslimat modları olabilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-111">Each call center can have its own users, payment methods, price groups, financial dimensions, and modes of delivery.</span></span> <span data-ttu-id="097c7-112">Çağrı merkezi oluşturduğunuzda, bu seçenekleri yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="097c7-112">You can configure these options when you create the call center.</span></span> <span data-ttu-id="097c7-113">Ek olarak **çağrı merkezi** sayfasını çağrı merkezlerine özgü aşağıdaki özellikler gruplarını etkinleştirmek veya devre dışı bırakmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="097c7-113">Additionally, you can use the **Call center** page to enable or disable the following groups of features that are unique to call centers:</span></span>

-   <span data-ttu-id="097c7-114">**Sipariş tamamlama** – Bu grup ödemelerle ve **satış sipariş** sayfasındaki sipariş tamamlamayla ilgili özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="097c7-114">**Order completion** – This group includes features that are related to payments and order completion on the **Sales order** page.</span></span>
-   <span data-ttu-id="097c7-115">**Yönlendirilen satış** – Bu grup kaynak kodlar, komut dosyaları ve katalog talepleriyle ilgili özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="097c7-115">**Directed selling** – This group includes features that are related to source codes, scripts, and catalog requests.</span></span>

<span data-ttu-id="097c7-116">Bu özellikleri çağrı Merkezi ayarlarında etkinleştirdikten sonra **satış sipariş** sayfasında çağrı merkezi ile ilişkili olan kullanıcılar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-116">After you enable these features in the call center settings, they are available on the **Sales order** page to users who are associated with the call center.</span></span> <span data-ttu-id="097c7-117">Bu özelliklerin çoğu kullanılabilmesi için önce ek kurulum gerektirir.</span><span class="sxs-lookup"><span data-stu-id="097c7-117">Most of these features require additional setup before they can be used.</span></span> <span data-ttu-id="097c7-118">Kullanıcılar çağrı merkezi siparişleri oluşturmadan üzere önce, bu kullanıcıları çağrı merkezine çağrı merkezi kullanıcıları olarak eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="097c7-118">Before users can create call center orders, you must add those users to the call center as call center users.</span></span> <span data-ttu-id="097c7-119">Bu adım çağrı merkezi kanal özgü yapılandırma ve işlevselliği sağlar.</span><span class="sxs-lookup"><span data-stu-id="097c7-119">This step enables the call center channel-specific configuration and functionality.</span></span> <span data-ttu-id="097c7-120">Burada, kullanılabilir hale gelen işlevlere bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="097c7-120">Here are some examples of the functionality that becomes available:</span></span>

-   <span data-ttu-id="097c7-121">Destekli satış, tele-satış kodları ve ürün resimleri, siparişler'i alırken satış elemanı rehberlik ve Yardım için yapılandırma seçenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="097c7-121">Guided selling provides configuration options for telesales scripts and product images to help and guide sales clerks while they take orders.</span></span>
-   <span data-ttu-id="097c7-122">Siparişler, satış elemanı en az bir ödeme yöntemi yakalayana kadar tamamlanamaz.</span><span class="sxs-lookup"><span data-stu-id="097c7-122">Orders can't be completed until sales clerks have captured at least one payment method.</span></span>
-   <span data-ttu-id="097c7-123">Üst model satış ve çapraz satış kuralları belirli ürünleri müşteriye tanıtmak satış elemanından istenecek şekilde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-123">Upsell and cross-sell rules can be configured to prompt sales clerks to promote specific products to the customer.</span></span>
-   <span data-ttu-id="097c7-124">Satış elemanı müşteri tarafından sipariş kataloğu için kaynak kodunu yakalayabilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-124">Sales clerks can capture the source code for the catalog that a customer is ordering from.</span></span>
-   <span data-ttu-id="097c7-125">Satış elemanı satıcısı kuponlarını siparişe ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-125">Sales clerks can add a retailer's coupons to the order.</span></span>
-   <span data-ttu-id="097c7-126">Satış elemanı süreklilik programları satabilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-126">Sales clerks can sell continuity programs.</span></span>
-   <span data-ttu-id="097c7-127">Siparişler el ile veya otomatik olarak, sipariş işlenmeden önce ek araştırma olduğunu göstermek için beklemeye alınabilir.</span><span class="sxs-lookup"><span data-stu-id="097c7-127">Orders can be put on hold manually or automatically, to indicate that additional investigation is required before the order can be processed.</span></span>





