---
title: Tümleşik vergi
description: Bu konu Finance and Operations ile Dataverse arasında vergi verileri tümleştirmesini açıklar.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 14c22dd6602b5fbf866c8dc6b057f6c8acb1f48f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679308"
---
# <a name="integrated-tax"></a><span data-ttu-id="79038-103">Tümleşik vergi</span><span class="sxs-lookup"><span data-stu-id="79038-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="79038-104">Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="79038-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="79038-105">Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.</span><span class="sxs-lookup"><span data-stu-id="79038-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="79038-106">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="79038-106">Templates</span></span>

<span data-ttu-id="79038-107">Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir tablo eşlemeleri koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="79038-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="79038-108">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="79038-108">Finance and Operations apps</span></span> | <span data-ttu-id="79038-109">Dynamics 365'teki model yönetimli uygulamalar</span><span class="sxs-lookup"><span data-stu-id="79038-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="79038-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="79038-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="79038-111">Madde satış vergisi grubu</span><span class="sxs-lookup"><span data-stu-id="79038-111">Item sales tax group</span></span> | <span data-ttu-id="79038-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="79038-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="79038-113">Satış vergisi makamları</span><span class="sxs-lookup"><span data-stu-id="79038-113">Sales tax authorities</span></span> | <span data-ttu-id="79038-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="79038-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="79038-115">Satış vergisi muafiyet kodu varlığı CDS</span><span class="sxs-lookup"><span data-stu-id="79038-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="79038-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="79038-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="79038-117">Satış vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="79038-117">Sales tax groups</span></span> | <span data-ttu-id="79038-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="79038-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="79038-119">Satış vergisi genel muhasebe deftere nakil grupları V2</span><span class="sxs-lookup"><span data-stu-id="79038-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="79038-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="79038-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="79038-121">Stopaj vergisi kodları</span><span class="sxs-lookup"><span data-stu-id="79038-121">Withholding tax codes</span></span> | <span data-ttu-id="79038-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="79038-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="79038-123">Stopaj vergisi grupları</span><span class="sxs-lookup"><span data-stu-id="79038-123">Withholding tax groups</span></span> | <span data-ttu-id="79038-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="79038-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

