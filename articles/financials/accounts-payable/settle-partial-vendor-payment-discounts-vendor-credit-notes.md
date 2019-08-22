---
title: Satıcı alacak dekontlarında iskontolar içeren bir kısmi satıcı ödemesini kapatma
description: Bu makalede bir faturaya karşılık bir alacak dekontunun kapanışın yapıldığı bir senaryoda size eşlik edilmektedir.
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
ms.search.scope: Core, Operations
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 923ab0305ac75c1156984c7a6d051f036479a16d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834523"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Satıcı alacak dekontlarında iskontolar içeren bir kısmi satıcı ödemesini kapatma

[!include [banner](../includes/banner.md)]

Bu makalede bir faturaya karşılık bir alacak dekontunun kapanışın yapıldığı bir senaryoda size eşlik edilmektedir.

Fabrikam satıcıları credit note'larında nakit iskontoları verir. Satıcı 3050 bir fatura 14 günde ödeniyorsa Fabrikam'ın yüzde 1'lik bir bir nakit iskontosu almasını sağlar.

## <a name="invoice-and-credit-memo"></a>Fatura ve credit memo
29 Haziran tarihinde April 3050 numaralı satıcı için 1.000,00 tutarında bir fatura oluşturuyor. 2 Temmuz'da 200,00 için alacak dekontu oluşturuyor. April, **Satıcılar** sayfasından **İşlemleri düzelt** sayfasını açar. April hem kredi notunu hem düzeltilecek faturayı işaretlemek için **İşlemleri düzelt** sayfasını kullanabilir. Credit note'ta 2.00 değerinde bir iskonto hespalanır. Bu nedenle, toplam credit note değeri 198.00'a düşürülür.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi                 | Normal            | Inv-10070 | 3050    | 29/6/2015 | 29/7/2015 | 10070   | -1.000,00                      | ABD Doları      | -990,00          |
| Seçildi ve vurgulandı | Normal            | CR-10070  | 3050    | 2/7/2015  | 29/7/2015 |         | 200,00                         | ABD Doları      | 198,00           |

Credit note için iskonto bilgileri **Açık işlemleri düzelt** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 13/7/2015 |
| Nakit iskontosu tutarı         | 2,00      |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 2,00      |

April, **Yayınla** düğmesini tıklar. Daha sonra tamamlanan işlemleri gözden geçirir. April, 198.00 değerindeki credit note'unun uygulandığını ve 2,00 değerinde bir iskontonun alındığını görür. Bu nedenle toplam 200,00'dır.

| İşaret                     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura  | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Seçildi ve vurgulandı | Normal            | Inv-10070 | 3050    | 29/6/2015 | 29/7/2015 | 10070    | -1.000,00                      | ABD Doları      | -200,00          |
| Seçildi                 | Normal            | CR-10070  | 3050    | 2/7/2015  | 29/7/2015 | CR-10070 | 200,00                         | ABD Doları      | 198,00           |

April, **Tüm satıcılar** sayfasını seçerek **Satıcı işlemleri** sayfasındaki satıcı işlemlerini gözden geçirebilir ve ardından İşlem Panosundan **İşlemler** düğmesini tıklayabilir. April, bu sayada faturanın -800,00 değerinde bir bakiyeye sahip olduğunu görür. Ayrıca, 198,00 değerinde bir credit note ve 2,00 değerinde bir iskonto bulunduğunu görür.

| Fiş    | Hareket türü | Tarih      | Fatura | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan | Para Birimi |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | Fatura          | 29/6/2015 | 10070   |                                      | 1.000,00                              | -800,00 | ABD Doları      |
| Inv-10071  |                  | 2/7/2015  | CR10071 | 200,00                               |                                       | 0,00    | ABD Doları      |
| DISC-10071 |  Nakit iskontosu   | 2/7/2015  |         | 2,00                                 |                                       | 0,00    | ABD Doları      |
| DISC-10071 |  Nakit iskontosu   | 2/7/2015  |         |                                      | 2,00                                  | 0,00    | ABD Doları      |





