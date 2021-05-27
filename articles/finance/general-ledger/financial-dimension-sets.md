---
title: Mali boyut kümeleri
description: Bu konu, finansal boyut kümelerini açıklar ve kullanımlarını en iyi duruma getirmek için bazı ipuçları sağlar.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021840"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="c6ff8-103">Mali boyut kümeleri</span><span class="sxs-lookup"><span data-stu-id="c6ff8-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6ff8-104">Bu konu, finansal boyut kümelerini açıklar ve kullanımlarını en iyi duruma getirmek için bazı ipuçları sağlar.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="c6ff8-105">Boyut kümesi, kullanıcı tanımlı bir şekilde Genel muhasebe verilerini özetlemek için kullanılabilen finansal boyutların sıralı bir listesidir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="c6ff8-106">Boyut kümelerinin birincil kullanımı mizan tanımlamaktır.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="c6ff8-107">Tek standart boyut kümesi yalnızca ana hesabı içeren boyut kümesidir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="c6ff8-108">**Mali boyut kümeleri** sayfası, finansal boyut kümeleri oluşturmak ve bunları yönetmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="c6ff8-109">Boyut kümesi bakiyeleri</span><span class="sxs-lookup"><span data-stu-id="c6ff8-109">Dimension set balances</span></span>

<span data-ttu-id="c6ff8-110">Boyut kümesinde, mali boyutlarına dayalı bakiyeler olabilir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="c6ff8-111">Bakiyeler Genel muhasebede bulunur ve boyut kümesi tanımını temel alır.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="c6ff8-112">Bakiyeler, alındıklarında (örneğin, bir mizan oluşturulduğunda) performansı artırmaya yardımcı olmak için Genel muhasebe verilerinden özetlenir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="c6ff8-113">Bakiyeleri oluştur</span><span class="sxs-lookup"><span data-stu-id="c6ff8-113">Create balances</span></span>

<span data-ttu-id="c6ff8-114">Henüz bakiyesi olmayan bir boyut kümesinin bakiyelerini başlatmak için **Bakiyeleri oluştur** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="c6ff8-115">Bakiye güncelleştirmeleri tüm Genel muhasebe deftere nakil faaliyetlerini etkilediğinden, bakiyeleri olan boyut kümeleri sayısını sınırlandırmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="c6ff8-116">Bakiyeleri güncelleştir</span><span class="sxs-lookup"><span data-stu-id="c6ff8-116">Update balances</span></span>

<span data-ttu-id="c6ff8-117">Bakiyelere en son Genel muhasebe deftere nakil faaliyetini dahil etmek için **Bakiyeleri güncelleştir** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="c6ff8-118">Bakiye güncelleştirmeleri hafif işlemlerdir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-118">Balance updates are light operations.</span></span> <span data-ttu-id="c6ff8-119">Bunlar yalnızca son güncelleştirmeden bu yana gerçekleşen Genel muhasebe deftere nakil etkinliğini işlemelidir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="c6ff8-120">Mizan görüntüleme gösterilen bakiyelerin güncel olmasını sağlamak üzere güncelleştirme yapmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="c6ff8-121">En sık kullanılan boyut kümelerinde yapılan güncelleştirmelerin hızlı olması için, tekrarlayan bir toplu iş kullanmayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="c6ff8-122">Bu şekilde, kullanıcıların deneme mizanı için beklemesi gereken zamanı en aza indirmeye yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="c6ff8-123">Bakiyeleri yeniden yapılandır</span><span class="sxs-lookup"><span data-stu-id="c6ff8-123">Rebuild balances</span></span>

<span data-ttu-id="c6ff8-124">Bakiyeleri sıfırdan oluşturmak için **Bakiyeleri yeniden oluştur** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="c6ff8-125">Bu şekilde, bunların Genel muhasebedeki verilerle eşleşmesini sağlamaya yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="c6ff8-126">Bakiyeleri yeniden oluşturma işlemi birçok işlem gerektirir ve genellikle gerekli olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="c6ff8-127">Bakiyeleri düzenli olarak yeniden oluşturmaya gerek duyan bir senaryonuz varsa, müşteri desteğine başvurmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="c6ff8-128">Müşteri desteği, bakiyelerin Genel muhasebedeki verilerle neden eşleşmediğini belirlemenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="c6ff8-129">Bakiyeleri temizle</span><span class="sxs-lookup"><span data-stu-id="c6ff8-129">Clear balances</span></span>

<span data-ttu-id="c6ff8-130">Bakiyeleri kaldırmak ve diğer güncelleştirmeleri durdurmak için **Bakiyeleri temizle** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="c6ff8-131">Boyut kümesinin artık Genel muhasebe deftere nakil faaliyetleri üzerinde bir etkisi olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="c6ff8-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="c6ff8-132">Daha fazla bilgi için bkz. [Mali boyutlar](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="c6ff8-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
