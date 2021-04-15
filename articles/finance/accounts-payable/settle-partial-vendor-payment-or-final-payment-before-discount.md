---
title: İskonto tarihinden önce bir kısmi satıcı ödemesini ve nihai ödemeyi tam olarak kapatın
description: Bu makale size, satıcı faturası için kısmi ödemelerin yapıldığı ve nakit iskontosunun alındığı bir senaryo sunar.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89cb38656766b23761665518f9ec39f78349f79b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810330"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>İskonto tarihinden önce bir kısmi satıcı ödemesini ve nihai ödemeyi tam olarak kapatın

[!include [banner](../includes/banner.md)]

Bu makale size, satıcı faturası için kısmi ödemelerin yapıldığı ve nakit iskontosunun alındığı bir senaryo sunar.

Fabrikam 3064 numaralı satıcıdan mal satın alıyor. Satıcı, bir faturanın 14 gün içinde ödenmesi durumunda Fabrikam'a yüzde 1 oranında bir nakit iskontosu veriyor. Faturaların 30 gün içinde ödenmesi gerekir. Satıcı ayrıca Fabrikam'ın kısmi ödemelerde nakit iskontolar alabilmesine izin verir. Kapatma parametreleri **Borç hesapları parametreleri** sayfasındadır. 25 Haziran tarihinde April, satıcı 3064 için 1.000,00 tutarında bir fatura giriyor.

## <a name="vendor-invoice-on-june-25"></a>25 Haziran tarihindeki satıcı faturası
25 Haziran tarihinde April 3064 numaralı satıcı için 1.000,00 tutarında bir fatura giriyor ve deftere naklediyor. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir.

| Fiş   | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan   | Para Birimi |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10010 | 25/6/2015 | 10010   |                                      | 1.000,00                              | -1.000,00 | ABD Doları      |

April, **Satıcılar** sayfasından **İşlemleri düzelt** sayfasını açar. April, nakit indirim tarihleri ve tutarlarını görmek için **Kapatma hareketleri** sayfasını kullanabilir. Vade tarihi, 25 Temmuzdur ve faturanın 9 Temmuz tarihinde tam olarak ödenmesi durumunda -10,00 tutarında bir iskonto indirimi uygulanacaktır.

| İşaret | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Inv-10010 | 3064    | 25/6/2015 | 25/7/2015 | 10010   | 1.000,00                       | ABD Doları      | 990,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|       &nbsp;                 | &nbsp;    |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | -10,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -10,00    |

April, iskonto tutarını görmek için **Nakit iskontosu** sekmesini tıklıyor.

| Nakit iskontosu tarihi | Nakit iskontosu tutarı | Hareket para birimi cinsinden tutar |
|--------------------|----------------------|--------------------------------|
| 9/7/2015           | 10,00                | 990,00                         |
| 25/7/2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Kapatma hareketleri sayfası kullanılarak 1 Temmuz tarihli kısmi ödeme
April, Borç hesapları altındaki **Ödeme günlüğü** sayfasını açarak bu ödeme için bir ödeme günlüğü oluşturabilir. Yeni bir günlük oluşturuyor ve 3064 numaralı satıcı için bir satır giriyor. Ardından, kapatılacak faturayı işaretleyebilmek için **Hareketleri kapat** sayfasını açıyor. April, faturayı işaretliyor ve **Kapatılacak tutar** alanındaki değeri **-500,00** olarak değiştiriyor. **Nakit iskonto tutarı** alanındaki değerin tam fatura için **-10,00** olduğunu ve **Alınacak nakit iskonto tutarı** alanındaki değerin **-5,05** olduğunu görüyor. Bu nedenle, April bu fatura için-505,05 tutarını kapatıyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1.000,00                       | ABD Doları      | -500,00          |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | -10,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -5,05     |

April faturanın tam olarak yarısını kapatmak istiyor. Bu nedenle, **Kapatılacak tutar** alanındaki değeri **-495,00** olarak değiştiriyor. Toplam tutar şimdi 500,00 olarak kapatılıyor. Bu tutar -5.00 nakit iskontosunu içermektedir.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1.000,00                       | ABD Doları      | -495,00          |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | -10,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -5,00     |

April, **Kapatma hareketleri** sayfasını kapatıyor. Günlükte 495,00 tutarı için bir ödeme satırı oluşturuluyor ve April daha sonra günlüğü naklediyor. April satıcı hareketlerini **Satıcı hareketleri** sayfasında görüntüleyebiliyor. Faturanın -500.00 bakiyede olduğunu görüyor. Ayrıca, 495.00 tutarında bir ödeme ve 5,00 tutarında bir nakit iskontosu görüyor.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Fatura          | 25/6/2015 | 10010   |                                      | 1.000,00                              | -500,00 | ABD Doları      |
| APP-10010  | Ödeme          | 1/7/2015  |         | 495,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10010 | Nakit iskontosu    | 1/7/2015  |         | 5,00                                 |                                       | 0,00    | ABD Doları      |

## <a name="remaining-amount-paid-on-july-8"></a>Kalan tutar 8 Temmuz tarihinde ödeniyor
April, satıcı 3064 için faturanın geri kalanını nakit iskontosu vadesi olan 8 Temmuz tarihinde ödüyor. April, 8 Temmuz tarihinde ödeme günlüğü oluşturuyor ve hareketi kapatmak üzere işaretliyor. Mutlaka kapatılması gereken tutarın 495.00 olduğunu görüyor. **Tahmini nakit iskontosu** alanındaki değer **-5.00**'dir, çünkü daha önce alınan iskonto 5.00'dır.

|  &nbsp;                 |  &nbsp; |
|-------------------------|--------|
| İşaretli toplam            | 495,00 |
| Tahmini nakit iskontosu | -5,00  |

İşaretlenen hareket hakkında bilgiler **Açık hareketleri kapatma** sayfasındaki ızgarada görüntüleniyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25/6/2015 | 25/7/2015 | 10010   | 1.000,00                       | ABD Doları      | 495,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|  &nbsp;                      | &nbsp;    |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 10,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 5,00      |
| Alınacak nakit iskontosu tutarı | 5,00      |

April, ödeme günlüğünü naklediyor ve **Satıcı hareketleri** sayfasından satıcı hareketlerini gözden geçiriyor. Fatura için bakiye şimdi 0,00 ve April iki ödeme ve iki nakit iskontosu görüyor.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10010  | Fatura          | 25/6/2015 | 10010   |                                      | 1.000,00                              | 0,00    | ABD Doları      |
| APP-10010  |  Ödeme         | 1/7/2015  |         | 495,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10010 | Nakit iskontosu    | 1/7/2015  |         | 5,00                                 |                                       | 0,00    | ABD Doları      |
| APP-10011  | Ödeme          | 8/7/2015  |         | 495,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10011 | Nakit iskontosu    | 8/7/2015  |         | 5,00                                 |                                       | 0,00    | ABD Doları      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]