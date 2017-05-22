---
title: "Stok boyutu başına cari ortalama maliyeti izleme"
description: "Her stok maddesine bir stok boyutu grubu eklenir. Dolayısıyla, cari ortalama maliyet fiyatı, mali olarak izlenmekte olan stok boyutlarından seçilenlere dayanarak hesaplanır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d9d92f436ce2e0757ce69f0dd5e11234e30c2df8
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Stok boyutu başına cari ortalama maliyeti izleme

[!include[banner](../includes/banner.md)]


Her stok maddesine bir stok boyutu grubu eklenir. Dolayısıyla, cari ortalama maliyet fiyatı, mali olarak izlenmekte olan stok boyutlarından seçilenlere dayanarak hesaplanır.

Stok boyutları üç türlüdür: ürün, depolama ve izleme. Ürün boyutları; yapılandırma, ebat ve rengi içerir. Ürün boyutları her zaman mali olarak izlenir. Depolama ve izleme boyutları tesis, ambar, konum, stok durumu, plaka, toplu iş numarası ve seri numarasını içerir. Hangi depolama ve izleme boyutlarının mali olarak izleneceğine karar verebilirsiniz. 

**Örnek 1** 

Maddeye iliştirilen depolama boyutu grubu ambar tarafından mali olarak izleniyorsa, cari ortalama maliyet fiyatı her ambar için hesaplanır. Aşağıdaki satınalma siparişleri faturalandırılmıştır:

-   GW ambarı için 10,00 ABD Doları maliyet fiyatında 2 miktarı için bir satınalma siparişi faturalandırılmıştır.
-   GW ambarı için 12,00 ABD Doları maliyet fiyatında 3 miktarı için bir satınalma siparişi faturalandırılmıştır.
-   MW ambarı için 15,00 ABD Doları maliyet fiyatında 5 miktarı için bir satınalma siparişi faturalandırılmıştır.

Ambar GW için yürütülen ortalama maliyet fiyatı 11,20 ABD dolarıdır ve ambar MW için yürütülen ortalama maliyet fiyatı 15,00 ABD dolarıdır. Ambar GW için bir satış emri faturası deftere nakledilir. Stokun değeri ve satılan malların maliyeti (stok kapanışı çalıştırılmadan önce ve işaretlenmemiş olarak) 11,20 ABD dolarıdır. Ambar MW için başka bir satış emri deftere nakledilir. Stokun değeri ve satılan malların maliyeti (stok kapanışı çalıştırılmadan önce ve işaretlenmemiş olarak) 15,00 ABD dolarıdır. 

**Örnek 2** Maddeye iliştirilmiş depolama boyut grubu mali olarak ambar tarafından izleniyorsa ve izleme boyutu grubu toplu iş numarası tarafından mali olarak izleniyorsa, her toplu iş için yürütülen ortalama maliyet fiyatı hesaplanır. 

**Not:** Maliyet fiyatını her zaman izlenen tüm mali boyutlarla görüntülemenizi öneririz. Aşağıdaki satınalma siparişleri faturalandırılmıştır:

-   10,00 ABD Doları maliyet fiyatında 2 miktarı için bir satınalma siparişi; GW ambarı ve AAA toplu işi için faturalandırılmıştır.
-   12,00 ABD Doları maliyet fiyatında 3 miktarı için bir satınalma siparişi; GW ambarı ve AAA toplu işi için faturalandırılmıştır.
-   15,00 ABD Doları maliyet fiyatında 2 miktarı için bir satınalma siparişi; GW ambarı ve BBB toplu işi için faturalandırılmıştır.

Ambar GW ve toplu iş AAA için yürütülen ortalama maliyet fiyatı 11,20 ABD dolarıdır ve ambar MW ve toplu iş BBB için yürütülen ortalama maliyet fiyatı 15,00 ABD dolarıdır.



