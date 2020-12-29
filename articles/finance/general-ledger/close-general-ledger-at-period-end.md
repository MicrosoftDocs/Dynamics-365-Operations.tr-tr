---
title: Genel muhasebeyi dönemi sonunda kapatma
description: Bu konu, genellikle bir dönem kapanışı için genel muhasebe gerçekleştirirken tamamlanmış görevleri açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cabdce5e23704fbf12e631a138235174ebc5772
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448809"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="0ac1c-103">Genel muhasebeyi dönemi sonunda kapatma</span><span class="sxs-lookup"><span data-stu-id="0ac1c-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ac1c-104">Bu konu, genellikle bir dönem kapanışı için genel muhasebe gerçekleştirirken tamamlanmış görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="0ac1c-105">Genel muhasebede bir dönem veya bir yıl için kapatma prosedürlerini tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="0ac1c-106">Kapanış işlemleri, sistemi yeni bir dönem için hazırlar.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="0ac1c-107">Sistemi yeni yıl için hazırlamak için mutlaka yıl sonu kapanış işlemini yürütmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="0ac1c-108">Her kuruluşun farklı işlemleri ve bir dönemin sonu için gerçekleştirdiği adımları vardır.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="0ac1c-109">Dönem sonu için bazı isteğe bağlı adımlar şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0ac1c-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="0ac1c-110">Borç hesapları, Alacak hesapları ve Stok gibi tüm diğer modüler için tüm görevleri tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="0ac1c-111">Tüm günlüklerin nakledildiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="0ac1c-112">Gerçekleşmemiş kazanç veya kayıp tutarları üretmek için yabancı para biriminde yeniden değerleme çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="0ac1c-113">Her bir genel muhasebe hesabı için hareketleri kapatın.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="0ac1c-114">Gerekli tahsisatları işleyin.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-114">Process any required allocations.</span></span>
-   <span data-ttu-id="0ac1c-115">Dönem sonu ayarlamaları el ile nakledin.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="0ac1c-116">Hareketleri günlüğe aktarın ve **Genel muhasebe günlüğü** raporunu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="0ac1c-117">Bir konsolidasyon şirketini veya Mali raporlamayı kullanarak bir konsolidasyon gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="0ac1c-118">Mali raporlamayı kullanarak dönem sonu mali beyanları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="0ac1c-119">Genel muhasebe dönemlerini **Beklemede** konumuna ayarlayın, böylece daha fazla nakil oluşmaz.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="0ac1c-120">Ayrıca, daha iyi bir kontrol için, dönem sonu faaliyetleri gerçekleşirken bir dönemi bir özel kullanıcı grubuyla sınırlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="0ac1c-121">Kapatılmış bir dönemi yeniden açamayacağınızdan dönemleri **Kalıcı olarak kapalı** olarak ayarlamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="0ac1c-122">Mali dönem kapanış çalışma alanı, gerekli çeşitli dönem sonu işlemlerini organize etmek ve izlemek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="0ac1c-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="0ac1c-123">Daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="0ac1c-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="0ac1c-124">Mali dönem kapatma çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="0ac1c-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="0ac1c-125">Yıl sonu kapanışı</span><span class="sxs-lookup"><span data-stu-id="0ac1c-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="0ac1c-126">Toplu mali dönem kapatma</span><span class="sxs-lookup"><span data-stu-id="0ac1c-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




