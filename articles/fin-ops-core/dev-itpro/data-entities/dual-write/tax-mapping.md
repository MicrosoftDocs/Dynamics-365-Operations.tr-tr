---
title: Tümleşik vergi
description: Bu konu Finance and Operations ile Dataverse arasında vergi verileri tümleştirmesini açıklar.
author: robinarh
ms.date: 09/06/2019
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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a7992520b57b4c19b6dc8e13bd8e9ffc87b40f5a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750654"
---
# <a name="integrated-tax"></a>Tümleşik vergi

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar. Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.

## <a name="templates"></a>Şablonlar

Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir tablo eşlemeleri koleksiyonudur.

Finance and Operations uygulamaları | Dynamics 365'teki model yönetimli uygulamalar | Tanım |
-------------------------|---------------------------------|----|
Madde satış vergisi grubu | msdyn_taxitemgroups |
Satış vergisi makamları | msdyn_taxauthorities |
Satış vergisi muafiyet kodu varlığı CDS | msdyn_taxexemptcodes |
Satış vergisi grupları | msdyn_taxgroups |
Satış vergisi genel muhasebe deftere nakil grupları V2 | msdyn_taxpostinggroups |
Stopaj vergisi kodları | msdyn_withholdingtaxcodes |
Stopaj vergisi grupları | msdyn_withholdingtaxgroups | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]