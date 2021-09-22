---
title: Eldekilerin listesi sayfasındaki filtre bölmesi beklendiği gibi çalışmıyor
description: "\"Eldekilerin listesi\" sayfasındaki filtre bölmesindeki filtreler, sonuçları beklediğiniz şekilde filtrelemiyor."
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477877"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Eldekilerin listesi sayfasındaki filtre bölmesi beklendiği gibi çalışmıyor

## <a name="symptoms"></a>Belirtiler

**Eldekilerin listesi** sayfasındaki filtre bölmesinde yer alan filtreler, sonuçları beklediğiniz şekilde filtrelemiyor.

## <a name="resolution"></a>Çözüm

 **Eldekilerin listesi** sayfası, kullanılabilir tüm boyutları içeren ayrıntılı bir eldeki stok tablosundan toplanır. Ancak bu sayfadaki liste bir özettir. Bu nedenle, gösterilen boyutlara göre değerleri toplayarak kaynak tablodaki satırları birleştirebilir.

Filtre bölmesinde ayarlanan filtreler, toplanan listeye değil, kaynak tabloya uygulanır. Bu davranış, [bu örneklerde](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples) gösterildiği gibi bazen beklenmeyen sonuçlar doğurabilir.

Ancak,  [ızgarada sağlanan filtreler](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) toplanan liste için *geçerlidir* . Bu filtreler kılavuzun üst kısmındaki hızlı filtreyi ve her sütun başlığının filtresini içerir.
