---
title: Çoklu SKU konumu yönergeleri için tüm eylemleri değerlendir
description: Birden çok SKU konum yönergesi için tüm eylemleri değerlendirmek üzere yeni bir özellik eklendi. Bu sayfa, bu özelliğin nasıl açılacağı hakkında bilgi edinmeniz için size yol gösterir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477831"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Birden çok SKU seçeneği, birden çok konum yönergesi eylemini değerlendirmez

## <a name="symptoms"></a>Belirtiler

*Satış siparişleri* iş emri türünün konum yönergeleri ve *Yerine koyma* iş türü, **Birden Fazla SKU** seçeneği seçiliyken, çoklu konum yönergesi eylemlerini değerlendirmez. Yalnızca ilk konum yönergesi eylemi değerlendirilir.

## <a name="resolution"></a>Çözüm

10.0.15 sürümüne *Çoklu SKU konum yönergeleri için tüm eylemleri değerlendir* adlı yeni bir özellik eklendi (bkz. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Bu özellik çoklu SKU konum yönergeleri için tüm eylemleri değerlendirir. Bu özelliğe gereksinim duyarsanız, etkinleştirmek için [Özellik yönetimi](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)'ni kullanın.