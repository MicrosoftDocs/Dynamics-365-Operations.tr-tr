---
title: Microsoft Dynamics 365 Field Service ile tümleştirmeye genel bakış
description: Bu konu Microsoft Dynamics 365 Field Service ile tümleştirme hakkında bilgi sağlar.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: cf1c4cbc18728b6094f862792d20a893b2a8d6ea
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815284"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="975b6-103">Microsoft Dynamics 365 Field Service ile tümleştirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="975b6-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="975b6-104">Supply Chain Management, Dynamics 365 Supply Chain Management ile Dynamics 365 Field Service arasında iş süreçlerinin eşitlenmesini sağlar</span><span class="sxs-lookup"><span data-stu-id="975b6-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="975b6-105">Tümleştirme senaryoları iş süreçlerinin eşitlenmesine olanak tanımak için genişletilebilir Veri tümleştirici şablonları ve Common Data Service kullanılarak yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="975b6-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="975b6-106">Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel iş ihtiyaçlarını karşılamak üzere eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="975b6-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="975b6-107">Field Service tümleştirmesi, mevcut aday-nakit işlevinin üzerine inşa olur.</span><span class="sxs-lookup"><span data-stu-id="975b6-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)

<span data-ttu-id="975b6-109">Field Service ile Supply Chain Management arasındaki tümleştirmenin birinci aşaması Field Service'taki iş emirlerinin ve sözleşmelerin Supply Chain Management'da faturalandırılmasını sağlamaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="975b6-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="975b6-110">Desteklenen akış Field Service'da başlar; iş emirlerinden alınan bilgiler Supply Chain Management'a satış siparişleri olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="975b6-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="975b6-111">Supply Chain Management'ta, satış siparişleri fatura belgeleri oluşturmak için faturalandırılır.</span><span class="sxs-lookup"><span data-stu-id="975b6-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="975b6-112">Ayrıca, Field Service sözleşme faturalarındaki bilgiler Supply Chain Management'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="975b6-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="975b6-113">Microsoft Dynamics 365 Veri tümleştirici verileri özelleştirilebilir projeleri kullanarak eşitler.</span><span class="sxs-lookup"><span data-stu-id="975b6-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="975b6-114">Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel gereksinimleri karşılamak üzere eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="975b6-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="975b6-115">Field Service ile Supply Chain Management arasındaki tümleştirmenin birinci aşaması aşağıdaki öğelerin eşitlenmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="975b6-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="975b6-116">Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="975b6-116">Synchronize products in Supply Chain Management to products in Field Service</span></span>](field-service-product.md)
- [<span data-ttu-id="975b6-117">Field Service'daki iş emirlerini Supply Chain Management'taki satış siparişleriyle eşitleme</span><span class="sxs-lookup"><span data-stu-id="975b6-117">Synchronize work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="975b6-118">Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme</span><span class="sxs-lookup"><span data-stu-id="975b6-118">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="975b6-119">Bir iş emrini Field Service ile Supply Chain Management arasında nasıl eşitleyeceğinize ilişkin bir örnek görmek için kısa YouTube videosunu izleyin: [İş emrini Microsoft Dynamics 365 Tümleştirmesi ile eşitleme](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="975b6-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="975b6-120">Field Service ile tümleştirme, stok ve proje bilgisi dahil.</span><span class="sxs-lookup"><span data-stu-id="975b6-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="975b6-121">Saha teknisyenlerine, Supply Chain Management'tan stok bilgisi hakkında içgörü vermeye odaklı bu ikinci aşamadaki ek işlev, onların stok düzeylerini güncelleştirmelerine ve malzeme aktarmaları yapmalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="975b6-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="975b6-122">Ek olarak, satılan malların kurulumunu yapan veya hizmet veren şirketleri, daha iyi kontrol ve tam satışa ve projelerle tümleştirmeye daha iyi görünürlük sahibi olacaklardır.</span><span class="sxs-lookup"><span data-stu-id="975b6-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="975b6-123">İşlev şunların tümleştirmesini içerir:</span><span class="sxs-lookup"><span data-stu-id="975b6-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="975b6-124">Ambar bilgisi</span><span class="sxs-lookup"><span data-stu-id="975b6-124">Warehouse information</span></span>
- <span data-ttu-id="975b6-125">Eldeki stok bilgileri</span><span class="sxs-lookup"><span data-stu-id="975b6-125">On-hand inventory information</span></span>
- <span data-ttu-id="975b6-126">Stok transferleri</span><span class="sxs-lookup"><span data-stu-id="975b6-126">Inventory transfers</span></span>
- <span data-ttu-id="975b6-127">Stok düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="975b6-127">Inventory adjustments</span></span>
- <span data-ttu-id="975b6-128">Dynamics 365 Field Service iş emirleriyle bağlantılı Supply Chain Management projeleri</span><span class="sxs-lookup"><span data-stu-id="975b6-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="975b6-129">Supply Chain Management projeleri ile bağlantıya sahip Dynamics 365 Field Service iş emirleri, bu proje numarasını satış siparişlerine proje içinden faturalamasına izin vermek için uygular.</span><span class="sxs-lookup"><span data-stu-id="975b6-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="975b6-131">Field Service ile Supply Chain Management arasındaki tümleştirmenin ikinci aşaması aşağıdaki şablonların eşitlenmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="975b6-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="975b6-132">Ambarlar (Supply Chain Management'tan Field Service'a) - Supply Chain Management'tan Field Service'a Ambarlar [Gelişmiş Sorgu]</span><span class="sxs-lookup"><span data-stu-id="975b6-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="975b6-133">Ürün Stoğu (Supply Chain Management'tan Field Service'a) - Supply Chain Management'tan Field Service'a stok düzeyinde bilgiler [Gelişmiş Sorgu]</span><span class="sxs-lookup"><span data-stu-id="975b6-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="975b6-134">Stok Düzenleme (Field Service'tan Supply Chain Management'a) - Field Service'tan Supply Chain Management'a stok düzenlemeleri [Gelişmiş Sorgu]</span><span class="sxs-lookup"><span data-stu-id="975b6-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="975b6-135">Stok Transferleri (Field Service'tan Supply Chain Management'a) - Field Service'tan Supply Chain Management'a stok transferleri [Gelişmiş Sorgu]</span><span class="sxs-lookup"><span data-stu-id="975b6-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="975b6-136">Projeler (Supply Chain Management'tan Field Service'a) - Supply Chain Management'tan Field Service'a Proje listesi</span><span class="sxs-lookup"><span data-stu-id="975b6-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="975b6-137">Proje ile İş Emirleri (Field Service'tan Supply Chain Management'a) - Field Service'taki iş emirlerinden Supply Chain Management'taki Satış siparişlerine , Proje desteği ile [Gelişmiş Sorgu]</span><span class="sxs-lookup"><span data-stu-id="975b6-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="975b6-138">Stok birimi ile Field Service Ürünleri (Supply Chain Management'tan Sales'a) -Supply Chain Management 'Satılabilir serbest bırakılmış ürünler'den Field Service için Sales 'Ürünlerine', Stok birimi dahil</span><span class="sxs-lookup"><span data-stu-id="975b6-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="975b6-139">Sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="975b6-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="975b6-140">Supply Chain Management için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="975b6-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="975b6-141">Field Service tümleştirmesi aşağıdaki sürümleri destekler:</span><span class="sxs-lookup"><span data-stu-id="975b6-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="975b6-142">Dynamics 365 for Finance and Operations sürüm 8.1.2 (Aralık 2018), Aralık 2018'da yayımlanmıştır ve uygulama yapı numarası 8.1.195 Platform güncelleştirmesi 22'ye (7.0.5095) sahiptir.</span><span class="sxs-lookup"><span data-stu-id="975b6-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="975b6-143">Field Service için sistem gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="975b6-143">System requirements for Field Service</span></span>
<span data-ttu-id="975b6-144">Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="975b6-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="975b6-145">Field Service (sürüm 8.2.0.286) veya sonraki sürüm Dynamics 365 9.1.x üzerinde - Kasım 2018'de yayımlandı</span><span class="sxs-lookup"><span data-stu-id="975b6-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="975b6-146">Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü.</span><span class="sxs-lookup"><span data-stu-id="975b6-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="975b6-147">Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) üzerinden indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="975b6-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="975b6-148">'Field Service Tümleştirmesi, Proje ve Stok' çözümü, Dynamics 365, sürüm 2.0.0.0 veya sonraki bir sürüm için.</span><span class="sxs-lookup"><span data-stu-id="975b6-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="975b6-149">Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) üzerinden indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="975b6-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
