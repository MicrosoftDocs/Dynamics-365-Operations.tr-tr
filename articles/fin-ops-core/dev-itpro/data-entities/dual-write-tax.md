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
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853871"
---
# <a name="integrated-tax"></a>Tümleşik vergi

[!include [banner](../includes/banner.md)]

Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar. Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.

## <a name="templates"></a>Şablonlar

Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir varlık eşlemeleri topluluğudur.

Finance and Operations   | Diğer Dynamics 365 uygulamaları
-------------------------|---------------------------------
Vergi kodları                  | msdyn\_taxcodes.md
Vergi grupları               | msdyn\_taxgroups.md
Vergi maddesi grupları          | msdyn\_taxitemgroups.md
Vergi Muafiyetleri           | msdyn\_taxexemptcodes.md
Vergi Daireleri          | msdyn\_taxauthorities.md
Stopaj vergisi kodları      | msdyn\_withholdingtaxcodes.md
Stopaj vergisi grupları   | msdyn\_withholdingtaxgroups.md
Vergi Genel Muhasebe Hesabı Grubu | msdyn\_taxpostinggroups  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

