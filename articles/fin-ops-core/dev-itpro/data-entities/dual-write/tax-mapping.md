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
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435572"
---
# <a name="integrated-tax"></a><span data-ttu-id="7446d-103">Tümleşik vergi</span><span class="sxs-lookup"><span data-stu-id="7446d-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="7446d-104">Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7446d-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="7446d-105">Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.</span><span class="sxs-lookup"><span data-stu-id="7446d-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="7446d-106">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="7446d-106">Templates</span></span>

<span data-ttu-id="7446d-107">Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir varlık eşlemeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="7446d-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="7446d-108">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="7446d-108">Finance and Operations apps</span></span> | <span data-ttu-id="7446d-109">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="7446d-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="7446d-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="7446d-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="7446d-111">Madde satış vergisi grubu</span><span class="sxs-lookup"><span data-stu-id="7446d-111">Item sales tax group</span></span> | <span data-ttu-id="7446d-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="7446d-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="7446d-113">Satış vergisi makamları</span><span class="sxs-lookup"><span data-stu-id="7446d-113">Sales tax authorities</span></span> | <span data-ttu-id="7446d-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="7446d-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="7446d-115">Satış vergisi muafiyet kodu varlığı CDS</span><span class="sxs-lookup"><span data-stu-id="7446d-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="7446d-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="7446d-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="7446d-117">Satış vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="7446d-117">Sales tax groups</span></span> | <span data-ttu-id="7446d-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="7446d-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="7446d-119">Satış vergisi genel muhasebe deftere nakil grupları V2</span><span class="sxs-lookup"><span data-stu-id="7446d-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="7446d-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="7446d-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="7446d-121">Stopaj vergisi kodları</span><span class="sxs-lookup"><span data-stu-id="7446d-121">Withholding tax codes</span></span> | <span data-ttu-id="7446d-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="7446d-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="7446d-123">Stopaj vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="7446d-123">Withholding tax groups</span></span> | <span data-ttu-id="7446d-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="7446d-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

