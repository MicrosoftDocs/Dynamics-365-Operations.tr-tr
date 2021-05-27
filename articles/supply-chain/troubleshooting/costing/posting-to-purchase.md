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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="37a39-103">Sıfır değerine sahip bir ürün makbuzu için sıfır miktarlı satınalma tahakkuku deftere nakledildi</span><span class="sxs-lookup"><span data-stu-id="37a39-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="37a39-104">KB numarası: 4612588</span><span class="sxs-lookup"><span data-stu-id="37a39-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="37a39-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="37a39-105">Symptoms</span></span>

<span data-ttu-id="37a39-106">Sıfır değerine sahip bir ürün girişi deftere nakledildiğinde, sistem tutarın 0 (sıfır) olduğu satınalma tahakkuku için bir deftere nakil işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37a39-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="37a39-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="37a39-107">Resolution</span></span>

<span data-ttu-id="37a39-108">Varsayılan olarak, *Satınalma tahakkuk* türü genel muhasebe nakilleri için, `IsTransferredIndetail` alanı alt genel muhasebe hareketlerinde her zaman *Özet* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="37a39-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="37a39-109">Bu nedenle, tutar 0 (sıfır) olsa bile sistem ilgili bir fiş girişi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37a39-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="37a39-110">Tutar 0 (sıfır) olduğunda bu deftere nakil türünü atlamak için, `subledgerJournalizer.markDoNotTransferEntries`yöntemini `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` kapsayacak şekilde genişletin (aşağıdaki örnekte gösterildiği şekilde).</span><span class="sxs-lookup"><span data-stu-id="37a39-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
