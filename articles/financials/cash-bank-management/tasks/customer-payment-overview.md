---
title: Müşteri ödemesine genel bakış
description: Bu görev kılavuzu, müşteri ödemelerini girmek için kullanılan çeşitli yöntemleri açıklar.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2168dd4074b6bd6da84dcf79db4dada9ca4d0138
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842076"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="c002c-103">Müşteri ödemesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c002c-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c002c-104">Bu görev kılavuzu, müşteri ödemelerini girmek için kullanılan çeşitli yöntemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="c002c-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="c002c-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c002c-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c002c-106">Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c002c-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="c002c-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-107">Click New.</span></span>
3. <span data-ttu-id="c002c-108">Müşteri ödemelerinin kaydedileceği ödeme günlüğünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c002c-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="c002c-109">Günlüğü seçin veya el ile girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="c002c-110">Müşteri ödemeleri gir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="c002c-111">Müşteri ödemeleri girmek aynı anda bir müşteri ödemesi kaydetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c002c-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="c002c-112">Üstte, ödeme bilgilerini girin ve sonra aynı sayfada ödeme tarafından ödenen faturaları işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c002c-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="c002c-113">Ödemeyi aldığınız müşteriyi girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="c002c-114">Müşteri bilmiyor ancak ödenen hareketi biliyorsanız, ödemeyi girmek için Hareket alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c002c-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="c002c-115">Hareket alanında faturayı girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c002c-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="c002c-116">Müşteri, siz hareketi seçtikten sonra otomatik olarak varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="c002c-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="c002c-117">Ödeme referansı alanına, bir ödeme referansı girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="c002c-118">Ödeme referansı, müşterinin çek numarası veya müşterinin elektronik ödemesinden bir referans olabilir.</span><span class="sxs-lookup"><span data-stu-id="c002c-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="c002c-119">Ödeme referansı, ödemeyi bir havale makbuzuna dahil etmek için seçmeniz durumunda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c002c-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="c002c-120">Ödemenin banka havalesi üzerine dahil edilecek olup olmadığını seçin.</span><span class="sxs-lookup"><span data-stu-id="c002c-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="c002c-121">Müşteri ödemesinin tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="c002c-122">Ödeme tutarı varsayılan olmaz.</span><span class="sxs-lookup"><span data-stu-id="c002c-122">The payment amount will not default.</span></span> <span data-ttu-id="c002c-123">El ile girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c002c-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="c002c-124">Müşteri tarafından ödenen faturaları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c002c-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="c002c-125">Ödeme bir ön ödemeyse, kapatma için herhangi bir fatura işaretlemeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="c002c-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="c002c-126">Ödeme yine de kaydedilebilir ve deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="c002c-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="c002c-127">Fatura için kapatma daha sonra gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c002c-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="c002c-128">Seçilen faturaya kapatılacak olan ödemenin miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="c002c-129">Bu alan, ödeme için kısmi bir ödeme olduğunda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c002c-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="c002c-130">Bir tutar girmezseniz, kapatılacak tutar sizin için otomatik olarak belirlenir.</span><span class="sxs-lookup"><span data-stu-id="c002c-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="c002c-131">Günlüğe kaydet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-131">Click Save in journal.</span></span>
    * <span data-ttu-id="c002c-132">Ödemeyi günlüğe kaydetmeden önce mahsup hesabın tanımlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c002c-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="c002c-133">Günlüğe kaydet seçeneğini kullanmak, ödemenin kaydedilip günlüğe taşınmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="c002c-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="c002c-134">Bir sonraki ödemeyi girerek devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c002c-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="c002c-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c002c-135">Close the page.</span></span>
14. <span data-ttu-id="c002c-136">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-136">Click Lines.</span></span>
    * <span data-ttu-id="c002c-137">Satırları açarken, Müşteri ödemeleri girin sayfasında kaydetmiş olduğunuz ve günlüğe kaydedilen tüm ödemeleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="c002c-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="c002c-138">Ayrıca, bu sayfayı yeni müşteri ödemeleri girmek veya mevcut müşteri ödemesini deftere nakletmeden önce düzenlemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c002c-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="c002c-139">Başka bir ödeme oluşturmak için Yeni seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="c002c-140">Ödemeyi aldığınız müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="c002c-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="c002c-141">Müşteriyi bilmiyor ancak ödeme tarafından ödenen bir faturayı biliyorsanız, Fatura alanını kullanarak faturayı el ile girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c002c-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="c002c-142">Fatura seçildikten sonra müşteri varsayılan olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="c002c-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="c002c-143">Ödenen faturaları işaretlemek için Hareketleri kapat seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="c002c-144">Ödemeyi herhangi bir fatura karşılık kapatmanıza gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="c002c-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="c002c-145">Bu bir ön ödemeyse veya hangi faturanın ödendiğini bilmiyorsanız, ödemeyi girebilir ve deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c002c-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="c002c-146">Ödeme, daha sonraki bir zamanda bir faturaya karşılık kapatılabilir.</span><span class="sxs-lookup"><span data-stu-id="c002c-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="c002c-147">Ödeme ile ödenen faturaları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c002c-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="c002c-148">Faturaya kapatılacak olan ödemenin tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="c002c-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c002c-149">Click OK.</span></span>
21. <span data-ttu-id="c002c-150">Ödeme referansı alanına, bir ödeme referansı girin.</span><span class="sxs-lookup"><span data-stu-id="c002c-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="c002c-151">'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c002c-151">.</span></span>
    * <span data-ttu-id="c002c-152">Ödeme referansı, ödemeyi bir havale makbuzuna dahil etmek için seçmeniz durumunda gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c002c-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="c002c-153">Müşteri ödemelerini deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="c002c-153">Post the customer payments.</span></span> 

