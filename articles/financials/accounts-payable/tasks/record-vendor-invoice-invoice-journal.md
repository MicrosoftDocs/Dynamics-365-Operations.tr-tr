---
title: Fatura günlüğüne satıcı faturası kaydetme
description: Bu görev kılavuzu satınalma siparişleriyle ilişkili olmayan satıcı faturalarının nasıl kaydedileceğini gösterir.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97dd03a96389ab22e441acd0af1ad35852570be4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837024"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Fatura günlüğüne satıcı faturası kaydetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
12. **Naklet**'e tıklayın.
13. Sayfayı kapatın.

