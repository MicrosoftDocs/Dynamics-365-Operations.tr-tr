---
title: Genel muhasebe tahsisat günlüğünü işleme
description: Bu konu, Dynamics 365 Finance'de bir tahsisat talebinin nasıl işlem yapılacağını açıklar.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448839"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="13d0e-103">Genel muhasebe tahsisat günlüğünü işleme</span><span class="sxs-lookup"><span data-stu-id="13d0e-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13d0e-104">Bu konuda bir tahsisat talebinin nasıl işleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="13d0e-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="13d0e-105">Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için Tahsisat talebini işleme koy sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="13d0e-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="13d0e-106">Bir tahsisatlar günlüğü oluşturmadan önce, en az bir aktif Muhasebe defteri tahsisat kuralı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13d0e-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="13d0e-107">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="13d0e-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="13d0e-108">Gezinti bölmesinde **Modüller > Genel muhasebe > Tahsilatlar > Tahsisat talebini işleme koy**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="13d0e-109">**Kural** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="13d0e-110">**Başlangıç tarihi** alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="13d0e-111">Genel muhasebe kural için bir Veri kaynağı olduğunda **Başlangıç Tarihi** çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="13d0e-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="13d0e-112">Bu tarih, tahsisat için eklenecek genel muhasebe bakiyelerini kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="13d0e-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="13d0e-113">**Sıfır kaynak** alanında **Dur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="13d0e-114">Bu, tahsisat işlemini durdurur ve sıfıra eşit bir kaynak tutar seçildiğini belirten bir ileti görüntüler.</span><span class="sxs-lookup"><span data-stu-id="13d0e-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="13d0e-115">**Teklif seçenekleri** alanında **Yalnızca teklif** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="13d0e-116">Tahsisatın genel muhasebe defterine nakledilmesinden önce Tahsisat günlüklerindeki sonucu isteğe bağlı olarak gözden geçirmek onaylamak için **Yalnızca teklif** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="13d0e-117">GM deftere nakil tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="13d0e-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-118">Select **OK**.</span></span>
7. <span data-ttu-id="13d0e-119">Gezinti bölmesinde **Modüller > Genel muhasebe > Tahsilatlar > Tahsisat günlükleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="13d0e-120">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-120">Select **Lines**.</span></span>
9. <span data-ttu-id="13d0e-121">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-121">Select **Post**.</span></span>
10. <span data-ttu-id="13d0e-122">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13d0e-122">Select **Post**.</span></span>

