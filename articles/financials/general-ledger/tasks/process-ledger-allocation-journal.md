--- 
title: "Genel muhasebe tahsisat günlüğünü işleme"
description: "Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için Tahsisat talebini işleme koy sayfasını kullanın."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="780ba-103">Genel muhasebe tahsisat günlüğünü işleme</span><span class="sxs-lookup"><span data-stu-id="780ba-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="780ba-104">Genel muhasebe defterine nakledilmeden önce gözden geçirilip onaylanabilecek veya doğrudan Genel muhasebe defterine nakledilebilecek bir tahsisat günlüğü oluşturmak için Tahsisat talebini işleme koy sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="780ba-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="780ba-105">Bir tahsisatlar günlüğü oluşturmadan önce, en az bir aktif Muhasebe defteri tahsisat kuralı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="780ba-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="780ba-106">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="780ba-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="780ba-107">Genel muhasebe > Tahsisatlar > Tahsisat talebini işlem koy'a gidin.</span><span class="sxs-lookup"><span data-stu-id="780ba-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="780ba-108">Kural alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="780ba-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="780ba-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="780ba-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="780ba-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="780ba-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="780ba-111">Başlangıç tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="780ba-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="780ba-112">Genel muhasebe kural için bir Veri kaynağı olduğunda Başlangıç Tarihi çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="780ba-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="780ba-113">Bu tarih, tahsisat için eklenecek genel muhasebe bakiyelerini kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="780ba-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="780ba-114">Sıfır kaynak alanında Dur'u seçin.</span><span class="sxs-lookup"><span data-stu-id="780ba-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="780ba-115">Bu, tahsisat işlemini durdurur ve sıfıra eşit bir kaynak tutar seçildiğini belirten bir ileti görüntüler.</span><span class="sxs-lookup"><span data-stu-id="780ba-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="780ba-116">Teklif alanında 'Yalnızca teklif' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="780ba-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="780ba-117">Tahsisatın genel muhasebe defterine nakledilmesinden önce Tahsisat günlüklerindeki sonucu isteğe bağlı olarak gözden geçirmek onaylamak için Yalnızca teklif öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="780ba-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="780ba-118">GM deftere nakil tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="780ba-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="780ba-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="780ba-119">Click OK.</span></span>
9. <span data-ttu-id="780ba-120">Genel muhasebe > Tahsisatlar > Tahsisat günlükleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="780ba-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="780ba-121">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="780ba-121">Click Lines.</span></span>
11. <span data-ttu-id="780ba-122">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="780ba-122">Click Post.</span></span>
12. <span data-ttu-id="780ba-123">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="780ba-123">Click Post.</span></span>


