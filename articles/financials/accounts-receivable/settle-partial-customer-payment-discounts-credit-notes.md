---
title: Alacak dekontlarında iskontolar içeren bir kısmi müşteri ödemesini kapatma
description: Bu makalede orijinal fatura da bir nakit iskontosu içeriyorken bir credit note'a nakit iskontosunun uygulandığı bir senaryo açıklanmıştır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa641f996d1ee516f588fcd1520bdc23d5d25f86
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561118"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Alacak dekontlarında iskontolar içeren bir kısmi müşteri ödemesini kapatma

[!include [banner](../includes/banner.md)]

Bu makalede orijinal fatura da bir nakit iskontosu içeriyorken bir credit note'a nakit iskontosunun uygulandığı bir senaryo açıklanmıştır. 

Fabrikam, kısmi ödemelerde ve de alacak dekontlarında (alacak makbuzları) müşterilerin nakit iskontoları almasını sağlar. Nakit iskontosu, alacak dekontu müşterinin nakit iskontosu aldığı fatura için kesildiğinde bir alacak dekontunda da alınabilir. Tam tutar için bir alacak oluşturmak yerine, müşteri bakiyesini müşterinin nakit iskontosu yüzdesini dışarıda tutan bit tutarla alacaklandırabilirsiniz. Kapatma parametreleri, **Alacak hesapları parametreleri** sayfasında bulunur.

## <a name="invoice-and-credit-note"></a>Fatura ve alacak dekontu
Müşteri 4035'in tutarı 1.000,00 olan bir faturası ve 100,00 tutarında bir alacak dekontu vardır. 14 günde ödeniyorsa, her belgede yüzde 1'lik bir indirim olur. Tamer, bu bilgileri **Müşteri hareketleri** sayfasında görüntüleyebilir.

| Fiş    | Hareket türü | Tarih      | Fatura  | Hareket para birimi borcundaki tutar | Hareket para birimi alacağındaki tutar | Kalan  | Para Birimi |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | Fatura          | 28/6/2015 | 10050    | 1.000,00                             |                                       | 1.000,00 | ABD Doları      |
| CCRN-10050 | Alacak dekontu      | 28/6/2015 | CR-10050 |                                      | 100,00                                | -100,00  | ABD Doları      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Bir alacak dekontunu fatura ile kapatma
Tamer, **Müşteri hareketleri** sayfasında **Hareketleri kapat** sayfasın açar. Faturayı ve alacak dekontunu kapatman için **Hareketleri kapat** sayfasını kullanabilir. Kapatma işleminin bir parçası olarak, nakit iskontosu tarihlerini ve tutarlarını görüntüler. İki belgeyi işaretler ve sonra hareketleri kapatmak için **Deftere naklet**'i tıklatır. Fabrikam, iskontoları alacak dekontlarında sağladığından alacak notunda -1.00 iskonto vardır.

| İşaret     | Nakit iskontosu kullan | Fiş    | Hesap | Tarih      | Vade tarihi  | Fatura  | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Seçildi | Normal            | FTI-10050  | 4035    | 28/6/2015 | 28/7/2015 | 10050    | 1.000,00                       | ABD Doları      | 990,00           |
| Seçildi | Normal            | CCRN-10050 | 4035    | 28/6/2015 | 28/7/2015 | CR-10050 | -100,00                        | ABD Doları      | -99,00           |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 12/7/2015 |
| Nakit iskontosu tutarı         | -1,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | -1,00     |

Kapatma 100,00 tutarında olur ve 99,00 tutarında bir ödeme ve 1,00 tutarında iskonto içerir.



