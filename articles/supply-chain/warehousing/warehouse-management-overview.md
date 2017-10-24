---
title: "Ambar yönetimi"
description: "Ambar yönetimini ambar işlemlerini izlemek ve otomatikleştirmek için kullanın."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2086a68379eec70d1e616959d2b3c4386950a6f0
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="warehouse-management"></a><span data-ttu-id="d64c2-103">Ambar yönetimi</span><span class="sxs-lookup"><span data-stu-id="d64c2-103">Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d64c2-104">Dynamics 365 for Finance and Operations, Enterprise edition içindeki Ambar yönetimi modülü, üretim, dağıtım ve perakende şirketlerinde ambar işlemlerini yönetmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="d64c2-104">The Warehouse management module for Dynamics 365 for Finance and Operations, Enterprise edition lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="d64c2-105">Bu modül, ambar tesisini her zaman, en iyi seviyede destekleyen çok çeşitli özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="d64c2-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="d64c2-106">Ambar yönetimi Finance and Operations içindeki diğer iş işlemleri tümüyle entegredir; örneğin taşıma, üretim, kalite kontrol, satınalma, transfer, satış ve iadeler gibi.</span><span class="sxs-lookup"><span data-stu-id="d64c2-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="d64c2-107">Başlayın</span><span class="sxs-lookup"><span data-stu-id="d64c2-107">Get started</span></span>
<span data-ttu-id="d64c2-108">Ambar yönetimiyle çalışmaya başlamak için, şirketinizin iş işlemlerini desteklemek için genel ambar parametrelerinin kurulumunu tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d64c2-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="d64c2-109">**Ambar yönetimi** > **Kurulum** altında **Ambar yönetimi parametreleri** sayfasına giderek genel ambar parametrelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d64c2-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="d64c2-110">İş gereksinimlerine göre gelen ve giden ambar işlemleri iş akışları için bileşenleri yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d64c2-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="d64c2-111">Yapılandırmanız gereken en önemli bileşenler dalga şablonları, iş şablonları, iş havuzları ve konum yönergeleridir.</span><span class="sxs-lookup"><span data-stu-id="d64c2-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="d64c2-112">Ambar yapılandırması</span><span class="sxs-lookup"><span data-stu-id="d64c2-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="d64c2-113">İş şablonları ve konum yönergeleri ile ambar işini denetleyin</span><span class="sxs-lookup"><span data-stu-id="d64c2-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="d64c2-114">Ambar işi için mobil cihazları ayarlama</span><span class="sxs-lookup"><span data-stu-id="d64c2-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="d64c2-115">Satınalma siparişini yerine koyma için yerleşim yönergesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="d64c2-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="d64c2-116">Satınalma siparişleri için iş şablonunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="d64c2-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="d64c2-117">Ambar yönetimi süreçleri</span><span class="sxs-lookup"><span data-stu-id="d64c2-117">Warehouse management processes</span></span>
- <span data-ttu-id="d64c2-118">Satış siparişleri, iadeler, transfer emirleri, üretim emirleri ve kanban için tümleşik destek belgeleri.</span><span class="sxs-lookup"><span data-stu-id="d64c2-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="d64c2-119">Sorgulara dayanan esnek, gelen ve giden malzeme akışı</span><span class="sxs-lookup"><span data-stu-id="d64c2-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="d64c2-120">Üretim ve Taşıma teklifleri ile tam tümleştirme</span><span class="sxs-lookup"><span data-stu-id="d64c2-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="d64c2-121">Stoklama limitleri ve konum volümleri üzerinde tam kontrol</span><span class="sxs-lookup"><span data-stu-id="d64c2-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="d64c2-122">Stok durumu üzerinden kontrol edilen stok özellikleri</span><span class="sxs-lookup"><span data-stu-id="d64c2-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="d64c2-123">Toplu iş ve seri haldeki maddelere tam destek</span><span class="sxs-lookup"><span data-stu-id="d64c2-123">Full batch and serial item support</span></span>
- <span data-ttu-id="d64c2-124">Çeşitli madde teslim alma özellikleri</span><span class="sxs-lookup"><span data-stu-id="d64c2-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="d64c2-125">Çoklu malzeme çekme stratejileri</span><span class="sxs-lookup"><span data-stu-id="d64c2-125">Multiple picking strategies</span></span>
- <span data-ttu-id="d64c2-126">Sonraki nesil barkod tarayıcılar için hazır destek</span><span class="sxs-lookup"><span data-stu-id="d64c2-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="d64c2-127">Ambar işlemleri için palet/konteyner türleri</span><span class="sxs-lookup"><span data-stu-id="d64c2-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="d64c2-128">Gelişmiş sayım yeterlikleri</span><span class="sxs-lookup"><span data-stu-id="d64c2-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="d64c2-129">Zebra ZPL desteği ile etiket yazdırma ve etiket iletme</span><span class="sxs-lookup"><span data-stu-id="d64c2-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="d64c2-130">Power BI ile İş zekası tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="d64c2-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="d64c2-131">Stok hareketlerini otomatik ve el ile yapılması</span><span class="sxs-lookup"><span data-stu-id="d64c2-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="d64c2-132">Tümüyle entegre kalite kontrolü (QMS)</span><span class="sxs-lookup"><span data-stu-id="d64c2-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="d64c2-133">Çalışanların tam izlenebilir malzeme işlemesi</span><span class="sxs-lookup"><span data-stu-id="d64c2-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="d64c2-134">Giden dalga işleme</span><span class="sxs-lookup"><span data-stu-id="d64c2-134">Outbound wave processing</span></span>
- <span data-ttu-id="d64c2-135">El ile paketleme ve otomatik konteynerleme desteği</span><span class="sxs-lookup"><span data-stu-id="d64c2-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="d64c2-136">Küme malzeme çekme</span><span class="sxs-lookup"><span data-stu-id="d64c2-136">Cluster picking</span></span>
- <span data-ttu-id="d64c2-137">Basit çapraz sevk</span><span class="sxs-lookup"><span data-stu-id="d64c2-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d64c2-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d64c2-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="d64c2-139">Geliştirmedeki yenilikler</span><span class="sxs-lookup"><span data-stu-id="d64c2-139">What's new and in development</span></span>
<span data-ttu-id="d64c2-140">Yayımlanmış ve geliştirilmekte olan yeni özellikleri görmek için [Microsoft Dynamics 365 Yol Haritası](https://roadmap.dynamics.com/) bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d64c2-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="d64c2-141">Bloglar</span><span class="sxs-lookup"><span data-stu-id="d64c2-141">Blogs</span></span>
<span data-ttu-id="d64c2-142">[Microsoft Dynamics 365 blogunda](https://community.dynamics.com/b/msftdynamicsblog) Ambar yönetimi ve diğer çözümler hakkında fikirlere, haberlere ve diğer bilgilere ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d64c2-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 


