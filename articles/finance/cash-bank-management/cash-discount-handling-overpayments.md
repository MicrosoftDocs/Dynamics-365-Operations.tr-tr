---
title: Fazla ödemeler için nakit iskontoları
description: Bu makale, bir müşteri nakit iskontosu alıp aynı zamanda fazla ödeme yaparsa, bunun nasıl işlendiğini gösteren senaryoyu sağlar.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1afc8aec18c61b1ce488472adf540e47540eaa17
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715537"
---
# <a name="cash-discounts-for-overpayments"></a>Fazla ödemeler için nakit iskontoları

[!include [banner](../includes/banner.md)]

Bu makale, bir müşteri nakit iskontosu alıp aynı zamanda fazla ödeme yaparsa, bunun nasıl işlendiğini gösteren senaryoyu sağlar. 

Ödeme tutarı, fatura tutarından nakit iskontosunun çıkarılmasıyla elde edilen tutardan yüksekse bir fatura fazla ödenmiş olarak kabul edilir. Bir fatura fazla ödendiyse elde edilebilir bir nakit iskontosu farkının nasıl işleneceğini belirtmek için **Alacak hesapları parametreleri** sayfasındaki **Nakit iskontoları yönetimi** ve **Maksimum fazla ödeme veya eksik ödeme** alanlarını kullanın. Aşağıdaki örnekte müşteri, faturasını 0.50 fazla ödemiştir.

| Fatura toplamı | Mevcut nakit iskontosu | Nakit iskontosunu içeren, ödenecek tutar | Müşterinin gerçekte ödediği tutar |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Nakit iskontosu yönetimi = Özel
**Otomatik hareketler için hesaplar** sayfasındaki **Nakit iskontosu yönetimi** alanından **Özel** seçimi yapılırsa tüm nakit iskontosu alınır. Fazla ödeme tutarı bir nakit iskontosu farkı defter hesabına nakledilir veya müşteri hesabında bir bakiye olarak kalır. Bu davranış, fazla ödeme tutarının 0,00 ile **Maksimum fazla ödeme veya eksik ödeme** alanında belirlenen tutar arasında olup olmadığına veya fazla ödeme tutarının **Maksimum fazla ödeme veya eksik ödeme** tutarından yüksek olup olmadığına göre değişir.

### <a name="scenario-1"></a>Senaryo 1

Bu senaryodaki fazla ödeme tutarı, 0,00 ile maksimum fazla ödeme veya eksik ödeme tutarı arasındadır. 105,00 tutarında bir fatura girilir ve fatura yedi gün içinde ödenirse bir nakit iskontosu uygulanabilir.

| Fatura toplamı | Mevcut nakit iskontosu | Nakit iskontosunu içeren, ödenecek tutar |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Müşteri, nakit iskontosu dönemi içinde 95,00 tutarında bir ödeme gönderir. Ödeme, 105,00 tutarındaki fatura için kapatılır. Fatura ve ödeme kapatıldıktan sonra Alacak hesapları altında müşteri için aşağıdaki hareketler oluşturulur.

| İşlem   | Tutar | Kalan |
|---------------|--------|---------|
| Fatura       | 105,00 | 0,00    |
| Ödeme       | -95,00 | 0,00    |
| Nakit iskontosu | -10,50 | 0,00    |

Ödeme ve kapatma için aşağıdaki hesap girdileri oluşturulur. **Ödeme**

| Hesap             | Borç tutarı | Alacak tutarı |
|---------------------|--------------|---------------|
| Nakit                | 95,00        |               |
| Alacak hesapları |              | 95,00         |

**Kapatma**

| Hesap                                                                                                          | Borç tutarı | Alacak tutarı |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Nakit iskontosu (**Nakit iskontoları** sayfasındaki **Müşteri iskontoları için ana hesap** alanı)                 | 10,50        |               |
| Alacak hesapları                                                                                              |              | 10,50         |
| Müşteri nakit iskontosu (**Otomatik hareketler için hesap** sayfasındaki **Müşteri nakit iskontosu** sayfası) |              | 0,50          |
| Alacak hesapları                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Senaryo 2

Bu senaryodaki fazla ödeme tutarı, maksimum fazla ödeme veya eksik ödeme tutarını aşıyor. 105,00 tutarında bir fatura girilir ve fatura yedi gün içinde ödenirse bir nakit iskontosu uygulanabilir.

| Fatura toplamı | Mevcut nakit iskontosu | Nakit iskontosunu içeren, ödenecek tutar |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Müşteri, nakit iskontosu dönemi içinde 95,00 tutarında bir ödeme gönderir. Ödeme, 105,00 tutarındaki fatura için kapatılır. Fatura ve ödeme kapatıldıktan sonra Alacak hesapları altında müşteri için aşağıdaki hareketler oluşturulur.

| İşlem   | Tutar | Kalan |
|---------------|--------|---------|
| Fatura       | 105,00 | 0,00    |
| Ödeme       | -95,00 | -0,50   |
| Nakit iskontosu | -10,50 | 0,00    |

0,50 tutarındaki fazla ödeme, ödemede bir açık bakiye olarak kalacak ve başka bir faturayla kapatılacaktır. Ödeme ve kapatma için aşağıdaki hesap girdileri oluşturulur. **Ödeme**

| Hesap             | Borç tutarı | Alacak tutarı |
|---------------------|--------------|---------------|
| Nakit                | 95,00        |               |
| Alacak hesapları |              | 95,00         |

**Kapatma**

| Hesap                                                                                          | Borç tutarı | Alacak tutarı |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Nakit iskontosu (**Nakit iskontoları** sayfasındaki **Müşteri iskontoları için ana hesap** alanı) | 10,50        |               |
| Alacak hesapları                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Nakit iskontosu yönetimi = Özel olmayan
**Otomatik hareketler için hesaplar** sayfasındaki **Nakit iskontosu yönetimi** alanından **Özel olmayan** seçimi yapılırsa nakit iskonto hesabı, fazla ödeme miktarı kadar düşürülür. Bu davranış her zaman, fazla ödeme tutarının **Maksimum fazla ödeme veya eksik ödeme** alanına girilen miktardan fazla veya düşük olup olmamasından bağımsız olarak uygulanır.

### <a name="scenario-3"></a>Senaryo 3

Bu senaryoda 105,00 tutarında bir fatura girilir ve fatura yedi gün içinde ödenirse bir nakit iskontosu uygulanabilir.

| Fatura toplamı | Mevcut nakit iskontosu | Nakit iskontosunu içeren, ödenecek tutar |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Müşteri, nakit iskontosu geçerlilik tarihi dolmadan 95,00 tutarında bir ödeme gönderir. Ödeme, 105,00 tutarındaki fatura için kapatılır. Fatura ve ödeme kapatıldıktan sonra Alacak hesapları altında müşteri için aşağıdaki hareketler oluşturulur.

| İşlem   | Tutar | Kalan |
|---------------|--------|---------|
| Fatura       | 105,00 | 0,00    |
| Ödeme       | -95,00 | -0,00   |
| Nakit iskontosu | -10,00 | 0,00    |

Nakit iskontosu tutarı 10,50'den 10,00'a düşürülür. Ödeme ve faturanın kapatıldığı kabul edilir. **Ödeme**

| Hesap             | Borç tutarı | Alacak tutarı |
|---------------------|--------------|---------------|
| Nakit                | 95,00        |               |
| Alacak hesapları |              | 95,00         |

**Kapatma**

| Hesap                                                                                          | Borç tutarı | Alacak tutarı |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Nakit iskontosu (**Nakit iskontoları** sayfasındaki **Müşteri iskontoları için ana hesap** alanı) | 10,50        |               |
| Alacak hesapları                                                                              |              | 10,50         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
