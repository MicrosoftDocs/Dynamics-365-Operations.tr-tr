---
title: Tümleşik vergi
description: Bu konu Finance and Operations ile Dataverse arasında vergi verileri tümleştirmesini açıklar.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e1b5d62e56dd1f87dbfedc6a8ca7379587481ff4
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542331"
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
