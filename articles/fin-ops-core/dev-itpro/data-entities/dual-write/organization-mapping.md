---
title: Common Data Service'da kuruluş hiyerarşisi
description: Bu konu Finance and Operations uygulamaları ile Common Data Service arasında kuruluş verileri tümleştirmesini açıklar.
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
ms.openlocfilehash: fc5db8d04a2860df0c917816e2910c6fbda941ff
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173166"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="ae220-103">Common Data Service'da kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="ae220-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="ae220-104">Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="ae220-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="ae220-105">İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ae220-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="ae220-106">Common Data Service'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="ae220-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="ae220-107">Common Data Service tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Common Data Service'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="ae220-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="ae220-108">Veri akışı</span><span class="sxs-lookup"><span data-stu-id="ae220-108">Data flow</span></span>

<span data-ttu-id="ae220-109">Finance and Operations uygulamaları ve Common Data Service'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="ae220-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="ae220-110">Bu kuruluş hiyerarşisi Finance and Operations uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Common Data Service'da kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="ae220-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="ae220-111">Aşağıdaki örnekte Common Data Service'ta Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ae220-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Mimari resmi](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="ae220-113">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="ae220-113">Templates</span></span>

<span data-ttu-id="ae220-114">Kuruluş hiyerarşisi varlık eşlemeleri, Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri eşitleme için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ae220-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="ae220-115">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="ae220-115">Templates</span></span>

<span data-ttu-id="ae220-116">Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="ae220-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="ae220-117">Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için varlık haritaları koleksiyonu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ae220-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="ae220-118">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="ae220-118">Finance and Operations apps</span></span> | <span data-ttu-id="ae220-119">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="ae220-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="ae220-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae220-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="ae220-121">Kuruluş hiyerarşisi amaçları</span><span class="sxs-lookup"><span data-stu-id="ae220-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="ae220-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="ae220-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="ae220-123">Bu şablon, Kuruluş Hiyerarşisi Amacı varlığının tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae220-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="ae220-124">Kuruluş hiyerarşisi türü</span><span class="sxs-lookup"><span data-stu-id="ae220-124">Organization hierarchy type</span></span> | <span data-ttu-id="ae220-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="ae220-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="ae220-126">Bu şablon, Kuruluş Hiyerarşisi Türü varlığının tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae220-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="ae220-127">Yayımlanan kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="ae220-127">Organization hierarchy - published</span></span> | <span data-ttu-id="ae220-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="ae220-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="ae220-129">Bu şablon, Yayımlanan Kuruluş Hiyerarşisi varlığının tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae220-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="ae220-130">Faaliyet birimi</span><span class="sxs-lookup"><span data-stu-id="ae220-130">Operating unit</span></span> | <span data-ttu-id="ae220-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ae220-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="ae220-132">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="ae220-132">Legal entities</span></span> | <span data-ttu-id="ae220-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ae220-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="ae220-134">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="ae220-134">Legal entities</span></span> | <span data-ttu-id="ae220-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="ae220-135">cdm_companies</span></span> | <span data-ttu-id="ae220-136">Tüzel kişilik (şirket) bilgilerinin iki yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ae220-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="ae220-137">Dahili Kuruluş</span><span class="sxs-lookup"><span data-stu-id="ae220-137">Internal Organization</span></span>

<span data-ttu-id="ae220-138">Common Data Service'daki dahili kuruluş bilgileri iki varlıktan gelir: **Faaliyet birimi** ve **Tüzel kişilikler**.</span><span class="sxs-lookup"><span data-stu-id="ae220-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

