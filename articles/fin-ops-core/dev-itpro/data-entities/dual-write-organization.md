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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572461"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="2ed4a-103">Common Data Service'da kuruluş hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="2ed4a-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="2ed4a-104">Dynamics 365 Finance finansal bir sistem olduğundan, *kuruluş* temel bir kavramdır ve sistem kurulumu bir kuruluş hiyerarşisi yapılandırmasıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="2ed4a-105">İşletme mali öğeleri kuruluş düzeyinde ve ayrıca kuruluş hiyerarşisindeki herhangi bir düzeyde izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="2ed4a-106">Common Data Service'da kuruluş hiyerarşisi kavramı bulunmasa da, toplam satış geliri gibi birkaç genel kavramlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="2ed4a-107">Common Data Service tümleştirmesinin bir parçası olarak, kuruluş hiyerarşisi veri yapısı Common Data Service'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="2ed4a-108">Veri akışı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-108">Data flow</span></span>

<span data-ttu-id="2ed4a-109">Finance and Operations uygulamaları ve Common Data Service'dan olan işletme ekosistemi bir kuruluş hiyerarşisine sahip olmaya devam edecektir.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="2ed4a-110">Bu kuruluş hiyerarşisi Finance and Operations uygulamaları üzerinde oluşturulur ancak bilgi ve genişletilebilirlik amaçları Common Data Service'da kullanıma sunulur.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="2ed4a-111">Aşağıdaki örnekte Common Data Service'ta Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri akışı olarak sunulan kuruluş hiyerarşisi bilgileri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Mimari resmi](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="2ed4a-113">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="2ed4a-113">Templates</span></span>

<span data-ttu-id="2ed4a-114">Kuruluş hiyerarşisi varlık eşlemeleri, Finance and Operations uygulamalarından Common Data Service'a tek yönlü veri eşitleme için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="2ed4a-115">Dahili Kuruluş Hiyerarşisi Amacı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="2ed4a-116">Bu şablon, Finance and Operations'tan diğer Dynamics 365 uygulamalarına Kuruluş Hiyerarşisi Amacı varlığı için tek yönlü eşitleme sağlar.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="2ed4a-117">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-117">Source field</span></span> | <span data-ttu-id="2ed4a-118">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-118">Map type</span></span> | <span data-ttu-id="2ed4a-119">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="2ed4a-119">Destination field</span></span>
---|---|---
<span data-ttu-id="2ed4a-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="2ed4a-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="2ed4a-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="2ed4a-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="2ed4a-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="2ed4a-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="2ed4a-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="2ed4a-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="2ed4a-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="2ed4a-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="2ed4a-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="2ed4a-127">msdyn\_immutable</span></span>
<span data-ttu-id="2ed4a-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="2ed4a-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="2ed4a-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="2ed4a-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="2ed4a-130">Dahili Kuruluş Hiyerarşisi Türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="2ed4a-131">Bu şablon, Finance and Operations'tan diğer Dynamics 365 uygulamalarına Kuruluş Hiyerarşisi Türü varlığı için tek yönlü eşitleme sağlar.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="2ed4a-132">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-132">Source field</span></span> | <span data-ttu-id="2ed4a-133">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-133">Map type</span></span> | <span data-ttu-id="2ed4a-134">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="2ed4a-134">Destination field</span></span>
---|---|---
<span data-ttu-id="2ed4a-135">AD</span><span class="sxs-lookup"><span data-stu-id="2ed4a-135">NAME</span></span> | \> | <span data-ttu-id="2ed4a-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="2ed4a-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="2ed4a-137">Dahili Kuruluş Hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="2ed4a-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="2ed4a-138">Bu şablon, Finance and Operations'tan diğer Dynamics 365 uygulamalarına Yayımlanan Kuruluş Hiyerarşisi varlığı için tek yönlü eşitleme sağlar.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="2ed4a-139">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-139">Source field</span></span> | <span data-ttu-id="2ed4a-140">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-140">Map type</span></span> | <span data-ttu-id="2ed4a-141">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="2ed4a-141">Destination field</span></span>
---|---|---
<span data-ttu-id="2ed4a-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="2ed4a-142">VALIDTO</span></span> | \> | <span data-ttu-id="2ed4a-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="2ed4a-143">msdyn\_validto</span></span>
<span data-ttu-id="2ed4a-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="2ed4a-144">VALIDFROM</span></span> | \> | <span data-ttu-id="2ed4a-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="2ed4a-145">msdyn\_validfrom</span></span>
<span data-ttu-id="2ed4a-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="2ed4a-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="2ed4a-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="2ed4a-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="2ed4a-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="2ed4a-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="2ed4a-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="2ed4a-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="2ed4a-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="2ed4a-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="2ed4a-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="2ed4a-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="2ed4a-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="2ed4a-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="2ed4a-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="2ed4a-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="2ed4a-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="2ed4a-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="2ed4a-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="2ed4a-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="2ed4a-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="2ed4a-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="2ed4a-158">Dahili Kuruluş</span><span class="sxs-lookup"><span data-stu-id="2ed4a-158">Internal Organization</span></span>

<span data-ttu-id="2ed4a-159">Common Data Service'daki dahili kuruluş bilgileri iki varlıktan gelir: **Faaliyet birimi** ve **Tüzel kişilikler**.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="2ed4a-160">Faaliyet birimi</span><span class="sxs-lookup"><span data-stu-id="2ed4a-160">Operating unit</span></span>

<span data-ttu-id="2ed4a-161">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-161">Source field</span></span> | <span data-ttu-id="2ed4a-162">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-162">Map type</span></span> | <span data-ttu-id="2ed4a-163">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="2ed4a-163">Destination field</span></span>
---|---|---
<span data-ttu-id="2ed4a-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="2ed4a-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="2ed4a-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="2ed4a-165">msdyn\_languageid</span></span>
<span data-ttu-id="2ed4a-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="2ed4a-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="2ed4a-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="2ed4a-167">msdyn\_namealias</span></span>
<span data-ttu-id="2ed4a-168">AD</span><span class="sxs-lookup"><span data-stu-id="2ed4a-168">NAME</span></span> | \> | <span data-ttu-id="2ed4a-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="2ed4a-169">msdyn\_name</span></span>
<span data-ttu-id="2ed4a-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="2ed4a-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="2ed4a-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="2ed4a-171">msdyn\_partynumber</span></span>
<span data-ttu-id="2ed4a-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="2ed4a-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="2ed4a-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="2ed4a-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="2ed4a-174">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="2ed4a-174">Legal entity</span></span>

<span data-ttu-id="2ed4a-175">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-175">Source field</span></span> | <span data-ttu-id="2ed4a-176">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-176">Map type</span></span> | <span data-ttu-id="2ed4a-177">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="2ed4a-177">Destination field</span></span>
---|---|---
<span data-ttu-id="2ed4a-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="2ed4a-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="2ed4a-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="2ed4a-179">msdyn\_namealias</span></span>
<span data-ttu-id="2ed4a-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="2ed4a-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="2ed4a-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="2ed4a-181">msdyn\_languageid</span></span>
<span data-ttu-id="2ed4a-182">AD</span><span class="sxs-lookup"><span data-stu-id="2ed4a-182">NAME</span></span> | \> | <span data-ttu-id="2ed4a-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="2ed4a-183">msdyn\_name</span></span>
<span data-ttu-id="2ed4a-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="2ed4a-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="2ed4a-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="2ed4a-185">msdyn\_partynumber</span></span>
<span data-ttu-id="2ed4a-186">yok</span><span class="sxs-lookup"><span data-stu-id="2ed4a-186">none</span></span> | \>\> | <span data-ttu-id="2ed4a-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="2ed4a-187">msdyn\_type</span></span>
<span data-ttu-id="2ed4a-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="2ed4a-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="2ed4a-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="2ed4a-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="2ed4a-190">Şirket</span><span class="sxs-lookup"><span data-stu-id="2ed4a-190">Company</span></span>

<span data-ttu-id="2ed4a-191">Finance and Operations ve diğer Dynamics 365 uygulamaları arasında tüzel kişi (şirket) bilgilerinin çift yönlü eşitlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2ed4a-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="2ed4a-192">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="2ed4a-192">Source field</span></span> | <span data-ttu-id="2ed4a-193">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="2ed4a-193">Map type</span></span> | <span data-ttu-id="2ed4a-194">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="2ed4a-194">Destination field</span></span>
---|---|---
<span data-ttu-id="2ed4a-195">AD</span><span class="sxs-lookup"><span data-stu-id="2ed4a-195">NAME</span></span> | = | <span data-ttu-id="2ed4a-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="2ed4a-196">cdm\_name</span></span>
<span data-ttu-id="2ed4a-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="2ed4a-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="2ed4a-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="2ed4a-198">cdm\_companycode</span></span>
