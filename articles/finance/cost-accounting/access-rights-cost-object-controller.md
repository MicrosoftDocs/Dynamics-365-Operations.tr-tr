---
title: Maliyet nesnesi denetleyicilerinin erişim haklarını tanımlama
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
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a1e9ead5a10b3f4e8bb989dd35936945afaf3f29
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180352"
---
# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="90e96-103">Bir maliyet nesnesi denetleyicisinin erişim hakları</span><span class="sxs-lookup"><span data-stu-id="90e96-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90e96-104">**Maliyet kontrolü** çalışma alanı, yöneticilerin maliyet nesnelerinin performanslarını görüntüleyebilecekleri merkezi noktadır.</span><span class="sxs-lookup"><span data-stu-id="90e96-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="90e96-105">Bu çalışma alanı, yöneticilerin Maliyet muhasebesi verisini, maliyet muhasebecisi olmasalar bile kullanmalarına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="90e96-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="90e96-106">Güvenlik nedeniyle, yöneticiler yalnızca sorumlu oldukları belirli maliyet nesnelerinin Maliyet muhasebesi verilerini görmelidirler.</span><span class="sxs-lookup"><span data-stu-id="90e96-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="90e96-107">Maliyet muhasebesinde dört benzersiz rol vardır.</span><span class="sxs-lookup"><span data-stu-id="90e96-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="90e96-108">Rol adı</span><span class="sxs-lookup"><span data-stu-id="90e96-108">Role name</span></span>               | <span data-ttu-id="90e96-109">Lisans</span><span class="sxs-lookup"><span data-stu-id="90e96-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="90e96-110">Maliyet muhasebesi yöneticisi</span><span class="sxs-lookup"><span data-stu-id="90e96-110">Cost accounting manager</span></span> | <span data-ttu-id="90e96-111">Faaliyet</span><span class="sxs-lookup"><span data-stu-id="90e96-111">Activity</span></span>     |
| <span data-ttu-id="90e96-112">Maliyet muhasebecisi</span><span class="sxs-lookup"><span data-stu-id="90e96-112">Cost accountant</span></span>         | <span data-ttu-id="90e96-113">Operations</span><span class="sxs-lookup"><span data-stu-id="90e96-113">Operations</span></span>   |
| <span data-ttu-id="90e96-114">Maliyet muhasebe memuru</span><span class="sxs-lookup"><span data-stu-id="90e96-114">Cost accountant clerk</span></span>   | <span data-ttu-id="90e96-115">Operations</span><span class="sxs-lookup"><span data-stu-id="90e96-115">Operations</span></span>   |
| <span data-ttu-id="90e96-116">Maliyet nesnesi denetleyicisi</span><span class="sxs-lookup"><span data-stu-id="90e96-116">Cost object controller</span></span>  | <span data-ttu-id="90e96-117">Takım üyeleri</span><span class="sxs-lookup"><span data-stu-id="90e96-117">Team members</span></span> |

<span data-ttu-id="90e96-118">Bu konu, **Maliyet nesnesi denetleyicisi** rolünü bir yöneticiye atamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="90e96-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="90e96-119">**Maliyet nesnesi denetleyicisi** rolü bir yöneticiye atandığı, yönetici aşağıdaki görevleri yerine getirebilir:</span><span class="sxs-lookup"><span data-stu-id="90e96-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="90e96-120">**Maliyet denetimi** çalışma alanına erişmek (istemci içinde).</span><span class="sxs-lookup"><span data-stu-id="90e96-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="90e96-121">Ayrıntıya inme deneyimini destekleyen sayfalarda ayrıntıya inme ve erişim sağlama.</span><span class="sxs-lookup"><span data-stu-id="90e96-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="90e96-122">**Maliyet denetimi** çalışma alanına erişmek (mobil uygulamada).</span><span class="sxs-lookup"><span data-stu-id="90e96-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="90e96-123">**Maliyet nesnesi denetçisi** rolü, kullanıcının hangi maliyet nesnesine erişebileceğini ve görünümüne sahip olacağını denetlemez.</span><span class="sxs-lookup"><span data-stu-id="90e96-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="90e96-124">Satır düzeyi güvenlik, boyut hiyerarşileri ve Erişim listesi hiyerarşisi tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="90e96-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="90e96-125">Erişim haklarını verme</span><span class="sxs-lookup"><span data-stu-id="90e96-125">Grant access rights</span></span>
<span data-ttu-id="90e96-126">Aşağıdaki örnek, bir boyut hiyerarşisinin nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="90e96-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="90e96-127">**Boyut hiyerarşisi ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="90e96-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="90e96-128">Boyut hiyerarşisi adı</span><span class="sxs-lookup"><span data-stu-id="90e96-128">Dimension hierarchy name</span></span> | <span data-ttu-id="90e96-129">Boyut</span><span class="sxs-lookup"><span data-stu-id="90e96-129">Dimension</span></span>    | <span data-ttu-id="90e96-130">Boyut hiyerarşisi türü adı</span><span class="sxs-lookup"><span data-stu-id="90e96-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="90e96-131">Erişim listesi hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="90e96-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="90e96-132">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="90e96-132">Organization</span></span>             | <span data-ttu-id="90e96-133">Maliyet merkezleri</span><span class="sxs-lookup"><span data-stu-id="90e96-133">Cost centers</span></span> | <span data-ttu-id="90e96-134">Boyut sınıflandırması hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="90e96-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="90e96-135">**Evet**</span><span class="sxs-lookup"><span data-stu-id="90e96-135">**Yes**</span></span>               |

<span data-ttu-id="90e96-136">Her bir düğüme bir veya birden fazla kullanıcı kimliği eklemek için hiyerarşi tasarımcısındaki **Kullanıcılar** hızlı sekmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90e96-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="90e96-137">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="90e96-137">Users</span></span>            | <span data-ttu-id="90e96-138">Boyut üyesi aralıkları</span><span class="sxs-lookup"><span data-stu-id="90e96-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="90e96-139">**Düğümler**</span><span class="sxs-lookup"><span data-stu-id="90e96-139">**Nodes**</span></span>                         | <span data-ttu-id="90e96-140">**Kullanıcı Kimliği**</span><span class="sxs-lookup"><span data-stu-id="90e96-140">**User ID**</span></span>      | <span data-ttu-id="90e96-141">**Kaynak boyut üyesi**</span><span class="sxs-lookup"><span data-stu-id="90e96-141">**From dimension member**</span></span> | <span data-ttu-id="90e96-142">**Hedef boyut üyesi**</span><span class="sxs-lookup"><span data-stu-id="90e96-142">**To dimension member**</span></span> |
| <span data-ttu-id="90e96-143">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="90e96-143">Organization</span></span>                      | <span data-ttu-id="90e96-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="90e96-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="90e96-145">&nbsp;&nbsp;Yönetici</span><span class="sxs-lookup"><span data-stu-id="90e96-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="90e96-146">Nisan</span><span class="sxs-lookup"><span data-stu-id="90e96-146">April</span></span>            |                           |                         |
| <span data-ttu-id="90e96-147">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="90e96-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="90e96-148">Alicia</span><span class="sxs-lookup"><span data-stu-id="90e96-148">Alicia</span></span>           | <span data-ttu-id="90e96-149">CC002</span><span class="sxs-lookup"><span data-stu-id="90e96-149">CC002</span></span>                     | <span data-ttu-id="90e96-150">CC003</span><span class="sxs-lookup"><span data-stu-id="90e96-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="90e96-151">CC007</span><span class="sxs-lookup"><span data-stu-id="90e96-151">CC007</span></span>                     | <span data-ttu-id="90e96-152">CC007</span><span class="sxs-lookup"><span data-stu-id="90e96-152">CC007</span></span>                   |
| <span data-ttu-id="90e96-153">&nbsp;&nbsp;&nbsp;&nbsp;İK</span><span class="sxs-lookup"><span data-stu-id="90e96-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="90e96-154">Arnie</span><span class="sxs-lookup"><span data-stu-id="90e96-154">Arnie</span></span>            | <span data-ttu-id="90e96-155">CC001</span><span class="sxs-lookup"><span data-stu-id="90e96-155">CC001</span></span>                     | <span data-ttu-id="90e96-156">CC001</span><span class="sxs-lookup"><span data-stu-id="90e96-156">CC001</span></span>                   |
| <span data-ttu-id="90e96-157">&nbsp;&nbsp;Üretim</span><span class="sxs-lookup"><span data-stu-id="90e96-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="90e96-158">David</span><span class="sxs-lookup"><span data-stu-id="90e96-158">David</span></span>            |                           |                         |
| <span data-ttu-id="90e96-159">&nbsp;&nbsp;&nbsp;&nbsp;Paketleme</span><span class="sxs-lookup"><span data-stu-id="90e96-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="90e96-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="90e96-160">Ellen</span></span>            | <span data-ttu-id="90e96-161">CC005</span><span class="sxs-lookup"><span data-stu-id="90e96-161">CC005</span></span>                     | <span data-ttu-id="90e96-162">CC005</span><span class="sxs-lookup"><span data-stu-id="90e96-162">CC005</span></span>                   |
| <span data-ttu-id="90e96-163">&nbsp;&nbsp;&nbsp;&nbsp;Montaj</span><span class="sxs-lookup"><span data-stu-id="90e96-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="90e96-164">Chris</span><span class="sxs-lookup"><span data-stu-id="90e96-164">Chris</span></span>            | <span data-ttu-id="90e96-165">CC006</span><span class="sxs-lookup"><span data-stu-id="90e96-165">CC006</span></span>                     | <span data-ttu-id="90e96-166">CC006</span><span class="sxs-lookup"><span data-stu-id="90e96-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="90e96-167">Maliyet muhasebesindeki tüm girişleri görebilmeleri için maliyet muhasebecileri, hiyerarşinin en üst düzeyine atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="90e96-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="90e96-168">Erişim listesi hiyerarşisi ve güvenlik ayarları uygulanabilmeden önce, **Maliyet nesnesi boyut üyelerini görüntüleme erişimini etkinleştir** seçeneği, **Maliyet muhasebesi parametreleri** sayfasında **Genel** sekmesi üzerinde **Evet** olarak ayarlanmalıdır (**Maliyet muhasebesi** > **Kurulum** > **Parametreler**).</span><span class="sxs-lookup"><span data-stu-id="90e96-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="90e96-169">Erişim listesi hiyerarşisi için ayarlar, aşağıdaki alanlarda gösterilen veriyi denetlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="90e96-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="90e96-170">**Maliyet kontrolü** çalışma alanı (istemci içinde):</span><span class="sxs-lookup"><span data-stu-id="90e96-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="90e96-171">Sayfalardaki veri ayrıntıya inme için kullanılır</span><span class="sxs-lookup"><span data-stu-id="90e96-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="90e96-172">**Maliyet kontrolü** çalışma alanı (mobil uygulama içinde):</span><span class="sxs-lookup"><span data-stu-id="90e96-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="90e96-173">Kartlardaki bakiyeler</span><span class="sxs-lookup"><span data-stu-id="90e96-173">Balances in cards</span></span>

- <span data-ttu-id="90e96-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="90e96-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="90e96-175">Veri, Power BI görselleştirmeleri içinde gösterilir</span><span class="sxs-lookup"><span data-stu-id="90e96-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="90e96-176">Dynamics 365 Finance istemcisine içine katıştırılmış veri Power BI görselleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="90e96-176">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="90e96-177">Erişim listesi hiyerarşisi Power BI içerisindeki veriyi etkileyebilmeden önce, Power BI içindeki Erişim listesi hiyerarşisi ve satır düzeyi güvenliği eşleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="90e96-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="90e96-178">Daha fazla bilgi için bkz [Maliyet muhasebesi İçerik Paketi için güvenlik kurma](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="90e96-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="90e96-179">Bu konu, **Maliyet kontrolü** çalışma alanını kullanmadan önce ayarlanması gereken önkoşulları gösterir.</span><span class="sxs-lookup"><span data-stu-id="90e96-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="90e96-180">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="90e96-180">Additional resources</span></span>

- [<span data-ttu-id="90e96-181">Maliyet kontrolü çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="90e96-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="90e96-182">Boyut hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="90e96-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="90e96-183">Maliyet muhasebesi içerik paketi için güvenliği kurmak</span><span class="sxs-lookup"><span data-stu-id="90e96-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
