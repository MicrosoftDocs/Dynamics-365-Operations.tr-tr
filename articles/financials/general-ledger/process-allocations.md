---
title: Tahsisatları işleme
description: Bu makalede tahsisatlar, Microsoft Dynamics 365 for Finance and Operations'te tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgiler verilmektedir. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gider ve gelirlerin muhasebede doğru nesneye yazılmasının garanti altına alınmasına yardımcı olurlar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a1946875460e9dfafb481b288a6d6a10ba8931d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846811"
---
# <a name="process-allocations"></a><span data-ttu-id="ffbc1-105">Tahsisatları işleme</span><span class="sxs-lookup"><span data-stu-id="ffbc1-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffbc1-106">Bu makalede tahsisatlar, Microsoft Dynamics 365 for Finance and Operations'te tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, and how they can be used in budget planning.</span></span> <span data-ttu-id="ffbc1-107">Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="ffbc1-108">Gider ve gelirlerin muhasebede doğru nesneye yazılmasının garanti altına alınmasına yardımcı olurlar.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="ffbc1-109">Microsoft Dynamics 365 for Finance and Operations bu süreci desteklemek için şu özellikleri sağlar:</span><span class="sxs-lookup"><span data-stu-id="ffbc1-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="ffbc1-110">Muhasebe dağılımlarında Böl eylemini kullanarak veya bir belgeye mali boyut varsayılan şablonları uygulayarak hareket tutarlarını el ile atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="ffbc1-111">Daha fazla bilgi için bkz.  [Hesap dağıtımları.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="ffbc1-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="ffbc1-112">Her bir ana hesapta tanımlanan atama şartlarına dayalı olarak hareket tutarlarını otomatik olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="ffbc1-113">Tahsisat hesabı girişleri, bir muhasebe girişinin kaynak defter hesabı olarak tanımlanan kriterleri karşılaması durumunda her bir günlük için yüzdeye ve hedef defter hesabına dayalı olarak üretilecektir.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="ffbc1-114">Defter bakiyelerini veya sabit tutarları defter tahsisat kurallarına dayalı olarak otomatik olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="ffbc1-115">Defter tahsisat kuralları, atama günlükleri kullanılarak düzenli olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="ffbc1-116">Bütçe planlamasında tahsisatlar</span><span class="sxs-lookup"><span data-stu-id="ffbc1-116">Allocations in budget planning</span></span>

<span data-ttu-id="ffbc1-117">Defter tahsisat kuralları, bütçe planları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="ffbc1-118">Defter tahsisat kurallarını bütçe planlamada kullanıyorsanız, tahsisat kuralları, defterdekiyle aynı şekilde çalışacaktır, ancak kaynak verileri ve hedef verileri bütçe planından gelir.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="ffbc1-119">Bütçe planları için kullanılacak genel muhasebe tahsisat kurallarını el ile seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="ffbc1-120">Alternatif olarak, bir iş akışı işleminin bir parçası olarak çalışan bir tahsisat zamanlaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="ffbc1-121">Bütçe planlama için şirketler arası defter tahsisat kurallarını kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="ffbc1-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>





