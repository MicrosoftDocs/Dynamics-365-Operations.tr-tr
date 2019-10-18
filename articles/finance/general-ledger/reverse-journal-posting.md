---
title: Ters günlük nakli
description: Bu konu, fiş hareket listesinden veya mali günlüklerden fişleri ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248597"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="31880-103">Ters günlük nakli</span><span class="sxs-lookup"><span data-stu-id="31880-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31880-104">Bu konu, Microsoft Dynamics 365 Finance'in bir günlüğün tamamını veya kaynağından bağımsız olarak, hareket listesinden bir veya daha fazla fişi ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="31880-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="31880-105">Günlükleri ters kaydetme</span><span class="sxs-lookup"><span data-stu-id="31880-105">Reversing journals</span></span>

<span data-ttu-id="31880-106">Günlük satırlarını tek tek ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="31880-107">Ters günlük nakli ile tüm mali günlüğü de tersine çevirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="31880-108">Bir günlüğü ters kaydetmek için:</span><span class="sxs-lookup"><span data-stu-id="31880-108">To reverse a journal:</span></span> 
- <span data-ttu-id="31880-109">Mali günlüğü açın ve deftere nakledilmiş günlükleri filtreleyin</span><span class="sxs-lookup"><span data-stu-id="31880-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="31880-110">Sayfanın üst tarafındaki Ters kaydet menüsüne tıklayın</span><span class="sxs-lookup"><span data-stu-id="31880-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="31880-111">Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz</span><span class="sxs-lookup"><span data-stu-id="31880-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="31880-112">Varolan hareket tarihlerini kullanmak için Evet'i, yeni bir hareket girmek için Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="31880-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="31880-113">Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="31880-114">Hayır'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="31880-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="31880-115">Ters kayıt hareketine eklenmesini istediğiniz bir açıklama girin</span><span class="sxs-lookup"><span data-stu-id="31880-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="31880-116">Ters kaydet düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="31880-116">Click the Reverse button</span></span>

<span data-ttu-id="31880-117">Hareketler ters kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="31880-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="31880-118">Fiş satırlarının sayısı 100'ü aşarsa, ters kayıt işlemi, toplu işlem kullanarak çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="31880-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="31880-119">Çalıştırılan toplu işlemdeki yorumları görüntüleyerek, ters kayıt sonuçlarını inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="31880-120">Tüm hatalar toplu iş geçmişine kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="31880-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="31880-121">Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="31880-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="31880-122">Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="31880-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="31880-123">İletişim kutusunu kapatmak için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31880-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="31880-124">Fiş hareket listesinden fişleri ters kaydetme.</span><span class="sxs-lookup"><span data-stu-id="31880-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="31880-125">Tüm alt defterlerdeki **Fiş hareket listesinden** fişleri de ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="31880-126">Ayrıca, bir kerede birden fazla fişi ters kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="31880-127">Bir veya daha fazla fişi ters kaydetmek için:</span><span class="sxs-lookup"><span data-stu-id="31880-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="31880-128">Sayfanın üst tarafındaki Ters kaydet menüsüne tıklayın</span><span class="sxs-lookup"><span data-stu-id="31880-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="31880-129">Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz</span><span class="sxs-lookup"><span data-stu-id="31880-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="31880-130">Varolan hareket tarihlerini kullanmak için Evet'i, yeni bir hareket girmek için Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="31880-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="31880-131">Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="31880-132">Hayır'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="31880-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="31880-133">Ters kayıt hareketine eklenmesini istediğiniz bir açıklama girin</span><span class="sxs-lookup"><span data-stu-id="31880-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="31880-134">Ters kaydet düğmesine tıklayın</span><span class="sxs-lookup"><span data-stu-id="31880-134">Click the Reverse button</span></span>

<span data-ttu-id="31880-135">Hareketler ters kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="31880-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="31880-136">Fiş satırlarının sayısı 100'ü aşarsa, ters kayıt işlemi, toplu işlem kullanarak çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="31880-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="31880-137">Çalıştırılan toplu işlemdeki yorumları görüntüleyerek, ters kayıt sonuçlarını inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="31880-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="31880-138">Tüm hatalar toplu iş geçmişine kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="31880-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="31880-139">Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="31880-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="31880-140">Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="31880-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="31880-141">İletişim kutusunu kapatmak için Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="31880-141">Click on Ok to close the dialog.</span></span>

