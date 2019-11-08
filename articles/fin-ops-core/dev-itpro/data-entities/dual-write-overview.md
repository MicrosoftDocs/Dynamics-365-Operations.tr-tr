---
title: Common Data Service ile yakın gerçek zamanlı veri tümleştirmesi
description: Bu konu Finance and Operations ve Common Data Service arasındaki tümleştirme hakkında bilgi sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d70bce4e47c05a7974c1b974fdca17682e5370aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550869"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="7a96a-103">Common Data Service ile yakın gerçek zamanlı veri tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="7a96a-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="7a96a-104">Günümüzün dijital dünyasında, işletme ekosistemleri Microsoft Dynamics 365 uygulamalarını bir bütün olarak kullanırlar.</span><span class="sxs-lookup"><span data-stu-id="7a96a-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="7a96a-105">Kişilerin, müşterilerin, işlemlerin ve Nesnelerin İnterneti'nin (IoT) verileri tek bir kaynağa aktığından, dijital geri bildirim döngüleri için bir fırsat vardır.</span><span class="sxs-lookup"><span data-stu-id="7a96a-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="7a96a-106">Bu deneyimi gerçekleştirmek için, Finance and Operations uygulamaları ve diğer Dynamics 365 uygulamaları arasındaki entegrasyon esastır.</span><span class="sxs-lookup"><span data-stu-id="7a96a-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="7a96a-107">Bazı uygulamalar Common Data Service üzerine inşa edilir.</span><span class="sxs-lookup"><span data-stu-id="7a96a-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="7a96a-108">Finance and Operations uygulamaları verileriyle Common Data Service arasındaki entegrasyon diğer uygulamaların Finance and Operations ile tutarlı ve akıcı bir şekilde iletişim kurmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="7a96a-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="7a96a-109">Finance and Operations uygulamaları ve Common Data Service çift yazma çerçevesi ile Finance and Operations uygumaları ile diğer Dynamics 365 uygulamaları arasında gerçek zamanlıya yakın veri eşitlemesi sağlarlar.</span><span class="sxs-lookup"><span data-stu-id="7a96a-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="7a96a-110">Kapsam çok geniş olup, uygulamanın 28 yüzey alanına yayılır.</span><span class="sxs-lookup"><span data-stu-id="7a96a-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="7a96a-111">Amaç, iş süreçlerini uygulamalar arasında bağlayan kesintisiz veri akışları üzerinden "Bir Dynamics 365" kullanıcı deneyimi sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="7a96a-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Mimariye genel bakış diyagramı](media/dual-write-overview.jpg)

<span data-ttu-id="7a96a-113">Müşteriler için aşağıdaki değer önermeleri kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="7a96a-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="7a96a-114">Common Data Service'te kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="7a96a-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="7a96a-115">Common Data Service'te şirket kavramı</span><span class="sxs-lookup"><span data-stu-id="7a96a-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="7a96a-116">Tümleşik müşteri aslı</span><span class="sxs-lookup"><span data-stu-id="7a96a-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="7a96a-117">Tümleşik satıcı aslı</span><span class="sxs-lookup"><span data-stu-id="7a96a-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="7a96a-118">Birleştirilmiş ana ürün</span><span class="sxs-lookup"><span data-stu-id="7a96a-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="7a96a-119">Sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="7a96a-119">System requirements</span></span>

<span data-ttu-id="7a96a-120">Eşzamanlı, iki yönlü, yakın zamanda gerçek zamanlı veri akışları aşağıdaki sürümleri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="7a96a-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="7a96a-121">Microsoft Dynamics 365 for Finance and Operations sürüm 10.0.4 (Temmuz 2019) Platform güncelleştirmesi 28 veya daha sonraki ile</span><span class="sxs-lookup"><span data-stu-id="7a96a-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="7a96a-122">Microsoft Dynamics 365 for Customer Engagement Platform sürüm 9.1 (4.2) veya üstü</span><span class="sxs-lookup"><span data-stu-id="7a96a-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="7a96a-123">Ayar yönergeleri</span><span class="sxs-lookup"><span data-stu-id="7a96a-123">Setup instructions</span></span>

<span data-ttu-id="7a96a-124">Finance and Operations uygulamaları ve Common Data Service arasındaki tümleştirmeyi ayarlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a96a-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="7a96a-125">İkili yazma sisteminin kurulumu için, Çift yazma önizlemesini duyurmada bkz. [adım adım kılavuz](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="7a96a-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="7a96a-126">Çözümü [Finance and Operations, Common Data Service, ve Customer Engagement Entegrasyonu](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer grup'tan indirin.</span><span class="sxs-lookup"><span data-stu-id="7a96a-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="7a96a-127">Paket beş çözüm içerir:</span><span class="sxs-lookup"><span data-stu-id="7a96a-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="7a96a-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="7a96a-128">Dynamics365Company</span></span>
    + <span data-ttu-id="7a96a-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="7a96a-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="7a96a-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="7a96a-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="7a96a-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="7a96a-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="7a96a-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="7a96a-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="7a96a-133">Kuralları yürütme sırası için [ilk başvuru verilerini eşitleme](dual-write-initial.md)'yi izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a96a-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="7a96a-134">Çift yazma eşitleme sorunlarıyla karşılaşırsanız veri tümleştirmesi için bkz. [Sorun giderme kılavuzu](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="7a96a-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a96a-135">Çift yazma ve [Aday müşteriden nakde](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct)'yi yan yana çalıştıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="7a96a-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="7a96a-136">Aday müşteriden nakde çözümünü çalıştırıyorsanız bunu kaldırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a96a-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="7a96a-137">Ayrıca Aday müşteriden nakde çözümünün bir parçası olan müşteri ve satıcı çift yazma şablonlarını devre dışı bırakmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a96a-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
