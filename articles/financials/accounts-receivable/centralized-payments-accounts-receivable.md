---
title: "Alacaklar hesapları için merkezi ödemeler"
description: "Birden çok tüzel kişilik içeren kuruluşlar tüm ödemeleri yöneten tek bir tüzel kişilik kullanarak ödemeleri oluşturabilir ve yönetebilirler. Bu nedenle, birden çok tüzel kişilikte aynı hareketin girilmesi gerekmez. Bu makalede, çeşitli senaryolarda deftere nakletmenin merkezi ödemeler için nasıl işlendiğini gösteren örnekler yer almaktadır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6327d9cab1651d22cd411f718f6e3a2f8733e13e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a>Alacaklar hesapları için merkezi ödemeler

[!include[banner](../includes/banner.md)]


Birden çok tüzel kişilik içeren kuruluşlar tüm ödemeleri yöneten tek bir tüzel kişilik kullanarak ödemeleri oluşturabilir ve yönetebilirler. Bu nedenle, birden çok tüzel kişilikte aynı hareketin girilmesi gerekmez. Bu makalede, çeşitli senaryolarda deftere nakletmenin merkezi ödemeler için nasıl işlendiğini gösteren örnekler yer almaktadır.

Birden çok tüzel kişilik içeren kuruluşlar tüm ödemeleri yöneten bir tüzel kişilik kullanarak ödemeleri oluşturabilir ve yönetebilirler. Bu nedenle, birden çok tüzel kişilikte aynı hareketin girilmesi gerekmez. Ayrıca kuruluş, ödeme teklifleri, kapatmalar ve merkezi ödemeler için açık ve kapalı hareketlerin düzenleme işlemleri verimli hale getirileceği için zamandan tasarruf sağlar. 

Bir merkezi ödeme organizasyonunda, işlemler için birçok tüzel kişilik vardır ve işlem yapan her bir tüzel kişilik kendi faturalarının alacak bilgilerini yönetir. İşlem yapan tüm tüzel kişilikler için ödemeler tek bir tüzel varlık tarafından alınır ve bu, ödemenin tüzel kişiliği olarak bilinir. Kapatma işlemi sırasında, ilgili vade sonu ve vade başlangıcı hareketleri oluşturulur. Organizasyondaki hangi tüzel kişiliğin gerçekleşmiş kar veya gerçekleşmiş zarar hareketlerini alacağını ve merkezi ödeme ile ilgili nakit iskonto işlemlerinin nasıl halledileceğini belirleyebilirsiniz. 

Aşağıdaki örneklerde, naklin çeşitli senaryolarda nasıl yönetildiği gösterilmektedir. Tüm bu örnekler için aşağıdaki yapılandırma varsayılır:

-   Tüzel kişilikler Fabrikam, Fabrikam East ve Fabrikam West şeklindedir. Müşteri ödemeleri, Fabrikam'a girilir.
-   **Şirketlerarası muhasebe** sayfasındaki **Nakit iskontosu nakli** alanında **Faturanın tüzel kişiliği** olarak ayarlanmıştır.
-   **Şirketlerarası muhasebe** sayfasındaki **Döviz kuru kazancını veya kaybını deftere naklet** alanında **Ödemenin tüzel kişiliği** olarak ayarlanmıştır.
-   Northwind Traders müşterisi, her bir tüzel kişilikte müşteri olarak ayarlanmıştır. Çeşitli tüzel kişiliklerden müşteriler aynı müşteri olarak tanımlanır çünkü bunlar aynı genel adres defteri kimliğine sahiptir.

| Adres defteri kodu | Müşteri hesabı | Dosya Adı              | Tüzel kişilik  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Doğu Fabrikam |
| 4050            | 10000            | Northwind Traders | Batı Fabrikam |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>Örnek 1: Başka bir tüzel kişilikten faturanın müşteri ödemesi
Fabrikam, Fabrikam müşteri hesabı 4000, Northwind Traders için 600,00 tutarında bir ödeme alıyor. Ödeme, Fabrikam East'te müşteri hesabı 4000'e ait açık bir faturayla kapatılıyor.

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>Müşteri 4000 için faturanın Fabrikam East'e nakledilmesi

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam East) | 600,00       |               |
| Satış (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Ödemenin müşteri 4000 için Fabrikam'da alınması ve nakledilmesi

| Hesap                        | Borç tutarı | Alacak tutarı |
|--------------------------------|--------------|---------------|
| Nakit (Fabrikam)                | 600,00       |               |
| Alacak hesapları (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesinin Fabrikam East faturasıyla kapatılması

**Fabrikam nakli**

| Hesap                         | Borç tutarı | Alacak tutarı |
|---------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam)  | 600,00       |               |
| Vade sonu Fabrikam East (Fabrikam) |              | 600,00        |

**Fabrikam East nakli**

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam (Fabrikam East)   | 600,00       |               |
| Alacak hesapları (Fabrikam East) |              | 600,00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>Örnek 2: Başka bir tüzel kişilikten nakit iskontosu ile müşterinin fatura ödemesi
Fabrikam, Fabrikam müşterisi 4000, Northwind Traders için 580,00 tutarında bir ödeme alıyor. Fabrikam East, müşteri 4000, Fourth Coffee için açık bir faturaya sahip. Fatura 20,00'lik nakit iskontosu içeriyor. Ödeme, Fabrikam East faturalarıyla kapatılıyor. Nakit iskontosu faturanın tüzel kişiliği olan Fabrikam East'e naklediliyor.

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Faturanın, Fabrikam East müşterisi 4000 için Fabrikam East'e nakledilmesi

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam East) | 600,00       |               |
| Satış (Fabrikam East)               |              | 600,00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Ödemenin Fabrikam müşterisi 4000 için Fabrikam'da alınması ve nakledilmesi

| Hesap                        | Borç tutarı | Alacak tutarı |
|--------------------------------|--------------|---------------|
| Nakit (Fabrikam)                | 600,00       |               |
| Alacak hesapları (Fabrikam) |              | 600,00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesinin Fabrikam East faturasıyla kapatılması

**Fabrikam nakli**

| Hesap                         | Borç tutarı | Alacak tutarı |
|---------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam)  | 580,00       |               |
| Vade sonu Fabrikam East (Fabrikam) |              | 580,00        |

**Fabrikam East nakli**

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam (Fabrikam East)   | 580,00       |               |
| Alacak hesapları (Fabrikam East) |              | 580,00        |
| Nakit iskontosu (Fabrikam East)       | 20,00        |               |
| Alacak hesapları (Fabrikam East) |              | 20,00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>Örnek 3: Başka bir tüzel kişilikten, gerçekleştirilen döviz kuru kazancı ile müşterinin fatura ödemesi
Fabrikam, Fabrikam müşterisi 4000, Northwind Traders'dan 600,00 tutarında bir ödeme alıyor. Ödeme, Fabrikam East'te müşteri 4000'e ait açık bir faturayla kapatılıyor. Kapatma işlemi sırasında bir para birimi döviz kuru kazancı hareketi oluşturulur.

-   Fatura tarihi itibariyle eurodan ABD dolarına (USD) döviz kuru: 1,2062
-   Ödeme tarihindeki EUR - USD döviz kuru: 1,2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>Faturanın, Fabrikam East müşterisi 4000 için Fabrikam East'e nakledilmesi

| Hesap                             | Borç tutarı            | Alacak tutarı           |
|-------------------------------------|-------------------------|-------------------------|
| Alacak hesapları (Fabrikam East) | 600,00 EUR / 723,72 USD |                         |
| Satış (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>Ödemenin Fabrikam müşterisi 4000 için Fabrikam'da alınması ve nakledilmesi

| Hesap                        | Borç tutarı            | Alacak tutarı           |
|--------------------------------|-------------------------|-------------------------|
| Nakit (Fabrikam)                | 600,00 EUR / 736,62 USD |                         |
| Alacak hesapları (Fabrikam) |                         | 600,00 EUR / 736,62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesinin Fabrikam East faturasıyla kapatılması

**Fabrikam nakli**

| Hesap                         | Borç tutarı            | Alacak tutarı           |
|---------------------------------|-------------------------|-------------------------|
| Alacak hesapları (Fabrikam)  | 600,00 EUR / 736,62 USD |                         |
| Vade sonu Fabrikam East (Fabrikam) |                         | 600,00 EUR / 736,62 USD |
| Vade sonu Fabrikam East (Fabrikam) | 0,00 EUR / 12,90 USD    |                         |
| Gerçekleşen kazanç (Fabrikam)        |                         | 0,00 EUR / 12,90 USD    |

**Fabrikam East nakli**

| Hesap                             | Borç tutarı            | Alacak tutarı           |
|-------------------------------------|-------------------------|-------------------------|
| Vade başlangıcı Fabrikam (Fabrikam East)   | 600,00 EUR / 736,62 USD |                         |
| Alacak hesapları (Fabrikam East) |                         | 600,00 EUR / 736,62 USD |
| Alacak hesapları (Fabrikam East) | 0,00 EUR / 12,90 USD    |                         |
| Vade başlangıcı Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 12,90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>Örnek 4: Başka bir tüzel kişilikten, nakit iskontosu ve gerçekleştirilen döviz kuru kazancı ile müşterinin fatura ödemesi
Fabrikam, Fabrikam East'teki açık bir fatura için, Fabrikam müşterisi 4000, Northwind Traders'a bir ödeme naklediyor. Faturada bir nakit iskontosu var ve satış vergisi hareketi oluşturuluyor. Ödeme, Fabrikam East faturasıyla kapatılıyor. Kapatma işlemi sırasında bir para birimi döviz kuru kazancı hareketi oluşturulur. Nakit iskontosu faturanın tüzel kişiliğine (Doğu Fabrikam) nakledilir ve para birimi döviz kuru kazanımı ödemenin tüzel kişiliğine (Fabrikam) nakledilir.

-   Fatura tarihindeki EUR - USD döviz kuru: 1,2062
-   Ödeme tarihindeki EUR - USD döviz kuru: 1,2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>Satıcı 4000 için Fabrikam East'e serbest metin faturasının nakledilmesi ve vergi hareketinin oluşturulması

| Hesap                             | Borç tutarı            | Alacak tutarı           |
|-------------------------------------|-------------------------|-------------------------|
| Alacak hesapları (Fabrikam East) | 638,22 EUR / 769,82 USD |                         |
| Satış (Fabrikam East)               |                         | 600,00 EUR / 723,72 USD |
| Satış vergisi (Fabrikam East)           |                         | 38,22 EUR / 46,10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>Ödemenin müşteri 4000 için Fabrikam'da alınması ve nakledilmesi

| Hesap                        | Borç tutarı            | Alacak tutarı           |
|--------------------------------|-------------------------|-------------------------|
| Nakit (Fabrikam)                | 626,22 EUR / 768,81 USD |                         |
| Alacak hesapları (Fabrikam) |                         | 626,22 EUR / 768,81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam ödemesinin Fabrikam East faturasıyla kapatılması

**Fabrikam nakli**

| Hesap                         | Borç tutarı            | Alacak tutarı           |
|---------------------------------|-------------------------|-------------------------|
| Alacak hesapları (Fabrikam)  | 626,22 EUR / 768,81 USD |                         |
| Vade sonu Fabrikam East (Fabrikam) |                         | 626,22 EUR / 768,81 USD |
| Vade sonu Fabrikam East (Fabrikam) | 0,00 EUR / 13,46 USD    |                         |
| Gerçekleşen kazanç (Fabrikam)        |                         | 0,00 EUR / 13,46 USD    |

**Fabrikam East nakli**

| Hesap                             | Borç tutarı            | Alacak tutarı           |
|-------------------------------------|-------------------------|-------------------------|
| Vade başlangıcı Fabrikam (Fabrikam East)   | 626,22 EUR / 768,81 USD |                         |
| Alacak hesapları (Fabrikam East) |                         | 626,22 EUR / 768,81 USD |
| Alacak hesapları (Fabrikam East)  | 0,00 EUR / 13,46 USD    |                         |
| Vade başlangıcı Fabrikam (Fabrikam East)   |                         | 0,00 EUR / 13,46 USD    |
| Nakit iskontosu (Fabrikam East)       | 12,00 EUR / 14,47 USD   |                         |
| Alacak hesapları (Fabrikam East) |                         | 12,00 EUR / 14,47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>Örnek 5: Birincil ödeme ile müşteri alacak dekontu
Fabrikam, müşteri 4000, Northwind Traders için 75,00'lik bir ödeme alıyor. Ödeme, Fabrikam West müşteri 10000 için olan bir açık faturayla ve Fabrikam East müşterisi 4000 için açık bir alacak dekontu ile kapatılıyor. Ödeme, **Hareketleri kapatma** sayfasında birincil ödeme olarak seçilmiştir.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Faturanın müşteri 10000 için Fabrikam West'e nakledilmesi

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam West) | 100,00       |               |
| Satış (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Alacak dekontunun müşteri 4000 için Fabrikam East'e nakledilmesi

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Satış iadeleri (Fabrikam East)       | 25,00        |               |
| Alacak hesapları (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Ödemenin müşteri 4000 için Fabrikam'a nakledilmesi

| Hesap                        | Borç tutarı | Alacak tutarı |
|--------------------------------|--------------|---------------|
| Nakit (Fabrikam)                | 75,00        |               |
| Alacak hesapları (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam ödemesinin, Fabrikam West faturası ve Fabrikam East alacak dekontuyla kapatılması

**Fabrikam nakli**

| Hesap                           | Borç tutarı | Alacak tutarı |
|-----------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam East (Fabrikam) | 25,00        |               |
| Alacak hesapları (Fabrikam)    |              | 25,00         |
| Alacak hesapları (Fabrikam)    | 100,00       |               |
| Vade sonu Fabrikam West (Fabrikam)   |              | 100,00        |

**Fabrikam East nakli**

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam East) | 25,00        |               |
| Vade sonu Fabrikam (Fabrikam East)     |              | 25,00         |

**Fabrikam West nakli**

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam (Fabrikam West)   | 100,00       |               |
| Alacak hesapları (Fabrikam West) |              | 100,00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>Örnek 6: Birincil ödeme olmadan müşteri alacak dekontu
Fabrikam, müşteri 4000, Northwind Traders için 75,00'lik bir ödeme alıyor. Ödeme, Fabrikam West müşteri 10000 için olan bir açık faturayla ve Fabrikam East müşterisi 4000 için açık bir alacak dekontu ile kapatılıyor. Ödeme, **Hareketleri kapatma** sayfasında birincil ödeme olarak seçilmemiştir.

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>Faturanın müşteri 10000 için Fabrikam West'e nakledilmesi

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam West) | 100,00       |               |
| Satış (Fabrikam West)               |              | 100,00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>Alacak dekontunun müşteri 4000 için Fabrikam East'e nakledilmesi

| Hesap                             | Borç tutarı | Alacak tutarı |
|-------------------------------------|--------------|---------------|
| Satış iadeleri (Fabrikam East)       | 25,00        |               |
| Alacak hesapları (Fabrikam East) |              | 25,00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>Ödemenin müşteri 4000 için Fabrikam'a nakledilmesi

| Hesap                        | Borç tutarı | Alacak tutarı |
|--------------------------------|--------------|---------------|
| Nakit (Fabrikam)                | 75,00        |               |
| Alacak hesapları (Fabrikam) |              | 75,00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam ödemesinin Fabrikam West faturası ve Fabrikam East alacak dekontuyla kapatılması

**Fabrikam nakli**

| Hesap                         | Borç tutarı | Alacak tutarı |
|---------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam)  | 75,00        |               |
| Vade sonu Fabrikam West (Fabrikam) |              | 75,00         |

**Fabrikam East nakli**

| Hesap                              | Borç tutarı | Alacak tutarı |
|--------------------------------------|--------------|---------------|
| Alacak hesapları (Fabrikam East)  | 25,00        |               |
| Vade sonu Fabrikam West (Fabrikam East) |              | 25,00         |

**Fabrikam West nakli**

| Hesap                                | Borç tutarı | Alacak tutarı |
|----------------------------------------|--------------|---------------|
| Vade başlangıcı Fabrikam (Fabrikam West)      | 75,00        |               |
| Alacak hesapları (Fabrikam West)    |              | 75,00         |
| Vade başlangıcı Fabrikam East (Fabrikam West) | 25,00        |               |
| Alacak hesapları (Fabrikam West)    |              | 25,00         |






