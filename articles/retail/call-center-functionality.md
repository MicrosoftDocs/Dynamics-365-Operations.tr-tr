---
title: "Çağrı merkezi işlevi"
description: "Bu konu Microsoft Dynamics 365 for Retail içerisindeki çağrı merkezi satış özelliği hakkında genel bakış sağlar."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e85b65e116b32adca09e46252d7d3bbe5101e1cf
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="call-center"></a><span data-ttu-id="f8913-103">Çağrı merkezi</span><span class="sxs-lookup"><span data-stu-id="f8913-103">Call center</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8913-104">Dynamics 365 for Retail'de çağrı merkezi uygulamada tanımlanabilen bir Perakende kanalı türüdür.</span><span class="sxs-lookup"><span data-stu-id="f8913-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="f8913-105">Çağrı merkezi varlıklarınız için özel bir kanal tanımlamak sistemin belirli veri varsayılanlarını ve sipariş işleme varsayılanlarını çağrı merkezi kanalı kullanıcısı tarafından oluşturulan satış siparişlerine bağlamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f8913-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="f8913-106">Çağrı merkezi özellikleri gelişmiş perakende fiyatı ve promosyonları, katalogları, hediye kartlarını, bağlılık programlarını ve kuponları içerir.</span><span class="sxs-lookup"><span data-stu-id="f8913-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="f8913-107">Çağrı merkezi siparişlerinden satış noktası (POS) uygulaması da kanallar arası sipariş karşılama senaryolarını desteklemek üzere yararlanır.</span><span class="sxs-lookup"><span data-stu-id="f8913-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="f8913-108">Çağrı merkezi modülünün Perakende dışındaki sektörler tarafından da kullanılabileceğini unutmamak önemlidir, bununla birlikte Dynamics 365 for Retail çağrı merkezi uygulamasının geçerli sürümü işletmeden işletmeye (B2B) sipariş işleme senaryoları veya siparişlerin çok fazla satış satırı içerdiği senaryolar için optimize edilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="f8913-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="f8913-109">Çağrı merkezi özelliklerini tipik doğrudan tüketici hareketi işleme dışında sipariş işleme için kullanmak isteyen kullanıcıların çağrı merkezi işlevini etkinleştirmenin işlev ve performans beklentilerini karşılayıp karşılamayacağını test etmek ve doğrulamak için uygun zamanı ayırmaları önerilir.</span><span class="sxs-lookup"><span data-stu-id="f8913-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="f8913-110">Sipariş oluşturmayı desteklemenin yanı sıra çağrı merkezi modülü, kullanıcılar için müşteri hesaplarını bulmayı ve tüm ilgili müşteri siparişi verileri ile özniteliklerini incelemeyi kolaylaştıran kullanıcı dostu müşteri hizmetleri uygulaması sunar.</span><span class="sxs-lookup"><span data-stu-id="f8913-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="f8913-111">Müşteri hizmetleri ekranı, kullanıcıya müşterilerden gelen siparişle ilgili en yaygın soruları yanıtlama olanağı sağlayan siparişle ilgili verilere hızlıca erişme olanağı sunar.</span><span class="sxs-lookup"><span data-stu-id="f8913-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="f8913-112">Bu sayfa Dynamics 365 for Retail'deki çağrı merkezi özelliklerinin kurulumu, yapılandırması ve işlevsel kullanımıyla ilişkili ilgili belgelere bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="f8913-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="f8913-113">Çağrı merkezini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f8913-113">Configure the call center</span></span>
[<span data-ttu-id="f8913-114">Sipariş işleme seçeneklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f8913-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="f8913-115">Sipariş işlemeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f8913-115">Configure order processing</span></span>
<span data-ttu-id="f8913-116">[Sahtekarlık uyarıları ayarlama](set-up-fraud-alerts.md)
[El ile Sipariş Tutmalar](work-with-order-holds.md)</span><span class="sxs-lookup"><span data-stu-id="f8913-116">[Set up fraud alerts](set-up-fraud-alerts.md)
[Manual Order Holds](work-with-order-holds.md)</span></span>

## <a name="configure-payment-processing"></a><span data-ttu-id="f8913-117">Ödeme işlemeyi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f8913-117">Configure payment processing</span></span>
[<span data-ttu-id="f8913-118">Bir çağrı merkezindeki ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="f8913-118">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="f8913-119">Doğrudan pazarlamayı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f8913-119">Configure direct marketing</span></span>
[<span data-ttu-id="f8913-120">Çağrı merkezi katalogları</span><span class="sxs-lookup"><span data-stu-id="f8913-120">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="f8913-121">RFM analizi ayarlama</span><span class="sxs-lookup"><span data-stu-id="f8913-121">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="f8913-122">Süreklilik programlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f8913-122">Configure continuity programs</span></span>
[<span data-ttu-id="f8913-123">Çağrı merkezi için bir süreklilik programı kurma</span><span class="sxs-lookup"><span data-stu-id="f8913-123">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)


