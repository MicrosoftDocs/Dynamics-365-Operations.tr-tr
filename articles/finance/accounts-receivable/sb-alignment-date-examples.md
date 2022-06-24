---
title: Sıralama tarihi senaryoları
description: Bu makale, uyumlu hale getirme tarihlerinin Abonelik faturalamasında işleyiş şeklini gösteren örnekler içermektedir.
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
ms.openlocfilehash: 102e3a104be5be287f914172160e95aff65d0b18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872629"
---
# <a name="alignment-date-scenarios"></a>Sıralama tarihi senaryoları

Bu makale, uyumlu hale getirme tarihlerinin Abonelik faturalamasında işleyiş şeklini gösteren örnekler içermektedir.

Bu örnekler için, faturalama zamanlamasıyla ilgili faturalama ayrıntısı 31 Ekim 2019 hizalama tarihine sahiptir. Satırın ilk faturalama ayrıntısı 31 Ekim 2019 tarihinde sona erer ve buna göre eşit olarak alınır. Satır otomatik olarak Kasım 11'in yenileme başlangıç tarihi kullanılarak yenilenir.

> [!NOTE]
> Bu yıl, hizalama tarihinin bir yıldan fazla veya az olmasına neden olabileceği için uygundur. Bu örnekler için, eşit dağıtma yöntemi **Yinelenen sözleşme faturalama parametreleri** sayfasında **Aylık** olarak ayarlanmıştır. **Günlük** olarak ayarlanmışsa, bazı kısmi tutarlar farklı olur.

## <a name="scenario-1-no-alignment"></a>Senaryo 1: Hizalama yok

Faturalama planı aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihi:** 1 Mayıs 2019
- **Bitiş tarihi:** 31 Aralık 2024
- **Tutar:** $1.000

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 30.04.2020 | | | 1,00 | | 1,00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1,00 | | 1,00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1,00 | | 1,00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Senaryo 2: Kısaltılmış hizalama

Faturalama planı aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihi:** 1 Mayıs 2019
- **Bitiş tarihi:** 31 Aralık 2024
- **Tutar:** $1.000
- **Hizalama tarihi:** 31 Aralık 2019

İlk yenileme tutarı bir yıldan az olmalıdır.

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1,00 | | 1,00 | 666.67 |
| 01.01.2020 | 31.12.2020 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 01.01.2022 | 12/31/2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1,00 | | 1,00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Senaryo 3: Uzatılmış hizalama

Faturalama planı aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihi:** 1 Mayıs 2019
- **Bitiş tarihi:** 31 Aralık 2024
- **Tutar:** $1.000
- **Hizalama tarihi:** 31 Aralık 2020

İlk yenileme tutarı bir yıldan fazla olmalıdır.

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 31.12.2020 | | | 1,00 | | 1,00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 01.01.2022 | 12/31/2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1,00 | | 1,00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Senaryo 4: Farklı bir bitiş ayına sahip hizalama

Faturalama planı aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihi:** 1 Mayıs 2019
- **Bitiş tarihi:** 31 Ekim 2024
- **Tutar:** $1.000
- **Hizalama tarihi:** 31 Aralık 2019

> [!NOTE]
> Bu senaryo şu anda yaygın değildir.

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1,00 | | 1,00 | 666.67 |
| 01.01.2020 | 31.12.2020 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1,00 | | 1,00 | 1,000.00 |
| 01.01.2022 | 12/31/2022 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1,00 | | 1,00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1,00 | | 1,00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Senaryo 5: Tek kısmi yıl

Faturalama planı aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihi:** 1 Mayıs 2019
- **Bitiş tarihi:** 31 Aralık 2019
- **Tutar:** $1.000
- **Hizalama tarihi**: 31 Aralık 2019

Bu senaryoda, hizalama tarihi gerekli değildir. Bu senaryo, otomatik yenilemeler için ortaktır.

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1,00 | | 1,00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Senaryo 6: Hesaplanan tarihler

Destek ve yenileme aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihini geçersiz kıl**: Hayır
- **Destek ve yenileme başlangıç tarihleri:** Sonraki ayın başı
- **Fatura deftere nakil tarihi:** 22 Haziran 2019
- **Hizalama tarihi:** 31 Aralık 2020

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1,00 | | 1,00 | 297.60 |
| 8/1/2019 | 31.12.2020 | | | 1,00 | | 1,00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Senaryo 7: Hesaplanan tarihler ve gelecekteki deftere nakil

Destek ve yenileme aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihini geçersiz kıl**: Hayır
- **Destek ve yenileme başlangıç tarihleri:** Sonraki ayın başı
- **Fatura deftere nakil tarihi:** 22 Haziran 2019
- **Hizalama tarihi:** 31 Aralık 2020

Bu senaryoda, hizalama tarihi 31 Aralık 2021 olarak değiştirilir.

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1,00 | | 1,00 | 0,00 |
| 8/1/2019 | 31.12.2020 | | | 1,00 | | 1,00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Senaryo 8: Manuel tarihler ve birden çok yıl

Destek ve yenileme aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihini geçersiz kıl:** Evet
- **Yenileme başlangıç tarihi:** 1 Temmuz 2020
- **Yenileme bitiş tarihi:** 31 Aralık 2024
- **Hizalama tarihi:** 31 Aralık 2021

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1,00 | | 1,00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1,00 | | 1,00 | 375.00 |
| 01.01.2022 | 12/31/2022 | | | 1,00 | | 1,00 | 250.00 |
| 1/1/2023 | 12/31/2023 | | | 1,00 | | 1,00 | 250.00 |
| 1/1/2024 | 12/31/2024 | | | 1,00 | | 1,00 | 250.00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Senaryo 9: Manuel tarihler, birden fazla yıl ve farklı bir bitiş ayı

Destek ve yenileme aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihini geçersiz kıl:** Evet
- **Yenileme başlangıç tarihi:** 1 Temmuz 2020
- **Yenileme bitiş tarihi:** 31 Ekim 2024
- **Hizalama tarihi:** 31 Aralık 2021

| Faturalama başlangıç tarihi | Faturalama bitiş tarihi | Önceki okuma | Geçerli okuma | Girilen miktar | Serbest miktar | Faturalandırılabilir miktar | Birim fiyatı |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1,00 | | 1,00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1,00 | | 1,00 | 375.00 |
| 01.01.2022 | 12/31/2022 | | | 1,00 | | 1,00 | 250.00 |
| 1/1/2023 | 12/31/2023 | | | 1,00 | | 1,00 | 250.00 |
| 1/1/2024 | 10/31/2024 | | | 1,00 | | 1,00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Senaryo 10: Eşit dağıtım olmadan hizalama

Destek ve yenileme aşağıdaki verilerle ayarlanır:

- **Başlangıç tarihini geçersiz kıl**: Hayır
- **Fatura deftere nakil tarihi:** 22 Haziran 2019
- **Hizalama tarihi:** 31 Aralık 2019

Yenileme başlangıç tarihi ve hizalama tarihleri, hem başlangıç tarihleri, hem de deftere nakil tarihinden sonra olacak şekilde düzeltilir.

- **Yenileme başlangıç tarihi:** 1 Ocak 2020
- **Yenileme bitiş tarihi:** 31 Aralık 2020
