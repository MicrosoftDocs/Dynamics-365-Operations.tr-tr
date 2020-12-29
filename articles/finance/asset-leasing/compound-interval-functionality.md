---
title: Bileşik aralık işlevi
description: Bu konuda aylık, üç aylık, yarı yıllık ve yıllık bileşik aralıklar arasından seçim yapmanıza yardımcı olacak bilgiler sağlanır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c37da09f50448c27b20dfacccf2e7134b828f13b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449021"
---
# <a name="compounding-interval-functionality"></a>Bileşik aralık işlevi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda aylık, üç aylık, yarı yıllık ve yıllık bileşik aralıklar arasından seçim yapmanıza yardımcı olacak bilgiler sağlanır. Bileşik aralık işlevi, bir kiralamanın ödeme planında yıl başına bileşik dönemlerin sayısını belirlemek için kullanılır. Bu konudaki dört örneğin her biri, farklı bir aralık için kiralama ödeme planının nasıl görüneceğini gösterir.

Kiralama ödeme sıklığından daha az sıklıkta bir bileşik aralık seçemezsiniz. Örneğin, üç aylık bileşik aralık aylık ödeme sıklığıyla kullanılamaz ve yıllık bileşik aralık yarı yıllık ödeme sıklığıyla birlikte kullanılamaz. Kiralama ödeme sıklığından daha az sıklıkta bir bileşik aralık seçmeye çalışırsanız bir hata iletisi alırsınız.

> [!NOTE]
> Bu konudaki dört örnekte, bileşik aralık ödeme sıklığıyla eşleşir.

## <a name="examples"></a>Örnekler

### <a name="setup-for-all-four-leases"></a>Dört kiralama için kurulum

Aşağıdaki tablolarda, örneklerde kullanılan dört kiralama için **Genel** ve **Ödeme planı satırları** sekmelerinde ayarlanan değerler gösterilir.

**Genel sekmesi**

| Alan                      | Değer                        |
|----------------------------|------------------------------|
| Alternatif borçlanma oranı | **%5**                       |
| Yıllık ödeme türü               | **Normal yıllık ödeme**         |
| Bileşim aralığı       | Ayrı örneklere bakın. |
| Ödeme sıklığı          | **Monthly**                  |
| Başlangıç tarihi          | **01.01.2020**                 |

**Ödeme planı satırları sekmesi**

| Alan             | Değer                        |
|-------------------|------------------------------|
| Başlangıç tarihi        | **01.01.2020**                 |
| Dönemler           | **120**                      |
| Dönem aralığı   | **Aylar**                   |
| Bitiş tarihi          | **31.12.2029**               |
| Ödeme sıklığı | Ayrı örneklere bakın. |
| Ödeme tutarı    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Kiralama 1: Aylık bileşik aralık ve aylık ödeme sıklığı

Aşağıdaki tabloda, ödeme planının ilk 12 ayı listelenir. Aaşağıdaki ayrıntıları unutmayın:

- Her ay yeni bir bileşik aralık olduğundan, "Dönem" sütunundaki değer her ay 1 artar.
- "Şu anki değer" sütunundaki formülde, yılda 12 bileşik dönem olduğu için oran 12'ye bölünür. Üs değeri (üst simge rakamı), "Dönem" sütunundaki değere eşittir.

| Dönem | Ay | Date       | Ödeme tutarı | Bugünkü değer                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31.01.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>1</sup> = 49.792,53  |
| 2      | 2     | 29.02.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>2</sup> = 49.585,92  |
| 3      | 3     | 31.03.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>3</sup> = 49.380,17  |
| 4      | 4     | 30.04.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>4</sup> = 49.175,28  |
| 5      | 5     | 31.05.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>5</sup> = 48.971,23  |
| 6      | 6     | 30.06.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>6</sup> = 48.768,03  |
| 7      | 7     | 31.07.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>7</sup> = 48.565,67  |
| 8      | 8     | 31.08.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>8</sup> = 48.364,15  |
| 9      | 9     | 30.09.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>9</sup> = 48.163,47  |
| 10     | 10    | 31.10.2020 | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>10</sup> = 47.963,62 |
| 11     | 11    | 30.11.2020 | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>11</sup> = 47.764,61 |
| 12     | 12    | 31.12.2020 | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 12\])<sup>12</sup> = 47.566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Kiralama 2: Üç aylık bileşik aralık ve üç aylık ödeme sıklığı

Aşağıdaki tabloda, ödeme planının ilk 12 ayı listelenir. Aaşağıdaki ayrıntıları unutmayın:

- Her üç ay yeni bir bileşik aralık olduğundan, "Dönem" sütunundaki değer her üç ayda (her çeyrekte) 1 artar.
- "Şu anki değer" sütunundaki formülde, yılda 4 bileşik dönem olduğu için oran dörde bölünür. Üs değeri, "Dönem" sütunundaki değere eşittir.

| Dönem | Ay | Date       | Ödeme tutarı | Bugünkü değer                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 4\])<sup>1</sup> = 49.382,72 |
| 2      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30.06.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 4\])<sup>2</sup> = 48.773,05 |
| 3      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30.09.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 4\])<sup>3</sup> = 48.170,92 |
| 4      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31.12.2020 | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 4\])<sup>4</sup> = 47.576,21 |

> [!NOTE]
> Yıllık ödeme türü **Vadesi yıllık ödeme** olarak değiştirilirse, ödeme üç aylık dönemin sonu yerine üç aylık dönemin başında olur.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Kiralama 3: Yarı yıllık bileşik aralık ve yarı yıllık ödeme sıklığı

Aşağıdaki tabloda, ödeme planının ilk 12 ayı listelenir. Aaşağıdaki ayrıntıları unutmayın:

- Her yarı yıl yeni bir bileşik aralık olduğundan, "Dönem" sütunundaki değer her altı ayda (yarı yılda) 1 artar.
- "Şu anki değer" sütunundaki formülde, yılda 2 bileşik dönem olduğu için oran ikiye bölünür. Üs değeri, "Dönem" sütunundaki değere eşittir.

| Dönem | Ay | Date       | Ödeme tutarı | Bugünkü değer                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020  | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 2\])<sup>1</sup> = 48.780,49 |
| 2      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30.09.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31.12.2020 | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 2\])<sup>2</sup> = 47.590,72 |

> [!NOTE]
> Yıllık ödeme türü **Vadesi yıllık ödeme** olarak değiştirilirse ödeme, Haziran ve Aralık yerine Ocak ve Temmuz ayında olur.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Kiralama 4: Yıllık bileşik aralık ve yıllık ödeme sıklığı

Aşağıdaki tabloda, ödeme planının ilk 12 ayı listelenir. Aaşağıdaki ayrıntıları unutmayın:

- Her yıl yeni bir bileşik aralık olduğundan, "Dönem" sütunundaki değer her 12 ayda (yılda) 1 artar.
- "Şu anki değer" sütunundaki formülde, yılda bir birleşik dönem olduğu için oran 1'e bölünür. Üs değeri, "Dönem" sütunundaki değere eşittir.

| Dönem | Ay | Date       | Ödeme tutarı | Bugünkü değer                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31.01.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29.02.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31.03.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30.04.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31.05.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30.06.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31.07.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31.08.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30.09.2020  | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31.10.2020 | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30.11.2020 | 0,00           | 0,00 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31.12.2020 | 50,000.00      | 50.000 ÷ (1 + \[%5 ÷ 1\])<sup>1</sup> = 47.619,05 |

> [!NOTE]
> Yıllık ödeme türü **Vadesi yıllık ödeme** olarak değiştirilirse ödeme, Aralık yerine Ocak ayında olur.
