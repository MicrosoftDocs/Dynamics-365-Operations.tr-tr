---
title: "Taşıma yönetimine genel bakış"
description: "Bu konuda, Microsoft Dynamics 365 for Finance and Operations'daki taşıma yönetimi işlevine genel bir bakış sunulur."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4dc2c15d35d93d1563c866b20ad7f2bbb5c8457
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="373db-103">Taşıma yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="373db-103">Transportation management overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="373db-104">Bu konuda, Microsoft Dynamics 365 for Finance and Operations'daki taşıma yönetimi işlevine genel bir bakış sunulur.</span><span class="sxs-lookup"><span data-stu-id="373db-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="373db-105">Taşıma yönetimi, şirketinizin taşımalarını kullanmanıza olanak tanır ve satıcı ile gelen ve giden siparişler için yönlendirme çözümlerini belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="373db-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="373db-106">Örneğin bir sevkiyat için en hızlı yolu veya en ucuz oranı tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="373db-107">Aşağıdaki tablo, Microsoft Dynamics 365 for Finance and Operations'daki Taşıma yönetiminin kullanılmasına ilişkin ana senaryoları açıklar.</span><span class="sxs-lookup"><span data-stu-id="373db-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="373db-108">Senaryo</span><span class="sxs-lookup"><span data-stu-id="373db-108">Scenario</span></span></th>
<th><span data-ttu-id="373db-109">Taşıma yönetimi nasıl yardımcı olur?</span><span class="sxs-lookup"><span data-stu-id="373db-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="373db-110">Taşıma faaliyetleri için dış lojistik sağlayıcılarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="373db-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="373db-111">Gelen ve/veya giden taşıma için Taşıma yönetimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="373db-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="373db-112">Şirketin teslimat/mal alımı için kullandığı kendi filosu vardır ve teslimat giderleri müşterilere aktarılır.</span><span class="sxs-lookup"><span data-stu-id="373db-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="373db-113">Giden işlemleri için, taşıma giderlerini belirlemek ve bunları müşterilere aktarmak için Taşıma yönetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="373db-114">Ancak, taşıyıcı fatura mutabakat işlemi gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="373db-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="373db-115">Teslimat/mal alımı için şirketin kendi filosu vardır ancak ürün fiyatı nakliyeyi içerdiğinden teslimat giderleri müşterilere aktarılmaz.</span><span class="sxs-lookup"><span data-stu-id="373db-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="373db-116">Çok sayıda Taşıma yönetimi işlevi gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="373db-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="373db-117">Bununla birlikte, taşıma fiyatlarını belirlemek ve satış fiyatını buna göre ayarlamak için Taşıma yönetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="373db-118">Lojistik hizmeti aynı şirketteki başka bir tüzel kişilik tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="373db-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="373db-119">Başka bir tüzel kişiliği herhangi bir sevkiyat yüklenicisi olarak kullanmak için Taşıma yönetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="373db-120">Tüzel kişilikler arasındaki ekonomik hareketleri otomatik hale getiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="373db-121">Bu nedenle, bu hareketleri el ile işlemeniz gerekir (örneğin, bir satınalma siparişi oluşturarak).</span><span class="sxs-lookup"><span data-stu-id="373db-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="373db-122">Lojistik hizmetler sunan tüzel kişilikte, Taşıma yönetimi taşıma ücretlerini belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="373db-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="373db-123">Finance ve Operations'ta taşımayı planlama</span><span class="sxs-lookup"><span data-stu-id="373db-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="373db-124">Taşıma yönetiminde , taşıma planlaması için siparişler veya bu siparişlere göre oluşturulan sevkiyatlar temel alınır.</span><span class="sxs-lookup"><span data-stu-id="373db-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="373db-125">Sevkiyatlar daima zaman içinde bir noktada bulunmaktadır ancak taşıma planlaması için gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="373db-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="373db-126">Transfer emirleri giden senaryosunun bir parçasıdır ve satış siparişleriyle birlikte planlanabilir.</span><span class="sxs-lookup"><span data-stu-id="373db-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Yük çekme](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="373db-128">Gelen taşıma</span><span class="sxs-lookup"><span data-stu-id="373db-128">Inbound transportation</span></span>
<span data-ttu-id="373db-129">Bir satıcıya madde siparişi verdiğiniz zaman ve bu maddelerin sizin ambarınıza teslim edilmesi gerektiğinde maddeleri taşımayı kendiniz düzenlemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="373db-130">Gelen yükün taşıma ve girişini planlamak için Dynamics 365 for Finance and Operations kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="373db-131">Aşağıdaki şekilde, gelen yük için taşıma planlamasına ilişkin iş süreci akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="373db-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Gelen yükün taşınmasına ilişkin iş süreci akışı](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="373db-133">Giden taşıma</span><span class="sxs-lookup"><span data-stu-id="373db-133">Outbound transportation</span></span>
<span data-ttu-id="373db-134">Belirli maddeleri şirketin ambarından müşteriye sevk etmek için giden yük planlaması yapabilir ve işleme koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="373db-135">Giden yükün nakliyesi ve sevkiyatını planlamak için Dynamics 365 for Finance and Operations kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="373db-136">Aşağıdaki şekilde, giden yükün sevkiyat için planlaması ve işleme konmasına ilişkin iş süreci akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="373db-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Giden yükleri planlama ve işleme](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="373db-138">Yapıyı yükle</span><span class="sxs-lookup"><span data-stu-id="373db-138">Load building</span></span>
<span data-ttu-id="373db-139">Finance and Operations, Hacim tabanlı yük oluşturma stratejisi olarak adlandırılan bir yük oluşturma stratejisi sunar.</span><span class="sxs-lookup"><span data-stu-id="373db-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="373db-140">Bu strateji, yük şablonunda yükseklik ve ağırlık için belirtilen maksimum değerleri kullanmanıza olanak tanır; veya yeni değerler girerek ayarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="373db-141">Kullanmak için **Yük oluşturma workbench'i** sayfasında bulunan **Ayar** Hızlı sekmesindeki **Yük oluşturma stratejisi** alanından bu stratejiyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="373db-142">Ayrıca, Uygulama Nesne Ağacı'nda (AOT) yeni bir sınıf oluşturarak kendi yük oluşturma stratejinizi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="373db-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




