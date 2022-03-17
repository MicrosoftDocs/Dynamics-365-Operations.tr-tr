---
title: Borç hesapları için merkezi ödemeler
description: Birden çok tüzel kişilik içeren kuruluşlar tüm ödemeleri yöneten tek bir tüzel kişilik kullanarak ödemeleri oluşturabilir ve yönetebilirler. Bu nedenle, birden çok tüzel kişilikte aynı ödemelerin girilmesi gerekmez. Bu konuda, çeşitli senaryolarda deftere nakletmenin merkezi ödemeler için nasıl işlendiğini gösteren örnekler yer almaktadır.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df0d2178d1ebd3dcb154e2c4f7821a4007da55d4
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/23/2022
ms.locfileid: "8331754"
---
# <a name="centralized-payments-for-accounts-payable"></a>Borç hesapları için merkezi ödemeler

[!include [banner](../includes/banner.md)]

Birden çok tüzel kişilik içeren kuruluşlar tüm ödemeleri yöneten tek bir tüzel kişilik kullanarak ödemeleri oluşturabilir ve yönetebilirler. Bu nedenle, birden çok tüzel kişilikte aynı ödemelerin girilmesi gerekmez. Bu konuda, çeşitli senaryolarda deftere nakletmenin merkezi ödemeler için nasıl işlendiğini gösteren örnekler yer almaktadır.

Bir merkezi ödemeler organizasyonunda, işlemler için birçok tüzel kişilik vardır ve işlem yapan her bir tüzel kişilik kendi satıcı faturalarını yönetir. İşlem yapan tüm tüzel kişilikler için ödemeler tek bir tüzel kişiden üretilir ve bu, ödemenin tüzel kişiliği olarak bilinir. Kapatma işlemi sırasında, ilgili vade sonu ve vade başlangıcı hareketleri oluşturulur. Organizasyondaki hangi tüzel kişiliğin gerçekleşmiş kar veya gerçekleşmiş zararı alacağını ve şirketler arası ödeme ile ilgili nakit iskonto işlemlerinin nasıl halledileceğini belirleyebilirsiniz. Merkezi ödeme günlük satırında **Hesap türünün** Satıcı olarak ayarlanması gerekir. **Mahsup hesap türü**'nün Banka veya Genel Muhasebe olarak ayarlanmış olması gerekir. Banka hesabı geçerli şirkette olmalıdır. 

Aşağıdaki örneklerde, naklin çeşitli senaryolarda nasıl yönetildiği gösterilmektedir. Tüm bu örnekler için aşağıdaki yapılandırma varsayılır:

-   Tüzel kişilikler Fabrikam, Fabrikam East ve Fabrikam West şeklindedir. Ödemeler Fabrikam'dan yapılır.
-   **Şirketlerarası muhasebe** sayfasındaki **Nakit iskontosu nakli** alanında **Faturanın tüzel kişiliği** olarak ayarlanmıştır.
-   **Şirketlerarası muhasebe** sayfasındaki **Döviz kuru kazancını veya kaybını deftere naklet** alanında **Ödemenin tüzel kişiliği** olarak ayarlanmıştır.
-   Satıcı Fourth Coffee, her bir tüzel kişilikte satıcı olarak ayarlanır. Çeşitli tüzel kişiliklerden satıcılar aynı satıcı olarak tanımlanır çünkü bunlar aynı genel adres defteri kimliğine sahiptir.

| Dizin Kodu | Satıcı hesabı | Dosya Adı          | Tüzel kişilik  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Doğu Fabrikam |
| 1050         | 3004           | Fourth Coffee | Batı Fabrikam |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>Örnek 1: Başka bir tüzel kişilikten faturanın satıcı ödemesi
Fabrikam East, satıcı hesabı 100, Fourth Coffee için açık bir faturaya sahip. Fabrikam, Fabrikam satıcı hesabı 3004, Fourth Coffee'ye bir ödeme girer ve nakleder. Ödeme açık faturayla kapatılır.

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>Fatura satıcı 100 için Fabrikam East'e nakledilir

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Masraf (Fabrikam East)          | 600,00       |               |
| Borç hesapları (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Ödeme satıcı 3004 için Fabrikam'da oluşturulur ve nakledilir

| Hesap                     | Borç tutarı | Alacak tutarı |
|-----------------------------|--------------|---------------|
| Borç hesapları (Fabrikam) | 600,00       |               |
| Nakit (Fabrikam)             |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesi Fabrikam East faturasıyla kapatılır

**Fabrikam nakli**

| Hesap                           | Borç tutarı | Alacak tutarı |
|-----------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam East (Fabrikam) | 600,00       |               |
| Borç hesapları (Fabrikam)       |              | 600,00        |

**Fabrikam East nakli**

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam East) | 600,00       |               |
| Vade sonu Fabrikam (Fabrikam East)  |              | 600,00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Örnek 2: Başka bir tüzel kişilikten nakit iskontosu ile satıcının fatura ödemesi
Fabrikam East, satıcı 100, Fourth Coffee için açık bir faturaya sahip. Fatura 20,00'lik nakit iskontosuna sahiptir. Fabrikam, Fabrikam satıcı 3004, Fourth Coffee'ye 580,00'lık bir ödeme girer ve nakleder. Ödeme, Fabrikam East faturalarıyla kapatılıyor. Nakit iskontosu faturanın tüzel kişiliği olan Fabrikam East'e naklediliyor.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Fatura, Fabrikam East satıcı 100 için Fabrikam East'e nakledilir

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Masraf (Fabrikam East)          | 600,00       |               |
| Borç hesapları (Fabrikam East) |              | 600,00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Ödeme Fabrikam satıcı 3004 için Fabrikam'da oluşturulur ve nakledilir

| Hesap                     | Borç tutarı | Alacak tutarı |
|-----------------------------|--------------|---------------|
| Borç hesapları (Fabrikam) | 580,00       |               |
| Nakit (Fabrikam)             |              | 580,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesi Fabrikam East faturasıyla kapatılır

**Fabrikam nakli**

| Hesap                           | Borç tutarı | Alacak tutarı |
|-----------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam East (Fabrikam) | 580,00       |               |
| Borç hesapları (Fabrikam)       |              | 580,00        |

**Fabrikam East nakli**

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam East) | 580,00       |               |
| Vade sonu Fabrikam (Fabrikam East)  |              | 580,00        |
| Borç hesapları (Fabrikam East) | 20,00        |               |
| Nakit iskontosu (Fabrikam East)    |              | 20,00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>Örnek 3: Başka bir tüzel kişilikten, gerçekleştirilen döviz kuru kaybı ile satıcının fatura ödemesi
Fabrikam East, satıcı 100, Fourth Coffee için açık bir faturaya sahip. Fabrikam, Fabrikam satıcı 3004, Fourth Coffee için bir ödeme girer ve nakleder. Ödeme, Fabrikam East faturasıyla kapatılır. Kapatma işlemi sırasında bir para birimi döviz kuru kaybı hareketi oluşturulur.

-   Fatura tarihi itibariyle avrodan (EUR) ABD dolarına (USD) döviz kuru: 1,2062
-   Ödeme tarihindeki EUR - USD döviz kuru: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>Fatura, Fabrikam East satıcı 100 için Fabrikam East'e nakledilir

| Hesap                          | Borç tutarı            | Alacak tutarı           |
|----------------------------------|-------------------------|-------------------------|
| Masraf (Fabrikam East)          | 600,00 EUR / 723,72 USD |                         |
| Borç hesapları (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>Ödeme Fabrikam satıcı 3004 için Fabrikam'da oluşturulur ve nakledilir

| Hesap                     | Borç tutarı            | Alacak tutarı           |
|-----------------------------|-------------------------|-------------------------|
| Borç hesapları (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Nakit (Fabrikam)             |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesi Fabrikam East faturasıyla kapatılır

**Fabrikam nakli**

| Hesap                           | Borç tutarı            | Alacak tutarı           |
|-----------------------------------|-------------------------|-------------------------|
| Vade başlangıcı Fabrikam East (Fabrikam) | 600,00 EUR / 736,62 USD |                         |
| Borç hesapları (Fabrikam)       |                         | 600,00 EUR / 736,62 USD |
| Gerçekleşen kayıp (Fabrikam)          | 0,00 EUR / 12,90 USD    |                         |
| Vade başlangıcı Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East nakli**

| Hesap                          | Borç tutarı            | Alacak tutarı           |
|----------------------------------|-------------------------|-------------------------|
| Borç hesapları (Fabrikam East) | 600,00 EUR / 736,62 USD |                         |
| Vade sonu Fabrikam (Fabrikam East)  |                         | 600,00 EUR / 736,62 USD |
| Vade sonu Fabrikam (Fabrikam East)  | 0,00 EUR / 12,90 USD    |                         |
| Borç hesapları (Fabrikam East) |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>Örnek 4: Başka bir tüzel kişilikten, nakit iskontosu ve gerçekleştirilen döviz kuru kaybı ile satıcının fatura ödemesi
Fabrikam East, satıcı 100, Fourth Coffee için açık bir faturaya sahip. Faturada bir nakit iskontosu var ve satış vergisi hareketi oluşturuluyor. Fabrikam, Fabrikam satıcı 3004, Fourth Coffee için bir ödeme nakleder. Ödeme, Fabrikam East faturasıyla kapatılır. Kapatma işlemi sırasında bir para birimi döviz kuru kaybı hareketi oluşturulur. Nakit iskontosu faturanın tüzel kişiliğine (Doğu Fabrikam) nakledilir ve para birimi döviz kuru kaybı ödemenin tüzel kişiliğine (Fabrikam) nakledilir.

-   Fatura tarihindeki EUR - USD döviz kuru: 1,2062
-   Ödeme tarihindeki EUR - USD döviz kuru: 1,2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>Satıcı 100 için Fabrikam East'te bir fatura nakledilir ve vergi hareketi oluşturulur

| Hesap                          | Borç tutarı            | Alacak tutarı           |
|----------------------------------|-------------------------|-------------------------|
| Masraf (Fabrikam East)          | 564,07 EUR / 680,38 USD |                         |
| Satış vergisi (Fabrikam East)        | 35,93 EUR / 43,34 USD   |                         |
| Borç hesapları (Fabrikam East) |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>Ödeme satıcı 3004 için Fabrikam'da oluşturulur ve nakledilir

| Hesap                     | Borç tutarı            | Alacak tutarı           |
|-----------------------------|-------------------------|-------------------------|
| Borç hesapları (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Nakit (Fabrikam East)        |                         | 588,72 EUR / 722,77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesi Fabrikam East faturasıyla kapatılır

**Fabrikam nakli**

| Hesap                           | Borç tutarı            | Alacak tutarı           |
|-----------------------------------|-------------------------|-------------------------|
| Vade başlangıcı Fabrikam East (Fabrikam) | 588,72 EUR / 722,77 USD |                         |
| Borç hesapları (Fabrikam)       |                         | 588,72 EUR / 722,77 USD |
| Gerçekleşen kayıp (Fabrikam)          | 0,00 EUR / 12,66 USD    |                         |
| Vade başlangıcı Fabrikam East (Fabrikam) |                         | 0,00 EUR / 12,66 USD    |

**Fabrikam East nakli**

| Hesap                          | Borç tutarı            | Alacak tutarı           |
|----------------------------------|-------------------------|-------------------------|
| Borç hesapları (Fabrikam East) | 588,72 EUR / 722,77 USD |                         |
| Vade sonu Fabrikam (Fabrikam East)  |                         | 588,72 EUR / 722,77 USD |
| Vade sonu Fabrikam (Fabrikam East   | 0,00 EUR / 12,66 USD    |                         |
| Borç hesapları (Fabrikam East) |                         | 0,00 EUR / 12,66 USD    |
| Borç hesapları (Fabrikam East) | 11,28 EUR / 13,61 USD   |                         |
| Nakit iskontosu (Fabrikam East)    |                         | 11,28 EUR / 13,61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>Örnek 5: Birincil ödeme ile satıcı alacak dekontu
Fabrikam, satıcı 3004, Fourth Coffee için 75,00'lik bir ödeme oluşturur. Ödeme, Fabrikam West satıcı 3004 için olan bir açık faturayla ve Fabrikam East satıcı 100 için açık bir alacak dekontu ile kapatılır. Ödeme, **Hareketleri kapatma** sayfasında birincil ödeme olarak seçilmiştir.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Fatura satıcı 3004 için Fabrikam West'e nakledilir

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Masraf (Fabrikam West)          | 100,00       |               |
| Borç hesapları (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Alacak dekontu satıcı 100 için Fabrikam East'e nakledilir

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam East) | 25,00        |               |
| Satın alma iadeleri (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Ödeme satıcı 3004 için Fabrikam'a nakledilir

| Hesap                     | Borç tutarı | Alacak tutarı |
|-----------------------------|--------------|---------------|
| Borç hesapları (Fabrikam) | 75,00        |               |
| Nakit (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam ödemesi Fabrikam West faturası ve Fabrikam East alacak dekontuyla kapatılır

**Fabrikam nakli**

| Hesap                           | Borç tutarı | Alacak tutarı |
|-----------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam)       | 25,00        |               |
| Vade sonu Fabrikam East (Fabrikam)   |              | 25,00         |
| Vade başlangıcı Fabrikam West (Fabrikam) | 100,00       |               |
| Borç hesapları (Fabrikam)       |              | 100,00        |

**Fabrikam East nakli**

| Hesap                           | Borç tutarı | Alacak tutarı |
|-----------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam (Fabrikam East) | 25,00        |               |
| Borç hesapları (Fabrikam East)  |              | 25,00         |

**Fabrikam West nakli**

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam West) | 100,00       |               |
| Vade sonu Fabrikam (Fabrikam West)  |              | 100,00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>Örnek 6: Birincil ödemesiz satıcı alacak dekontu
Fabrikam, satıcı 3004, Fourth Coffee için 75,00'lik bir ödeme oluşturur. Ödeme, Fabrikam West satıcı 3004 için olan bir açık faturayla ve Fabrikam East satıcı 100 için açık bir alacak dekontu ile kapatılır. Ödeme, **Hareketleri kapatma** sayfasında birincil ödeme olarak seçilmemiştir.

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>Fatura satıcı 3004 için Fabrikam West'e nakledilir

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Masraf (Fabrikam West)          | 100,00       |               |
| Borç hesapları (Fabrikam West) |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>Alacak dekontu satıcı 100 için Fabrikam East'e nakledilir

| Hesap                          | Borç tutarı | Alacak tutarı |
|----------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam East) | 25,00        |               |
| Satın alma iadeleri (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>Ödeme satıcı 3004 için Fabrikam'a nakledilir

| Hesap                     | Borç tutarı | Alacak tutarı |
|-----------------------------|--------------|---------------|
| Borç hesapları (Fabrikam) | 75,00        |               |
| Nakit (Fabrikam)             |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam ödemesi Fabrikam West faturası ve Fabrikam East alacak dekontuyla kapatılır

**Fabrikam nakli**

| Hesap                           | Borç tutarı | Alacak tutarı |
|-----------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam West (Fabrikam) | 75,00        |               |
| Borç hesapları (Fabrikam)       |              | 75,00         |

**Fabrikam East nakli**

| Hesap                                | Borç tutarı | Alacak tutarı |
|----------------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam West (Fabrikam East) | 25,00        |               |
| Borç hesapları (Fabrikam East)       |              | 25,00         |

**Fabrikam West nakli**

| Hesap                              | Borç tutarı | Alacak tutarı |
|--------------------------------------|--------------|---------------|
| Borç hesapları (Fabrikam West)     | 75,00        |               |
| Vade sonu Fabrikam (Fabrikam West)      |              | 75,00         |
| Borç hesapları (Fabrikam West)     | 25,00        |               |
| Vade sonu Fabrikam East (Fabrikam West) |              | 25,00         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
