---
title: Tümleşik vergi
description: Bu konu Finance and Operations ile Dataverse arasında vergi verileri tümleştirmesini açıklar.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1e74bbbeba019ca48dd823b58251643e96edd0c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782222"
---
# <a name="integrated-tax"></a>Tümleşik vergi

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar. Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.

## <a name="templates"></a>Şablonlar

Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir tablo eşlemeleri koleksiyonudur.

| Finance and Operations uygulamaları | Müşteri etkileşimi uygulamaları | Tanım |
|-----------------------------|-----------------------------------|-------------|
[Madde satış vergisi grubu](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Satış vergisi makamları](mapping-reference.md#193) | msdyn_taxauthorities | |
[Satış vergisi muafiyet kodu varlığı CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Satış vergisi grupları](mapping-reference.md#195) | msdyn_taxgroups | |
[Satış vergisi genel muhasebe deftere nakil grupları V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Stopaj vergisi kodları](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Stopaj vergisi grupları](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
