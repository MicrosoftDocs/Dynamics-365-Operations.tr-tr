---
title: Stok değer raporu örnekleri ve mantığı
description: Bu konu, her bir stok değer raporu türünde sunulan sonuç örneklerini içerir. Stok değer raporları, stoğunuzun fiziksel ve mali miktarları ve tutarlarınız hakkında ayrıntılar sağlar.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d594fc18a104c434a334a5b6d1d249330a6be9a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675333"
---
# <a name="inventory-value-report-examples-and-logic"></a>Stok değer raporu örnekleri ve mantığı

[!include [banner](../includes/banner.md)]

Stok değer raporları, stoğunuzun fiziksel ve mali miktarları ve tutarlarınız hakkında ayrıntılar sağlar. Bu konu, her bir stok değer raporu türünde sunulan sonuç örneklerini içerir.

Her stok değer raporu türünün nasıl oluşturulacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Stok değeri raporları](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Bu örneklerde kullanılan örnek veriler

Bu konudaki örnekler, bu bölümde açıklanan örnek stok hareketi verilerini temel almaktadır.

### <a name="storage-dimension-setup"></a>Depolama boyutu kurulumu

Örnek sistem, aşağıdaki depolama boyutları kurulumunu içerir.

| Dosya Adı | Active | Fiziksel stok | Mali stok |
|---|---|---|---|
| Tesis | Evet | Evet | Evet |
| Ambar | Evet | Evet | Hayır |

### <a name="inventory-model"></a>Stok modeli

Örnek sistem için, serbest bırakılan ürünlerin stok modeli *FIFO* ve stok modeli için **Maliyet fiyatı** alanı *Fiziksel değeri dahil et* olarak ayarlanmıştır.

### <a name="inventory-transactions"></a>Stok hareketleri

Örnek sistem, *B0001* madde numarasına sahip olan serbest bırakılan ürün için aşağıdaki stok hareketlerini içerir.

| Referans | Tesis | Ambar | Giriş | Sorun | Fiili tarih | Mali tarih | Miktar | Maliyet tutarı | Fiziksel maliyet tutarı |
|---|---|---|---|---|---|---|---|---|---|
| Satın alma siparişi | 1 | 11 | Satın alınan | | Mart 15 | Mart 15 | 10 | 1,000 | 1,000 |
| Satın alma siparişi | 2 | 21 | Satın alınan | | Mart 15 | Mart 15 | 10 | 2,000 | 2,000 |
| Satın alma siparişi | 1 | 11 | Alınan | | Nisan 15 | | 5 | | 375 |
| Transfer emri | 1 | 11 | | Satılan | Mayıs 2 | Mayıs 2 | -5 | -458,33 | -458,33 |
| Transfer emri | 1 | 12 | Satın alınan | | Mayıs 2 | Mayıs 2 | 5 | 458.33 | 458.33 |
| Satış siparişi | 1 | 12 | | Satılan | Mayıs 3 | Mayıs 3 | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Stok değeri raporu yapılandırması

Örnek sistem, aşağıdaki ayarlara sahip bir stok değeri raporu konfigürasyonu içerir:

- **Aralık:**  *Deftere nakil tarihi*
- **Stok:** *Evet*
- **Ortalama birim maliyeti hesapla:** *Evet*
- **Toplam miktar ve değer:** *Evet*
- **Tesis, Görünüm:** *Seçili*
- **Kaynak Kodu, Görüntüle:** *Evet*
- **Düzey:** *Toplamlar*

## <a name="inventory-value-report-example-1"></a>Stok değeri raporu örnek 1

Aşağıdaki tablo ve çizimler, bu konunun önceki kısımlarında açıklanan örnek verileri ve rapor yapılandırmasını kullandığınızda sonuçları gösterir.

| Kaynak türü | Kaynak | Tesis | Referans | Stok Mali miktar | Stok: Mali tutar | Stok: Deftere nakledilen fiziksel miktar | Stok: Deftere nakledilen fiziksel tutar | Stok: Miktar | Stok: Tutar | Ortalama birim maliyeti |
|---|---|---|---|---|---|---|---|---|---|---|
| Malzeme | B0001 | 1 | Kapanış bakiyesi | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Malzeme | B0001 | 2 | Kapanış bakiyesi | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standart Stok değeri raporu örnek 1 için

Aşağıdaki şekil, örnek 1 için standart **Stok değeri** raporunu göstermektedir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Standart Stok değeri raporu örnek 1 için.](media/inventory-value-report-ex1-small.png "Standart Stok değeri raporu örnek 1 için")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Stok değeri rapor depolama raporunu örnek 1 için

Aşağıdaki şekil, örnek 1 için standart **Stok değeri rapor depolama** raporunu göstermektedir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Stok değeri rapor depolama raporunu örnek 1 için.](media/inventory-value-report-storage-ex1-small.png "Stok değeri rapor depolama raporunu örnek 1 için")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Stok değeri raporu örnek 2

Aşağıdaki tablo ve çizimler, bu konuda daha önce açıklanan örnek verileri kullandığınızda sonuçları gösterir, ancak rapor konfigürasyonundaki **Düzey** alanını *Hareketler* olarak değiştirirsiniz ve raporu çalıştırdığınızda **Başlangıç tarihi** alanını *15 Mart* olarak ayarlarsınız.

| Kaynak türü | Kaynak | Tesis | Tarih | Numara | Referans | Stok Mali miktar | Stok: Mali tutar | Stok: Deftere nakledilen fiziksel miktar | Stok: Deftere nakledilen fiziksel tutar | Stok: Miktar | Stok: Tutar |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Malzeme | B0001 | 1 | 3/15/2021 | 00000126 | Satın alma siparişi | 0,00 | 0,00 | 10,00 | 1,000.00 | **10.00** | **1,000.00** |
| Malzeme | B0001 | 1 | 3/15/2021 | 00000126 | Satın alma siparişi | 10,00 | 1,000.00 | -10,00 | -1.000,00 | **0.00** | **0.00** |
| Malzeme | B0001 | 1 | 4/15/2021 | 00000128 | Satın alma siparişi | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Malzeme | B0001 | 1 | 5/2/2021 | 000003 | Transfer emri sevkiyatı | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Malzeme | B0001 | 1 | 5/2/2021 | 000003 | Transfer emri teslim alma | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Malzeme | B0001 | 1 | 5/3/2021 | 000835 | Satış siparişi | 0,00 | 0,00 | -1,00 | -91,67 | **-1.00** | **-91.67** |
| Malzeme | B0001 | 1 | 5/3/2021 | 000835 | Satış siparişi | -1,00 | -91,67 | 1,00 | 91.67 | **0.00** | **0.00** |
| Malzeme | B0001 | 2 | 3/15/2021 | 00000127 | Satın alma siparişi | 0,00 | 0,00 | 10,00 | 2,000.00 | **10.00** | **2,000.00** |
| Malzeme | B0001 | 2 | 3/15/2021 | 00000127 | Satın alma siparişi | 10,00 | 2,000.00 | -10,00 | -2.000,00 | **0.00** | **0.00** |
| Malzeme | B0001 | 2 | 5/2/2021 | 000003 | Transfer emri sevkiyatı | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Malzeme | B0001 | 2 | 5/2/2021 | 000003 | Transfer emri teslim alma | -5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standart Stok değeri raporu örnek 2 için

Aşağıdaki şekil, örnek 2 için standart **Stok değeri** raporunu göstermektedir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Standart Stok değeri raporu örnek 2 için.](media/inventory-value-report-ex2-small.png "Standart Stok değeri raporu örnek 2 için")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Stok değeri rapor depolama raporunu örnek 2 için

Aşağıdaki şekil, örnek 2 için standart **Stok değeri rapor depolama** raporunu göstermektedir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Stok değeri rapor depolama raporunu örnek 2 için.](media/inventory-value-report-storage-ex2-small.png "Stok değeri rapor depolama raporunu örnek 2 için")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Stok değeri raporu örnek 3

Yeniden hesaplama veya stok kapanışından etkilenecek hareketleri ve tutarları içerecek şekilde stok değeri raporlarını çalıştırmanızı öneririz.

Aşağıdaki alt kısımlar 30 Mayıs'a kadar stoğu kapattıktan sonra oluşturulan stok değeri raporlarını gösterir.

### <a name="example-3-when-the-totals-level-is-used"></a>Toplam düzeyi kullanıldığında örnek 3

Aşağıdaki tablo, bu konunun önceki kısımlarında açıklanan örnek verileri ve rapor yapılandırmasını kullandığınızda sonuçları gösterir. (Bu rapor yapılandırmasında, **Düzey** alanı *Toplamlar* olarak ayarlanır.)

| Kaynak türü | Kaynak | Tesis | Referans | Stok Mali miktar | Stok: Mali tutar | Stok: Deftere nakledilen fiziksel miktar | Stok: Deftere nakledilen fiziksel tutar | Stok: Miktar | Stok: Tutar | Ortalama birim maliyeti |
|---|---|---|---|---|---|---|---|---|---|---|
| Malzeme | B0001 | 1 | Kapanış bakiyesi | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Malzeme | B0001 | 2 | Kapanış bakiyesi | 10,00 | 2,000.00 | 0,00 | 0,00 | 10,00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Hareketler düzeyi kullanıldığında örnek 3

Aşağıdaki tablo, bu konunun önceki bölümlerinde açıklanan örnek verileri kullandığınızda sonuçları gösterir, ancak **Düzey** alanının değerini rapor konfigürasyonundaki *Hareketler* olarak değiştirirsiniz.

| Kaynak türü | Kaynak | Tesis | Tarih | Numara | Referans | Stok Mali miktar | Stok: Mali tutar | Stok: Deftere nakledilen fiziksel miktar | Stok: Deftere nakledilen fiziksel tutar | Stok: Miktar | Stok: Tutar |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Malzeme | B0001 | 1 | 3/15/2021 | 00000126 | Satın alma siparişi | 0,00 | 0,00 | 10,00 | 1,000.00 | 10,00 | 1,000.00 |
| Malzeme | B0001 | 1 | 3/15/2021 | 00000126 | Satın alma siparişi | 10,00 | 1,000.00 | -10,00 | -1.000,00 | 0,00 | 0,00 |
| Malzeme | B0001 | 1 | 4/15/2021 | 00000128 | Satın alma siparişi | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Malzeme | B0001 | 1 | 5/2/2021 | 000003 | Transfer emri sevkiyatı | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Malzeme | B0001 | 1 | 5/2/2021 | 000003 | Transfer emri teslim alma | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Malzeme | B0001 | 1 | 5/3/2021 | 000835 | Satış siparişi | 0,00 | 0,00 | -1,00 | -91,67 | -1,00 | -91,67 |
| Malzeme | B0001 | 1 | 5/3/2021 | 000835 | Satış siparişi | -1,00 | -91,67 | 1,00 | 91.67 | 0,00 | 0,00 |
| Malzeme | B0001 | 1 | 5/31/2021 | 000835 | Satış siparişi | 0,00 | -8.33 | 0,00 | 0,00 | 0,00 | -8.33 |
| Malzeme | B0001 | 1 | 5/31/2021 | 000003 | Transfer emri sevkiyatı | 0,00 | -41.67 | 0,00 | 0,00 | 0,00 | -41.67 |
| Malzeme | B0001 | 1 | 5/31/2021 | 000003 | Transfer emri teslim alma | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Malzeme | B0001 | 2 | 3/15/2021 | 00000127 | Satın alma siparişi | 0,00 | 0,00 | 10,00 | 2,000.00 | 10,00 | 2,000.00 |
| Malzeme | B0001 | 2 | 3/15/2021 | 00000127 | Satın alma siparişi | 10,00 | 2,000.00 | -10,00 | -2.000,00 | 0,00 | 0,00 |
| Malzeme | B0001 | 2 | 5/2/2021 | 000003 | Transfer emri sevkiyatı | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Malzeme | B0001 | 2 | 5/2/2021 | 000003 | Transfer emri teslim alma | -5,00 | -458,33 | 0,00 | 0,00 | -5,00 | -458,33 |
| Malzeme | B0001 | 2 | 5/31/2021 | 000003 | Transfer emri sevkiyatı | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Malzeme | B0001 | 2 | 5/31/2021 | 000003 | Transfer emri teslim alma | 0,00 | -41.67 | 0,00 | 0,00 | 0,00 | -41.67 |
