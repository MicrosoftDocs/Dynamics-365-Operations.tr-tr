---
title: Çağrı merkezi satış özelliği
description: Bu konuda, Dynamics 365 Retail'daki çağrı merkezi satışları işlevine genel bir bakış sağlar.
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2e44770af4a30f539e56d38b21c897cacd2707e7
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812351"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="bfcc5-103">Çağrı merkezi satış işlevi</span><span class="sxs-lookup"><span data-stu-id="bfcc5-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="bfcc5-104">Dynamics 365 Retail'de çağrı merkezi uygulamada tanımlanabilen bir Perakende kanalı türüdür.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-104">In Dynamics 365 Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="bfcc5-105">Çağrı merkezi varlıklarınız için özel bir kanal tanımlamak sistemin belirli veri varsayılanlarını ve sipariş işleme varsayılanlarını çağrı merkezi kanalı kullanıcısı tarafından oluşturulan satış siparişlerine bağlamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="bfcc5-106">Çağrı merkezi özellikleri gelişmiş perakende fiyatı ve promosyonları, katalogları, hediye kartlarını, bağlılık programlarını ve kuponları içerir.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="bfcc5-107">Çağrı merkezi siparişlerinden satış noktası (POS) uygulaması da kanallar arası sipariş karşılama senaryolarını desteklemek üzere yararlanır.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="bfcc5-108">Çağrı merkezi modülünün Perakende dışındaki sektörler tarafından da kullanılabileceğini unutmamak önemlidir, bununla birlikte Retail çağrı merkezi uygulamasının geçerli sürümü işletmeden işletmeye (B2B) sipariş işleme senaryoları veya siparişlerin çok fazla satış satırı içerdiği senaryolar için optimize edilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="bfcc5-109">Çağrı merkezi özelliklerini tipik doğrudan tüketici hareketi işleme dışında sipariş işleme için kullanmak isteyen kullanıcıların çağrı merkezi işlevini etkinleştirmenin işlev ve performans beklentilerini karşılayıp karşılamayacağını test etmek ve doğrulamak için uygun zamanı ayırmaları önerilir.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="bfcc5-110">Sipariş oluşturmayı desteklemenin yanı sıra çağrı merkezi modülü, kullanıcılar için müşteri hesaplarını bulmayı ve tüm ilgili müşteri siparişi verileri ile özniteliklerini incelemeyi kolaylaştıran kullanıcı dostu müşteri hizmetleri uygulaması sunar.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="bfcc5-111">Müşteri hizmetleri ekranı, kullanıcıya müşterilerden gelen siparişle ilgili en yaygın soruları yanıtlama olanağı sağlayan siparişle ilgili verilere hızlıca erişme olanağı sunar.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="bfcc5-112">Bu sayfa Retail'deki çağrı merkezi özelliklerinin kurulumu, yapılandırması ve işlevsel kullanımıyla ilişkili ilgili belgelere bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="bfcc5-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Retail.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="bfcc5-113">Çağrı merkezini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-113">Configure the call center</span></span>

[<span data-ttu-id="bfcc5-114">Çağrı merkezi kanalları ayarlama</span><span class="sxs-lookup"><span data-stu-id="bfcc5-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="bfcc5-115">Sipariş işlemeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-115">Configure order processing</span></span>

[<span data-ttu-id="bfcc5-116">Çağrı merkezi sahtekarlık uyarılarını ayarlama ve bu uyarılarla çalışma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="bfcc5-117">Çağrı merkezi sipariş tutmalarını yapılandırma ve bunlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="bfcc5-118">Ödeme işlemeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-118">Configure payment processing</span></span>

[<span data-ttu-id="bfcc5-119">Çağrı merkezlerinde ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="bfcc5-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="bfcc5-120">Teslimat şekillerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-120">Configure delivery modes</span></span>

[<span data-ttu-id="bfcc5-121">Çağrı merkezi teslimat şekillerini ve masraflarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="bfcc5-122">Doğrudan pazarlamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-122">Configure direct marketing</span></span>

[<span data-ttu-id="bfcc5-123">Çağrı merkezi katalogları</span><span class="sxs-lookup"><span data-stu-id="bfcc5-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="bfcc5-124">Yenilik, Sıklık ve Parasal (RFM) analiz ayarlama</span><span class="sxs-lookup"><span data-stu-id="bfcc5-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="bfcc5-125">Süreklilik programlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bfcc5-125">Configure continuity programs</span></span>

[<span data-ttu-id="bfcc5-126">Çağrı merkezleri için süreklilik programları ayarlama</span><span class="sxs-lookup"><span data-stu-id="bfcc5-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
