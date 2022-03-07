---
title: Stok yaşlandırma raporu örnekleri ve mantığı
description: Bu konu, Stok yaşlandırma raporunun sonuçlarının nasıl yorumlanacağını gösteren bazı örnekler sunar.
author: AndersGirke
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59c1740f6e07be08ad9379d4ccb6aeca29220d557aceb38bf6faef946e16fee7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752790"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Stok yaşlandırma raporu örnekleri ve mantığı

[!include [banner](../includes/banner.md)]

Bu konu, **Stok yaşlandırma** raporunun sonuçlarının nasıl yorumlanacağını gösteren bazı örnekler sunar. Bu rapor, seçili bir madde veya madde grubu için eldeki miktar ve stok değerlerini çeşitli dönem demetlerinde kategorileştirir. Bu konu ayrıca raporun iç mantığını da gösterir.

Bu konudaki örneklerde, standart **Stok yaşlandırma** raporunda sunulan sonuçlar gösterilmektedir. Ancak genel olarak, özellikle de işlenmesi gereken çok sayıda madde ve ambara sahipseniz bu raporun [Stok yaşlandırma raporu depolama](inventory-aging-report-storage.md) sürümünü kullanmanız önerilir. Stok yaşlandırma raporu depolaması, oluşturduğunuz her raporu kaydeder, sonuçları etkileşimli bir sayfa ve bir grafik olarak gösterir ve kaydedilmiş herhangi bir raporu dışa aktarmanızı sağlar.

## <a name="sample-data-that-is-used-in-these-examples"></a>Bu örneklerde kullanılan örnek veriler

Bu konudaki örnekler, bu bölümde açıklanan örnek stok hareketi verilerini temel almaktadır.

### <a name="storage-dimension-setup"></a>Depolama boyutu kurulumu

Örnek sistem, aşağıdaki depolama boyutları kurulumunu içerir.

| Dosya Adı      | Active | Fiziksel stok | Mali stok |
|-----------|--------|--------------------|---------------------|
| Tesis      | Evet    | Evet                | Evet                 |
| Ambar | Evet    | Evet                | Hayır                  |

### <a name="inventory-model"></a>Stok modeli

Örnek sistem için, serbest bırakılan ürünlerin stok modeli *FIFO* ve stok modeli için **Maliyet fiyatı** ayarı *Fiziksel değeri dahil et*'tir.

### <a name="inventory-transactions"></a>Stok hareketleri

Örnek sistem, *1000* madde numarasına sahip olan serbest bırakılan ürün için aşağıdaki stok hareketlerini içerir.

| Referans      | Tesis | Ambar | Giriş   | Çıkış | Fiili tarih | Mali tarih | Miktar | Maliyet tutarı | Fiziksel maliyet tutarı |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Satın alma siparişi | 1    | 11        | Satın alınan |       | Mart 15      | Mart 15       | 10       | 1,000       | 1,000                |
| Satın alma siparişi | 2    | 21        | Satın alınan |       | Mart 15      | Mart 15       | 10       | 2,000       | 2,000                |
| Satın alma siparişi | 1    | 11        | Alınan  |       | Nisan 15      |                | 5        |             | 375                  |
| Transfer emri | 1    | 11        |           | Satılan  | Mayıs 2         | Mayıs 2          | -5       | -458,33     | -458,33              |
| Transfer emri | 1    | 12        | Satın alınan |       | Mayıs 2         | Mayıs 2          | 5        | 458.33      | 458.33               |
| Satış siparişi    | 1    | 12        |           | Satılan  | Mayıs 3         | Mayıs 3          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Her dönem demetindeki miktarların ve tutarların hesaplanması

Önceki bölümlerde açıklanan örnek verileri kullanarak, aşağıdaki ayarlara sahip bir **Stok yaşlandırma** raporu çalıştırabilirsiniz:

- **Başlangıç tarihi:** *9 Mayıs 2020*
- **Tesis:** *Görüntüle*
- **Ambar:** *Hayır*
- **Madde numarası:** *Toplam*
- **Yaşlandırma dönemi:** Bu alanı aylık demetler oluşturmak üzere ayarlayın.

Bu durumda, oluşturulan raporun içeriği aşağıdaki örneğe benzeyecektir.

<table>
<thead>
<tr>
    <th rowspan="2">Madde kodu</th>
    <th rowspan="2">Tesis</th>
    <th rowspan="2">Eldeki miktar</th>
    <th rowspan="2">Eldeki değer</th>
    <th rowspan="2">Stok değeri miktarı</th>
    <th rowspan="2">Stok değeri</th>
    <th rowspan="2">Ortalama birim maliyeti</th>
    <th colspan="2">8/5/2020 - 1/5/2020</th>
    <th colspan="2">30/4/2020 - 1/4/2020</th>
    <th colspan="2">31/3/2020 - 1/3/2020</th>
</tr>
<tr>
    <th>P1:Miktar</th>
    <th>P1:Tutar</th>
    <th>P2:Miktar</th>
    <th>P2:Tutar</th>
    <th>P3:Miktar</th>
    <th>P3:Tutar</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Toplam</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Bu örnek raporda aşağıdaki ayrıntılara dikkat edin:

- Raporda gösterilen **Stok değeri miktarı**, **Stok değeri** ve **Ortalama birim maliyet** değerleri, mali stok boyutu (bu durumda **Tesis**) için olan değerlerdir.

    Örneğin, 1 numaralı tesiste, rapor aşağıdaki bilgileri gösterir:

    - **Stok değeri miktarı** değeri *14*'tür (= 10 + 5 – 5 + 5 – 1).
    - **Stok değeri** değeri *1.283,33*'tür (= 1.000 + 375 – 458,33 + 458,33 – 91,67).
    - **Ortalama birim maliyet** değeri *91,67*'dir.
    - Her bir dönem demetindeki **Eldeki stok değeri** değeri ve **Tutar** değeri **Ortalama birim maliyet** değeri kullanılarak hesaplanır.

- Rapor, her dönem demeti için alınan toplam stok miktarını özetleyerek her bir dönem demeti için eldeki miktarı belirler. Daha sonra, maddelerin kullandığı stok modelini dikkate almaksızın, verilen toplam miktarı düşmek için ilk giren, ilk çıkan (FIFO) ilkesini uygular.

Aynı raporu tekrar çalıştırırsanız, ancak bu kez hem **Tesis** hem de **Ambar** alanlarını *Görüntüle* olarak ayarlarsanız, yeni rapor aşağıdaki örneğe benzer.

<table>
<thead>
<tr>
    <th rowspan="2">Madde kodu</th>
    <th rowspan="2">Tesis</th>
    <th rowspan="2">Ambar</th>
    <th rowspan="2">Eldeki miktar</th>
    <th rowspan="2">Eldeki değer</th>
    <th rowspan="2">Stok değeri miktarı</th>
    <th rowspan="2">Stok değeri</th>
    <th rowspan="2">Ortalama birim maliyeti</th>
    <th colspan="2">8/5/2020 - 1/5/2020</th>
    <th colspan="2">30/4/2020 - 1/4/2020</th>
    <th colspan="2">31/3/2020 - 1/3/2020</th>
</tr>
<tr>
    <th>P1:Miktar</th>
    <th>P1:Tutar</th>
    <th>P2:Miktar</th>
    <th>P2:Tutar</th>
    <th>P3:Miktar</th>
    <th>P3:Tutar</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Toplam</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Bu kez, tesis 1, biri ambar 11 diğeri ise 12 için olmak üzere iki satıra ayrılır. Ancak, **Stok değeri miktarı**, **Stok değeri** ve **Ortalama birim maliyet** değerleri aynıdır çünkü **Ambar** mali bir stok boyutu değildir.

Ek olarak, tesis 1'in miktar dağılımının farklı olduğuna dikkat edin. Çalıştırdığınız ilk raporda, sistem aynı tesiste oluşan transfer emrini yok saymış ve satış faturası tutarını tesis 1'de **31/3/2020-1/3/2020** dönem aralığından düşürmüştü. Ancak, yeni raporda, sistem satış faturasının miktarını, Ambar 12'deki **8/5/2020-1/5/2020** dönem aralığından düşürdü.

## <a name="effects-of-inventory-closing"></a>Stok kapanışının etkileri

Mayıs için stok kapanışı çalıştırır ve ardından önceki raporu yeniden çalıştırırsanız ancak **Başlangıç tarihi** alanını *31 Mayıs 2020* olarak ayarlarsanız, aşağıdaki sonuçları görürsünüz:

- **Stok değeri** ve **Ortalama birim maliyet** değerleri güncelleştirilir.
- Her dönem demetindeki **Eldeki stok değeri** değeri ve **Tutar** değerleri buna göre güncelleştirilir.

Yeni rapor aşağıdaki örneğe benzeyecektir.

<table>
<thead>
<tr>
    <th rowspan="2">Madde kodu</th>
    <th rowspan="2">Tesis</th>
    <th rowspan="2">Ambar</th>
    <th rowspan="2">Eldeki miktar</th>
    <th rowspan="2">Eldeki değer</th>
    <th rowspan="2">Stok değeri miktarı</th>
    <th rowspan="2">Stok değeri</th>
    <th rowspan="2">Ortalama birim maliyeti</th>
    <th colspan="2">31/5/2020 - 1/5/2020</th>
    <th colspan="2">30/4/2020 - 1/4/2020</th>
    <th colspan="2">31/3/2020 - 1/3/2020</th>
</tr>
<tr>
    <th>P1:Miktar</th>
    <th>P1:Tutar</th>
    <th>P2:Miktar</th>
    <th>P2:Tutar</th>
    <th>P3:Miktar</th>
    <th>P3:Tutar</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 Toplam</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]