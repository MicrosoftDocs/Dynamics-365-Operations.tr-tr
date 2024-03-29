---
title: Kısmi ve son ödemeleri iskonto tarihinden önce tamamen kapatma
description: Bu makalede, bir müşteri için nasıl kısmi ödeme kaydı yapılacağına ve nakit indirimi periyodu içinde nakit indirimler alınacağına yönelik senaryolar verilmektedir.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
ms.openlocfilehash: a8da366b1e770ea649603ae85d4acc5e377ed9fb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780564"
---
# <a name="settle-partial-and-final-payments-in-full-before-the-discount-date"></a>Kısmi ve son ödemeleri iskonto tarihinden önce tamamen kapatma

[!include [banner](../includes/banner.md)]

Bu makalede, bir müşteri için nasıl kısmi ödeme kaydı yapılacağına ve nakit indirimi periyodu içinde nakit indirimler alınacağına yönelik senaryolar verilmektedir.

Fabrikam 4028 müşteriye mal satmaktadır. Fabrikam, fatura 14 gün içerisinde ödenirse yüzde 1'lik nakit iskontosu sunar. Faturaların 30 gün içinde ödenmesi gerekir. Fabrikam, kısmi ödemeler için de nakit iskontoları sunmaktadır. Kapatma parametreleri, **Alacak hesapları parametreleri** sayfasında bulunur.

## <a name="customer-invoice"></a>Müşteri faturası
25 Haziran Tamer 4028 müşteri için 1.000,00 değerinde bir faturayı girip deftere naklediyor. Arnie bu hareketi **Müşteri hareketleri** sayfasında görüntüleyebilir.

| Fiş   | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye  | Para birimi |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10010 | Fatura          | 25.06.2020 | 10010   | 1,000.00                             |                                       | 1,000.00 | ABD Doları      |

**Müşteri** veya **Müşteri hareketleri** sayfasından Arnie, **Kapatma hareketleri** sayfasını açarak fatura için kullanılabilecek nakit iskontolarının tarihlerini ve tutarlarını görüntüleyebilir. Vade tarihi 25 Temmuzdur ve faturanın 9 Temmuz tarihine kadar ödenmesi durumunda 10.00 tutarında bir nakit iskontosu uygulanır.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25.06.2020 | 25.07.2020 | 10010   | 1,000.00                       | ABD Doları      | 990.00           |

Credit note için iskonto bilgileri, işaretlenen fatura için **Kapatma hareketleri** sayfasının altında görüntülenir.

|    &nbsp;                    |  &nbsp;   |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | 10,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 10,00     |

Arnie, iskonto tutarını görmek için **Nakit iskontosu** sekmesini tıklıyor.

| Nakit iskontosu tarihi | Nakit iskontosu tutarı | Hareket para birimi cinsinden tutar |
|--------------------|----------------------|--------------------------------|
| 09.07.2020           | 10,00                | 990.00                         |
| 25.07.2020          | 0,00                 | 1,000.00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Müşteri ödemelerini girme sayfası kullanılarak kısmi ödeme
Müşteri 4028 1 Temmuz'da 500,00 için bir ödeme gönderir. Bu ödemeyi girmek için Tamer **Satırlar**'a tıklamıyor. Bunun yerine Arnie, yeni bir ödeme günlüğü oluşturarak ve ardından **Müşteri ödemelerini gir** sayfasını açarak ödemeyi kaydediyor. Arnie, ödeme bilgilerini giriyor ve girdiği faturayı işaretliyor. Arnie, tutar olarak **500,00** girdiğinde aynı zamanda ızgaradaki **Ödenecek tutar** alanına **500,00** tutarını giriyor. Fabrikam, kısmi ödemelerde bir nakit iskontosu verdiğinden Arnie 5.05 tutarında bir kısmi nakit iskontosunun da alınacağını görüyor. Bu iskonto hesaplaması şu şekildedir; 500.00 ÷ 0.99 × 0.01 = 5.05. (Yüzde 1'lik bir iskonto mevcut olduğundan bu hesaplamada 500.00 tutarı 0.99'a bölünüyor. Bu nedenle, müşteri, faturanın yüzde 99'unu ödüyor. Sonuç sonra yüzde 1, yani 0,01 iskonto yüzdesi ile çarpılıyor. Müşteri 10,00 tutarında tam iskonto alırsa, kapatılması gereken tutar 990.00 olacaktır.) İskonto bilgileri görünür **Müşteri ödemeleri gir** sayfasının altındaki kılavuzda görünür.

| Alınacak nakit iskontosu tutarı | Alınan nakit iskontosu | Ödenecek tutar |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Günlük satırları kullanılarak kısmi ödeme
Ödeme günlüğünde **Müşteri ödemelerini gir** sayfası yerine Arnie bir ödeme girmek için **Satırlar** öğesini tıklıyor. Tamer'in 4028 numaralı müşteri için bir satır girebildiği ödeme günlüğü görüntülenir. Arnie ardından, kapatmanın faturasını işaretleyebilmek için **Hareketleri kapat** sayfasını açar. Arnie, faturayı işaretliyor ve **Kapatılacak tutar** alanındaki değeri **500.00** olarak değiştiriyor. Arnie burada da **Nakit iskontosu tutarı** alanındaki değerin tam fatura için **10,00** ve **Alınacak nakit iskontosu tutarı** alanındaki değerin **5,05** olduğunu görüyor. Bu nedenle, Arnie bu fatura için 505,05 tutarını kapatıyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25.06.2020 | 25.07.2020 | 10010   | 1,000.00                       | ABD Doları      | 500.00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|        &nbsp;                | &nbsp;    |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | 10,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 5,05      |

Müşteri, faturanın tam olarak yarısını kapatmak isterse, 495,00 tutarında bir ödeme gönderir. Bu durumda Arnie **Kapatılacak tutar** alanına **495,00** değerini giriyor. 5,00 için nakit iskontosu da alınacaktır, böylece kapatılan toplam miktar 500,00 olur.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25.06.2020 | 25.07.2020 | 10010   | 1,000.00                       | ABD Doları      | 495,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|     &nbsp;                   | &nbsp;    |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | 10,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 5,00      |

Arnie, **Kapatma hareketleri** sayfasını kapatıyor. Günlükte 495.00 tutarı için bir ödeme satırı oluşturuluyor ve Arnie daha sonra günlüğü naklediyor. Arnie müşteri hareketlerini **Müşteri hareketleri** sayfasında gözden geçirebilir. Arnie bu sayada faturanın 500.00 değerinde bir bakiyeye sahip olduğunu görür. Arnie ayrıca 495.00 tutarında bir ödeme ve 5.00 tutarında bir iskonto görüyor.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye | Para birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Fatura          | 25.06.2020 | 10010   | 1,000.00                             |                                       | 500.00  | ABD Doları      |
| ARP-10010  |  Ödeme         | 7/1/2020  |         |                                      | 495,00                                | 0,00    | ABD Doları      |
| DISC-10010 |  Nakit iskontosu   | 7/1/2020  |         |                                      | 5.00                                  | 0,00    | ABD Doları      |

## <a name="payment-for-the-remaining-amount"></a>Kalan tutar için ödeme
Müşteri 4028, nakit iskontosu dönemi içinde kalan 8 Temmuz tarihine 495,00'lık kalan tutarı ödüyor. Arnie 8 Temmuz tarihinde ödeme günlüğü oluşturuyor ve hareketi kapatmak üzere işaretliyor. Arnie mutlaka kapatılması gereken tutarın 495.00 olduğunu görüyor. **Tahmini nakit iskontosu** alanındaki değer **5,00**'dir, çünkü daha önce alınan iskonto 5,00'dır.

|   &nbsp;                | &nbsp; |
|-------------------------|--------|
| İşaretli toplam            | 495,00 |
| Tahmini nakit iskontosu | 5,00   |

İşaretlenen hareket hakkında bilgiler **Açık hareketleri kapatma** sayfasındaki ızgarada görüntüleniyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10010 | 4028    | 25.06.2020 | 25.07.2020 | 10010   | 1,000.00                       | ABD Doları      | 495,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|  &nbsp;                      |  &nbsp;   |
|------------------------------|-----------|
| Nakit iskonto tarihi           | 09.07.2020 |
| Nakit iskontosu tutarı         | 10,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 5,00      |
| Alınacak nakit iskontosu tutarı | 5,00      |

Arnie bu ödeme günlüğünü naklediyor ve **Müşteri hareketleri** sayfasından müşteri hareketlerini gözden geçiriyor. Fatura için bakiye şimdi 0,00 ve Arnie iki ödeme ve iki nakit iskontosu görüyor.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Bakiye | Para birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI-10010  | Fatura          | 25.06.2020 | 10010   | 1,000.00                             |                                       | 0,00    | ABD Doları      |
| ARP-10010  | Ödeme          | 7/1/2020  |         |                                      | 495,00                                | 0,00    | ABD Doları      |
| DISC-10010 | Nakit iskontosu    | 7/1/2020  |         |                                      | 5.00                                  | 0,00    | ABD Doları      |
| ARP-10011  | Ödeme          | 08.07.2020  |         |                                      | 495,00                                | 0,00    | ABD Doları      |
| DISC-10011 | Nakit iskontosu    | 08.07.2020  |         |                                      | 5.00                                  | 0,00    | ABD Doları      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
