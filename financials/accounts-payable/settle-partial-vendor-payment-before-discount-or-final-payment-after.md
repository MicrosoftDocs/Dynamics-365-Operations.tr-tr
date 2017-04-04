---
title: "Kısmi Satıcı ödeme iskontosu tarihinden önce son bir ödeme iskontosu tarihinden sonra olan tasfiye et"
description: "Bu makalede, bazısı nakit iskonto dönemi dahilinde, diğerleri nakit iskonto dönemi haricinde olmak üzere birden fazla kısmi ödemenin yapıldığı bir senaryo boyunca size eşlik edilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 33851ff7c9ee2c50544589ade0191798a13706e7
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Kısmi Satıcı ödeme iskontosu tarihinden önce son bir ödeme iskontosu tarihinden sonra olan tasfiye et

Bu makalede, bazısı nakit iskonto dönemi dahilinde, diğerleri nakit iskonto dönemi haricinde olmak üzere birden fazla kısmi ödemenin yapıldığı bir senaryo boyunca size eşlik edilmektedir.

Fabrikam mal 3057 satıcıdan yapılan satınalmalar. 14 gün içinde faturası ödeniyorsa Fabrikam yüzde 1'lik bir nakit iskontosu alır. Faturaların 30 gün içinde ödenmesi gerekir. Satıcı ayrıca Fabrikam'ın kısmi ödemelerde nakit iskontolar alabilmesine izin verir. Kapatma parametreleri üzerinde bulunan **hesaplarına borç parametreleri** sayfa.

## <a name="invoice-on-june-25"></a>25 Haziran tarihindeki fatura
Haziran 25 Nisan girer ve satıcı 3057 için 1.000,00 ait faturayı deftere nakleder. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir.

| Fiş   | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan   | Para Birimi |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Fatura          | 25/6/2015 | 10020   |                                      | 1.000,00                              | -1.000,00 | ABD Doları      |

## <a name="partial-payment-on-july-2"></a>2 Temmuz'da kısmi ödeme
2 Temmuz'da, April bu faturanın 300,00'ünü kapatmak istiyor. Fabrikam kısmi ödemelerde indirim kabul ettiği için, bu ödeme bir indirime hak kazanır. Bu nedenle, April 297,00 öder ve 3,00 indirim alır. Ödeme günlüğü oluşturur ve 3057 satıcı için bir satır girer. Daha sonra açılır **kapatma hareketleri** sayfa, böylece o fatura kapatması için işaretleyebilirsiniz.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | Inv-10020 | 3057    | 25/6/2015 | 25/7/2015 | 10020   | -1.000,00                      | ABD Doları      | -297,00          |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | -10,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -3,00     |

April sonra ödemeyi deftere nakleder. Faturanın artık 700,00 miktarında bakiyesi vardır. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Fatura          | 25/6/2015 | 10020   |                                      | 1.000,00                              | -700,00 | ABD Doları      |
| APP-10020  | Ödeme          | 1/7/2015  |         | 297,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10020 | Nakit iskontosu    | 1/7/2015  |         | 3,00                                 |                                       | 0,00    | ABD Doları      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Kalan ödeme Temmuz 15'te, Nakit indirimi kullanın = Normal
April, faturanın geri kalanını, iskonto döneminden sonra olan, 15 Temmuz'da öder. **Açık hareketleri kapatma** sayfasında, **Tahmini nakit iskontosu **alanında hiçbir indirim tutarı görüntülenmez ve **Nakit iskontosu tutarı** alanında değer **0,00** olur. April kalan 700,00'ü ödediğinde, hiçbir ek iskonto alınmaz.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | Inv-10020 | 3057    | 25/6/2015 | 25/7/2015 | 10020   | -700,00                        | ABD Doları      | -700,00          |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir. April kendisinin zaten 3,00 indirim aldığını görebilir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 0,00      |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | -3,00     |
| Alınacak nakit iskontosu tutarı | 0,00      |

April sonra ödemeyi deftere nakleder. **Satıcı hareketleri** sayfasını açtığında, faturanın bakiyesinin 0,00 olduğunu görür. Ayrı,ca, iki ödeme olduğunu görür. Bir ödeme 297,00 içindir ve 3,00 indirimi vardır, diğer ödeme de 700,00 içindir.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Fatura          | 25/6/2015 | 10020   |                                      | 1.000,00                              | 0,00    | ABD Doları      |
| APP-10020  | Ödeme          | 1/7/2015  |         | 297,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10020 | Nakit iskontosu    | 1/7/2015  |         | 3,00                                 |                                       | 0,00    | ABD Doları      |
| APP-10021  | Ödeme          | 15/7/2015 |         | 700,00                               |                                       | 0,00    | ABD Doları      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Kalan ödeme Temmuz 15'te, Nakit indirimi kullanın = Her zaman
Satıcı Nisan Filiz iskonto tarihinden sonra ödeme olsa da bir indirim almak sağlar, Filiz değeri değiştirebilirsiniz **nakit iskontosu kullan** alanı **her zaman**. **Kısmi ödemeler için nakit iskontolarını hesaplamak** ayarını geçersiz kılınmıştır ve iskonto alınır. Ödeme tutarı 693,00'dür ve kalan 7,00'de indirimdir.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Seçildi | Her zaman            | Inv-10020 | 3057    | 25/6/2015 | 25/7/2015 | 10020   | 700,00                               |                                       | ABD Doları      | -693,00          |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 09/7/2015 |
| Nakit iskontosu tutarı         | 7,00      |
| Nakit iskontosu kullan            | Her zaman    |
| Alınan nakit iskontosu          | -3,00     |
| Alınacak nakit iskontosu tutarı | -7,00     |

April sonra ödemeyi deftere nakleder. **Satıcı hareketleri** sayfasını açtığında, faturanın bakiyesinin 0,00 olduğunu görür. Ayrı,ca, iki ödeme olduğunu görür. Bir ödeme 297,00 içindir ve 3,00 indirimi vardır, diğer ödeme de 693,00 içindir ve 7,00 indirimi vardır.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Fatura          | 25/6/2015 | 10020   |                                      | 1.000,00                              | 0,00    | ABD Doları      |
| APP-10020  | Ödeme          | 1/7/2015  |         | 297,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10020 | Nakit iskontosu    | 1/7/2015  |         | 3,00                                 |                                       | 0,00    | ABD Doları      |
| APP-10021  | Ödeme          | 15/7/2015 |         | 693,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10021 | Nakit iskontosu    | 15/7/2015 |         | 7,00                                 |                                       | 0,00    | ABD Doları      |




