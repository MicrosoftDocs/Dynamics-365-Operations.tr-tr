---
title: Konsolidasyon şirketinde para birimi yeniden değerleme
description: Bu makalede, bir konsolidasyon şirketinde para biriminin nasıl yeniden değerleneceği açıklanmaktadır.
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779675"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Konsolidasyon şirketinde para birimi yeniden değerleme

[!include [banner](../includes/banner.md)]

Verileri bir hesap para biriminden öbürüne birleştirdiğinizde, para biriminde değişiklik varsa para birimi yeniden değerlendirmesini hâlâ çalıştırmanız gerekir, böylece hesap bakileri doğru yeniden değerlendirilir. Özgün verileri birleştirdiğinizde, **para birimi çeviri** sekmesini kullanarak ilk birleştirme işlemi sırasında döviz kurları çevirmek için seçin. Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir. Gerçekleşmemiş Kazançlar veya zararlar sonra buna göre yeni döviz kuru ve tarihe göre güncelleştirilir. Aşağıdaki örnek işlem sırasında oluşturulan hesap girişlerini gösterir.

## <a name="company-setup"></a>Şirket ayarı
-   **Kaynak ve işletim şirketi (USMF)** – ABD doları (USD), muhasebe ve raporlama para birimi kullanılır.
-   **Konsolide şirket (CON)** – muhasebe ve raporlama para birimi Euro (EUR) kullanılır.
    -   **Gerçekleşmiş Kazanç** – genel muhasebe hesabı 801500
    -   **Gerçekleşmiş kayıp** – genel muhasebe hesabı 801600
    -   **Gerçekleşmemiş Kazanç**– genel muhasebe hesabı 801600
    -   **Gerçekleşmemiş kayıp**– genel muhasebe hesabı 801400

## <a name="original-transactions"></a>Özgün hareketler
### <a name="cash-receipt-transactions-in-usmf"></a>USMF'de Nakit Tahsilat hareketleri

| Tarih       | Genel muhasebe hesabı               | Para birimi | Tutar |
|------------|------------------------------|----------|--------|
| 11.10.2020 | 110110 – Nakit                | ABD Doları      | 500    |
| 11.10.2020 | 130100 – Alacak Hesapları | ABD Doları      | -500   |

## <a name="exchange-rates"></a>Döviz kurları

| Kaynak para birimi | Hedef para birimi | Başlangıç tarihi | Döviz kuru |
|---------------|-------------|------------|---------------|
| EUR           | ABD Doları         | 01.10.2020  | 200           |
| EUR           | ABD Doları         | 01.11.2020  | 150           |
| EUR           | ABD Doları         | 01.12.2017  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>Ekim 2020 için konsolidasyon gerçekleştirme
### <a name="balances-in-the-consolidation-company"></a>Konsolidasyon şirketinde bakiyeler

| Genel muhasebe hesabı | Para birimi | Tutar | Hesaplama    |
|----------------|----------|--------|----------------|
| 110110         | Euro      | 250    | 500 USD × %50  |
| 130100         | Euro      | -250   | -500 USD × %50 |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>1 Ekim 2020 ile 30 Kasım 2020 hesaplarından para birimi yeniden değerleme gerçekleştirme
### <a name="balances-in-the-consolidation-company"></a>Konsolidasyon şirketinde bakiyeler

| Genel muhasebe hesabı | Para birimi | Tutar  | Hesaplama                        |
|----------------|----------|---------|------------------------------------|
| 110110         | Euro      | 333.33  | Orijinal tutar 500 × %66,6667  |
| 130100         | Euro      | -333.33 | Orijinal tutar -500 × %66,6667 |
| 801400         | Euro      | 83.33   | 333.33 – 250                       |
| 801600         | Euro      | -83.33  | -333.33 – (-250)                   |

Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>1 Ekim 2020 ile 31 Aralık 2020 hesaplarından para birimi yeniden değerleme gerçekleştirme
### <a name="balances-in-the-consolidation-company"></a>Konsolidasyon şirketinde bakiyeler

| Genel muhasebe hesabı | Para birimi | Tutar  | Hesaplama                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | Euro      | 500.00  | Orijinal tutar of 500 × 1                           |
| 130100         | Euro      | -500.00 | Orijinal tutar -500 × 1                          |
| 801400         | Euro      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | Euro      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
