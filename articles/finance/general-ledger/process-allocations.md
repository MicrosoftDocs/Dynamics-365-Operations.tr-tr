---
title: Tahsisatları işleme
description: Bu makalede tahsisatlar, Microsoft Dynamics 365 Finance'te tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgi verilmektedir. Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır. Gelir ve giderlerin muhasebede doğru nesneye yazılmasını sağlamaya yardımcı olurlar.
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
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13496e764f907201a23f0dd6772ee22efffb250
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204990"
---
# <a name="process-allocations"></a><span data-ttu-id="0aec5-105">Tahsisatları işleme</span><span class="sxs-lookup"><span data-stu-id="0aec5-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aec5-106">Bu makalede tahsisatlar, tahsisatları işleme seçenekleri ve bütçe planlamasında tahsisatların nasıl kullanılabileceği hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0aec5-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="0aec5-107">Tahsisatlar, tutarları birden fazla genel muhasebe hesabı birleşimleri arasında dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0aec5-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="0aec5-108">Gelir ve giderlerin muhasebede doğru nesneye yazılmasını sağlamaya yardımcı olurlar.</span><span class="sxs-lookup"><span data-stu-id="0aec5-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="0aec5-109">Aşağıdaki özellikler bu işlemi destekler:</span><span class="sxs-lookup"><span data-stu-id="0aec5-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="0aec5-110">Muhasebe dağılımlarında Böl eylemini kullanarak veya bir belgeye mali boyut varsayılan şablonları uygulayarak hareket tutarlarını el ile atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0aec5-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="0aec5-111">Daha fazla bilgi için bkz. [Muhasebe dağılımları](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="0aec5-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="0aec5-112">Her bir ana hesapta tanımlanan atama şartlarına dayalı olarak hareket tutarlarını otomatik olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="0aec5-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="0aec5-113">Tahsisat hesabı girişleri, bir muhasebe girişinin kaynak defter hesabı olarak tanımlanan kriterleri karşılaması durumunda her bir günlük için yüzdeye ve hedef defter hesabına dayalı olarak üretilecektir.</span><span class="sxs-lookup"><span data-stu-id="0aec5-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="0aec5-114">Daha fazla bilgi için bkz. [Ana hesap tahsisat koşulları](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="0aec5-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="0aec5-115">Defter bakiyelerini veya sabit tutarları defter tahsisat kurallarına dayalı olarak otomatik olarak atayın.</span><span class="sxs-lookup"><span data-stu-id="0aec5-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="0aec5-116">Defter tahsisat kuralları, atama günlükleri kullanılarak düzenli olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="0aec5-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="0aec5-117">Daha fazla bilgi için bkz. [Tahsisat kuralları](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="0aec5-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="0aec5-118">Bütçe planlamasında tahsisatlar</span><span class="sxs-lookup"><span data-stu-id="0aec5-118">Allocations in budget planning</span></span>

<span data-ttu-id="0aec5-119">Defter tahsisat kuralları, bütçe planları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0aec5-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="0aec5-120">Defter tahsisat kurallarını bütçe planlamada kullanıyorsanız, tahsisat kuralları, defterdekiyle aynı şekilde çalışacaktır, ancak kaynak verileri ve hedef verileri bütçe planından gelir.</span><span class="sxs-lookup"><span data-stu-id="0aec5-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="0aec5-121">Bütçe planları için kullanılacak genel muhasebe tahsisat kurallarını el ile seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0aec5-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="0aec5-122">Alternatif olarak, bir iş akışı işleminin bir parçası olarak çalışan bir tahsisat zamanlaması kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0aec5-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="0aec5-123">Bütçe planlama için şirketler arası defter tahsisat kurallarını kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="0aec5-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]