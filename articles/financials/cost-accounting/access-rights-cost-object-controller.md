---
title: "Maliyet nesnesi denetleyicilerinin erişim haklarını tanımlama"
description: "Bu konu, maliyet nesnesi denetleyicileri için erişim hakları hakkında bilgi sağlar."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2ba38ddc5c717df29462e4316dc5045d0eef8c1a
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="551f1-103">Bir maliyet nesnesi denetleyicisinin erişim hakları</span><span class="sxs-lookup"><span data-stu-id="551f1-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="551f1-104">**Maliyet kontrolü** çalışma alanı, yöneticilerin maliyet nesnelerinin performanslarını görüntüleyebilecekleri merkezi noktadır.</span><span class="sxs-lookup"><span data-stu-id="551f1-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="551f1-105">Bu çalışma alanı, yöneticilerin Maliyet muhasebesi verisini, maliyet muhasebecisi olmasalar bile kullanmalarına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="551f1-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="551f1-106">Güvenlik nedeniyle, yöneticiler yalnızca sorumlu oldukları belirli maliyet nesnelerinin Maliyet muhasebesi verilerini görmelidirler.</span><span class="sxs-lookup"><span data-stu-id="551f1-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="551f1-107">Maliyet muhasebesinde dört benzersiz rol vardır.</span><span class="sxs-lookup"><span data-stu-id="551f1-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="551f1-108">Rol adı</span><span class="sxs-lookup"><span data-stu-id="551f1-108">Role name</span></span>               | <span data-ttu-id="551f1-109">Lisans</span><span class="sxs-lookup"><span data-stu-id="551f1-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="551f1-110">Maliyet muhasebesi yöneticisi</span><span class="sxs-lookup"><span data-stu-id="551f1-110">Cost accounting manager</span></span> | <span data-ttu-id="551f1-111">Faaliyet</span><span class="sxs-lookup"><span data-stu-id="551f1-111">Activity</span></span>     |
| <span data-ttu-id="551f1-112">Maliyet muhasebecisi</span><span class="sxs-lookup"><span data-stu-id="551f1-112">Cost accountant</span></span>         | <span data-ttu-id="551f1-113">Operations</span><span class="sxs-lookup"><span data-stu-id="551f1-113">Operations</span></span>   |
| <span data-ttu-id="551f1-114">Maliyet muhasebe memuru</span><span class="sxs-lookup"><span data-stu-id="551f1-114">Cost accountant clerk</span></span>   | <span data-ttu-id="551f1-115">Operations</span><span class="sxs-lookup"><span data-stu-id="551f1-115">Operations</span></span>   |
| <span data-ttu-id="551f1-116">Maliyet nesnesi denetleyicisi</span><span class="sxs-lookup"><span data-stu-id="551f1-116">Cost object controller</span></span>  | <span data-ttu-id="551f1-117">Takım üyeleri</span><span class="sxs-lookup"><span data-stu-id="551f1-117">Team members</span></span> |

<span data-ttu-id="551f1-118">Bu konu, **Maliyet nesnesi denetleyicisi** rolünü bir yöneticiye atamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="551f1-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="551f1-119">**Maliyet nesnesi denetleyicisi** rolü bir yöneticiye atandığı, yönetici aşağıdaki görevleri yerine getirebilir:</span><span class="sxs-lookup"><span data-stu-id="551f1-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="551f1-120">**Maliyet denetimi** çalışma alanına erişmek (istemci içinde).</span><span class="sxs-lookup"><span data-stu-id="551f1-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="551f1-121">Ayrıntıya inme deneyimini destekleyen sayfalarda ayrıntıya inme ve erişim sağlama.</span><span class="sxs-lookup"><span data-stu-id="551f1-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="551f1-122">**Maliyet denetimi** çalışma alanına erişmek (mobil uygulamada).</span><span class="sxs-lookup"><span data-stu-id="551f1-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="551f1-123">**Maliyet nesnesi denetçisi** rolü, kullanıcının hangi maliyet nesnesine erişebileceğini ve görünümüne sahip olacağını denetlemez.</span><span class="sxs-lookup"><span data-stu-id="551f1-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="551f1-124">Satır düzeyi güvenlik, boyut hiyerarşileri ve Erişim listesi hiyerarşisi tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="551f1-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="551f1-125">Erişim haklarını verme</span><span class="sxs-lookup"><span data-stu-id="551f1-125">Grant access rights</span></span>
<span data-ttu-id="551f1-126">Aşağıdaki örnek, bir boyut hiyerarşisinin nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="551f1-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="551f1-127">**Boyut hiyerarşisi ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="551f1-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="551f1-128">Boyut hiyerarşisi adı</span><span class="sxs-lookup"><span data-stu-id="551f1-128">Dimension hierarchy name</span></span> | <span data-ttu-id="551f1-129">Boyut</span><span class="sxs-lookup"><span data-stu-id="551f1-129">Dimension</span></span>    | <span data-ttu-id="551f1-130">Boyut hiyerarşisi türü adı</span><span class="sxs-lookup"><span data-stu-id="551f1-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="551f1-131">Erişim listesi hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="551f1-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="551f1-132">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="551f1-132">Organization</span></span>             | <span data-ttu-id="551f1-133">Maliyet merkezleri</span><span class="sxs-lookup"><span data-stu-id="551f1-133">Cost centers</span></span> | <span data-ttu-id="551f1-134">Boyut sınıflandırması hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="551f1-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="551f1-135">**Evet**</span><span class="sxs-lookup"><span data-stu-id="551f1-135">**Yes**</span></span>               |

<span data-ttu-id="551f1-136">Her bir düğüme bir veya birden fazla kullanıcı kimliği eklemek için hiyerarşi tasarımcısındaki **Kullanıcılar** hızlı sekmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="551f1-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="551f1-137">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="551f1-137">Users</span></span>            | <span data-ttu-id="551f1-138">Boyut üyesi aralıkları</span><span class="sxs-lookup"><span data-stu-id="551f1-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="551f1-139">**Düğümler**</span><span class="sxs-lookup"><span data-stu-id="551f1-139">**Nodes**</span></span>                         | <span data-ttu-id="551f1-140">**Kullanıcı Kimliği**</span><span class="sxs-lookup"><span data-stu-id="551f1-140">**User ID**</span></span>      | <span data-ttu-id="551f1-141">**Kaynak boyut üyesi**</span><span class="sxs-lookup"><span data-stu-id="551f1-141">**From dimension member**</span></span> | <span data-ttu-id="551f1-142">**Hedef boyut üyesi**</span><span class="sxs-lookup"><span data-stu-id="551f1-142">**To dimension member**</span></span> |
| <span data-ttu-id="551f1-143">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="551f1-143">Organization</span></span>                      | <span data-ttu-id="551f1-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="551f1-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="551f1-145">&nbsp;&nbsp;Yönetici</span><span class="sxs-lookup"><span data-stu-id="551f1-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="551f1-146">Nisan</span><span class="sxs-lookup"><span data-stu-id="551f1-146">April</span></span>            |                           |                         |
| <span data-ttu-id="551f1-147">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="551f1-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="551f1-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="551f1-148">Alicia</span></span>           | <span data-ttu-id="551f1-149">CC002</span><span class="sxs-lookup"><span data-stu-id="551f1-149">CC002</span></span>                     | <span data-ttu-id="551f1-150">CC003</span><span class="sxs-lookup"><span data-stu-id="551f1-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="551f1-151">CC007</span><span class="sxs-lookup"><span data-stu-id="551f1-151">CC007</span></span>                     | <span data-ttu-id="551f1-152">CC007</span><span class="sxs-lookup"><span data-stu-id="551f1-152">CC007</span></span>                   |
| <span data-ttu-id="551f1-153">&nbsp;&nbsp;&nbsp;&nbsp;İK</span><span class="sxs-lookup"><span data-stu-id="551f1-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="551f1-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="551f1-154">Arnie</span></span>            | <span data-ttu-id="551f1-155">CC001</span><span class="sxs-lookup"><span data-stu-id="551f1-155">CC001</span></span>                     | <span data-ttu-id="551f1-156">CC001</span><span class="sxs-lookup"><span data-stu-id="551f1-156">CC001</span></span>                   |
| <span data-ttu-id="551f1-157">&nbsp;&nbsp;Üretim</span><span class="sxs-lookup"><span data-stu-id="551f1-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="551f1-158">David</span><span class="sxs-lookup"><span data-stu-id="551f1-158">David</span></span>            |                           |                         |
| <span data-ttu-id="551f1-159">&nbsp;&nbsp;&nbsp;&nbsp;Paketleme</span><span class="sxs-lookup"><span data-stu-id="551f1-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="551f1-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="551f1-160">Ellen</span></span>            | <span data-ttu-id="551f1-161">CC005</span><span class="sxs-lookup"><span data-stu-id="551f1-161">CC005</span></span>                     | <span data-ttu-id="551f1-162">CC005</span><span class="sxs-lookup"><span data-stu-id="551f1-162">CC005</span></span>                   |
| <span data-ttu-id="551f1-163">&nbsp;&nbsp;&nbsp;&nbsp;Montaj</span><span class="sxs-lookup"><span data-stu-id="551f1-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="551f1-164">Chris</span><span class="sxs-lookup"><span data-stu-id="551f1-164">Chris</span></span>            | <span data-ttu-id="551f1-165">CC006</span><span class="sxs-lookup"><span data-stu-id="551f1-165">CC006</span></span>                     | <span data-ttu-id="551f1-166">CC006</span><span class="sxs-lookup"><span data-stu-id="551f1-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="551f1-167">Maliyet muhasebesindeki tüm girişleri görebilmeleri için maliyet muhasebecileri, hiyerarşinin en üst düzeyine atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="551f1-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="551f1-168">Erişim listesi hiyerarşisi ve güvenlik ayarları uygulanabilmeden önce, **Maliyet nesnesi boyut üyelerini görüntüleme erişimini etkinleştir** seçeneği, **Maliyet muhasebesi parametreleri** sayfasında **Genel** sekmesi üzerinde **Evet** olarak ayarlanmalıdır (**Maliyet muhasebesi** > **Kurulum** > **Parametreler**).</span><span class="sxs-lookup"><span data-stu-id="551f1-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="551f1-169">Erişim listesi hiyerarşisi için ayarlar, aşağıdaki alanlarda gösterilen veriyi denetlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="551f1-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="551f1-170">**Maliyet kontrolü** çalışma alanı (istemci içinde):</span><span class="sxs-lookup"><span data-stu-id="551f1-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="551f1-171">Sayfalardaki veri ayrıntıya inme için kullanılır</span><span class="sxs-lookup"><span data-stu-id="551f1-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="551f1-172">**Maliyet kontrolü** çalışma alanı (mobil uygulama içinde):</span><span class="sxs-lookup"><span data-stu-id="551f1-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="551f1-173">Kartlardaki bakiyeler</span><span class="sxs-lookup"><span data-stu-id="551f1-173">Balances in cards</span></span>

- <span data-ttu-id="551f1-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="551f1-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="551f1-175">Veri, Power BI görselleştirmeleri içinde gösterilir</span><span class="sxs-lookup"><span data-stu-id="551f1-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="551f1-176">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition istemcisinde gömülü veri Power BI görselleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="551f1-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="551f1-177">Erişim listesi hiyerarşisi Power BI içerisindeki veriyi etkileyebilmeden önce, Power BI içindeki Erişim listesi hiyerarşisi ve satır düzeyi güvenliği eşleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="551f1-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="551f1-178">Daha fazla bilgi için bkz [Maliyet muhasebesi İçerik Paketi için güvenlik kurma](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="551f1-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="551f1-179">Bu konu, **Maliyet kontrolü** çalışma alanını kullanmadan önce ayarlanması gereken önkoşulları gösterir.</span><span class="sxs-lookup"><span data-stu-id="551f1-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="551f1-180">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="551f1-180">See also</span></span>

- [<span data-ttu-id="551f1-181">Maliyet kontrolü çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="551f1-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="551f1-182">Boyut hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="551f1-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="551f1-183">Maliyet muhasebesi içerik paketi için güvenliği kurmak</span><span class="sxs-lookup"><span data-stu-id="551f1-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

