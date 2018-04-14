---
title: "Genel muhasebe tahsisat kuralları"
description: "Bu makalede genel muhasebe atama kuralları hakkında bilgiler sağlanmıştır. Bu atama kurallarının çeşitli bileşenleri ve bunlar için kullanılabilecek atama yöntemleri açıklanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e5eb9d79fee7ec2e288db24aee9535d6414fdeed
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="0783c-104">Genel muhasebe tahsisat kuralları</span><span class="sxs-lookup"><span data-stu-id="0783c-104">Ledger allocation rules</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="0783c-105">Bu makalede genel muhasebe atama kuralları hakkında bilgiler sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0783c-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="0783c-106">Bu atama kurallarının çeşitli bileşenleri ve bunlar için kullanılabilecek atama yöntemleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0783c-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="0783c-107">Genel muhasebe tahsisat kuralları, otomatik olarak hesaplama yapmak ve sabit tutarların veya genel muhasebe bakiyelerinin tahsisatı için tahsisat günlükleri ve hesap girişleri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0783c-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="0783c-108">Tahsisat yöntemleri, değişken veya sabit olabilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="0783c-109">Aşağıdaki tahsisat yöntemleri genel muhasebe tahsisat kuralları için kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="0783c-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="0783c-110">**Temel** – Bu değişken yöntemi, tahsisat, filtre ölçütü temel alınarak fiili genel muhasebe bakiyesine bağlı olduğunda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0783c-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="0783c-111">Örneğin, reklamcılık giderleri tüm departman satışlarının toplam departman satışlarına oranına dayalı olarak tahsis edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="0783c-112">**Sabit yüzde** ve **Sabit ağırlık** – Bu yöntemler için, tahsisat yüzdesi veya ağırlığı doğrudan kural için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="0783c-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="0783c-113">Örneğin, reklam giderleri reklam giderlerinin yüzde 70'ini Departman A ve yüzde 30'unu Departman B alacak şekilde tahsis edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="0783c-114">**Eşit olarak** – Bu yöntem, tutarları tanımlanan her bir hedefe eşit olarak dağıtır.</span><span class="sxs-lookup"><span data-stu-id="0783c-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="0783c-115">Örneğin, Departman A ve Departman B için hedefler tanımlandıysa, reklam giderleri hem Departman A hem de Departman B giderlerin yüzde 50'sini alacak şekilde tahsis edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="0783c-116">Bir tahsisat kuralının tahsisat yöntemi olarak Temel kullanılırsa, başka bir temel genel muhasebe tahsisat kuralları da oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0783c-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="0783c-117">"Tahsisat talebini işleme koy" işlemi kullanıcıların genel muhasebe kuralını işleme almasını ve hesaplanmış tahsisatları deftere nakletmeden ya da silmeden önce ortaya çıkan günlük girişlerini önizlemelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0783c-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="0783c-118">Genel muhasebe tahsisat kuralları bileşenleri</span><span class="sxs-lookup"><span data-stu-id="0783c-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="0783c-119">Her tahsisat kuralının dört bileşenini vardır: Genel, kaynak, hedef ve mahsup.</span><span class="sxs-lookup"><span data-stu-id="0783c-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="0783c-120">Tahsisat yöntemi olarak Temel kullanılıyorsa, ek bir bileşen ve genel muhasebe tahsisat kuralları gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0783c-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="0783c-121">Her bir bileşen tahsisatları işleme almak için gerekli bilgilerin önemli bir kısmını sağlar.</span><span class="sxs-lookup"><span data-stu-id="0783c-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="0783c-122">**Genel** – Bu bileşen; tahsisat yöntemi, şirketlerarası kural ayarı ve kuralın etkin olup olmadığı gibi seçenekleri belirlediği yerdir.</span><span class="sxs-lookup"><span data-stu-id="0783c-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="0783c-123">**Kaynak** – Bu bileşen; kullanıcının tahsisat için veri kaynaklarını belirlediği yerdir.</span><span class="sxs-lookup"><span data-stu-id="0783c-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="0783c-124">Tahsisat, genel muhasebeye (**Veri kaynağı** =  **Genel muhasebe**) veya sabit tutarlara (**Veri kaynağı** =  **Sabit değer**) dayalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="0783c-125">**Veri kaynağı**, **Genel muhasebe** olarak ayarlandığında, kaynak filtresi ölçütünün genel muhasebe kuralı için (örneğin reklam giderleri için) tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0783c-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="0783c-126">**Hedef** – Bu bileşen, tahsisat sonucunun nasıl dağıtılacağını ve hesaplanacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0783c-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="0783c-127">Örneğin, her departman için bir hedef satır olabilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="0783c-128">**Mahsup** – Bu bileşen, ana hesapların ve boyutların bakiye hedef girişleri için nasıl belirlenmesi gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0783c-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="0783c-129">Kullanıcı tanımlı seçenekler genellikle kaynağa dayalı hesapların ve boyutların yerine kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0783c-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="0783c-130">**Veri kaynağı** **Sabit değer** olarak ayarlandığında, **Kaynak** bir seçenek olarak kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="0783c-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="0783c-131">**Temel genel muhasebe kuralları** – Bu kurallar, tahsisat için hangi genel muhasebe bakiyesinin (örneğin, departman başına gelir) kullanılması gerektiğini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0783c-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="0783c-132">Her bir genel tahsisat kuralı birden çok tahsisat kuralıyla birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0783c-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





