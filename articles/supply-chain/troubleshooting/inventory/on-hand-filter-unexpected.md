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
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920510"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Eldekilerin listesi sayfasındaki filtre bölmesi beklendiği gibi çalışmıyor

## <a name="symptoms"></a>Belirtiler

**Eldeki liste** sayfasındaki filtre bölmesinde bulunan filtreler, sonuçları beklediğiniz şekilde filtrelemiyor.

## <a name="resolution"></a>Çözüm

**Eldeki liste** sayfası, kullanılabilir tüm boyutları içeren ayrıntılı bir eldeki stok tablosundan toplanır. Ancak bu sayfadaki liste bir özettir. Bu nedenle, gösterilen boyutlara göre değerleri toplayarak kaynak tablodaki satırları birleştirebilir.

Filtre bölmesinde ayarlanan filtreler, toplanan listeye değil, kaynak tabloya uygulanır. Bu davranış, [bu örneklerde](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples) gösterildiği gibi bazen beklenmeyen sonuçlar doğurabilir.

Ancak, [kılavuzda sağlanan filtreler](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) toplanan liste için *geçerlidir*. Bu filtreler kılavuzun üst kısmındaki hızlı filtreyi ve her sütun başlığının filtresini içerir.
