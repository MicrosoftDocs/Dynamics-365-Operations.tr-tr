---
title: Sıfır değerine sahip bir ürün makbuzu için sıfır miktarlı satınalma tahakkuku deftere nakledildi
description: Sıfır değerine sahip bir ürün girişi deftere nakledildiğinde, sistem tutarın 0 (sıfır) olduğu satınalma tahakkuku için bir deftere nakil işlemi oluşturur.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026999"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Sıfır değerine sahip bir ürün makbuzu için sıfır miktarlı satınalma tahakkuku deftere nakledildi

KB numarası: 4612588

## <a name="symptoms"></a>Belirtiler

Sıfır değerine sahip bir ürün girişi deftere nakledildiğinde, sistem tutarın 0 (sıfır) olduğu satınalma tahakkuku için bir deftere nakil işlemi oluşturur.

## <a name="resolution"></a>Çözünürlük

Varsayılan olarak, *Satınalma tahakkuk* türü genel muhasebe nakilleri için, `IsTransferredIndetail` alanı alt genel muhasebe hareketlerinde her zaman *Özet* olarak ayarlanır. Bu nedenle, tutar 0 (sıfır) olsa bile sistem ilgili bir fiş girişi oluşturur.

Tutar 0 (sıfır) olduğunda bu deftere nakil türünü atlamak için, `subledgerJournalizer.markDoNotTransferEntries`yöntemini `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` kapsayacak şekilde genişletin (aşağıdaki örnekte gösterildiği şekilde).

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
