---
title: Ters günlük nakli
description: Bu konu, fiş hareket listesinden veya mali günlüklerden fişleri ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08aec836ce4b7b6a59c445f138365f101a78c68e
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030934"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="c0f11-103">Ters günlük nakli</span><span class="sxs-lookup"><span data-stu-id="c0f11-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0f11-104">Bu konu, Microsoft Dynamics 365 Finance'in bir günlüğün tamamını veya kaynağından bağımsız olarak, hareket listesinden bir veya daha fazla fişi ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c0f11-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="c0f11-105">Günlükleri ters kaydetme</span><span class="sxs-lookup"><span data-stu-id="c0f11-105">Reversing journals</span></span>

<span data-ttu-id="c0f11-106">Günlük satırlarını tek tek ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="c0f11-107">Ters günlük nakli ile tüm mali günlüğü de tersine çevirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="c0f11-108">Bir günlüğü ters kaydetmek için:</span><span class="sxs-lookup"><span data-stu-id="c0f11-108">To reverse a journal:</span></span> 

- <span data-ttu-id="c0f11-109">Mali günlüğü açın ve deftere nakledilmiş günlükleri filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="c0f11-110">Sayfanın üst tarafındaki **Ters kaydet** menüsüne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c0f11-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="c0f11-111">Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz</span><span class="sxs-lookup"><span data-stu-id="c0f11-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="c0f11-112">Varolan hareket tarihlerini kullanmak için **Evet**'i, yeni bir hareket girmek için **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="c0f11-113">Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="c0f11-114">**Hayır**'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="c0f11-115">Ters kayıt hareketine eklenmesini istediğiniz bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="c0f11-116">**Ters kaydet** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="c0f11-117">Hareketler ters kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="c0f11-118">Fiş 100'den fazla satır içeriyorsa ters kayıt işlemi, toplu işlem kullanarak çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="c0f11-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="c0f11-119">Toplu işlemdeki yorumları görüntüleyerek sonuçları inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="c0f11-120">Geri döndürülemeyen hareketler toplu iş geçmişinde listelenecektir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="c0f11-121">Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="c0f11-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="c0f11-122">Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="c0f11-123">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="c0f11-124">Fiş hareket listesinden fişleri ters kaydetme.</span><span class="sxs-lookup"><span data-stu-id="c0f11-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="c0f11-125">Tüm alt defterlerdeki **Fiş hareket listesinden** fişleri de ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="c0f11-126">Ayrıca, bir kerede birden fazla fişi ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="c0f11-127">Bir veya daha fazla fişi ters kaydetmek için:</span><span class="sxs-lookup"><span data-stu-id="c0f11-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="c0f11-128">Sayfanın üst tarafındaki **Ters kaydet** menüsünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="c0f11-129">Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="c0f11-130">Varolan hareket tarihlerini kullanmak için **Evet**'i, yeni bir hareket girmek için **Hayır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="c0f11-131">Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="c0f11-132">**Hayır**'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="c0f11-133">Ters işlem hareketini açıklamak için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="c0f11-134">**Ters kaydet** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="c0f11-135">Hareketler ters kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="c0f11-136">100'den fazla fiş satırı varsa ters kayıt işlemi, toplu işlem kullanarak çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="c0f11-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="c0f11-137">Toplu işlemdeki yorumları görüntüleyerek sonuçları inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c0f11-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="c0f11-138">Geri döndürülemeyen hareketler toplu iş geçmişine not edilir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="c0f11-139">Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="c0f11-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="c0f11-140">Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="c0f11-141">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c0f11-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="c0f11-142">Hareketler ancak ters işlem uygulanabilecek iş kurallarına uygun olduklarında ters kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="c0f11-143">Bu konuda açıklanan özellik kullanılarak satıcı ödemeleri tersine çevrilemez.</span><span class="sxs-lookup"><span data-stu-id="c0f11-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="c0f11-144">Satıcı ödemelerinin [Satıcı ödemesini tersine çevirme](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment) bölümünde listelenen adımlar kullanılarak tersine çevrilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c0f11-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

