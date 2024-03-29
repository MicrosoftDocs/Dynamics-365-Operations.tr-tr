---
title: Kısmi ödemeyi iskonto tarihinden önce ve iskonto tarihinden sonraki bir son ödeme ile kapatma
description: Bu makalede, bazısı nakit iskonto dönemi dahilinde, diğerleri nakit iskonto dönemi haricinde olmak üzere birden fazla kısmi ödemenin yapıldığı bir senaryo boyunca size eşlik edilmektedir.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 828c82d88bef1d942af1219505af591d27043fa5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780602"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Kısmi ödemeyi iskonto tarihinden önce ve iskonto tarihinden sonraki bir son ödeme ile kapatma

[!include [banner](../includes/banner.md)]

Bu makalede, bazısı nakit iskonto dönemi dahilinde, diğerleri nakit iskonto dönemi haricinde olmak üzere birden fazla kısmi ödemenin yapıldığı bir senaryo boyunca size eşlik edilmektedir.

Fabrikam 3057 numaralı satıcıdan mal satın alıyor. Fabrikam, fatura 14 gün içinde ödenirse yüzde 1'lik nakit iskontosu alıyor. Faturaların 30 gün içinde ödenmesi gerekir. Satıcı ayrıca Fabrikam'ın kısmi ödemelerde nakit iskontolar alabilmesine izin verir. Kapatma parametreleri **Borç hesapları parametreleri** sayfasındadır.

## <a name="invoice-on-june-25"></a>25 Haziran tarihindeki fatura
25 Haziran tarihinde April 3057 numaralı satıcı için 1.000,00 tutarında bir fatura giriyor ve deftere naklediyor. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir.

| Fiş   | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye   | Para birimi |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Inv-10020 | Fatura          | 25.06.2020 | 10020   |                                      | 1,000.00                              | -1.000,00 | ABD Doları      |

## <a name="partial-payment-on-july-2"></a>2 Temmuz'da kısmi ödeme
2 Temmuz'da, April bu faturanın 300,00'ünü kapatmak istiyor. Fabrikam kısmi ödemelerde indirim kabul ettiği için, bu ödeme bir indirime hak kazanır. Bu nedenle, April 297,00 öder ve 3,00 indirim alır. Bir ödeme günlüğü oluşturuyor ve 3057 numaralı satıcı için bir satır giriyor. Ardından, kapatılacak faturayı işaretleyebilmek için **Hareketleri kapat** sayfasını açıyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | Inv-10020 | 3057    | 25.06.2020 | 25.07.2020 | 10020   | -1.000,00                      | ABD Doları      | -297,00          |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

| Alan                        | Değer     |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | -10,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -3,00     |

April sonra ödemeyi deftere nakleder. Faturanın artık 700,00 miktarında bakiyesi vardır. April bu hareketi **Satıcı hareketleri** sayfasında görüntüleyebilir.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye | Para birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Fatura          | 25.06.2020 | 10020   |                                      | 1,000.00                              | -700,00 | ABD Doları      |
| APP-10020  | Ödeme          | 7/1/2020  |         | 297,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10020 | Nakit iskontosu    | 7/1/2020  |         | 3.00                                 |                                       | 0,00    | ABD Doları      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Kalan ödeme Temmuz 15'te, Nakit indirimi kullanın = Normal
April, faturanın geri kalanını, iskonto döneminden sonra olan, 15 Temmuz'da öder. **Açık hareketleri kapatma** sayfasında, **Tahmini nakit iskontosu** alanında hiçbir indirim tutarı görüntülenmez ve **Nakit iskontosu tutarı** alanında değer **0,00** olur. April kalan 700,00'ü ödediğinde, hiçbir ek iskonto alınmaz.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | Inv-10020 | 3057    | 25.06.2020 | 25.07.2020 | 10020   | -700,00                        | ABD Doları      | -700,00          |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir. April kendisinin zaten 3,00 indirim aldığını görebilir.

| Alan                        | Değer     |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | 0,00      |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | -3,00     |
| Alınacak nakit iskontosu tutarı | 0,00      |

April sonra ödemeyi deftere nakleder. **Satıcı hareketleri** sayfasını açtığında, faturanın bakiyesinin 0,00 olduğunu görür. Ayrı,ca, iki ödeme olduğunu görür. Bir ödeme 297,00 içindir ve 3,00 indirimi vardır, diğer ödeme de 700,00 içindir.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye | Para birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Fatura          | 25.06.2020 | 10020   |                                      | 1,000.00                              | 0,00    | ABD Doları      |
| APP-10020  | Ödeme          | 7/1/2020  |         | 297,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10020 | Nakit iskontosu    | 7/1/2020  |         | 3.00                                 |                                       | 0,00    | ABD Doları      |
| APP-10021  | Ödeme          | 15.07.2020 |         | 700.00                               |                                       | 0,00    | ABD Doları      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Kalan ödeme Temmuz 15'te, Nakit indirimi kullanın = Her zaman
Satıcı, April iskonto tarihinden sonra ödeme yapsa da bir iskonto almasına izin veriyor ve April **Nakit iskontosu kullan** alanındaki değeri değiştirip **Her zaman** yapabiliyor. **Kısmi ödemeler için nakit iskontolarını hesapla** ayarı geçersiz kılınmıştır ve iskonto alınır. Ödeme tutarı 693,00'dür ve kalan 7,00'de indirimdir.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para birimi | Kapatılacak tutar |
|----------|----------|------|------|-----------|-----------|---------|-----------------------|---------------------------------------|----------|------------------|
| Seçildi | Her zaman            | Inv-10020 | 3057    | 25.06.2020 | 25.07.2020 | 10020   | 700.00                   |                   | ABD Doları      | -693,00          |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.

| Alan                        | Değer     |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | 7.00      |
| Nakit iskontosu kullan            | Her zaman    |
| Alınan nakit iskontosu          | -3,00     |
| Alınacak nakit iskontosu tutarı | -7,00     |

April sonra ödemeyi deftere nakleder. **Satıcı hareketleri** sayfasını açtığında, faturanın bakiyesinin 0,00 olduğunu görür. Ayrı,ca, iki ödeme olduğunu görür. Bir ödeme 297,00 içindir ve 3,00 indirimi vardır, diğer ödeme de 693,00 içindir ve 7,00 indirimi vardır.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye | Para birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10020  | Fatura          | 25.06.2020 | 10020   |                                      | 1,000.00                              | 0,00    | ABD Doları      |
| APP-10020  | Ödeme          | 7/1/2020  |         | 297,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10020 | Nakit iskontosu    | 7/1/2020  |         | 3.00                                 |                                       | 0,00    | ABD Doları      |
| APP-10021  | Ödeme          | 15.07.2020 |         | 693,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10021 | Nakit iskontosu    | 15.07.2020 |         | 7.00                                 |                                       | 0,00    | ABD Doları      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
