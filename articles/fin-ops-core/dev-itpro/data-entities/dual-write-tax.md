---
title: Tümleşik vergi
description: Bu konu Finance and Operations ile Common Data Service arasındaki vergi tümleştirmesini açıklar.
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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772422"
---
## <a name="integrated-tax"></a><span data-ttu-id="39789-103">Tümleşik vergi</span><span class="sxs-lookup"><span data-stu-id="39789-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39789-104">Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="39789-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="39789-105">Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.</span><span class="sxs-lookup"><span data-stu-id="39789-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="39789-106">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="39789-106">Templates</span></span>

<span data-ttu-id="39789-107">Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir varlık eşlemeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="39789-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="39789-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="39789-108">Finance and Operations</span></span>   | <span data-ttu-id="39789-109">Customer Engagement uygulaması</span><span class="sxs-lookup"><span data-stu-id="39789-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="39789-110">Vergi kodları</span><span class="sxs-lookup"><span data-stu-id="39789-110">Tax codes</span></span>                  | <span data-ttu-id="39789-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="39789-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="39789-112">Vergi grupları</span><span class="sxs-lookup"><span data-stu-id="39789-112">Tax groups</span></span>               | <span data-ttu-id="39789-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="39789-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="39789-114">Vergi maddesi grupları</span><span class="sxs-lookup"><span data-stu-id="39789-114">Tax item groups</span></span>          | <span data-ttu-id="39789-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="39789-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="39789-116">Vergi Muafiyetleri</span><span class="sxs-lookup"><span data-stu-id="39789-116">Tax Exemptions</span></span>           | <span data-ttu-id="39789-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="39789-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="39789-118">Vergi Daireleri</span><span class="sxs-lookup"><span data-stu-id="39789-118">Tax Authorities</span></span>          | <span data-ttu-id="39789-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="39789-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="39789-120">Stopaj vergisi kodları</span><span class="sxs-lookup"><span data-stu-id="39789-120">Withholding tax codes</span></span>      | <span data-ttu-id="39789-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="39789-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="39789-122">Stopaj vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="39789-122">Withholding tax groups</span></span>   | <span data-ttu-id="39789-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="39789-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="39789-124">Vergi Genel Muhasebe Hesabı Grubu</span><span class="sxs-lookup"><span data-stu-id="39789-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="39789-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="39789-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

