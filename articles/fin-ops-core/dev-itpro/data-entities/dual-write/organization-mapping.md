---
title: Dataverse'da kuruluş hiyerarşisi
description: Bu konu Finance and Operations uygulamaları ile Dataverse arasında kuruluş verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750824"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="0d76b-103">Dataverse'da kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="0d76b-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0d76b-104">Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="0d76b-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="0d76b-105">İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="0d76b-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="0d76b-106">Dataverse'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="0d76b-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="0d76b-107">Dataverse tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Dataverse'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="0d76b-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="0d76b-108">Veri akışı</span><span class="sxs-lookup"><span data-stu-id="0d76b-108">Data flow</span></span>

<span data-ttu-id="0d76b-109">Finance and Operations uygulamaları ve Dataverse'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="0d76b-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="0d76b-110">Bu kuruluş hiyerarşisi Finance and Operations uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Dataverse'da kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="0d76b-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="0d76b-111">Aşağıdaki örnekte Dataverse'ta Finance and Operations uygulamalarından Dataverse'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0d76b-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Mimari resmi](media/dual-write-data-flow.png)

<span data-ttu-id="0d76b-113">Kuruluş hiyerarşisi tablo eşlemeleri, Finance and Operations uygulamalarından Dataverse'e tek yönlü veri eşitleme için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0d76b-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="0d76b-114">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="0d76b-114">Templates</span></span>

<span data-ttu-id="0d76b-115">Ürün bilgileri, ürün boyutları veya izleme ve depolama boyutları gibi ürünle ve ürün tanımıyla ilgili tüm bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="0d76b-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="0d76b-116">Aşağıdaki tabloda gösterildiği gibi, ürün ve ilgili bilgileri eşitlemek için tablo haritaları koleksiyonu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0d76b-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="0d76b-117">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="0d76b-117">Finance and Operations apps</span></span> | <span data-ttu-id="0d76b-118">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="0d76b-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="0d76b-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d76b-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="0d76b-120">Kuruluş hiyerarşisi amaçları</span><span class="sxs-lookup"><span data-stu-id="0d76b-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="0d76b-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="0d76b-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="0d76b-122">Bu şablon, Kuruluş Hiyerarşisi Amacı tablosunun tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d76b-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="0d76b-123">Kuruluş hiyerarşisi türü</span><span class="sxs-lookup"><span data-stu-id="0d76b-123">Organization hierarchy type</span></span> | <span data-ttu-id="0d76b-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="0d76b-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="0d76b-125">Bu şablon, Kuruluş Hiyerarşisi Türü tablosunun tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d76b-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="0d76b-126">Kuruluş hiyerarşisi - yayımlandı</span><span class="sxs-lookup"><span data-stu-id="0d76b-126">Organization hierarchy - published</span></span> | <span data-ttu-id="0d76b-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="0d76b-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="0d76b-128">Bu şablon, Yayımlanan Kuruluş Hiyerarşisi tablosunun tek yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d76b-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="0d76b-129">Faaliyet birimi</span><span class="sxs-lookup"><span data-stu-id="0d76b-129">Operating unit</span></span> | <span data-ttu-id="0d76b-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="0d76b-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="0d76b-131">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="0d76b-131">Legal entities</span></span> | <span data-ttu-id="0d76b-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="0d76b-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="0d76b-133">Tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="0d76b-133">Legal entities</span></span> | <span data-ttu-id="0d76b-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="0d76b-134">cdm_companies</span></span> | <span data-ttu-id="0d76b-135">Tüzel kişilik (şirket) bilgilerinin iki yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0d76b-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="0d76b-136">Dahili Kuruluş</span><span class="sxs-lookup"><span data-stu-id="0d76b-136">Internal Organization</span></span>

<span data-ttu-id="0d76b-137">Dataverse'teki dahili kuruluş bilgileri iki tablodan gelir: **faaliyet birimi** ve **tüzel kişilikler**.</span><span class="sxs-lookup"><span data-stu-id="0d76b-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]