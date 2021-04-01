---
title: Taşıma yönetimine genel bakış
description: Bu konuda, Supply Chain Management'taki taşıma yönetimi işlevine genel bir bakış sunulmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 511cc3459ce5d99f0a3e6dae0a70af0109326118
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233403"
---
# <a name="transportation-management-overview"></a><span data-ttu-id="c7f93-103">Taşıma yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c7f93-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7f93-104">Bu konuda, Supply Chain Management'taki taşıma yönetimi işlevine genel bir bakış sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7f93-104">This topic gives an overview of the transportation management functionality in Supply Chain Management.</span></span>

<span data-ttu-id="c7f93-105">Taşıma yönetimi, şirketinizin taşımalarını kullanmanıza olanak tanır ve satıcı ile gelen ve giden siparişler için yönlendirme çözümlerini belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c7f93-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="c7f93-106">Örneğin bir sevkiyat için en hızlı yolu veya en ucuz oranı tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="c7f93-107">Aşağıdaki tabloda, Taşıma yönetiminin kullanılmasına ilişkin ana senaryolar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7f93-107">The following table describes the main scenarios for using Transportation management.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c7f93-108">Senaryo</span><span class="sxs-lookup"><span data-stu-id="c7f93-108">Scenario</span></span></th>
<th><span data-ttu-id="c7f93-109">Taşıma yönetimi nasıl yardımcı olur?</span><span class="sxs-lookup"><span data-stu-id="c7f93-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c7f93-110">Taşıma faaliyetleri için dış lojistik sağlayıcılarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7f93-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="c7f93-111">Gelen ve/veya giden taşıma için Taşıma yönetimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7f93-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7f93-112">Şirketin teslimat/mal alımı için kullandığı kendi filosu vardır ve teslimat giderleri müşterilere aktarılır.</span><span class="sxs-lookup"><span data-stu-id="c7f93-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="c7f93-113">Giden işlemleri için, taşıma giderlerini belirlemek ve bunları müşterilere aktarmak için Taşıma yönetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="c7f93-114">Ancak, taşıyıcı fatura mutabakat işlemi gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c7f93-115">Teslimat/mal alımı için şirketin kendi filosu vardır ancak ürün fiyatı nakliyeyi içerdiğinden teslimat giderleri müşterilere aktarılmaz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="c7f93-116">Çok sayıda Taşıma yönetimi işlevi gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="c7f93-117">Bununla birlikte, taşıma fiyatlarını belirlemek ve satış fiyatını buna göre ayarlamak için Taşıma yönetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c7f93-118">Lojistik hizmeti aynı şirketteki başka bir tüzel kişilik tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="c7f93-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="c7f93-119">Başka bir tüzel kişiliği herhangi bir sevkiyat yüklenicisi olarak kullanmak için Taşıma yönetimini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="c7f93-120">Tüzel kişilikler arasındaki ekonomik hareketleri otomatik hale getiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="c7f93-121">Bu nedenle, bu hareketleri el ile işlemeniz gerekir (örneğin, bir satınalma siparişi oluşturarak).</span><span class="sxs-lookup"><span data-stu-id="c7f93-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="c7f93-122">Lojistik hizmetler sunan tüzel kişilikte, Taşıma yönetimi taşıma ücretlerini belirlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a><span data-ttu-id="c7f93-123">Supply Chain Management'ta taşımayı planlama</span><span class="sxs-lookup"><span data-stu-id="c7f93-123">Planning transportation in Supply Chain Management</span></span>
<span data-ttu-id="c7f93-124">Taşıma yönetiminde , taşıma planlaması için siparişler veya bu siparişlere göre oluşturulan sevkiyatlar temel alınır.</span><span class="sxs-lookup"><span data-stu-id="c7f93-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="c7f93-125">Sevkiyatlar daima zaman içinde bir noktada bulunmaktadır ancak taşıma planlaması için gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="c7f93-126">Transfer emirleri giden senaryosunun bir parçasıdır ve satış siparişleriyle birlikte planlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Yük çekme](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="c7f93-128">Gelen taşıma</span><span class="sxs-lookup"><span data-stu-id="c7f93-128">Inbound transportation</span></span>
<span data-ttu-id="c7f93-129">Bir satıcıya madde siparişi verdiğiniz zaman ve bu maddelerin sizin ambarınıza teslim edilmesi gerektiğinde maddeleri taşımayı kendiniz düzenlemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="c7f93-130">Gelen yükün taşıma ve girişini planlamak için Supply Chain Management kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-130">You can use Supply Chain Management to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="c7f93-131">Aşağıdaki şekilde, gelen yük için taşıma planlamasına ilişkin iş süreci akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Gelen yükün taşınmasına ilişkin iş süreci akışı](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="c7f93-133">Giden taşıma</span><span class="sxs-lookup"><span data-stu-id="c7f93-133">Outbound transportation</span></span>
<span data-ttu-id="c7f93-134">Belirli maddeleri şirketin ambarından müşteriye sevk etmek için giden yük planlaması yapabilir ve işleme koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="c7f93-135">Giden yükün taşıma ve sevkiyatını planlamak için Supply Chain Management kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-135">You can use Supply Chain Management to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="c7f93-136">Aşağıdaki şekilde, giden yükün sevkiyat için planlaması ve işleme konmasına ilişkin iş süreci akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c7f93-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Giden yükleri planlama ve işleme](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="c7f93-138">Yapıyı yükle</span><span class="sxs-lookup"><span data-stu-id="c7f93-138">Load building</span></span>
<span data-ttu-id="c7f93-139">Supply Chain Management, Hacim tabanlı yük oluşturma stratejisi olarak adlandırılan bir yük oluşturma stratejisi sunar.</span><span class="sxs-lookup"><span data-stu-id="c7f93-139">Supply Chain Management provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="c7f93-140">Bu strateji, yük şablonunda yükseklik ve ağırlık için belirtilen maksimum değerleri kullanmanıza olanak tanır; veya yeni değerler girerek ayarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="c7f93-141">Kullanmak için **Yük oluşturma workbench'i** sayfasında bulunan **Ayar** Hızlı sekmesindeki **Yük oluşturma stratejisi** alanından bu stratejiyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="c7f93-142">Ayrıca, Uygulama Nesne Ağacı'nda (AOT) yeni bir sınıf oluşturarak kendi yük oluşturma stratejinizi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7f93-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]