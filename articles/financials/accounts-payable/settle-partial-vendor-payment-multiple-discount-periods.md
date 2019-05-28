---
title: Birden fazla iskonto dönemi olan bir kısmi satıcı ödemesini kapatma
description: Bu makalede, birden fazla nakit indirimi öneren bir satıcıya birden fazla kısmi ödemenin yapıldığı bir senaryo açıklanmaktadır.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84f8721c3bea232b7930e174eaf43ad550dd8ab6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512257"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Birden fazla iskonto dönemi olan bir kısmi satıcı ödemesini kapatma

[!include [banner](../includes/banner.md)]

Bu makalede, birden fazla nakit indirimi öneren bir satıcıya birden fazla kısmi ödemenin yapıldığı bir senaryo açıklanmaktadır. 

Satıcı 3054, Fabrikam'a ilk beş gün içinde ödenen fatura için yüzde 2 nakit iskontosu ve faturanın 14 gün içinde ödenmesi durumunda %1 nakit iskontosu yapmaktadır.

## <a name="invoice"></a>Fatura
28 Haziran tarihinde April 3054 numaralı satıcı için 1.000,00 tutarında bir fatura oluşturuyor. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir.

| Fiş   | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan   | Para Birimi |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10060 | 28/6/2015 | 10060   |                                      | 1.000,00                              | -1.000,00 | ABD Doları      |

Aşağıdaki nakit iskontosu tarihleri ve tutarları bu fatura için kullanılabilir.

| Nakit iskontosu tarihi | Nakit iskontosu tutarı | Hareket para birimi cinsinden tutar |
|--------------------|----------------------|--------------------------------|
| 3/7/2015           | 20,00                | 980,00                         |
| 12/7/2015          | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1.000,00                       |

## <a name="payment-on-july-2"></a>2 Temmuz'da ödeme
2 Temmuz'da, April bu faturanın 300,00'ünü ödemek istiyor. Borç hesapları'nda **Ödeme günlüğü** sayfasını kullanarak tek seferlik bir ödeme oluşturuyor. Satıcı 3054 için bir satır ekler ve **300,00** değerinde ödeme tutarı girer. Ardından April, kapatılacak faturayı işaretleyeceği **Kapatma hareketleri** sayfasını açar. **Kapatılacak tutar** alanındaki değeri **300,00** olarak günceller ve **Alınacak nakit iskontosu tutarı** alanındaki değerin **6.12** olarak değiştiğini görür. Bu ödeme ilk indirim döneminde yapıldığından, yüzde 2 oranında iskonto alınır.

| İşaret | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 28/6/2015 | 28/7/2015 | 10060   | 1.000,00                       | ABD Doları      | 300,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 02/7/2015 |
| Nakit iskontosu tutarı         | -20,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -6,12     |

Nakit iskontosu bulunduğundan, April ödeme tutarını, hem ödeme hem de nakit iskontosu için toplam kapatılan tutar 300,00 olacak şekilde değiştirmek ister. **Kapatılacak tutar** alanındaki değeri **294,00** olarak değiştirir ve **Alınacak nakit iskontosu tutarı** alanındaki değerin **6.00** olarak değiştiğini görür.

| İşaret | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 28/6/2015 | 28/7/2015 | 10060   | 1.000,00                       | ABD Doları      | 294,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 02/7/2015 |
| Nakit iskontosu tutarı         | -20,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -6,00     |

April ödemeyi deftere nakleder. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir. Faturaya 300,00 değerinde bir tutar uygulandığını görür. Bu tutar 6,00 tutarındaki nakit iskontosunu içermektedir. Bu nedenle, kalan bakiye 700,00 olur.

| Fiş    | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28/6/2015 | 10060   |                                      | 1.000,00                              | -700,00 | ABD Doları      |
| APP-10060  | 2/7/2015  |         | 294,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10060 | 2/7/2015  |         | 6,00                                 |                                       | 0,00    | ABD Doları      |

## <a name="payment-on-july-8"></a>8 Temmuz'da ödeme
8 Temmuz'da April fatura için ek bir ödeme yapar. Tutarı girmek için **Hareketleri kapat** sayfasını açar ve **Nakit iskontosu** sekmesine tıklar. Kullanılabilir olan iki nakit indirimin tarihlerini ve tutarlarını görüntüler. Bu ödeme ikinci indirim döneminde yapıldığından, yüzde 1 oranında veya 5,00 değerinde iskonto alınır. Bu tutar, 1.000,00 tutarı için yüzde 1'in yarısı veya 10,00 değerinin yarısı olarak hesaplanır.

| Nakit iskontosu tarihi | Nakit iskontosu tutarı | Hareket para birimi cinsinden tutar |
|--------------------|----------------------|--------------------------------|
| 3/7/2015           | 20,00                | 680,00                         |
| 12/7/2015          | 10,00                | 690,00                         |
| 25/7/2015          | 0,00                 | 700,00                         |

April, 495,00 tutarında ödeme yapmaya karar verir ve 5,00 tutarında nakit iskontosu alır. Bu nedenle toplam tutar 500,00 olarak kapatılır.

| İşaret | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10060 | 3054    | 28/6/2015 | 28/7/2015 | 10060   | 1.000,00                       | ABD Doları      | 495,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 12/7/2015 |
| Nakit iskontosu tutarı         | -10,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | -6,00     |
| Alınacak nakit iskontosu tutarı | -5,00     |

**Satıcı hareketleri** sayfasında, April yeni bakiyenin 200,00 olduğunu görür.

| Fiş    | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28/6/2015 | 10060   |                                      | 1.000,00                              | -200,00 | ABD Doları      |
| APP-10060  | 2/7/2015  |         | 294,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10060 | 2/7/2015  |         | 6,00                                 |                                       | 0,00    | ABD Doları      |
| APP-10061  | 12/7/2015 |         | 495,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10061 | 12/7/2015 |         | 5,00                                 |                                       | 0,00    | ABD Doları      |

## <a name="payment-on-july-20"></a>20 Temmuz'da ödeme
20 Temmuz'da April 200,00 tutarında son bir ödeme yapar. Ödeme her iki iskonto döneminden sonra yapıldığı için herhangi bir iskonto alınmaz. Fatura bakiyesi 0,00 olur.

| Fiş    | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10060  | 28/6/2015 | 10060   |                                      | 1.000,00                              | -200,00 | ABD Doları      |
| APP-10060  | 2/7/2015  |         | 294,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10060 | 2/7/2015  |         | 6,00                                 |                                       | 0,00    | ABD Doları      |
| APP-10061  | 12/7/2015 |         | 495,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10061 | 12/7/2015 |         | 5,00                                 |                                       | 0,00    | ABD Doları      |
| APP-10062  | 20/7/2015 |         | 200,00                               |                                       | 0,00    | ABD Doları      |





