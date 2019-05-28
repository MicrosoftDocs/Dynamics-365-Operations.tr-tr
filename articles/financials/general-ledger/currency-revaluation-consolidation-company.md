---
title: Konsolidasyon şirketinde para birimi yeniden değerleme
description: Bu konu, para birimini bir konsolidasyon şirketinde yeniden değerlemeyi açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567295"
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

| Tarih       | Genel muhasebe hesabı               | Para Birimi | Tutar |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 – Nakit                | ABD Doları      | 500    |
| 10/11/2015 | 130100 – Alacak Hesapları | ABD Doları      | -500   |

## <a name="exchange-rates"></a>Döviz kurları

| Kaynak para birimi | Hedef para birimi | Başlangıç tarihi | Döviz kuru |
|---------------|-------------|------------|---------------|
| Euro           | ABD Doları         | 10/1/2015  | 200           |
| Euro           | ABD Doları         | 11/1/2015  | 150           |
| Euro           | ABD Doları         | 12/1/2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Ekim 2015 için konsolidasyon gerçekleştirme
### <a name="balances-in-the-consolidation-company"></a>Konsolidasyon şirketinde bakiyeler

| Genel muhasebe hesabı | Para Birimi | Tutar | Hesaplama    |
|----------------|----------|--------|----------------|
| 110110         | Euro      | 250    | 500 USD × %50  |
| 130100         | Euro      | -250   | -500 USD × %50 |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>1 Ekim 2015 ile 30 Kasım 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme
### <a name="balances-in-the-consolidation-company"></a>Konsolidasyon şirketinde bakiyeler

| Genel muhasebe hesabı | Para Birimi | Tutar  | Hesaplama                        |
|----------------|----------|---------|------------------------------------|
| 110110         | Euro      | 333.33  | Orijinal tutar 500 × %66,6667  |
| 130100         | Euro      | -333.33 | Orijinal tutar -500 × %66,6667 |
| 801400         | Euro      | 83.33   | 333.33 – 250                       |
| 801600         | Euro      | -83.33  | -333.33 – (-250)                   |

Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>1 Ekim 2015 ile 31 Aralık 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme
### <a name="balances-in-the-consolidation-company"></a>Konsolidasyon şirketinde bakiyeler

| Genel muhasebe hesabı | Para Birimi | Tutar  | Hesaplama                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | Euro      | 500.00  | Orijinal tutar of 500 × 1                           |
| 130100         | Euro      | -500.00 | Orijinal tutar -500 × 1                          |
| 801400         | Euro      | 250     | 500 – 333.33 = 166.67 166.67 + 83.33 = 250           |
| 801600         | Euro      | -250    | -500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250 |





