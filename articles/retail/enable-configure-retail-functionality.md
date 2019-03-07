---
title: Yeni Retail ortamlarında çekirdek verileri başlatma
description: Bu konu, Microsoft Dynamics 365 for Retail için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "327907"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a><span data-ttu-id="ec33e-103">Yeni Retail ortamlarında çekirdek verileri başlatma</span><span class="sxs-lookup"><span data-stu-id="ec33e-103">Initialize seed data in new Retail environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec33e-104">Bu konu, Microsoft Dynamics 365 for Retail için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="ec33e-104">This article describes the data that's created as part of the initialization process for Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="ec33e-105">Perakende çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için perakende yapılandırmasını başlatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec33e-105">After the Retail solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the retail configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec33e-106">Perakende yapılandırmasını başlatmadan önce, perakende mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun.</span><span class="sxs-lookup"><span data-stu-id="ec33e-106">Before you initialize the retail configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up retail stores.</span></span> <span data-ttu-id="ec33e-107">Bu adımın, perakende için kullandığınız her bir tüzel kişilik için tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec33e-107">This step must be completed for each legal entity that you use for retail.</span></span>

<span data-ttu-id="ec33e-108">Perakende yapılandırmasını başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ec33e-108">To initialize the retail configuration, follow these steps.</span></span>

1. <span data-ttu-id="ec33e-109">Dynamics 365 for Retail istemcisini başlatın.</span><span class="sxs-lookup"><span data-stu-id="ec33e-109">Start the Dynamics 365 for Retail client.</span></span>
2. <span data-ttu-id="ec33e-110">**Perakende** &gt; **Genel merkez kurulumu** &gt; **Parametreler** &gt; **Perakende parametreleri** menüsüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec33e-110">Click **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail parameters**.</span></span>
3. <span data-ttu-id="ec33e-111">**Başlat** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec33e-111">Click **Initialize**.</span></span>

<span data-ttu-id="ec33e-112">Başlatma, aşağıdaki varsayılan yapılandırma verilerini oluşturur:</span><span class="sxs-lookup"><span data-stu-id="ec33e-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="ec33e-113">Perakende planlayıcısı görevleri ve alt görevleri</span><span class="sxs-lookup"><span data-stu-id="ec33e-113">Retail scheduler jobs and subjobs</span></span>
- <span data-ttu-id="ec33e-114">Perakende kanalı şeması</span><span class="sxs-lookup"><span data-stu-id="ec33e-114">Retail channel schema</span></span>
- <span data-ttu-id="ec33e-115">Perakende dağıtım planlamaları</span><span class="sxs-lookup"><span data-stu-id="ec33e-115">Retail distribution schedules</span></span>
- <span data-ttu-id="ec33e-116">Düğme grupları, görüntüler ve temaları içeren varsayılan ekran düzenleri</span><span class="sxs-lookup"><span data-stu-id="ec33e-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="ec33e-117">Zaman dilimi bilgileri</span><span class="sxs-lookup"><span data-stu-id="ec33e-117">Time zone information</span></span>
- <span data-ttu-id="ec33e-118">Satış noktası (POS) işlemleri</span><span class="sxs-lookup"><span data-stu-id="ec33e-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="ec33e-119">POS izinleri</span><span class="sxs-lookup"><span data-stu-id="ec33e-119">POS permissions</span></span>
- <span data-ttu-id="ec33e-120">Kanal raporları</span><span class="sxs-lookup"><span data-stu-id="ec33e-120">Channel reports</span></span>
- <span data-ttu-id="ec33e-121">Öznitelik meta verileri</span><span class="sxs-lookup"><span data-stu-id="ec33e-121">Attribute metadata</span></span>
- <span data-ttu-id="ec33e-122">Varlık doğrulama şablonları</span><span class="sxs-lookup"><span data-stu-id="ec33e-122">Entity validation templates</span></span>
- <span data-ttu-id="ec33e-123">Commerce Data Exchange oturum geçmişini silmek için toplu iş</span><span class="sxs-lookup"><span data-stu-id="ec33e-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="ec33e-124">Ayrıca, Dynamics 365 for Retail veritabanı için ödeme kartı sektörü ile ilgili günlük kaydı etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ec33e-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Dynamics 365 for Retail database.</span></span>

> [!NOTE]
> <span data-ttu-id="ec33e-125">Perakende planlayıcısını ayrıca yapılandırmak seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="ec33e-125">There is an option to separately configure the Retail scheduler.</span></span> <span data-ttu-id="ec33e-126">Bu seçenek, Perakende planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ec33e-126">This option lets you reset the Retail scheduler configuration to its default settings.</span></span>

<span data-ttu-id="ec33e-127">Başlatma tamamlandıktan sonra ek perakende verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec33e-127">After initialization is completed, you must configure additional retail data.</span></span> <span data-ttu-id="ec33e-128">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="ec33e-128">Here are some examples:</span></span>

- <span data-ttu-id="ec33e-129">Perakende parametreleri</span><span class="sxs-lookup"><span data-stu-id="ec33e-129">Retail parameters</span></span>
- <span data-ttu-id="ec33e-130">Perakende Planlayıcısı parametreleri</span><span class="sxs-lookup"><span data-stu-id="ec33e-130">Retail scheduler parameters</span></span>
- <span data-ttu-id="ec33e-131">Perakende kanalları</span><span class="sxs-lookup"><span data-stu-id="ec33e-131">Retail channels</span></span>
- <span data-ttu-id="ec33e-132">Kayıtlar ve cihazlar</span><span class="sxs-lookup"><span data-stu-id="ec33e-132">Registers and devices</span></span>
- <span data-ttu-id="ec33e-133">Sınıflamalar</span><span class="sxs-lookup"><span data-stu-id="ec33e-133">Assortments</span></span>
