---
title: Şirketlerarası planlama
description: Bu konu, şirketlerarası planlamayı açıklar ve Microsoft Dynamics 365 Supply Chain Management'taki Planlama İyileştirmesi ile şirketlerarası planlamayı nasıl yapılandıracağınızı açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672212"
---
# <a name="intercompany-planning"></a><span data-ttu-id="f98ba-103">Şirketlerarası planlama</span><span class="sxs-lookup"><span data-stu-id="f98ba-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f98ba-104">Lojistik işlemleri, bazı kuruluşlar için kuruluştaki diğer tüzel kişiliklere (şirketler) bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f98ba-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="f98ba-105">Bu işlemler, şirketlerarası satış ve satın alma işlemleri kullanılarak yönetildiğinden, her tüzel kişiliğin ayrı bir hesap planı vardır.</span><span class="sxs-lookup"><span data-stu-id="f98ba-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="f98ba-106">Bu konu, şirketlerarası planlamayı açıklar ve Microsoft Dynamics 365 Supply Chain Management'taki Planlama İyileştirmesi ile şirketlerarası planlamayı nasıl yapılandıracağınızı açıklar.</span><span class="sxs-lookup"><span data-stu-id="f98ba-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f98ba-107">Bu konu, aşağıdaki önemli şirketlerarası hükümleri kullanır:</span><span class="sxs-lookup"><span data-stu-id="f98ba-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="f98ba-108">**Yukarı akış**: Bir firma veya tedarik zincirindeki göreli bir başvurudur.</span><span class="sxs-lookup"><span data-stu-id="f98ba-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="f98ba-109">Ham madde tedarikçisi yönüne doğru hareketi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="f98ba-110">**Aşağı akış**: Bir firma veya tedarik zincirindeki göreli bir başvurudur.</span><span class="sxs-lookup"><span data-stu-id="f98ba-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="f98ba-111">Müşteri yönüne doğru hareketi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="f98ba-112">**Şirketlerarası planlı talep**: Bir aşağı akış şirketindeki ürünün planlı talebine göre bir şirketteki ürün için planlanan talep.</span><span class="sxs-lookup"><span data-stu-id="f98ba-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="f98ba-113">Master planlamada, bir şirketteki plan, başka bir şirketteki bir plandaki planlı siparişlerle ilgili planlı şirketlerarası talep içerebilir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="f98ba-114">Şirketler arasında planlı siparişlerde tam görünürlük sağladığından, bu özellikler faydalıdır.</span><span class="sxs-lookup"><span data-stu-id="f98ba-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="f98ba-115">Ayrıca, planlı siparişlerin şirketlerarası talep için kesinleştirilmesini gerektirmeden, gerekli tüm planlı tedarik emirlerinin oluşturulmasını da sağlar.</span><span class="sxs-lookup"><span data-stu-id="f98ba-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="f98ba-116">Master planlamayı planlı aşağı akış talebini içeren bir ana plandan çalıştırırsanız, ilgili şirketlerarası satıcılardan planlı satın alma siparişleri talep olarak plana dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="f98ba-117">Gerekli kurulum</span><span class="sxs-lookup"><span data-stu-id="f98ba-117">Required setup</span></span>

<span data-ttu-id="f98ba-118">Şirketlerarası planlamayı kullanmak için sisteminizi aşağıdaki şekilde hazırlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="f98ba-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="f98ba-119">İlgili ürünlerin ilgili tüm şirketlerde serbest bırakılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="f98ba-120">Daha fazla bilgi için bkz. Microsoft Learn'deki [Dynamics 365 Supply Chain Management'ta şirketlerarası ticareti yapılandırma ve kullanma](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).</span><span class="sxs-lookup"><span data-stu-id="f98ba-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="f98ba-121">Aşağı akış talebi, yukarı akış şirketi ve müşterinin ilgili varsayılan stok boyutlarına (tesis ve ambar) şirketlerarası ilşikisi olan bir satıcıdan yapılan satın almalarla kapsanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f98ba-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="f98ba-122">Daha fazla bilgi için bkz. Microsoft Learn'deki [Dynamics 365 Supply Chain Management'ta şirketlerarası ticareti yapılandırma ve kullanma](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).</span><span class="sxs-lookup"><span data-stu-id="f98ba-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="f98ba-123">Yukarı akış şirketindeki master plan, planlanan aşağı akış talebini içermeli ve ilgili şirket ile master plan, aşağı akış planlarında belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="f98ba-124">Çıkıştaki planlanan talebi ekle</span><span class="sxs-lookup"><span data-stu-id="f98ba-124">Include planned downstream demand</span></span>

<span data-ttu-id="f98ba-125">Master planınızı planlanan aşağı akış talebini içerecek şekilde yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f98ba-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="f98ba-126">**Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="f98ba-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="f98ba-127">Bir master plan seçin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f98ba-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="f98ba-128">**Şirketlerarası planlama** hızlı sekmesinde, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="f98ba-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="f98ba-129">**Planlanan aşağı akış talebini dahil et**: Master plan için şirketlerarası planlamayı etkinleştirmek üzere bu seçeneği *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f98ba-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="f98ba-130">**Aşağı akış planları**: **Planlanan aşağı akış talebini dahil et** seçeneğini *Evet* olarak ayarlarsanız diğer şirketlerdeki istediğiniz master planları eklemek için araç çubuğunu ve kılavuzu kullanın.</span><span class="sxs-lookup"><span data-stu-id="f98ba-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="f98ba-131">Çok düzeyli bir ilişkilendirme kullanarak şirketler arasında ilişkilendirme yapma</span><span class="sxs-lookup"><span data-stu-id="f98ba-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="f98ba-132">Çok düzeyli bir ilişkilendirmede, arz ile kapsanmakta olan talebin ilk kaynağını görmek için şirketler arasındaki ilişkilendirmeyi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f98ba-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="f98ba-133">Çok düzeyli bilgileri görüntülemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f98ba-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="f98ba-134">**Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f98ba-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="f98ba-135">Planlanan bir sipariş seçin veya açın.</span><span class="sxs-lookup"><span data-stu-id="f98ba-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="f98ba-136">Eylem Bölmesinde **Görünüm** sekmesinde **Gereklilikler** grubunda **Çok düzeyli ilişkilendirme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f98ba-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="f98ba-137">İki şirket içeren şirketlerarası ilişki örneği</span><span class="sxs-lookup"><span data-stu-id="f98ba-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="f98ba-138">Bu örnekte, USMF şirketinde DEMF şirketindeki bir satış siparişini kapsayacak bir planlanan üretim emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f98ba-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="f98ba-139">USMF'de, doğrudan talep, planlanan şirketlerarası taleptir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="f98ba-140">Bu talebin USMF'de görünmesini sağlamak için önce DEMF ve sonra USMF'de master planlama çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="f98ba-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="f98ba-141">Aşağıdaki şekil, bu örneğin planlanan üretim emri için **Çok düzeyli bir ilişkilendirme** sayfasında nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![İki şirket içeren şirketlerarası ilişki örneği](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="f98ba-143">Üç şirket içeren şirketlerarası ilişki örneği</span><span class="sxs-lookup"><span data-stu-id="f98ba-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="f98ba-144">Bu örnekte, USMF şirketinde FRRT şirketindeki bir satış siparişini kapsayacak bir planlanan satın alma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f98ba-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="f98ba-145">DEMF ve USMF şirketlerinde, doğrudan talep, planlanan şirketlerarası taleptir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="f98ba-146">Bu talebin USMF'de görünmesini sağlamak için önce FRRT ve sonra DEMF'de ve son olarak USMF'de master planlama çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="f98ba-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="f98ba-147">Aşağıdaki şekil, bu örneğin planlanan üretim emri için **Çok düzeyli bir ilişkilendirme** sayfasında nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f98ba-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Üç şirket içeren şirketlerarası ilişki örneği](media/IntercompanyPlanning2.png)
