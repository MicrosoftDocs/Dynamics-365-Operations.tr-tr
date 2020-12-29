---
title: Birden fazla iskonto dönemine yayılan birden fazla faturayı kapatmak için bir müşteri ödemesi kullanma
description: Bu konuda, her bir fatura nakit indirimine uygunsa birden fazla faturanın nasıl ödeneceği gösterilmektedir. Bu makaledeki senaryolar, alınan nakit iskontolarının ödemenin ne zaman yapıldığına bağlı olarak nasıl değiştiğini açıklamaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ae0bdc8245db1391103ca0f214fb3120f93f5b
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2020
ms.locfileid: "4449038"
---
# <a name="use-a-customer-payment-to-settle-multiple-invoices-that-span-multiple-discount-periods"></a>Birden fazla iskonto dönemine yayılan birden fazla faturayı kapatmak için bir müşteri ödemesi kullanma

[!include [banner](../includes/banner.md)]

Bu konuda, her bir fatura nakit indirimine uygunsa birden fazla faturanın nasıl ödeneceği gösterilmektedir. Bu makaledeki senaryolar, alınan nakit iskontolarının ödemenin ne zaman yapıldığına bağlı olarak nasıl değiştiğini açıklamaktadır.

Fabrikam, 4032 müşteriye mal satmaktadır. Fabrikam, fatura 14 gün içerisinde ödenirse yüzde 1'lik nakit iskontosu sunar. Fabrikam, kısmi ödemeler için de nakit iskontoları sunmaktadır. Kapatma parametreleri, **Alacak hesapları parametreleri** sayfasında bulunur.

## <a name="invoices"></a>Faturalar
Müşteri 4032'nin toplam tutarı 3.000,00 olan üç faturası vardır:

-   1.000,00 için fatura FTI-10040, 15 Mayıs'ta girildi. Bu fatura 14 gün içerisinde ödenirse, yüzde 1'lik nakit iskontosuna uygundur.
-   1.000,00 için fatura FTI-10041, 25 Haziran'da girildi. Bu fatura 14 gün içerisinde ödenirse, yüzde 1'lik nakit iskontosuna uygundur.
-   1.000,00 için fatura FTI-10042, 25 Haziran'da girildi. Bu fatura, beş gün içerisinde ödenirse yüzde 2'lik nakit iskontosuna hak kazanır ve 14 gün içerisinde ödenirse yüzde 1'lik nakit iskontosuna hak kazanır.

## <a name="settle-all-invoices-on-june-29"></a>Tüm faturaları 29 Haziran'da kapatma
Arnie, bu faturaların tamamını 29 Haziran'da kapatmak üzere bir ödeme günlüğü oluşturursa, ödeme tutarı 2.970,00 olur. Tüm iskonto tutarları toplamı 30,00'dur. Arnie müşteri 4032 için bir ödeme oluşturur ve **Kapatma hareketleri** sayfasını açar. **Kapatma hareketleri** sayfasında, Arnie üç fatura satırını da kapatmak üzere işaretler:

-   Fatura FTI 10040 için ödeme 1.000,00'dir. Nakit iskontosu yapılmaz.
-   Fatura FTI-10041 için ödeme 990,00'dır. Yüzde 1 veya 10,00 tutarında nakit iskontosu alınır.
-   Fatura FTI-10042 için ödeme 980,00'dir. Yüzde 2 veya 20,00 tutarında nakit iskontosu alınır.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Seçildi                 | Normal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1.000,00                             |                                       | ABD Doları      | 1.000,00         |
| Seçildi                 | Normal            | FTI-10041 | 4032    | 25/6/2015 | 25/7/2015 | 10041   | 1.000,00                             |                                       | ABD Doları      | 990,00           |
| Seçildi ve vurgulandı | Normal            | FTI-10042 | 4032    | 25/6/2015 | 25/7/2015 | 10042   | 1.000,00                             |                                       | ABD Doları      | 980,00           |

Ödeme deftere nakledildikten sonra müşteri bakiyesi 0,00 olur.

## <a name="settle-all-invoices-on-july-1"></a>Tüm faturaları 1 Temmuz'da kapatma
Arnie, bu faturaların tamamını 1 Temmuz'da kapatmak üzere bir ödeme günlüğü oluşturursa, ödeme tutarı 2.980,00 olur. Arnie müşteri 4032 için bir ödeme oluşturur ve **Kapatma hareketleri** sayfasını açar. **Kapatma hareketleri** sayfasında, Arnie üç fatura satırını da kapatmak üzere işaretler:

-   Fatura FTI 10040 için ödeme 1.000,00'dir. Nakit iskontosu yapılmaz.
-   Fatura FTI-10041 için ödeme 990,00'dır. Yüzde 1 veya 10,00 tutarında nakit iskontosu alınır.
-   Fatura FTI-10042 için ödeme 990,00'dır. Yüzde 1 veya 10,00 tutarında nakit iskontosu alınır. 1 Temmuz, yüzde 2 oranında indirim uygulanan dönemden sonra olsa da, hala yüzde 1 iskonto uygulanan dönem aralığındadır.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Seçildi                 | Normal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1.000,00                             |                                       | ABD Doları      | 1.000,00         |
| Seçildi                 | Normal            | FTI-10041 | 4032    | 25/6/2015 | 25/7/2015 | 10041   | 1.000,00                             |                                       | ABD Doları      | 990,00           |
| Seçildi ve vurgulandı | Normal            | FTI-10042 | 4032    | 25/6/2015 | 25/7/2015 | 10042   | 1.000,00                             |                                       | ABD Doları      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>29 Haziran'da kısmi kapatma
Müşteri 4032 her fatura yarısı gibi kısmi bir tutarı ödeyebilir. Arnie müşteri 4032 için bir ödeme oluşturur ve **Kapatma hareketleri** sayfasını açar. **Kapatma hareketleri** sayfasında, Arnie üç fatura satırını da kapatmak üzere işaretler. Her satırda, o müşteriye sağlanan yönergelere dayalı olarak kapatılacak tutarı girer. Arnie bir satırı seçtiğinde, bu satır için geçerli iskonto tutarını ve alınan nakit iskontosu tutarını görür. Müşteri faturanın yarısını ödediğinden Arnie FTI-10042 için **Nakit iskontosu tutarı** alanındaki değerin **20,00** olduğunu ancak **Alınan nakit iskontosu** alanındaki tutarın **10,00** olduğunu görür. Ödeme tutarı 1.485,00'tir.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Seçildi                 | Normal            | FTI-10040 | 4032    | 15/5/2015 | 15/6/2015 | 10040   | 1.000,00                             |                                       | ABD Doları      | 500,00           |
| Seçildi                 | Normal            | FTI-10041 | 4032    | 25/6/2015 | 25/7/2015 | 10041   | 1.000,00                             |                                       | ABD Doları      | 495,00           |
| Seçildi ve vurgulandı | Normal            | FTI-10042 | 4032    | 25/6/2015 | 25/7/2015 | 10042   | 1.000,00                             |                                       | ABD Doları      | 490,00           |

Tamer, 1.485,00'lik ödeme tutarını, **Hareketleri kapatma** sayfasını açmadan önce el ile de girebilir. Tamer ödeme tutarını el ile girerse ve daha sonra her üç hareketi de seçerse ancak **Kapatılacak tutar** alanının değerini her bir hareket için ayarlamazsa, sayfayı kapattığında aşağıdaki iletiyi alır:

> İşaretlenen hareketlerin toplam tutarı günlük tutarından farklı. Günlükteki tutar değiştirilsin mi?

Arnie ödemenin sadece 1.485,00 olmasını istiyorsa **Hayır** seçeneğini tıklar veya günlüğü deftere nakleder. Hareketler aşağıdaki şekilde kapatılır:

1.  FTI-10040, 15 Mayıs'ta girildiğinden ve en eski fatura olduğundan 1.000,00 tutarı tamamen kapatılır. Nakit iskontosu yapılmaz. Ödeme hareketinde kalan tutar 485,00'tir.
2.  Fatura FTI 10041 için hiçbir tutar kapatılmaz. Faturala FTI-10041 ve FTI-10042 aynı tarihte girilmiştir. Ancak, fatura FTI-10041 için yüzde 1 oranında ve fatura FTI-10042 için yüzde 2 oranında iskonto uygulanabilir. Fatura FTI-10042 için daha iyi bir iskonto sunulduğundan, kalan 485,00 fatura FTI-10042 ile kapatılır.
3.  Fatura FTI-10042 kalan 485,00 ile kapatılır. Fabrikam kısmi iskontolar sunar. Bu durumda, indirim 9,90 (= 485,00 ÷ 0,98 × 0,02) olur. Yüzde 2 iskonto olduğundan tutar (485,00) 0,98 ile bölünür (bu nedenle müşteri faturanın yüzde 98'ini öder). Sonu. iskonto yüzdesi olan 2 ile çarpılır. 485,00 ödeme artı 9,90 iskonto 494,90'a eşittir. Orijinal fatura tutarı 1.000,00'dir. Bu nedenle, hareket bakiyesi 505,10 (1.000,00 – 494.90 =) olur.

Arnie, bilgileri **Müşteri hareketleri** sayfasında görür.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan  | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10040  | Fatura          | 15/5/2015 | 10040   | 1.000,00                             |                                       | 0,00     | ABD Doları      |
| FTI-10041  | Fatura          | 25/6/2015 | 10041   | 1.000,00                             |                                       | 1.000,00 | ABD Doları      |
| FTI-10042  | Fatura          | 25/6/2015 | 10042   | 1.000,00                             |                                       | 505,10   | ABD Doları      |
| ARP-10040  | Ödeme          | 29/6/2015 |         |                                      | 1.485,00                              | 0,00     | ABD Doları      |
| DISC-10040 | Nakit iskontosu    | 29/6/2015 |         |                                      | 9,90                                  | 0,00     | ABD Doları      |





