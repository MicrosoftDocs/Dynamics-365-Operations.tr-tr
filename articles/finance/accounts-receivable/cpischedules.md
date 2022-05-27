---
title: Tüketici fiyat endeksi planı
description: Bu konu, abonelik faturalamasındaki artış masrafının belirlenmesine yardımcı olmak amacıyla, internetten elde ettiğiniz tüketici fiyat endeksi (TÜFE) planlarının listesinin nasıl oluşturulacağını açıklamaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 54114fae25565ed1aae7056ef9be5a4a159291e9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686533"
---
# <a name="consumer-price-index-schedule"></a>Tüketici fiyat endeksi planı

[!include [banner](../includes/banner.md)]

Bu konu, tüketici fiyat endeksi (TÜFE) planlarının nasıl oluşturulacağını, silineceğini, gözden geçirileceğini ve işleneceğini açıklamaktadır. TÜFE planı, faturalama planı satırları olarak eklediğiniz tüketici mal ve hizmetlerinin fiyatlarını belirlemek için kullanılabilir. TÜFE planı daha sonra bir faturalama planında artış ve indirim fiyatlandırmasıyla kullanılabilir veya faturalama planlarındaki faturalama tutarlarını güncelleştirmek için el ile işlenebilir. TÜFE planlarını el ile girebilir veya TÜFE planı bileşik varlığını kullanarak içe aktarabilirsiniz.

TÜFE planı eklemek için şu adımları izleyin.

1. **Tüketici fiyat endeksi planı** sayfasında **Yeni**'yi seçin.
2. **Tüketici fiyat endeksi planı** alanına benzersiz bir ad girin.
3. **Açıklama** alanına bir açıklama girin.
4. **Tüketici fiyat endeksi planı** sekmesinde **Ekle**'yi seçin.
5. **Müşteri fiyat endeksi tarihi** alanında, yeni TÜFE planının etkin olacağı tarihi belirtin.
6. **Müşteri fiyat endeksi planı** alanında, adım 2'de girdiğiniz adı girin.
7. **Kaydet**'i seçin.

TÜFE planı tarihini silmek için bu adımları izleyin.

1. **Tüketici fiyat endeksi planı** sayfasında, silmek istediğiniz bir veya daha fazla satırı seçin ve ardından **Kaldır**'ı seçin.
2. Tüm TÜFE planını silmek için Eylem bölmesinde, **Sil**'i seçin. Seçili TÜFE planını, herhangi bir faturalama planıyla ilişkiliyse silemezsiniz.
3. Eylem bölmesinde, seçili TÜFE planını kullanan faturalama planlarını güncelleştirmek için **İşlem**'i seçin. Faturalama planı fiyatlarını güncelleştirmek için en son TÜFE tarihleri ve plan tutarları kullanılır.
4. **Tüketici fiyat endeksi işlemi** hızlı sekmesinde, güncelleştirilmiş **Faturalama planı numarası**, **Madde numarası**, **Faturalama başlangıç tarihi**, **Faturalama bitiş tarihi**, **Artış tarihi** ve **Artış sıklığı** alanlarını gözden geçirin.

TÜFE planları ayarlandıktan sonra, faturalama planlarındaki fiyat artışı ve iskontosu değişiklikleri için kullanılabilir.

## <a name="cpi-calculation"></a>TÜFE hesaplama

Bu örnekler için dönem, 1 Ocak 2020 ile 31 Aralık 2022 arasındadır. Temel TÜFE değeri (sözleşme başladığındaki TÜFE değeri) 105,65'tir. 1 Ocak 2021 tarihinde geçerli TÜFE 110,5'tir. 1 Ocak 2022 tarihinde geçerli TÜFE 114,25'tir. Başlangıç tutarı 1.000 $'dır.

**Örnek 1**

**Yinelenen sözleşme faturalama parametreleri** sayfasında, **Tüketici fiyat endeksi hesaplama** alanını **Temel tüketici fiyat endeksi** olarak ayarlarsınız.

1 Ocak 2021 dönemi için ilk artış tutarı, başlangıçtaki tutara göre aşağıdaki şekilde hesaplanır:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

1 Ocak 2022 dönemi için artış tutarı, aşağıdaki şekilde hesaplanır:

1.000 + (114,25 – 105,65) &divide; 105,65 &times; 1.000 = 1.081,40

**Örnek 2**

**Yinelenen sözleşme faturalama parametreleri** sayfasında, **Tüketici fiyat endeksi hesaplama** alanını **Önceki tüketici fiyat endeksi** olarak ayarlarsınız.

1 Ocak 2021 dönemi için ilk artış tutarı, başlangıçtaki tutara göre aşağıdaki şekilde hesaplanır:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

1 Ocak 2022 dönemi için artış tutarı, ilk artış tutarına göre aşağıdaki şekilde hesaplanır:

1.045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1.045,91 = 1.081,40

> [!NOTE]
> Artış işlemi, endeks tarihinden bağımsız olarak her zaman en son TÜFE değerini kullanır. Örneğin, artış Eylül'de gerçekleşmiş ancak en son TÜFE değeri Temmuz için ise, Temmuz endeksi kullanılır. Eylül endeksi girildikten sonra hiçbir düzeltme yapılmaz.

## <a name="prorated-escalation"></a>Orantılı olarak dağıtılmış artış

Artış bir faturalama döneminin ortasında gerçekleşirse, tutar orantılı olarak dağıtılır. Örneğin, faturalama dönemi 1 Ağustos 2020 ile 31 Temmuz 2021 arasındadır. 1 Eylül 2019 olan TÜFE tarihinde TÜFE değeri 244'tür. 1 Eylül 2020 olan TÜFE tarihinde bu TÜFE değeri 250'dir. Önceki değer 1.000 ise, döneme ait faturalama tutarını hesaplamak için aşağıdaki formüller kullanılır:

* *TÜFE değişimleri* = (250 – 244) &divide; 244 = %2,459
* *Geçerli değer* = 1.000 &times; %2,459 = 1.024,59
* *Geçerli değerin uygulandığı gün sayısı* = 31 Temmuz 2021 – 1 Eylül 2020 = 334
* *Önceki değer* = 1.000
* *Önceki değerin uygulandığı gün sayısı* = 31 Ağustos 2020 – 1 Ağustos 2020 = 31
* *Faturalama dönemindeki toplam gün sayısı* = 31 Temmuz 2021 – 1 Ağustos 2020 + 1 = 365
* *Bu dönem için faturalama tutarı* = (1.000 &times; 31 &divide; 365) + (1.024,59 &times; 334 &divide; 365) = 1.022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>TÜFE ve yüzdeyi kullanan artış

Artışlar TÜFE kullanılarak uygulanabilir. TÜFE artı yüzde 3 artış 1 Ocak 2020 tarihinde başlar ve yıllık sıklığa sahiptir.

- 1 Ocak 2019 ile 31 Aralık 2020 arasında faturalanan tutar 4.000'dir.
- Fiyat artışı yapılacak faturalama dönemi 1 Ocak 2020 ile 31 Aralık 2020 arasındadır.
- 1 Aralık 2018 olan TÜFE tarihinde TÜFE değeri 205,3'tür. 1 Aralık 2019 olan TÜFE tarihinde TÜFE değeri 219,6'dır.

Önceki değer 4.000 ise, bu döneme ait faturalama tutarı aşağıdaki şekilde hesaplanır:

- *TÜFE değişimleri* = (219.6 – 205.3) &divide; 205.3 = %6,965
- *Geçerli değer* = (4.000 &times; %6,965) – 4000 = 278,60
- *Yüzde değişimleri* = (4.000 &times; 1,03) – 4.000 = 120
- *Faturalama tutarı* = 4.000 + 278,6 + 120 = 4.398,6
