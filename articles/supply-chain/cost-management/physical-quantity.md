---
title: Stok nesnesi değerleri
description: Bu makalede, stok nesnesi değerlerinin nasıl hesaplandığı hakkında bilgiler verilmektedir.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a5dd487b9213f8f1289412a6a7b8112e6b57df6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670398"
---
# <a name="inventory-object-values"></a>Stok nesnesi değerleri

[!include [banner](../includes/banner.md)]

Bu makalede, stok nesnesi değerlerinin nasıl hesaplandığı hakkında bilgiler verilmektedir. 

**Fiziksel miktar** adı yeni bir işlev, belirli bir stok nesnenin değerlerini görmenizi sağlıyor. 

Maliyet nesnesi, stok muhasebesinin uygulandığı varlık düzeyini temsil eder. Maliyet nesneleri hakkında daha fazla bilgi için bkz. [Maliyet nesneleri](cost-object.md). 

Belirli stok nesnesinin değerlerini görmek için **Maliyet nesnesi** sayfasında **Fiziksel miktar**'a tıklayın. Bir stok nesnesinin değerinin nasıl hesaplanacağı aşağıda verilmiştir: 

Stok nesnesi.Değer = Maliyet nesnesi.Ortalama birim maliyeti x Stok nesnesi.Miktar 

Aşağıdaki örnekler, bir stok nesnesinin ve maliyet nesnesinin değerlerinin nasıl hesaplanacağını gösterir. A maddesinde iki ürün girişi etkinliği kayıtlıdır:

-   Ürün girişi 1: Miktar = 100 parça, Tutar = $1.000,00, Tesis = 1, Ambar = 11, Toplu İşlem No. = B1
-   Ürün girişi 2: Miktar = 50 parça, Tutar = $800,00, Tesis = 1, Ambar = 11, Toplu İşlem No. = B2

Aşağıdaki tabloda, bir maliyet nesnesi için yapılan hesaplamanın sonucu gösteriliyor. Sonucu **Maliyet nesnesi** sayfasında görüntüleyebilirsiniz.

<table>
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

<table>
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
<td>A</td>
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



## <a name="additional-resources"></a>Ek kaynaklar

[Maliyet nesneleri](cost-object.md)

[Maliyet girişleri](cost-entries.md)

[Yenilikler ve değişiklikler](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]