---
title: Deftere nakil tanımları
description: Bu makalede, nakil tanımları ve bu tanımların nasıl belirlenip bağlantı verildiği hakkında bilgiler verilmektedir. Desteklenen nakil türleri ve belgeler ile ilgili olarak, muhasebe girişlerindeki ana hesapları ve finansal boyutları sınıflandırmak için nakil profilleri yerine nakil tanımlarını kullanabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76bae24a975c922ea49ee2584e87cf43ccca61c7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180290"
---
# <a name="posting-definitions"></a><span data-ttu-id="e5053-104">Deftere nakil tanımları</span><span class="sxs-lookup"><span data-stu-id="e5053-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5053-105">Bu makalede, nakil tanımları ve bu tanımların nasıl belirlenip bağlantı verildiği hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e5053-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="e5053-106">Desteklenen nakil türleri ve belgeler ile ilgili olarak, muhasebe girişlerindeki ana hesapları ve finansal boyutları sınıflandırmak için nakil profilleri yerine nakil tanımlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="e5053-107">Desteklenen belgeleri ve nakil türlerini **İşlem nakil tanımları** sayfasında görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="e5053-108">Nakil tanımlarını kullanmaya başlatmak için **Genel muhasebe parametreleri** sayfasındaki **Nakil tanımlarını kullan** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="e5053-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="e5053-109">Nakil tanımlarını kullanıyor olsanız dahi, orijinal girişler ve desteklenmeyen nakil türleri ve belgeleri için nakil profillerini yine de mutlaka tanımlanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5053-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="e5053-110">Satın alma siparişleri için sorumluluk muhasebesini ve satın alma talepleri için ön sorumluluk muhasebesini etkinleştirmek için nakil tanımlarını kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="e5053-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="e5053-111">Nakil tanımlarının tanımlanması</span><span class="sxs-lookup"><span data-stu-id="e5053-111">Defining posting definitions</span></span>
<span data-ttu-id="e5053-112">Eşleşme kriterlerini belirlemek ve bir eşleşme meydana geldiğinde oluşturulması gereken girişleri tanımlamak için **Nakil tanımları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5053-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="e5053-113">Eşleştirme kriterleri, muhasebe dağıtımları olarak orijinal girişler için değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e5053-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="e5053-114">**Nakil tanımları** sayfasında ayrıca satırların değerlendirileceği siparişi kontrol etmek için giriş satırlarına öncelik numaraları da atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="e5053-115">En düşük öncelik numarasına sahip satırlar ilk olarak değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e5053-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="e5053-116">Örneğin, önceliği 1 olan tüm satırlar değerlendirilir ve ardından önceliği 2 olan satırlar değerlendirilir ve işlem bu şekilde devam eder.</span><span class="sxs-lookup"><span data-stu-id="e5053-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="e5053-117">Bir eşleşme bulunduğunda, diğer eşleştirme ölçütleri dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="e5053-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="e5053-118">Ayrıca, sadece grupta orijinal işlemle eşleşen kriterleri üretilen girişleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5053-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="e5053-119">**Nakil tanımını test et** sihirbazını kullanarak nakil tanımlarınızı doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="e5053-120">Bir nakil tanımı için bir örnek orijinal giriş tanımladıktan sonra oluşturulan girişleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e5053-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="e5053-121">Nakil tanımı sürülerini geçerlilik tarihleri ile birlikte kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="e5053-122">Örneğin, yeni bir mali yılda farklı bir muhasebe hesabına nakletmek üzere bir nakil tanımının gelecek bir sürümünü oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="e5053-123">İşlem türlerine nakil tanımları atamak için **İşlem nakil tanımları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5053-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="e5053-124">Nakil tanımlarının ilişkilendirilmesi</span><span class="sxs-lookup"><span data-stu-id="e5053-124">Linking posting definitions</span></span>
<span data-ttu-id="e5053-125">Nakil tanımları oluştururken bir nakil tanımını başka bir nakil tanımıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="e5053-126">İlişkilendirdiğiniz tanım için kriterler, mevcut nakil tanımına ait kriterlere ilave olarak düşünülür.</span><span class="sxs-lookup"><span data-stu-id="e5053-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="e5053-127">Bu özellik zaman kazandırır, çünkü başka bir tanım için halihazırda girdiğiniz için, **Nakil tanımları** sayfasında **Girişler** hızlı sekmesi altına kriterleri mevcut nakil tanımı için tekrar girmenize gerek kalmaz.</span><span class="sxs-lookup"><span data-stu-id="e5053-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="e5053-128">Şemalarda veya tablolarda kullanabilirsiniz tüm bağlantılar bulunur.</span><span class="sxs-lookup"><span data-stu-id="e5053-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="e5053-129">Mevcut nakil tanımı ile çakışmaları önlemek için ilişkilendirdiğiniz nakil tanımlarındaki satırların benzersiz olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e5053-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="e5053-130">Aşağıdaki kısıtlamalar, nakil tanımlarında bağlantılar oluştururken geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="e5053-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="e5053-131">Verilen nakil tanımı başka bir nakil tanımına veya başka bir nakil tanımından bağlanabilir, ancak her ikisi aynı anda gerçekleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="e5053-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="e5053-132">Ancak, bir nakil tanımı birden fazla nakil tanımına bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e5053-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="e5053-133">Bağlantıları sadece aynı modülde bulunan nakil tanımları arasında ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5053-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="e5053-134">Bir nakil tanımını herhangi bir işlem türüne atayabilirsiniz, ancak işlem türünün mutlaka nakil tanımıyla aynı modülde olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5053-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="e5053-135">Bir işlem türünün hangi modülde olduğunu görmek için **İşlem nakil tanımları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e5053-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="e5053-136">Daha fazla bilgi için bkz. [Deftere naik tanımı örnekleri](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e5053-136">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 


