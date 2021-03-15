---
title: Nakit iskonto döneminin dışında bir nakit iskontosu almak
description: Bu makalede, bir nakit indiriminin ödeme nakit indirimi periyodu dışında yapılsa bile nasıl alınabileceğini gösteren iki senaryo verilmiştir.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7698a244c57d027d07fa7df324d3010eea6e2fe8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979375"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Nakit iskonto döneminin dışında bir nakit iskontosu almak

[!include [banner](../includes/banner.md)]

Bu makalede, bir nakit indiriminin ödeme nakit indirimi periyodu dışında yapılsa bile nasıl alınabileceğini gösteren iki senaryo verilmiştir.

28 Haziran tarihinde April 3052 numaralı satıcı için 2.000,00 tutarında bir fatura oluşturuyor. Faturada 14 gün içerisinde ödeme durumunda yüzde 1'lik bir nakit iskontosu var.

## <a name="use-cash-discount-option--always"></a>Nakit iskontosu seçeneği kullan = Her zaman
April, iskonto tarihinden sonraya denk gelen 1 Temmuz tarihinde bir ödeme yapıyor. April, kapatılabilecek hareketleri görmek için **Hareketleri kapat** sayfasını açıyor. 

April, ödeme için faturayı işaretliyor. Ödeme, iskonto tarihinden sonra yapıldığı için nakit iskontosu alınmıyor. Ancak, satıcı her durumda April'e nakit iskontosu alma onayı veriyor. Bu yüzden, April **Nakit iskontosu kullan** alanındaki değeri **Her zaman** olarak değiştiriyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Nakit iskontosu tarihi | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Her zaman            | Inv-10030 | 3052    | 28/6/2015          | 12/7/2015 | 10030   | -2.000,00                      | ABD Doları      | -1.980,00        |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 12/7/2015 |
| Nakit iskontosu tutarı         | -20,00    |
| Nakit iskontosu kullan            | Her zaman    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>İskontoların hesaplanması için kullanılacak tarih = Seçilen tarih
Hem fatura hem ödeme nakledilirse, **Hareketleri kapat** sayfasında hareketler kapatıldığında nakit iskontosu alınabilir. April, **İskontoların hesaplanması için kullanılacak tarih** alanındaki değeri **Seçilen tarih** olarak değiştiriyor. Ardından, fatura için nakit iskontosu dönemi içinde kalan 28 Haziran tarihini giriyor. Bu tarih, hareket için bir nakit iskontosunun hesaplanması için kullanılır. **Açık hareketleri kapat** sayfasında April, varsayılan olarak, 20.00 tutarında tam iskontonun görüntülendiğini görüyor. Fatura satırı, kapatılacak tutarın 1,980.00 olduğunu gösteriyor.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Nakit iskontosu tarihi | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi ve vurgulandı | Normal            | Inv-10030 | 3052    | 28/6/2015          | 12/7/2015 | 10030   | -2.000,00                      | ABD Doları      | -1.980,00        |
| Seçildi                 | Normal            | APP-10030 | 3052    | 15/7/2015          | 15/7/2015 |         | 500,00                         | ABD Doları      | 500,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir. Alınan iskonto tutarı 20,00'dir, çünkü fatura için kapatılacak tutar, varsayılan tutar olan 1.980,00'dır.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 12/7/2015 |
| Nakit iskontosu tutarı         | -20,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -20,00    |

April, **Kapatılacak tutar** alanındaki değeri **500,00** olarak güncelliyor. **Alınacak nakit iskontosu tutarı** alanındaki değer **5,05** olarak hesaplanıyor.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi ve vurgulandı | Normal            | Inv-10030 | 3052    | 28/6/2015 | 12/7/2015 | 10030   | 2.000,00                       | ABD Doları      | -500,00          |
| Seçildi                 | Normal            | APP-10030 | 3052    | 15/7/2015 | 15/7/2015 |         | 500,00                         | ABD Doları      | 500,00           |

İskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir. **Alınacak nakit iskontosu tutarı** alanındaki değer **5,05**'dir çünkü fatura için kapatılacak tutar, ödeme tutarı olan 500,00 olarak değiştirilmiştir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 12/7/2015 |
| Nakit iskontosu tutarı         | -20,00    |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -5,05     |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]