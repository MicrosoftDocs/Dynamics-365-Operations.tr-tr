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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020056"
---
# <a name="integrated-tax"></a><span data-ttu-id="1c096-103">Tümleşik vergi</span><span class="sxs-lookup"><span data-stu-id="1c096-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="1c096-104">Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1c096-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="1c096-105">Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.</span><span class="sxs-lookup"><span data-stu-id="1c096-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="1c096-106">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="1c096-106">Templates</span></span>

<span data-ttu-id="1c096-107">Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir varlık eşlemeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="1c096-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="1c096-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1c096-108">Finance and Operations</span></span>   | <span data-ttu-id="1c096-109">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="1c096-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="1c096-110">Vergi kodları</span><span class="sxs-lookup"><span data-stu-id="1c096-110">Tax codes</span></span>                  | <span data-ttu-id="1c096-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="1c096-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="1c096-112">Vergi grupları</span><span class="sxs-lookup"><span data-stu-id="1c096-112">Tax groups</span></span>               | <span data-ttu-id="1c096-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="1c096-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="1c096-114">Vergi maddesi grupları</span><span class="sxs-lookup"><span data-stu-id="1c096-114">Tax item groups</span></span>          | <span data-ttu-id="1c096-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="1c096-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="1c096-116">Vergi Muafiyetleri</span><span class="sxs-lookup"><span data-stu-id="1c096-116">Tax Exemptions</span></span>           | <span data-ttu-id="1c096-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="1c096-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="1c096-118">Vergi Daireleri</span><span class="sxs-lookup"><span data-stu-id="1c096-118">Tax Authorities</span></span>          | <span data-ttu-id="1c096-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="1c096-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="1c096-120">Stopaj vergisi kodları</span><span class="sxs-lookup"><span data-stu-id="1c096-120">Withholding tax codes</span></span>      | <span data-ttu-id="1c096-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="1c096-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="1c096-122">Stopaj vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="1c096-122">Withholding tax groups</span></span>   | <span data-ttu-id="1c096-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="1c096-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="1c096-124">Vergi Genel Muhasebe Hesabı Grubu</span><span class="sxs-lookup"><span data-stu-id="1c096-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="1c096-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="1c096-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

