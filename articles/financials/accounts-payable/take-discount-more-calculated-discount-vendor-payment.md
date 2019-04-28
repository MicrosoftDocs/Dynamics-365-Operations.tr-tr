---
title: Bir satıcı ödemesi için hesaplanan iskontodan daha fazla iskonto alma
description: Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir. Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 730ea9bb23368d24c5a09f98fbf6bbb41d685702
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/25/2019
ms.locfileid: "896109"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Bir satıcı ödemesi için hesaplanan iskontodan daha fazla iskonto alma

[!include [banner](../includes/banner.md)]

Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir. Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir. 

Satıcı 3051, bir faturanın yedi gün içinde ödenmesi durumunda Fabrikam'a yüzde 4 oranında bir nakit iskontosu veriyor. 29 Haziran tarihinde April, 1.000,00 tutarında bir fatura giriyor. Satıcı, April'in fatura için kullanılabilecek, 40,00 tutarındaki varsayılan iskonto yerine 60.00 tutarında bir iskonto almasına izin veriyor. April, Borç hesapları ödeme günlüğünü kullanarak bir tek seferlik ödeme kaydediyor. Ödeme için satıcı giriyor ve **Hareketleri kapat** sayfasını açıyor. April, faturayı işaretliyor ve **Nakit iskontosu tutarı** alanındaki değeri **60,00** olarak değiştiriyor.

| İşaret     | Nakit iskontosu kullan | Fiş   | Hesap | Tarih      | Vade tarihi  | Fatura | Hareket para birimi cinsinden tutar | Para Birimi | Kapatılacak tutar |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Seçildi | Normal            | Inv-10040 | 3051    | 29/6/2015 | 29/7/2015 | 10040   | 1.000,00                       | ABD Doları      | 940,00           |

İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.

|                              |           |
|------------------------------|-----------|
| Nakit iskontosu tarihi           | 12/7/2015 |
| Nakit iskontosu tutarı         | 60,00     |
| Nakit iskontosu kullan            | Normal    |
| Alınan nakit iskontosu          | 0,00      |
| Alınacak nakit iskontosu tutarı | 60,00     |

April sonra ödeme günlüğünü naklediyor. Fatura, 940,00 tutarında bir ödeme ve 60,00 tutarında bir iskonto kullanılarak tamamen kapatılıyor.



