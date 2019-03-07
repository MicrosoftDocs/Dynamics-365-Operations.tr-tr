---
title: Fatura günlüğüne satıcı faturası kaydetme
description: Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "348952"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Fatura günlüğüne satıcı faturası kaydetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir. Malzeme veya hizmet giderleri bu fatura türünün örneklerindendir.  Bu kayıtta USMF demo şirketi kullanılmaktadır.

1. Borç hesapları > Çalışma alanları > Satıcı faturası girişi'ne gidin.
2. Yeni fatura günlüğü'ne tıklayın.
3. Yeni'ye tıklayın.
4. Ad alanına günlük adını girin veya açılır menü düğmesine tıklayarak aramayı açın.
5. Açıklama alanına bir değer girin.
6. Satırlar seçeneğine tıklayın.
    * Tarih alanında, Genel Muhasebenin güncelleştirileceği nakil tarihini girin.  
7. Hesap alanında, Satıcı hesabını belirtin.
8. Fatura alanına fatura numarasını girin.
9. Tanım alanına bir değer girin.
10. Alacak alanına bir sayı girin.
11. Mahsıp hesap alanına hesap numarasını girin veya açılır menü düğmesine tıklayarak aramayı açın
    * Satış vergisi grubunun varsayılan değeri satıcı hesabından alınır.  
    * Madde satış vergisi grubu, Mahsup hesap alanında belirtilen ana hesaptan alınır.  
    * Vade tarihi, Ödeme koşullarına göre hesaplanır.  
    * Nakit iskontosunun varsayılan değeri Satıcı hesabından alınır.  
12. Deftere Naklet öğesine tıklayın.
13. Sayfayı kapatın.

