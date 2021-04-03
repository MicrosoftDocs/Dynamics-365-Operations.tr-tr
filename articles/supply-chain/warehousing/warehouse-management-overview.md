---
title: Ambar yönetimi genel bakış
description: Ambar yönetimini ambar işlemlerini izlemek ve otomatikleştirmek için kullanın.
author: ShylaThompson
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSWorkPool
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7d48ecd834c226fb40bede7519a476bd4c5f0ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248583"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="cdb8b-103">Ambar yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="cdb8b-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdb8b-104">Ambar yönetim modülü, üretim, dağıtım ve perakende şirketlerindeki ambar işlemlerini yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-104">The Warehouse management module lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="cdb8b-105">Bu modül, ambar tesisini her zaman, en iyi seviyede destekleyen çok çeşitli özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="cdb8b-106">Ambar yönetimi diğer iş süreçleriyle (taşıma, üretim, kalite kontrol, satınalma, transfer, satış ve iadeler vb.) tümüyle entegredir.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-106">Warehouse management is fully integrated with other business processes such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="cdb8b-107">Başlayın</span><span class="sxs-lookup"><span data-stu-id="cdb8b-107">Get started</span></span>
<span data-ttu-id="cdb8b-108">Ambar yönetimiyle çalışmaya başlamak için, şirketinizin iş işlemlerini desteklemek için genel ambar parametrelerinin kurulumunu tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of your company.</span></span>

- <span data-ttu-id="cdb8b-109">**Ambar yönetimi** > **Kurulum** altında **Ambar yönetimi parametreleri** sayfasına giderek genel ambar parametrelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="cdb8b-110">İş gereksinimlerine göre gelen ve giden ambar işlemleri iş akışları için bileşenleri yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="cdb8b-111">Yapılandırmanız gereken en önemli bileşenler dalga şablonları, iş şablonları, iş havuzları ve konum yönergeleridir.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="cdb8b-112">Ambar yapılandırmasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="cdb8b-112">Warehouse configuration overview</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="cdb8b-113">İş şablonları ve konum yönergeleri ile ambar işini denetleyin</span><span class="sxs-lookup"><span data-stu-id="cdb8b-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="cdb8b-114">Ambar işi için mobil cihazları ayarlama</span><span class="sxs-lookup"><span data-stu-id="cdb8b-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="cdb8b-115">Satınalma siparişini yerine koyma için yerleşim yönergesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="cdb8b-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="cdb8b-116">Satınalma siparişleri için iş şablonunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="cdb8b-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="cdb8b-117">Ambar yönetimi süreçleri</span><span class="sxs-lookup"><span data-stu-id="cdb8b-117">Warehouse management processes</span></span>
- <span data-ttu-id="cdb8b-118">Satış siparişleri, iadeler, transfer emirleri, üretim emirleri ve kanban için tümleşik destek belgeleri.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="cdb8b-119">Sorgulara dayanan esnek, gelen ve giden malzeme akışı</span><span class="sxs-lookup"><span data-stu-id="cdb8b-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="cdb8b-120">Üretim ve Taşıma teklifleri ile tam tümleştirme</span><span class="sxs-lookup"><span data-stu-id="cdb8b-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="cdb8b-121">Stoklama limitleri ve konum volümleri üzerinde tam kontrol</span><span class="sxs-lookup"><span data-stu-id="cdb8b-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="cdb8b-122">Stok durumu üzerinden kontrol edilen stok özellikleri</span><span class="sxs-lookup"><span data-stu-id="cdb8b-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="cdb8b-123">Toplu iş ve seri haldeki maddelere tam destek</span><span class="sxs-lookup"><span data-stu-id="cdb8b-123">Full batch and serial item support</span></span>
- <span data-ttu-id="cdb8b-124">Çeşitli madde teslim alma özellikleri</span><span class="sxs-lookup"><span data-stu-id="cdb8b-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="cdb8b-125">Çoklu malzeme çekme stratejileri</span><span class="sxs-lookup"><span data-stu-id="cdb8b-125">Multiple picking strategies</span></span>
- <span data-ttu-id="cdb8b-126">Sonraki nesil barkod tarayıcılar için hazır destek</span><span class="sxs-lookup"><span data-stu-id="cdb8b-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="cdb8b-127">Ambar işlemleri için palet/konteyner türleri</span><span class="sxs-lookup"><span data-stu-id="cdb8b-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="cdb8b-128">Gelişmiş sayım yeterlikleri</span><span class="sxs-lookup"><span data-stu-id="cdb8b-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="cdb8b-129">Zebra ZPL desteği ile etiket yazdırma ve etiket iletme</span><span class="sxs-lookup"><span data-stu-id="cdb8b-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="cdb8b-130">Power BI ile İş zekası tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="cdb8b-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="cdb8b-131">Stok hareketlerini otomatik ve el ile yapılması</span><span class="sxs-lookup"><span data-stu-id="cdb8b-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="cdb8b-132">Tümüyle entegre kalite kontrolü (QMS)</span><span class="sxs-lookup"><span data-stu-id="cdb8b-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="cdb8b-133">Çalışanların tam izlenebilir malzeme işlemesi</span><span class="sxs-lookup"><span data-stu-id="cdb8b-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="cdb8b-134">Giden dalga işleme</span><span class="sxs-lookup"><span data-stu-id="cdb8b-134">Outbound wave processing</span></span>
- <span data-ttu-id="cdb8b-135">El ile paketleme ve otomatik konteynerleme desteği</span><span class="sxs-lookup"><span data-stu-id="cdb8b-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="cdb8b-136">Küme malzeme çekme</span><span class="sxs-lookup"><span data-stu-id="cdb8b-136">Cluster picking</span></span>
- <span data-ttu-id="cdb8b-137">Basit çapraz sevk</span><span class="sxs-lookup"><span data-stu-id="cdb8b-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdb8b-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cdb8b-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="cdb8b-139">Yenilikler ve geliştirilen özellikler</span><span class="sxs-lookup"><span data-stu-id="cdb8b-139">What's new and in development</span></span>
<span data-ttu-id="cdb8b-140">Yayımlanmış ve geliştirilmekte olan yeni özellikleri görmek için [Microsoft Dynamics 365 Yol Haritası](https://roadmap.dynamics.com/) başlıklı makaleye gidin.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="cdb8b-141">Bloglar</span><span class="sxs-lookup"><span data-stu-id="cdb8b-141">Blogs</span></span>
<span data-ttu-id="cdb8b-142">[Microsoft Dynamics 365 bloğunda](https://community.dynamics.com/b/msftdynamicsblog) Ambar yönetimi ve diğer çözümler hakkındaki fikir, haber ve diğer bilgilere ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cdb8b-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]