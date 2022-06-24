---
title: Satış vergisi hesaplama ve yuvarlama
description: Bu makale, satış vergisi hesaplaması ve yuvarlama hakkında genel bir bakış sağlar ve satış vergisi hesaplama ve yuvarlama kurulumunun parametrelerini açıklar.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939247"
---
# <a name="sales-tax-calculation-and-rounding"></a>Satış vergisi hesaplama ve yuvarlama

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Finance'te satış vergisi hesaplama ve yuvarlamaya dair genel bir bakış sunulmaktadır. Ayrıca, kurulumda satış vergisi hesaplama ve yuvarlama ile ilgili parametreleri ve bu parametrelerin birlikte nasıl çalıştığı da açıklanmaktadır.

## <a name="parameters"></a>Parametreler

Satış vergisi hesaplama ve yuvarlama işlemini kontrol eden birden fazla parametre bulunur:

- **Hesaplama yöntemi**: Bu parametre **Genel muhasebe parametreleri** sayfasında ayarlanır ve vergi matrahı tutarının belge başına mı yoksa satır başına mı hesaplandığını tanımlar. Satış vergisi kodunun **Marjinal taban** parametresi **Fatura bakiyesinin net tutarı** olarak ayarlanmışsa, bu parametrenin ayarından bağımsız olarak vergi matrahı tutarı her zaman belge başına hesaplanır.
- **Yuvarlama ölçütü**: Bu parametre satış vergisi grubu için ayarlanır ve vergi tutarının satış vergisi kodu başına mı satış vergisi kodu birleşimi başına mı yuvarlanacağını tanımlar.
- **Kaynak**: Bu parametre satış vergisi kodu için ayarlanır ve vergi tutarının nasıl hesaplandığını tanımlar. Daha fazla bilgi için bkz. [Kaynak alanında satış vergisi hesaplama yöntemleri](sales-tax-calculation-methods-origin-field.md).
- **Marjinal taban**: Bu parametre satış vergisi kodu için ayarlanır ve **Satış vergisi kodu değerleri** sayfasında uygun vergi oranlarını seçmek için hangi tutarın kullanılacağını belirler. Daha fazla bilgi için bkz. [Marjinal taban ve Hesaplama yöntemlerini temel alan satış vergisi oranları](marginal-base-field.md).
- **Satış vergisi yuvarlama kuralı**: Bu parametre satış vergisi kodu için ayarlanır ve belirlenen satış vergisi tutarının nasıl yuvarlanacağını (yuvarlama duyarlığı ve yuvarlama yöntemi dahil) tanımlar.

Bu makalenin geri kalanında, önceki parametrelerin birleşimini kullanan satış vergisi hesaplama ve yuvarlama işlemine dair bazı örnekler sunulmaktadır.

## <a name="scenario-for-the-examples"></a>Örnekler için senaryo

- Vergilendirilebilir belgede iki satır vardır ve her satırın vergi matrahı tutarı 42,42'dir.
- Her satır için iki satış vergisi kodu tanımlanmıştır: satış vergisi kodu 1 ve satış vergisi kodu 2.
- Vergi kodu 1 ve vergi kodu 2'nin vergi oranı yüzde 10'dur.
- Fiyata vergi dahil değildir.
- Yuvarlama duyarlığı 0,01'dir.
- Yuvarlama yöntemi **Yukarı yuvarla** olarak ayarlanmıştır.

## <a name="example-1"></a>Örnek 1

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü    | Kaynak                   | Marjinal taban       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Satır               | Satış vergisi kodu | Net tutar yüzdesi | Satır başına net tutar |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ------------| ---------------| --------------| -----------------|
| 1           | Kod 1         | 42.42         | 4.25             |
| 1           | Kod 2         | 42.42         | 4.25             |
| 2           | Kod 1         | 42.42         | 4.25             |
| 2           | Kod 2         | 42.42         | 4.25             |

Vergi matrahı tutarı satır başına hesaplanır:

- **Satır 1:** 42,42
- **Satır 2:** 42,42

Vergi tutarı satış vergisi koduna göre hesaplanır:

- **Satır 1:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 = 4,242
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 = 4,242

- **Satır 2:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 = 4,242
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 = 4,242

Vergi tutarı satış vergisi koduna göre yuvarlanır:

- **Satır 1:**

    - Satış vergisi kodu 1 için yuvarlanmış vergi tutarı = 4,25
    - Satış vergisi kodu 2 için yuvarlanmış vergi tutarı = 4,25

- **Satır 2:**

    - Satış vergisi kodu 1 için yuvarlanmış vergi tutarı = 4,25
    - Satış vergisi kodu 2 için yuvarlanmış vergi tutarı = 4,25

## <a name="example-2"></a>Örnek 2

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü    | Kaynak                   | Marjinal taban                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Satır/Toplam         | Satış vergisi kodu | Net tutar yüzdesi | Fatura bakiyesinin net tutarı |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.25             |
| 1           | Kod 2         | 42.42         | 4.25             |
| 2           | Kod 1         | 42.42         | 4.24             |
| 2           | Kod 2         | 42.42         | 4.24             |

Vergi matrahı tutarı belge başına hesaplanır:

- Vergi matrahı tutarı = 42,42 + 42,42 = 84,84

Vergi tutarı satış vergisi koduna göre hesaplanır:

- Satış vergisi kodu 1'in vergi tutarı = 84,84 &times; yüzde 10 = 8,484
- Satış vergisi kodu 2'nin vergi tutarı = 84,84 &times; yüzde 10 = 8,484

Vergi tutarı satış vergisi koduna göre yuvarlanır:

- Satış vergisi kodu 1 için yuvarlanmış vergi tutarı = 8,49
- Satış vergisi kodu 2 için yuvarlanmış vergi tutarı = 8,49

Yuvarlanmış vergi tutarı, satış vergisi koduna göre her bir satıra bölüştürülür:

- Satış vergisi kodu 1'in yuvarlanmış vergi tutarını (8,49) satır 1'e (4,25) ve satır 2'ye (4,24) bölüştürün.
- Satış vergisi kodu 2'nin yuvarlanmış vergi tutarını (8,49) satır 1'e (4,25) ve satır 2'ye (4,24) bölüştürün.

## <a name="example-3"></a>Örnek 3

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü    | Kaynak                              | Marjinal taban       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Satır               | Satış vergisi kodu | Net tutar için hesaplanan yüzde | Satır başına net tutar |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.72             |
| 1           | Kod 2         | 42.42         | 4.72             |
| 2           | Kod 1         | 42.42         | 4.72             |
| 2           | Kod 2         | 42.42         | 4.72             |

Vergi matrahı tutarı satır başına hesaplanır:

- **Satır 1:** 42,42
- **Satır 2:** 42,42

Vergi tutarı satış vergisi koduna göre hesaplanır:

- **Satır 1:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133

- **Satır 2:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133

Vergi tutarı satış vergisi koduna göre yuvarlanır:

- **Satır 1:**

    - Satış vergisi kodu 1 için yuvarlanmış vergi tutarı = 4,72
    - Satış vergisi kodu 2 için yuvarlanmış vergi tutarı = 4,72

- **Satır 2:**

    - Satış vergisi kodu 1 için yuvarlanmış vergi tutarı = 4,72
    - Satış vergisi kodu 2 için yuvarlanmış vergi tutarı = 4,72

## <a name="example-4"></a>Örnek 4

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü    | Kaynak                              | Marjinal taban                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Satır/Toplam         | Satış vergisi kodu | Net tutar için hesaplanan yüzde | Fatura bakiyesinin net tutarı |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.72             |
| 1           | Kod 2         | 42.42         | 4.72             |
| 2           | Kod 1         | 42.42         | 4.71             |
| 2           | Kod 2         | 42.42         | 4.71             |

Vergi matrahı tutarı belge başına hesaplanır:

- Vergi matrahı tutarı = 42,42 + 42,42 = 84,84

Vergi tutarı satış vergisi koduna göre hesaplanır:

- Satış vergisi kodu 1'in vergi tutarı = 84,84 &times; yüzde 10 &divide; (1 – yüzde 10) = 9,4267
- Satış vergisi kodu 2'nin vergi tutarı = 84,84 &times; yüzde 10 &divide; (1 – yüzde 10) = 9,4267

Vergi tutarı satış vergisi koduna göre yuvarlanır:

- Satış vergisi kodu 1 için yuvarlanmış vergi tutarı = 9,43
- Satış vergisi kodu 2 için yuvarlanmış vergi tutarı = 9,43

Yuvarlanmış vergi tutarı, satış vergisi koduna göre her bir satıra bölüştürülür:

- Satış vergisi kodu 1'in vergi tutarını (9,43) satır 1'e (4,72) ve satır 2'ye (4,71) bölüştürün.
- Satış vergisi kodu 2'nin vergi tutarını (9,43) satır 1'e (4,72) ve satır 2'ye (4,71) bölüştürün.

## <a name="example-5"></a>Örnek 5

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü                | Kaynak                   | Marjinal taban       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Satır               | Satış vergisi kodu kombinasyonu | Net tutar yüzdesi | Satır başına net tutar |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.25             |
| 1           | Kod 2         | 42.42         | 4.24             |
| 2           | Kod 1         | 42.42         | 4.24             |
| 2           | Kod 2         | 42.42         | 4.24             |

Vergi matrahı tutarı satır başına hesaplanır:

- **Satır 1:** 42,42
- **Satır 2:** 42,42

Vergi tutarı satış vergisi koduna göre hesaplanır:

- **Satır 1:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 = 4,242
    - satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 = 4,242

- **Satır 2:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 = 4,242
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 = 4,242

Vergi tutarı satış vergisi kodu kombinasyonuna göre yuvarlanır:

- Toplam satış vergisi tutarı = 4,242 + 4,242 + 4,242 + 4,242 = 16,968; 16,97'ye yuvarlanır

Yuvarlanmış vergi tutarı, satış vergisi koduna göre her bir satıra bölüştürülür:

- Satış vergisi tutarını (16,97) satır 1 ve satır 2'ye bölüştürün:

    - **Satır 1:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,25
        - Satış vergisi kodu 2 için vergi tutarı = 4,24

    - **Satır 2:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,24
        - Satış vergisi kodu 2 için vergi tutarı = 4,24

## <a name="example-6"></a>Örnek 6

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü                | Kaynak                   | Marjinal taban                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Satır/Toplam         | Satış vergisi kodu kombinasyonu | Net tutar yüzdesi | Fatura bakiyesinin net tutarı |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.25             |
| 1           | Kod 2         | 42.42         | 4.24             |
| 2           | Kod 1         | 42.42         | 4.24             |
| 2           | Kod 2         | 42.42         | 4.24             |

Vergi matrahı tutarı belge başına hesaplanır:

- Vergi matrahı tutarı = 42,42 + 42,42 = 84,84

Vergi tutarı satış vergisi koduna göre hesaplanır:

- Satış vergisi kodu 1'in vergi tutarı = 84,84 &times; yüzde 10 = 8,484
- Satış vergisi kodu 2'nin vergi tutarı = 84,84 &times; yüzde 10 = 8,484

Vergi tutarı satış vergisi kodu kombinasyonuna göre yuvarlanır:

- Toplam satış vergisi tutarı = 8,484 + 8,484 = 16,968; 16,97'ye yuvarlanır

Yuvarlanmış vergi tutarı, satış vergisi koduna göre her bir satıra bölüştürülür:

- Satış vergisi tutarını (16,97) satır 1 ve satır 2'ye bölüştürün:

    - **Satır 1:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,25
        - Satış vergisi kodu 2 için vergi tutarı = 4,24

    - **Satır 2:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,24
        - Satış vergisi kodu 2 için vergi tutarı = 4,24

## <a name="example-7"></a>Örnek 7

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü                | Kaynak                              | Marjinal taban       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Satır               | Satış vergisi kodu kombinasyonu | Net tutar için hesaplanan yüzde | Satır başına net tutar |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.72             |
| 1           | Kod 2         | 42.42         | 4.71             |
| 2           | Kod 1         | 42.42         | 4.71             |
| 2           | Kod 2         | 42.42         | 4.72             |

Vergi matrahı tutarı satır başına hesaplanır:

- **Satır 1:** 42,42
- **Satır 2:** 42,42

Vergi tutarı satış vergisi koduna göre hesaplanır:

- **Satır 1:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133

- **Satır 2:**

    - Satış vergisi kodu 1'in vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133
    - Satış vergisi kodu 2'nin vergi tutarı = 42,42 &times; yüzde 10 &divide; (1 – yüzde 10) = 4,7133

Vergi tutarı satış vergisi kodu kombinasyonuna göre yuvarlanır:

- Toplam satış vergisi tutarı = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532; 18,86'ya yuvarlanır

Yuvarlanmış vergi tutarı, satış vergisi koduna göre her bir satıra bölüştürülür:

- Satış vergisi tutarını (18,86) satır 1 ve satır 2'ye bölüştürün:

    - **Satır 1:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,72
        - Satış vergisi kodu 2 için vergi tutarı = 4,71

    - **Satır 2:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,71
        - Satış vergisi kodu 2 için vergi tutarı = 4,72

## <a name="example-8"></a>Örnek 8

### <a name="parameter-values"></a>Parametre değerleri

| Hesaplama yöntemi | Yuvarlama ölçütü                | Kaynak                              | Marjinal taban                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Satır/Toplam         | Satış vergisi kodu kombinasyonu | Net tutar için hesaplanan yüzde | Fatura bakiyesinin net tutarı |

### <a name="calculation-and-rounding-behavior"></a>Hesaplama ve yuvarlama davranışı

| Satır numarası | Satış vergisi kodu | Matrah tutarı | Satış vergisi tutarı |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kod 1         | 42.42         | 4.72             |
| 1           | Kod 2         | 42.42         | 4.71             |
| 2           | Kod 1         | 42.42         | 4.71             |
| 2           | Kod 2         | 42.42         | 4.72             |

Vergi matrahı tutarı belge başına hesaplanır:

- Vergi matrahı tutarı = 42,42 + 42,42 = 84,84

Vergi tutarı satış vergisi koduna göre hesaplanır:

- Satış vergisi kodu 1'in vergi tutarı = 84,84 &times; yüzde 10 &divide; (1 – yüzde 10) = 9,4267
- Satış vergisi kodu 2'nin vergi tutarı = 84,84 &times; yüzde 10 &divide; (1 – yüzde 10) = 9,4267

Vergi tutarı satış vergisi kodu kombinasyonuna göre yuvarlanır:

- Toplam satış vergisi tutarı = 9,4267 + 9,4267 = 18,8534; 18,86'ya yuvarlanır

Yuvarlanmış vergi tutarı, satış vergisi koduna göre her bir satıra bölüştürülür:

- Satış vergisi tutarını (18,86) satır 1 ve satır 2'ye bölüştürün:

    - **Satır 1:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,72
        - Satış vergisi kodu 2 için vergi tutarı = 4,71

    - **Satır 2:**

        - Satış vergisi kodu 1 için vergi tutarı = 4,71
        - Satış vergisi kodu 2 için vergi tutarı = 4,72

## <a name="additional-resources"></a>Ek kaynaklar

- [Kaynak alanında satış vergisi hesaplama yöntemleri](sales-tax-calculation-methods-origin-field.md)
- [Marjinal taban ve Hesaplama yöntemi temel alınarak Satış vergisi oranları](marginal-base-field.md)
- [Satış vergisi kodları için Tam tutar ve Aralık hesaplama seçenekleri](whole-amount-interval-options-sales-tax-codes.md)
