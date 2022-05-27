---
title: Vergi hesaplama yuvarlama kuralları
description: Bu konuda, vergi hesaplama hizmetinin vergi hesaplama parametrelerindeki yuvarlama kuralları hakkında bilgi sağlanmaktadır.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 167db4d836aa754509bb28677916a30901cebbbb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694188"
---
# <a name="tax-calculation-rounding-rules"></a>Vergi hesaplama yuvarlama kuralları

[!include [banner](../includes/banner.md)]

Bu konuda, vergi hesaplama hizmetinin vergi hesaplama parametrelerindeki yuvarlama kurallarının nasıl çalıştığı hakkında bilgi sağlanmaktadır.

> [!NOTE] 
> Vergi hesaplama hizmeti etkinleştirildiğinde **Satış vergisi kodu** ve **Satış vergisi grubu** sayfalarındaki yuvarlama kuralları etkin değildir.

Vergi hesaplama hizmetine yönelik yuvarlama kuralları yapılandırmasını, **Vergi hesaplama parametreleri** sayfasının **Genel** sekmesindeki **Hesaplama** hızlı sekmesinde **Satış vergisi yuvarlama kuralları** bölümünde görüntüleyebilirsiniz. (**Vergi** \> **Kurulum** \> **Vergi yapılandırması** \> **Vergi hesaplama parametreleri**).

[![Vergi hesaplama parametreleri sayfasında yuvarlama kuralı yapılandırması](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

**Yuvarlama hassasiyeti** ve **Yuvarlama yöntemi** alanları, vergi hesaplama hizmetindeki yükte hesaplanan tutarların nasıl yuvarlanacağını belirler.

## <a name="rounding-precision"></a>Yuvarlama hassasiyeti

**Yuvarlama hassasiyeti** alanları, en fazla altı ondalık basamağa sahip bir değeri destekler. Örneğin, **Yuvarlama duyarlılığı** alanını **0,000000** olarak ayarlarsanız hesaplanan tutarlar altı ondalık basamağa yuvarlanır ve ardından Microsoft Dynamics 365 Finance'e gönderilir. Örneğin, **Normal** yuvarlama yöntemi kullanılıyorsa **987,1234567** tutarı **987,123457** tutarına yuvarlanır.

> [!NOTE]
> Finance, tutarları para birimi yuvarlama kurallarına göre yuvarlar. Bu nedenle, hareketlerde gösterilen ve kaydedilen vergi tutarları vergi hesaplama yuvarlama kurallarından ve para birimi yuvarlama kurallarından etkilenir.

## <a name="rounding-method"></a>Yuvarlama yöntemi

Vergi hesaplamaya yönelik yuvarlama yöntemi her tüzel kişilik için yapılandırılabilir. **Yuvarlama yöntemi** alanında, üç seçenek arasından seçim yapabilirsiniz: **Normal**, **Aşağı yuvarlama** ve **Yukarı yuvarlama**.

### <a name="rounding-example"></a>Yuvarlama örneği

Aşağıdaki tabloda, **987,345** tutarının farklı yuvarlama hassasiyetleri ve yuvarlama yöntemleri birleşimleri için nasıl yuvarlandığını gösteren bir örnek verilmiştir.

<table>
<thead>
<tr>
<th rowspan="2">Yuvarlama yöntemi</th>
<th colspan="8">Yuvarlama hassasiyeti</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10,00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normal</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Aşağı yuvarlama</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Yukarı yuvarlama</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Vergi tutarlarını hesaplama ve yuvarlama mantığı, vergilendirme kurallarına göre yapılandırılabilir.

## <a name="rounding-by"></a>Yuvarlama ölçütü 

**Yuvarlama ölçütü** alanında, vergiler için geçerli olan yuvarlama ilkesini seçin. Aşağıdaki seçenekler bulunur:

- **Vergi kodları**: Her vergi kodunun içindeki vergi tutarını yuvarlayın.
- **Vergi kodu birleşimleri**: Satırdaki vergi kodu birleşiminin içindeki vergi tutarını yuvarlayın.

## <a name="calculation-method"></a>Hesaplama yöntemi

**Hesaplama yöntemi** alanında, faturalardaki vergilerin her satır için mi yoksa tüm satırlar için mi hesaplanacağını seçin. Aşağıdaki seçenekler bulunur:

- **Satır**: Vergi tutarını satır temelinde hesaplayın. Her bir satırdaki vergi tutarı, diğer satırlardaki vergi tutarından etkilenmez.
- **Toplam**: Tek bir belgedeki tüm satırlarda vergi tutarını hesaplayın.

### <a name="rounding-calculation-example"></a>Yuvarlama hesaplaması örneği

Bu örnekte, **Yuvarlama ölçütü** ve **Hesaplama yöntemi** değerlerinin farklı birleşimleri için bir faturada yapılabilecek farklı hesaplamalar gösterilmektedir. Bu örnekte, aşağıdaki ayarlar belirlenir:

- Faturada dört satır vardır.
- İki vergi kodu vardır: **VAT1** (yüzde 10) ve **VAT2** (yüzde 10).
- Yuvarlama duyarlılığı **0,01** olarak ayarlanmıştır.
- Yuvarlama yöntemi **Yukarı yuvarlama** olarak ayarlanmıştır.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Yuvarlama ölçütü = Vergi kodları ve Hesaplama yöntemi = Satır

| Satır numarası | Satır net tutarı | Belirlenen vergi kodları | Yuvarlamadan önceki vergi tutarı | Yuvarlanan vergi tutarı |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4           | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Yuvarlama ölçütü = Vergi kodu birleşimleri ve Hesaplama yöntemi = Satır

| Satır numarası | Satır net tutarı | Belirlenen vergi kodları | Yuvarlamadan önceki vergi tutarı | Yuvarlanan vergi tutarı |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | VAT1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,45; 4,44         |

\* Satır 2 = Yuvarlama\[22,22 × (yüzde 10 + yüzde 10)\] = 2,23 + 2,22

\*\* Satır 4 = Yuvarlama\[44,44 × (yüzde 10 + yüzde 10)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Yuvarlama ölçütü = Vergi kodları ve Hesaplama yöntemi = Toplam

| Satır numarası | Satır net tutarı | Belirlenen vergi kodları | Yuvarlamadan önceki vergi tutarı | Yuvarlanan vergi tutarı |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | VAT1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | VAT1\*; VAT2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | VAT1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | VAT1\*; VAT2\*\*     | 4,444; 4;444               | 4,44; 4,44         |

\* VAT1(Satır 1, Satır 2, Satır 3, Satır 4) = Yuvarlama\[(11,11 + 22,22 + 33,33 + 44,44) × yüzde 10\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* VAT2(Satır 2, Satır 4) = Yuvarlama\[(22,22 + 44,44) × yüzde 10\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Yuvarlama ölçütü = Vergi kodu birleşimleri ve Hesaplama yöntemi = Toplam

| Satır numarası | Satır net tutarı | Belirlenen vergi kodları | Yuvarlamadan önceki vergi tutarı | Yuvarlanan vergi tutarı |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | VAT1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | VAT1; VAT2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | VAT1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | VAT1; VAT2           | 4,444; 4;444               | 4,44; 4,45         |

\* Satır 1, Satır 3 = Yuvarlama\[(11,11 + 33,33) × yüzde 10\] = 1,12 + 3,33

\*\* Satır 2, Satır 4 = Yuvarlama\[(22,22 + 44,44) × (yüzde 10 + yüzde 10)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
