---
title: Yeni Commerce ortamlarında çekirdek verileri başlatma
description: Bu konu, Dynamics 365 Commerce için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.
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
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8fd0b2743deab758538922f312853b622a512c0a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000758"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a><span data-ttu-id="616ef-103">Yeni Commerce ortamlarında çekirdek verileri başlatma</span><span class="sxs-lookup"><span data-stu-id="616ef-103">Initialize seed data in new Commerce environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="616ef-104">Bu konu, Dynamics 365 Commerce için başlatma işleminin parçası olarak oluşturulan veriyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="616ef-104">This article describes the data that's created as part of the initialization process for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="616ef-105">Commerce çözümü Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtıldıktan sonra, temel yapılandırma verilerini oluşturmak için Commerce yapılandırmasını başlatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="616ef-105">After the Commerce solution has been deployed through Microsoft Dynamics Lifecycle Services (LCS), you must initialize the Commerce configuration to create the basic configuration data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="616ef-106">Commerce yapılandırmasını başlatmadan önce mağazaları ayarlayacağınız bir dil ve her bir tüzel kişilik için bir posta adresi belirtmiş olduğunuza emin olun.</span><span class="sxs-lookup"><span data-stu-id="616ef-106">Before you initialize the commerce configuration, make sure that you've specified a language and a postal address for each legal entity where you will set up stores.</span></span> <span data-ttu-id="616ef-107">Bu adımın, Commerce için kullandığınız her bir tüzel kişilik için tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="616ef-107">This step must be completed for each legal entity that you use for commerce.</span></span>

<span data-ttu-id="616ef-108">Yapılandırmayı başlatmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="616ef-108">To initialize the configuration, follow these steps.</span></span>

1. <span data-ttu-id="616ef-109">Commerce istemcisini başlatın.</span><span class="sxs-lookup"><span data-stu-id="616ef-109">Start the Commerce client.</span></span>
2. <span data-ttu-id="616ef-110">**Retail ve Commerce** &gt; **Headquarters kurulumu** &gt; **Parametreler** &gt; **Commerce parametreleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="616ef-110">Click **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
3. <span data-ttu-id="616ef-111">**Başlat** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="616ef-111">Click **Initialize**.</span></span>

<span data-ttu-id="616ef-112">Başlatma, aşağıdaki varsayılan yapılandırma verilerini oluşturur:</span><span class="sxs-lookup"><span data-stu-id="616ef-112">Initialization creates the following default configuration data:</span></span>

- <span data-ttu-id="616ef-113">Commerce planlayıcısı görevleri ve alt görevleri</span><span class="sxs-lookup"><span data-stu-id="616ef-113">Commerce scheduler jobs and subjobs</span></span>
- <span data-ttu-id="616ef-114">Ticaret kanalı şeması</span><span class="sxs-lookup"><span data-stu-id="616ef-114">Commerce channel schema</span></span>
- <span data-ttu-id="616ef-115">Commerce dağıtım planlamaları</span><span class="sxs-lookup"><span data-stu-id="616ef-115">Commerce distribution schedules</span></span>
- <span data-ttu-id="616ef-116">Düğme grupları, görüntüler ve temaları içeren varsayılan ekran düzenleri</span><span class="sxs-lookup"><span data-stu-id="616ef-116">Default screen layouts, which include button grids, images, and themes</span></span>
- <span data-ttu-id="616ef-117">Zaman dilimi bilgileri</span><span class="sxs-lookup"><span data-stu-id="616ef-117">Time zone information</span></span>
- <span data-ttu-id="616ef-118">Satış noktası (POS) işlemleri</span><span class="sxs-lookup"><span data-stu-id="616ef-118">Point-of-sale (POS) operations</span></span>
- <span data-ttu-id="616ef-119">POS izinleri</span><span class="sxs-lookup"><span data-stu-id="616ef-119">POS permissions</span></span>
- <span data-ttu-id="616ef-120">Kanal raporları</span><span class="sxs-lookup"><span data-stu-id="616ef-120">Channel reports</span></span>
- <span data-ttu-id="616ef-121">Öznitelik meta verileri</span><span class="sxs-lookup"><span data-stu-id="616ef-121">Attribute metadata</span></span>
- <span data-ttu-id="616ef-122">Varlık doğrulama şablonları</span><span class="sxs-lookup"><span data-stu-id="616ef-122">Entity validation templates</span></span>
- <span data-ttu-id="616ef-123">Commerce Data Exchange oturum geçmişini silmek için toplu iş</span><span class="sxs-lookup"><span data-stu-id="616ef-123">Batch job to purge Commerce Data Exchange session history</span></span>

<span data-ttu-id="616ef-124">Ayrıca, Commerce veritabanı için ödeme kartı sektörü ile ilgili günlük kaydı etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="616ef-124">Additionally, logging that is related to the payment card industry (PCI) is enabled for the Commerce database.</span></span>

> [!NOTE]
> <span data-ttu-id="616ef-125">Commerce planlayıcısını ayrıca yapılandırmak seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="616ef-125">There is an option to separately configure the Commerce scheduler.</span></span> <span data-ttu-id="616ef-126">Bu seçenek, Commerce planlayıcısı yapılandırmasını varsayılan ayarlarına sıfırlama olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="616ef-126">This option lets you reset the Commerce scheduler configuration to its default settings.</span></span>

<span data-ttu-id="616ef-127">Başlatma tamamlandıktan sonra ek Commerce verilerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="616ef-127">After initialization is completed, you must configure additional commerce data.</span></span> <span data-ttu-id="616ef-128">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="616ef-128">Here are some examples:</span></span>

- <span data-ttu-id="616ef-129">Ticaret parametreleri</span><span class="sxs-lookup"><span data-stu-id="616ef-129">Commerce parameters</span></span>
- <span data-ttu-id="616ef-130">Ticaret planlayıcı parametreleri</span><span class="sxs-lookup"><span data-stu-id="616ef-130">Commerce scheduler parameters</span></span>
- <span data-ttu-id="616ef-131">Commerce kanalları</span><span class="sxs-lookup"><span data-stu-id="616ef-131">Commerce channels</span></span>
- <span data-ttu-id="616ef-132">Kayıtlar ve cihazlar</span><span class="sxs-lookup"><span data-stu-id="616ef-132">Registers and devices</span></span>
- <span data-ttu-id="616ef-133">Sınıflamalar</span><span class="sxs-lookup"><span data-stu-id="616ef-133">Assortments</span></span>
