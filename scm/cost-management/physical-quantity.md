---
title: "Stok nesne değerleri"
description: "Bu makalede, stok nesnesi değerlerinin nasıl hesaplandığı hakkında bilgiler verilmektedir."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Stok nesne değerleri

Bu makalede, stok nesnesi değerlerinin nasıl hesaplandığı hakkında bilgiler verilmektedir. 

Adlı yeni bir işlevsellik ** fiziksel miktar ** belirli stok nesnenin değerlerini görmenizi sağlar. Maliyet nesnesi, stok muhasebesinin uygulandığı varlık düzeyini temsil eder. Maliyet nesneleri hakkında daha fazla bilgi için bkz. [Maliyet nesneleri](cost-object.md). Belirli stok nesnenin değerlerini görmek için tıklatın **fiziksel miktar** üzerinde **Maliyet nesnesine** sayfa. İşte bir stok nesnesinin değeri nasıl hesaplanır: Inventory nesnesi. Değer = maliyet nesne. Ortalama birim maliyeti × Inventory nesnesi. Aşağıdaki örnek miktarı, Inventory nesnesi ve maliyet nesnesi değerleri nasıl hesaplandığını gösterir. A maddesinde iki ürün girişi etkinliği kayıtlıdır:

-   Ürün bilgisi 1: miktar = 100 pcs., tutarı = $1,000.00, Site = 1, ambar = 11, toplu işlem No = B1
-   Ürün Bilgisi 2: Miktar = 50 pcs., tutarı = $800.00, Site = 1, ambar = 11, toplu işlem No = B2

Aşağıdaki tabloda, bir maliyet nesnesi için yapılan hesaplamanın sonucu gösteriliyor. Sonucu **Maliyet nesnesi** sayfasında görüntüleyebilirsiniz.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Nesne türü</th>
<th>Madde kodu</th>
<th>Tesis</th>
<th>Miktar</th>
<th>Stok birimi</th>
<th>Değer</th>
<th>Ortalama birim maliyeti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Maliyet nesnesi</td>
<td>A:</td>
<td>1</td>
<td>150</td>
<td>Prç</td>
<td><p>1.800,00 lira</p></td>
<td><p>12,00 lira</p></td>
</tr>
</tbody>
</table>

Aşağıdaki tabloda, bir stok nesnesi için yapılan hesaplamanın sonucu gösteriliyor. **Maliyet nesnesi** sayfasındaki **Fiziksel miktar**'a tıklayarak sonucu görüntüleyebilirsiniz.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Nesne türü</th>
<th>Madde kodu</th>
<th>Tesis</th>
<th>Ambar</th>
<th>Bordro Numarası</th>
<th>Miktar</th>
<th>Stok birimi</th>
<th>Değer</th>
<th>Ortalama birim maliyeti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stok nesnesi</td>
<td>A:</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Prç</td>
<td><p>1.200,00 lira</p></td>
<td><p>12,00 lira</p></td>
</tr>
<tr class="even">
<td>Stok nesnesi</td>
<td>A:</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Prç</td>
<td><p>600,00 lira.</p></td>
<td><p>12,00 lira</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Ayrıca bkz.
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Yeni ve değiştirilen Microsoft Dynamics AX'te nedir](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


