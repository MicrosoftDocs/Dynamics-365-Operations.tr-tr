---
title: Tümleşik vergi
description: Bu konu Finance and Operations ile Common Data Service arasında vergi verileri tümleştirmesini açıklar.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173097"
---
# <a name="integrated-tax"></a><span data-ttu-id="630cb-103">Tümleşik vergi</span><span class="sxs-lookup"><span data-stu-id="630cb-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="630cb-104">Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="630cb-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="630cb-105">Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.</span><span class="sxs-lookup"><span data-stu-id="630cb-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="630cb-106">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="630cb-106">Templates</span></span>

<span data-ttu-id="630cb-107">Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir varlık eşlemeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="630cb-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="630cb-108">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="630cb-108">Finance and Operations apps</span></span> | <span data-ttu-id="630cb-109">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="630cb-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="630cb-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="630cb-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="630cb-111">Vergi kodları</span><span class="sxs-lookup"><span data-stu-id="630cb-111">Tax codes</span></span>                   | <span data-ttu-id="630cb-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="630cb-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="630cb-113">Vergi grupları</span><span class="sxs-lookup"><span data-stu-id="630cb-113">Tax groups</span></span>                 | <span data-ttu-id="630cb-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="630cb-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="630cb-115">Vergi maddesi grupları</span><span class="sxs-lookup"><span data-stu-id="630cb-115">Tax item groups</span></span>             | <span data-ttu-id="630cb-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="630cb-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="630cb-117">Vergi Muafiyetleri</span><span class="sxs-lookup"><span data-stu-id="630cb-117">Tax Exemptions</span></span>             | <span data-ttu-id="630cb-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="630cb-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="630cb-119">Vergi Daireleri</span><span class="sxs-lookup"><span data-stu-id="630cb-119">Tax Authorities</span></span>             | <span data-ttu-id="630cb-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="630cb-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="630cb-121">Stopaj vergisi kodları</span><span class="sxs-lookup"><span data-stu-id="630cb-121">Withholding tax codes</span></span>       | <span data-ttu-id="630cb-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="630cb-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="630cb-123">Stopaj vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="630cb-123">Withholding tax groups</span></span>     | <span data-ttu-id="630cb-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="630cb-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="630cb-125">Vergi Genel Muhasebe Hesabı Grubu</span><span class="sxs-lookup"><span data-stu-id="630cb-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="630cb-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="630cb-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

