---
title: Fatura günlüğüne satıcı faturası kaydetme
description: Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d0e81ca37c9a59adc3acce3610fd17fd954a8b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716705"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Fatura günlüğüne satıcı faturası kaydetme

[!include [banner](../../includes/banner.md)]

Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir. Malzeme veya hizmet giderleri bu fatura türünün örneklerindendir.  Bu kayıtta USMF demo şirketi kullanılmaktadır.

1. **Gezinti bölmesi > Modüller > Borç hesapları > Çalışma alanları > Satıcı faturası girişi**'ne gidin.
2. **Eylem Bölmesi**'nde, **Yeni fatura günlüğü**'ne tıklayın.
3. **Yeni**'ye tıklayın.
4. **Ad** alanına günlük adını girin veya açılır menü düğmesine tıklayarak aramayı açın.
5. **Tanım** alanına bir değer girin.
6. **Eylem Bölmesi**'nde, **Satırlar** öğesine tıklayın. **Tarih** alanında, Genel Muhasebenin güncelleştirileceği nakil tarihini girin.  
7. **Hesap** alanında, **Satıcı hesabı**'nı belirtin.
8. **Fatura** alanına fatura numarasını girin.
9. **Tanım** alanına bir değer girin.
10. **Alacak** alanına bir sayı girin.
11. **Mahsup hesap** alanına hesap numarasını girin veya açılır menü düğmesine tıklayarak aramayı açın
    * **Satış vergisi grubu**'nun varsayılan değeri satıcı hesabından alınır.  
    * **Madde satış vergisi grubu**, **Mahsup hesap** alanında belirtilen ana hesaptan alınır.  
    * **Vade tarihi**, Ödeme koşullarına göre hesaplanır.  
    * **Nakit iskontosu**'nun varsayılan değeri Satıcı hesabından alınır.
12. Satıcı faturası günlüğü iş akışını etkinleştirdiyseniz **İş Akışı > Gönder**'i tıklayın.
    * Gönderiminiz onaylandığında, hareket deftere nakil tarihi genel muhasebe defterine nakil için Beklemede veya Kapalı olan bir döneme denk geliyorsa tarih bir sonraki açık dönemin ilk gününe ertelenir.
12. **Naklet**'e tıklayın.
13. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
