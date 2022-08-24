---
title: Tümleşik vergi
description: Bu makale, finans ve operasyon uygulamaları ile Dataverse arasındaki vergi tümleştirmesini açıklar.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288809"
---
# <a name="integrated-tax"></a>Tümleşik vergi

[!include [banner](../../includes/banner.md)]



Vergi ayarı verileri hem dolaylı vergilerin (KDV, GST, Satış vergisi) hem de stopaj vergisinin ayarını tanımlar. Vergi hesaplama kuralını, vergi oranını, vergi muhasebesini, kapatma işlemini ve diğer kavramları açıklar.

## <a name="templates"></a>Şablonlar

Vergi verileri, aşağıdaki tabloda gösterildiği gibi veri etkileşimi sırasında birlikte çalışan bir tablo eşlemeleri koleksiyonudur.

| Finans ve Operasyon uygulamaları | Müşteri etkileşimi uygulamaları | Açıklama |
|-----------------------------|-----------------------------------|-------------|
[Madde satış vergisi grubu](mapping-reference.md#196) | msdyn_taxitemgroups | |
[Satış vergisi makamları](mapping-reference.md#193) | msdyn_taxauthorities | |
[Satış vergisi muafiyet kodu varlığı CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[Satış vergisi grupları](mapping-reference.md#195) | msdyn_taxgroups | |
[Satış vergisi genel muhasebe deftere nakil grupları V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[Stopaj vergisi kodları](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[Stopaj vergisi grupları](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

