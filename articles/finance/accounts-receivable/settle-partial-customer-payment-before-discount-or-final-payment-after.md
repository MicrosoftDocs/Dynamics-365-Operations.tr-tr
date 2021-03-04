---
title: Kısmi müşteri ödemesini iskonto tarihinden önce, iskonto tarihinden sonraki son bir ödeme ile tasfiye et
description: Bu makalede müşteriler için ödemelerin kapatılmasının faturalar üzerindeki etkisi tartışılmıştır. Senaryo, Genel muhasebeye değil, yardımcı deftere etkileri üzerinde durmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a71d0931445f3501f1b74f26c5eef583ab598b3c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448711"
---
# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Kısmi müşteri ödemesini iskonto tarihinden önce, iskonto tarihinden sonraki son bir ödeme ile tasfiye et

[!include [banner](../includes/banner.md)]

Bu makalede müşteriler için ödemelerin kapatılmasının faturalar üzerindeki etkisi tartışılmıştır. Senaryo, Genel muhasebeye değil, yardımcı deftere etkileri üzerinde durmaktadır.

Fabrikam 4027 müşteriye mal satmaktadır. Fabrikam, fatura 14 gün içerisinde ödenirse yüzde 1'lik nakit iskontosu sunar. Faturaların 30 gün içinde ödenmesi gerekir. Fabrikam, kısmi ödemeler için de nakit iskontoları sunmaktadır. Kapatma parametreleri, **Alacak hesapları parametreleri** sayfasında bulunur.

## <a name="invoice"></a>Fatura
25 Haziran Tamer 4027 müşteri için 1.000,00 değerinde bir faturayı girip deftere nakleder. Tamer, bu faturayı **Müşteriler** sayfasındaki **Hareketler** düğmesini kullanarak görüntüleyebilir.

| Fiş   | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan  | Para Birimi |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10020 | Fatura          | 25/6/2015 | 10020   | 1.000,00                             |                                       | 1.000,00 | ABD Doları      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Nakit iskonto tarihinden önce kısmi ödeme
2 Temmuz, müşteri 4027 fatura için 297,00 kısmi ödeme yapar. Fabrikam kısmi ödemelerde nakit iskontosu sunduğundan ve kısmi ödeme nakit iskontosu tarihinden önce yapıldığından ödeme bir nakit iskontosu için uygundur. Bu nedenle, müşteri 4027 3,00 nakit iskontosu alır. Tamer, müşteri 4027 için Ödeme günlüğünü kullanarak ödemeyi kaydeder. Ardından, kapatmanın faturasını işaretleyebilmek için **Hareketleri kapat** sayfasını açar.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10020 | 4027    | 25/6/2015 | 25/7/2015 | 10020   | 1.000,00                             | ABD Doları      | 297,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir. **Kapatılacak tutar** değerini 297,00 olarak değiştirmezseniz, görünen **Nakit iskontosu tutarı** değerleri farklı olur. Ancak, kapatma işlemi, **Kapatılacak tutar** değerini sizin için otomatik olarak düzenleyeceğinden ödeme nakledildiğinde nakit iskontosu olarak 3,00 alınacaktır.

|                              |           |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 10,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 3,00      |

Tamer, bu ödemeyi deftere nakleder. Faturanın artık 700,00 miktarında bakiyesi vardır. Müşterinin aşağıdaki hareketleri görülebilir.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Fatura          | 25/6/2015 | 10020   | 1.000,00                             |                                       | 700,00  | ABD Doları      |
| ARP-10020  |  Ödeme         | 1/7/2015  |         |                                      | 297,00                                | 0,00    | ABD Doları      |
| DISC-10020 |  Nakit iskontosu   | 1/7/2015  |         |                                      | 3,00                                  | 0,00    | ABD Doları      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Nakit iskonto tarihinden sonra kalan ödeme
Müşteri 4027 faturanın geri iskonto dönemindan sonra, 11 Temmuz tarihinde faturanın kalanını öder. **Hareketleri kapat** sayfasında, **Tahmini nakit iskontosu** alanında bir iskonto tutarı görünmez ve **Nakit iskontosu tutarı** alanında **0,00** değeri görünür. Müşteri 4027 kalan 700,00'lük tutarı ödediğinde, hiçbir ek iskonto alınmaz.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10020 | 4027    | 25/6/2015 | 25/7/2015 | 10020   | 700,00                               | ABD Doları      | 700,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 0,00      |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 3,00      |
| Alınacak nakit iskontosu tutarı | 0,00      |

Tamer **Nakit iskontosu kullan** alanındaki değeri **Her zaman** olarak değiştirirse, **Kısmi ödemeler için nakit iskontolarını hesapla** ayarı geçersiz kılınır ve nakit iskontosu alınır. Ödeme tutarı 693,00 olarak değişir ve kalan 7,00'lik tutar nakit iskontosudur.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Seçildi | Her zaman            | FTI-10020 | 4027    | 25/6/2015 | 25/7/2015 | 10020   | 700,00                               |                                       | ABD Doları      | 693,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 7,00      |
| Nakit iskontosu kullan            | Her zaman    |
| Alınan nakit iskontosu          | 3,00      |
| Alınacak nakit iskontosu tutarı | 7,00      |

Tamer, bu müşterinin 7.00'lik kalan nakit iskontosunu almasına izin vermediğinden **Nakit iskontosu kullan** alanındaki değeri tekrar **Normal** olarak değiştirir. Sonra ödemeyi deftere nakleder. Tamer **Müşteri hareketleri** sayfasını açtığında, faturanın bakiyesinin 0,00 olduğunu görür. Ayrıca, iki ödeme olduğunu da görür. Ödemelerden biri 297,00 içindir ve 3,00 tutarında nakit iskontosu vardır; diğer ödeme ise 700,00 içindir.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10020  | Fatura          | 25/6/2015 | 10020   | 1.000,00                             |                                       | 0,00    | ABD Doları      |
| ARP-10020  |                  | 1/7/2015  |         |                                      | 297,00                                | 0,00    | ABD Doları      |
| DISC-10020 |                  | 1/7/2015  |         |                                      | 3,00                                  | 0,00    | ABD Doları      |
| ARP-10021  |                  | 11/7/2015 |         |                                      | 700,00                                | 0,00    | ABD Doları      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]