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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000746"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="d0b20-103">Common Data Service'da kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="d0b20-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0b20-104">Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="d0b20-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="d0b20-105">İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="d0b20-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="d0b20-106">Common Data Service'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="d0b20-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="d0b20-107">Common Data Service tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Common Data Service'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="d0b20-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="d0b20-108">Veri akışı</span><span class="sxs-lookup"><span data-stu-id="d0b20-108">Data flow</span></span>

<span data-ttu-id="d0b20-109">Finance and Operations uygulamaları ve Common Data Service'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="d0b20-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="d0b20-110">Bu kuruluş hiyerarşisi Finance and Operations uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Common Data Service'da kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="d0b20-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="d0b20-111">Aşağıdaki örnekte Common Data Service'ta Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d0b20-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Mimari resmi](media/dual-write-data-flow.png)

<span data-ttu-id="d0b20-113">Kuruluş hiyerarşisi varlık eşlemeleri, Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri eşitleme için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d0b20-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="d0b20-114">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="d0b20-114">Templates</span></span>

<span data-ttu-id="d0b20-115">Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="d0b20-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="d0b20-116">Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için varlık haritaları koleksiyonu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d0b20-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="d0b20-117">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="d0b20-117">Finance and Operations apps</span></span> | <span data-ttu-id="d0b20-118">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="d0b20-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d0b20-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0b20-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="d0b20-120">Kuruluş hiyerarşisi amaçları</span><span class="sxs-lookup"><span data-stu-id="d0b20-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="d0b20-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="d0b20-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="d0b20-122">Bu şablon, Kuruluş Hiyerarşisi Amacı varlığının tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d0b20-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="d0b20-123">Kuruluş hiyerarşisi türü</span><span class="sxs-lookup"><span data-stu-id="d0b20-123">Organization hierarchy type</span></span> | <span data-ttu-id="d0b20-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="d0b20-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="d0b20-125">Bu şablon, Kuruluş Hiyerarşisi Türü varlığının tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d0b20-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="d0b20-126">Yayımlanan kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="d0b20-126">Organization hierarchy - published</span></span> | <span data-ttu-id="d0b20-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="d0b20-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="d0b20-128">Bu şablon, Yayımlanan Kuruluş Hiyerarşisi varlığının tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d0b20-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="d0b20-129">Faaliyet birimi</span><span class="sxs-lookup"><span data-stu-id="d0b20-129">Operating unit</span></span> | <span data-ttu-id="d0b20-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d0b20-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d0b20-131">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="d0b20-131">Legal entities</span></span> | <span data-ttu-id="d0b20-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d0b20-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d0b20-133">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="d0b20-133">Legal entities</span></span> | <span data-ttu-id="d0b20-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="d0b20-134">cdm_companies</span></span> | <span data-ttu-id="d0b20-135">Tüzel kişilik (şirket) bilgilerinin iki yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d0b20-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="d0b20-136">Dahili Kuruluş</span><span class="sxs-lookup"><span data-stu-id="d0b20-136">Internal Organization</span></span>

<span data-ttu-id="d0b20-137">Common Data Service'daki dahili kuruluş bilgileri iki varlıktan gelir: **Faaliyet birimi** ve **Tüzel kişilikler**.</span><span class="sxs-lookup"><span data-stu-id="d0b20-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
