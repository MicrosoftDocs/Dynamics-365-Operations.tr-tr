---
title: Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri
description: Bu makalede satış vergisi kodları için Hesaplama yöntemi alanının seçenekleri ve satış vergisinin aralıklar ve tüm tutarlar için nasıl hesaplanacağı açıklanmıştır.
author: kailiang
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b81780e60825021ad7a700d85257ba0f5a2447a
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715290"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Satış vergisi kodları için tüm tutar ve Aralık hesaplaması seçenekleri

[!include [banner](../includes/banner.md)]

Bu makalede, satış vergisi kodları için **Hesaplama yöntemi** alanının seçenekleri ve satış vergisinin aralıklar ve tüm tutarlar için nasıl hesaplanacağı açıklanmaktadır.

Tam tutar veya bir aralık tutarına dayalı olarak hesaplanacak bir satış vergisi kodu ayarlayabilirsiniz. **Satış vergisi kodları** sayfasında, **Hesaplama** hızlı sekmesindeki **Hesaplama yöntemi** alanını kullanarak satış vergisi kodunun nasıl hesaplanacağını seçin.
- Tüm tutar – Vergi oranı tüm vergilendirilebilir tutara uygulanır.
- Aralık – Vergilendirilebilir tutar, her biri belirli bir satış vergisi oranına sahip bir aralıkta yer alan parçalara bölünür. Belirli bir aralıkta yer alan tutarın parçası söz konusu aralığa ait vergi oranına göre vergilendirilir. Satış vergisi her tutar aralığı için hesaplanan vergi tutarlarının toplamıdır.
  > [!NOTE]                                                                                                                              
  > Aralık seçeneği, yalnızca Genel muhasebe parametreleri sayfasındaki Satış vergisi alanında Hesaplama yöntemi alanında Satır'ı seçtiğinizde kullanılabilir. 

Aralıklar, Satış vergisi kodu değerlerinde vergi oranı başına Minimum ve Maksimum sınır miktarlarını girerek ayarlanır. Seçilen hesaplama yönteminden bağımsız olarak, tüm vergilendirilebilir tutarlarda hesaplanacak vergiler için aralıkların aşağıdaki kurallara uygun olması gerekir:
-   İlk aralık sıfır şeklinde bir Minimum sınıra sahip olmalıdır.
-   Son aralıkta, sonsuzluğu belirtecek şekilde sıfır değerinde bir Maksimum sınır olması gerekir.
-   Bir aralığın Maksimum sınırı sonraki aralığın Minimum sınırı olmalıdır.

Bir tutarın önceki bir aralığın Maksimum sınırı ve sonraki aralığın Minimum sınırı olması durumunda, birinci aralığın satış vergisi oranı tutar için geçerli olacaktır. Bir tutarın üst ve alt limitlerle tanımlanan aralıkların dışında kalması durumunda, sıfıra karşılık gelen bir satış vergisi oranı uygulanır.

## <a name="example-whole-amount-method-of-calculation"></a>Örnek: Tüm tutar hesaplama yöntemi
Satış vergisi kod değerleri sayfasında, satış vergisi oranları aşağıdaki aralıklarda ayarlanır:

| Minimum sınır     | Maksimum sınır     | Vergi oranı     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | %30          |
| 50,00             | 100,00            | %20          |
| 100,00            | 0,00              | %10          |

Satış vergisi, vergiye tabi tüm tutar üzerinde hesaplanır.

| Vergiye tabi tutar (fiyat) | Hesaplama    | Satış vergisi |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a>Örnek: Aralık hesaplama yöntemi
Değerler sayfasında, satış vergisi oranları aşağıdaki aralıklarda belirlenir:

| Minimum sınır     | Maksimum sınır     | Vergi oranı     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | %30          |
| 50,00             | 100,00            | %20          |
| 100,00            | 0,00              | %10          |

Satış vergisi her tutar aralığı için hesaplanan vergi tutarlarının toplamıdır.

| Vergiye tabi tutar (fiyat) | Hesaplama                                                               | Satış vergisi |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Daha fazla bilgi için bkz. [Marjinal taban ve Hesaplama yöntemlerini temel alan satış vergisi oranları](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
