---
title: "Tahsisatları işleme"
description: "Bu makale; tahsisatlar, Microsoft Dynamics 365 for Finance and Operations'ta tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgiler sağlar. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gider ve gelirlerin muhasebede doğru nesneye yazılmasının garanti altına alınmasına yardımcı olurlar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 70e6c17b5c7e38c2f9f7a5087175e7cfd2e5542a
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="process-allocations"></a><span data-ttu-id="5ef3c-105">Tahsisatları işleme</span><span class="sxs-lookup"><span data-stu-id="5ef3c-105">Process allocations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="5ef3c-106">Bu makale; tahsisatlar, Microsoft Dynamics 365 for Finance and Operations'ta tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, and how they can be used in budget planning.</span></span> <span data-ttu-id="5ef3c-107">Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="5ef3c-108">Gider ve gelirlerin muhasebede doğru nesneye yazılmasının garanti altına alınmasına yardımcı olurlar.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="5ef3c-109">Microsoft Dynamics 365 for Finance and Operations bu süreci desteklemek için şu özellikleri sağlar:</span><span class="sxs-lookup"><span data-stu-id="5ef3c-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="5ef3c-110">Muhasebe dağılımlarında Böl eylemini kullanarak veya bir belgeye mali boyut varsayılan şablonları uygulayarak hareket tutarlarını el ile atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="5ef3c-111">Daha fazla bilgi için bkz.  [Hesap dağıtımları.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="5ef3c-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="5ef3c-112">Her bir ana hesapta tanımlanan atama şartlarına dayalı olarak hareket tutarlarını otomatik olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="5ef3c-113">Tahsisat hesabı girişleri, bir muhasebe girişinin kaynak defter hesabı olarak tanımlanan kriterleri karşılaması durumunda her bir günlük için yüzdeye ve hedef defter hesabına dayalı olarak üretilecektir.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="5ef3c-114">Defter bakiyelerini veya sabit tutarları defter tahsisat kurallarına dayalı olarak otomatik olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="5ef3c-115">Defter tahsisat kuralları, atama günlükleri kullanılarak düzenli olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="5ef3c-116">Bütçe planlamasında tahsisatlar</span><span class="sxs-lookup"><span data-stu-id="5ef3c-116">Allocations in budget planning</span></span>

<span data-ttu-id="5ef3c-117">Defter tahsisat kuralları, bütçe planları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="5ef3c-118">Defter tahsisat kurallarını bütçe planlamada kullanıyorsanız, tahsisat kuralları, defterdekiyle aynı şekilde çalışacaktır, ancak kaynak verileri ve hedef verileri bütçe planından gelir.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="5ef3c-119">Bütçe planları için kullanılacak genel muhasebe tahsisat kurallarını el ile seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="5ef3c-120">Alternatif olarak, bir iş akışı işleminin bir parçası olarak çalışan bir tahsisat zamanlaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="5ef3c-121">Bütçe planlama için şirketler arası defter tahsisat kurallarını kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="5ef3c-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






