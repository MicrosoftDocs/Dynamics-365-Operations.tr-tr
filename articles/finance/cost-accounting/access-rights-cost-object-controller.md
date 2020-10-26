---
title: Maliyet nesnesi denetleyicilerinin erişim hakları
description: Bu konu, maliyet nesnesi denetleyicileri için erişim hakları hakkında bilgi sağlar.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fd1ed875e5c6e3f8ada3b13ea8cc05f98526691d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977755"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="1953a-103">Maliyet nesnesi denetleyicilerinin erişim hakları</span><span class="sxs-lookup"><span data-stu-id="1953a-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1953a-104">**Maliyet kontrolü** çalışma alanı, yöneticilerin maliyet nesnelerinin performanslarını görüntüleyebilecekleri merkezi noktadır.</span><span class="sxs-lookup"><span data-stu-id="1953a-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="1953a-105">Bu çalışma alanı, yöneticilerin Maliyet muhasebesi verisini, maliyet muhasebecisi olmasalar bile kullanmalarına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="1953a-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="1953a-106">Güvenlik nedeniyle, yöneticiler yalnızca sorumlu oldukları belirli maliyet nesnelerinin Maliyet muhasebesi verilerini görmelidirler.</span><span class="sxs-lookup"><span data-stu-id="1953a-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="1953a-107">Maliyet muhasebesinde dört benzersiz rol vardır.</span><span class="sxs-lookup"><span data-stu-id="1953a-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="1953a-108">Rol adı</span><span class="sxs-lookup"><span data-stu-id="1953a-108">Role name</span></span>               | <span data-ttu-id="1953a-109">Lisans</span><span class="sxs-lookup"><span data-stu-id="1953a-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="1953a-110">Maliyet muhasebesi yöneticisi</span><span class="sxs-lookup"><span data-stu-id="1953a-110">Cost accounting manager</span></span> | <span data-ttu-id="1953a-111">Faaliyet</span><span class="sxs-lookup"><span data-stu-id="1953a-111">Activity</span></span>     |
| <span data-ttu-id="1953a-112">Maliyet muhasebecisi</span><span class="sxs-lookup"><span data-stu-id="1953a-112">Cost accountant</span></span>         | <span data-ttu-id="1953a-113">Operations</span><span class="sxs-lookup"><span data-stu-id="1953a-113">Operations</span></span>   |
| <span data-ttu-id="1953a-114">Maliyet muhasebe memuru</span><span class="sxs-lookup"><span data-stu-id="1953a-114">Cost accountant clerk</span></span>   | <span data-ttu-id="1953a-115">Operations</span><span class="sxs-lookup"><span data-stu-id="1953a-115">Operations</span></span>   |
| <span data-ttu-id="1953a-116">Maliyet nesnesi denetleyicisi</span><span class="sxs-lookup"><span data-stu-id="1953a-116">Cost object controller</span></span>  | <span data-ttu-id="1953a-117">Takım üyeleri</span><span class="sxs-lookup"><span data-stu-id="1953a-117">Team members</span></span> |

<span data-ttu-id="1953a-118">Bu konu, **Maliyet nesnesi denetleyicisi** rolünü bir yöneticiye atamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="1953a-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="1953a-119">**Maliyet nesnesi denetleyicisi** rolü bir yöneticiye atandığı, yönetici aşağıdaki görevleri yerine getirebilir:</span><span class="sxs-lookup"><span data-stu-id="1953a-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="1953a-120">**Maliyet denetimi** çalışma alanına erişmek (istemci içinde).</span><span class="sxs-lookup"><span data-stu-id="1953a-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="1953a-121">Ayrıntıya inme deneyimini destekleyen sayfalarda ayrıntıya inme ve erişim sağlama.</span><span class="sxs-lookup"><span data-stu-id="1953a-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="1953a-122">**Maliyet denetimi** çalışma alanına erişmek (mobil uygulamada).</span><span class="sxs-lookup"><span data-stu-id="1953a-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="1953a-123">**Maliyet nesnesi denetçisi** rolü, kullanıcının hangi maliyet nesnesine erişebileceğini ve görünümüne sahip olacağını denetlemez.</span><span class="sxs-lookup"><span data-stu-id="1953a-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="1953a-124">Satır düzeyi güvenlik, boyut hiyerarşileri ve Erişim listesi hiyerarşisi tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="1953a-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="1953a-125">Erişim haklarını verme</span><span class="sxs-lookup"><span data-stu-id="1953a-125">Grant access rights</span></span>
<span data-ttu-id="1953a-126">Aşağıdaki örnek, bir boyut hiyerarşisinin nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1953a-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="1953a-127">**Boyut hiyerarşisi ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="1953a-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="1953a-128">Boyut hiyerarşisi adı</span><span class="sxs-lookup"><span data-stu-id="1953a-128">Dimension hierarchy name</span></span> | <span data-ttu-id="1953a-129">Boyut</span><span class="sxs-lookup"><span data-stu-id="1953a-129">Dimension</span></span>    | <span data-ttu-id="1953a-130">Boyut hiyerarşisi türü adı</span><span class="sxs-lookup"><span data-stu-id="1953a-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="1953a-131">Erişim listesi hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="1953a-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="1953a-132">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="1953a-132">Organization</span></span>             | <span data-ttu-id="1953a-133">Maliyet merkezleri</span><span class="sxs-lookup"><span data-stu-id="1953a-133">Cost centers</span></span> | <span data-ttu-id="1953a-134">Boyut sınıflandırması hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="1953a-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="1953a-135">**Evet**</span><span class="sxs-lookup"><span data-stu-id="1953a-135">**Yes**</span></span>               |

<span data-ttu-id="1953a-136">Her bir düğüme bir veya birden fazla kullanıcı kimliği eklemek için hiyerarşi tasarımcısındaki **Kullanıcılar** hızlı sekmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1953a-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="1953a-137">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="1953a-137">Users</span></span>            | <span data-ttu-id="1953a-138">Boyut üyesi aralıkları</span><span class="sxs-lookup"><span data-stu-id="1953a-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="1953a-139">**Düğümler**</span><span class="sxs-lookup"><span data-stu-id="1953a-139">**Nodes**</span></span>                         | <span data-ttu-id="1953a-140">**Kullanıcı Kimliği**</span><span class="sxs-lookup"><span data-stu-id="1953a-140">**User ID**</span></span>      | <span data-ttu-id="1953a-141">**Kaynak boyut üyesi**</span><span class="sxs-lookup"><span data-stu-id="1953a-141">**From dimension member**</span></span> | <span data-ttu-id="1953a-142">**Hedef boyut üyesi**</span><span class="sxs-lookup"><span data-stu-id="1953a-142">**To dimension member**</span></span> |
| <span data-ttu-id="1953a-143">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="1953a-143">Organization</span></span>                      | <span data-ttu-id="1953a-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="1953a-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="1953a-145">&nbsp;&nbsp;Yönetici</span><span class="sxs-lookup"><span data-stu-id="1953a-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="1953a-146">Nisan</span><span class="sxs-lookup"><span data-stu-id="1953a-146">April</span></span>            |                           |                         |
| <span data-ttu-id="1953a-147">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="1953a-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="1953a-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="1953a-148">Alicia</span></span>           | <span data-ttu-id="1953a-149">CC002</span><span class="sxs-lookup"><span data-stu-id="1953a-149">CC002</span></span>                     | <span data-ttu-id="1953a-150">CC003</span><span class="sxs-lookup"><span data-stu-id="1953a-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="1953a-151">CC007</span><span class="sxs-lookup"><span data-stu-id="1953a-151">CC007</span></span>                     | <span data-ttu-id="1953a-152">CC007</span><span class="sxs-lookup"><span data-stu-id="1953a-152">CC007</span></span>                   |
| <span data-ttu-id="1953a-153">&nbsp;&nbsp;&nbsp;&nbsp;İK</span><span class="sxs-lookup"><span data-stu-id="1953a-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="1953a-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="1953a-154">Arnie</span></span>            | <span data-ttu-id="1953a-155">CC001</span><span class="sxs-lookup"><span data-stu-id="1953a-155">CC001</span></span>                     | <span data-ttu-id="1953a-156">CC001</span><span class="sxs-lookup"><span data-stu-id="1953a-156">CC001</span></span>                   |
| <span data-ttu-id="1953a-157">&nbsp;&nbsp;Üretim</span><span class="sxs-lookup"><span data-stu-id="1953a-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="1953a-158">David</span><span class="sxs-lookup"><span data-stu-id="1953a-158">David</span></span>            |                           |                         |
| <span data-ttu-id="1953a-159">&nbsp;&nbsp;&nbsp;&nbsp;Paketleme</span><span class="sxs-lookup"><span data-stu-id="1953a-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="1953a-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="1953a-160">Ellen</span></span>            | <span data-ttu-id="1953a-161">CC005</span><span class="sxs-lookup"><span data-stu-id="1953a-161">CC005</span></span>                     | <span data-ttu-id="1953a-162">CC005</span><span class="sxs-lookup"><span data-stu-id="1953a-162">CC005</span></span>                   |
| <span data-ttu-id="1953a-163">&nbsp;&nbsp;&nbsp;&nbsp;Montaj</span><span class="sxs-lookup"><span data-stu-id="1953a-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="1953a-164">Chris</span><span class="sxs-lookup"><span data-stu-id="1953a-164">Chris</span></span>            | <span data-ttu-id="1953a-165">CC006</span><span class="sxs-lookup"><span data-stu-id="1953a-165">CC006</span></span>                     | <span data-ttu-id="1953a-166">CC006</span><span class="sxs-lookup"><span data-stu-id="1953a-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="1953a-167">Maliyet muhasebesindeki tüm girişleri görebilmeleri için maliyet muhasebecileri, hiyerarşinin en üst düzeyine atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1953a-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="1953a-168">Erişim listesi hiyerarşisi ve güvenlik ayarları uygulanabilmeden önce, **Maliyet nesnesi boyut üyelerini görüntüleme erişimini etkinleştir** seçeneği, **Maliyet muhasebesi parametreleri** sayfasında **Genel** sekmesi üzerinde **Evet** olarak ayarlanmalıdır (**Maliyet muhasebesi** > **Kurulum** > **Parametreler**).</span><span class="sxs-lookup"><span data-stu-id="1953a-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="1953a-169">Erişim listesi hiyerarşisi için ayarlar, aşağıdaki alanlarda gösterilen veriyi denetlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="1953a-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="1953a-170">**Maliyet kontrolü** çalışma alanı (istemci içinde):</span><span class="sxs-lookup"><span data-stu-id="1953a-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="1953a-171">Sayfalardaki veri ayrıntıya inme için kullanılır</span><span class="sxs-lookup"><span data-stu-id="1953a-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="1953a-172">**Maliyet kontrolü** çalışma alanı (mobil uygulama içinde):</span><span class="sxs-lookup"><span data-stu-id="1953a-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="1953a-173">Kartlardaki bakiyeler</span><span class="sxs-lookup"><span data-stu-id="1953a-173">Balances in cards</span></span>

- <span data-ttu-id="1953a-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="1953a-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="1953a-175">Veri, Power BI görselleştirmeleri içinde gösterilir</span><span class="sxs-lookup"><span data-stu-id="1953a-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="1953a-176">Dynamics 365 Finance istemcisine içine katıştırılmış veri Power BI görselleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="1953a-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="1953a-177">Erişim listesi hiyerarşisi Power BI içerisindeki veriyi etkileyebilmeden önce, Power BI içindeki Erişim listesi hiyerarşisi ve satır düzeyi güvenliği eşleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1953a-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="1953a-178">Daha fazla bilgi için bkz [Maliyet muhasebesi İçerik Paketi için güvenlik kurma](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="1953a-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="1953a-179">Bu konu, **Maliyet kontrolü** çalışma alanını kullanmadan önce ayarlanması gereken önkoşulları gösterir.</span><span class="sxs-lookup"><span data-stu-id="1953a-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="1953a-180">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1953a-180">Additional resources</span></span>

- [<span data-ttu-id="1953a-181">Maliyet kontrolü çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="1953a-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="1953a-182">Boyut hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="1953a-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="1953a-183">Maliyet muhasebesi içerik paketi için güvenliği kurmak</span><span class="sxs-lookup"><span data-stu-id="1953a-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
