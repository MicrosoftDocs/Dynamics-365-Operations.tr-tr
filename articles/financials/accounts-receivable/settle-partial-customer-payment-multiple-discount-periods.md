---
title: "Birden fazla iskonto dönemi olan bir kısmi müşteri ödemesini kapatma"
description: "Bu makale, birden fazla iskonto dönemi olduğunda kısmi müşteri ödemelerinin nasıl kapatıldığını gösterir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 048a4ca44d457849e2f632da1686dfbeb81dd61b
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Birden fazla iskonto dönemi olan bir kısmi müşteri ödemesini kapatma

[!include[banner](../includes/banner.md)]


Bu makale, birden fazla iskonto dönemi olduğunda kısmi müşteri ödemelerinin nasıl kapatıldığını gösterir.

Fabrikam, müşteri 4031'e iki nakit iskonto dönemi sunuyor. Müşteri, faturayı beş gün içinde öderse yüzde 2'lik bir nakit iskontosu ve 14 gün içinde öderse yüzde 1'lik bir nakit iskontosu alır. Fabrikam, kısmi ödemeler için de nakit iskontoları sunmaktadır. Kapatma parametreleri, **Alacak hesapları parametreleri** sayfasında bulunur.

## <a name="invoice"></a>Fatura
25 Haziran Tamer 4031 müşteri için 1.000,00 değerinde bir faturayı girip deftere naklediyor. Bu fatura için nakit iskontoları inceleyen Tamer, fatura 30 Haziran'a kadar ödendiği zaman 4031 numaralı müşterinin 20,00 iskonto alacağını görür. Fatura 9 Temmuz'a kadar ödenirse, müşteri 10,00 iskonto alır.

| Nakit iskontosu tarihi | Nakit iskontosu tutarı | Hareket para birimi cinsinden tutar |
|--------------------|----------------------|--------------------------------|
| 30/6/2015          | 20,00                | 980,00                         |
| 9/7/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1.000,00                       |

Arnie bu hareketi **Müşteri hareketleri** sayfasında görüntüleyebilir.

| Fiş   | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan  | Para Birimi |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10030 | Fatura          | 25/6/2015 | 10030   | 1.000,00                             |                                       | 1.000,00 | ABD Doları      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Nakit iskonto tarihinden önce kısmi ödeme
28 Haziran tarihinde müşteri 4031, 294.00 tutarında bir kısmi ödeme yapıyor. 28 Haziran ilk nakit iskontosu süresi içinde olduğundan, müşteri 6.00 tutarında bir iskonto alıyor. **Kapatma hareketleri** sayfasında, **Nakit iskonto tutarı** değeri, 20.00 ve **Alınacak nakit iskonto tutarı** değeri, 6.00'dır.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10030 | 4031    | 25/6/2015 | 25/7/2015 | 10030   | 1.000,00                       | ABD Doları      | 294,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir. **Kapatılacak tutar** değerini **294,00** olarak değiştirmezseniz görüntülenen **Nakit iskonto tutarı** değerleri değişecektir. Ancak, kapatma işlemi, **Kapatılacak tutar** değerini sizin için otomatik olarak düzenleyeceğinden ödeme nakledildiğinde nakit iskontosu olarak 6,00 alınacaktır.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 30/6/2015 |
| Nakit iskontosu tutarı         | 20,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 6,00      |

Arnie, ödemeyi naklettikten sonra fatura bakiyesi 700,00 olur.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>İkinci nakit iskontosu tarihinden önce kısmi ödeme
8 Temmuz tarihinde müşteri fatura tutarının geri kalanını ödüyor. Ödeme ikinci nakit iskontosu dönemi içinde yapıldığından 7,00 tutarında bir iskonto (yüzde 1) alınır.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10030 | 4031    | 25/6/2015 | 25/7/2015 | 10030   | 700,00                               |                                       | ABD Doları      | 693,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 30,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 6,00      |
| Alınacak nakit iskontosu tutarı | 7,00      |

Fatura bakiyesi şimdi 0,00 olur. Arnie, bilgileri **Müşteri hareketleri** sayfasında görür.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10030  | Fatura          | 25/6/2015 | 10030   | 1.000,00                             |                                       | 0,00    | ABD Doları      |
| ARP-10030  |  Ödeme         | 28/6/2015 |         |                                      | 294,00                                | 0,00    | ABD Doları      |
| DISC-10030 |  Nakit iskontosu   | 28/6/2015 |         |                                      | 6,00                                  | 0,00    | ABD Doları      |
| ARP-10031  |  Ödeme         | 8/7/2015  |         |                                      | 693,00                                | 0,00    | ABD Doları      |
| DISC-1031  |  Nakit iskontosu   | 8/7/2015  |         |                                      | 7,00                                  | 0,00    | ABD Doları      |






