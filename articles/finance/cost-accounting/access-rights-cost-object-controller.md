---
title: Maliyet nesnesi denetleyicilerinin erişim hakları
description: Bu konu, maliyet nesnesi denetleyicileri için erişim hakları hakkında bilgi sağlar.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897636"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="c7100-103">Maliyet nesnesi denetleyicilerinin erişim hakları</span><span class="sxs-lookup"><span data-stu-id="c7100-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7100-104">**Maliyet kontrolü** çalışma alanı, yöneticilerin maliyet nesnelerinin performanslarını görüntüleyebilecekleri merkezi noktadır.</span><span class="sxs-lookup"><span data-stu-id="c7100-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="c7100-105">Bu çalışma alanı, yöneticilerin Maliyet muhasebesi verisini, maliyet muhasebecisi olmasalar bile kullanmalarına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="c7100-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="c7100-106">Güvenlik nedeniyle, yöneticiler yalnızca sorumlu oldukları belirli maliyet nesnelerinin Maliyet muhasebesi verilerini görmelidirler.</span><span class="sxs-lookup"><span data-stu-id="c7100-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="c7100-107">Maliyet muhasebesinde dört benzersiz rol vardır.</span><span class="sxs-lookup"><span data-stu-id="c7100-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="c7100-108">Rol adı</span><span class="sxs-lookup"><span data-stu-id="c7100-108">Role name</span></span>               | <span data-ttu-id="c7100-109">Lisans</span><span class="sxs-lookup"><span data-stu-id="c7100-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="c7100-110">Maliyet muhasebesi yöneticisi</span><span class="sxs-lookup"><span data-stu-id="c7100-110">Cost accounting manager</span></span> | <span data-ttu-id="c7100-111">Faaliyet</span><span class="sxs-lookup"><span data-stu-id="c7100-111">Activity</span></span>     |
| <span data-ttu-id="c7100-112">Maliyet muhasebecisi</span><span class="sxs-lookup"><span data-stu-id="c7100-112">Cost accountant</span></span>         | <span data-ttu-id="c7100-113">Operations</span><span class="sxs-lookup"><span data-stu-id="c7100-113">Operations</span></span>   |
| <span data-ttu-id="c7100-114">Maliyet muhasebe memuru</span><span class="sxs-lookup"><span data-stu-id="c7100-114">Cost accountant clerk</span></span>   | <span data-ttu-id="c7100-115">Operations</span><span class="sxs-lookup"><span data-stu-id="c7100-115">Operations</span></span>   |
| <span data-ttu-id="c7100-116">Maliyet nesnesi denetleyicisi</span><span class="sxs-lookup"><span data-stu-id="c7100-116">Cost object controller</span></span>  | <span data-ttu-id="c7100-117">Takım üyeleri</span><span class="sxs-lookup"><span data-stu-id="c7100-117">Team members</span></span> |

<span data-ttu-id="c7100-118">Bu konu, **Maliyet nesnesi denetleyicisi** rolünü bir yöneticiye atamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="c7100-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="c7100-119">**Maliyet nesnesi denetleyicisi** rolü bir yöneticiye atandığı, yönetici aşağıdaki görevleri yerine getirebilir:</span><span class="sxs-lookup"><span data-stu-id="c7100-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="c7100-120">**Maliyet denetimi** çalışma alanına erişmek (istemci içinde).</span><span class="sxs-lookup"><span data-stu-id="c7100-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="c7100-121">Ayrıntıya inme deneyimini destekleyen sayfalarda ayrıntıya inme ve erişim sağlama.</span><span class="sxs-lookup"><span data-stu-id="c7100-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="c7100-122">**Maliyet denetimi** çalışma alanına erişmek (mobil uygulamada).</span><span class="sxs-lookup"><span data-stu-id="c7100-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="c7100-123">**Maliyet nesnesi denetçisi** rolü, kullanıcının hangi maliyet nesnesine erişebileceğini ve görünümüne sahip olacağını denetlemez.</span><span class="sxs-lookup"><span data-stu-id="c7100-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="c7100-124">Satır düzeyi güvenlik, boyut hiyerarşileri ve Erişim listesi hiyerarşisi tarafından sağlanır.</span><span class="sxs-lookup"><span data-stu-id="c7100-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="c7100-125">Erişim haklarını verme</span><span class="sxs-lookup"><span data-stu-id="c7100-125">Grant access rights</span></span>
<span data-ttu-id="c7100-126">Aşağıdaki örnek, bir boyut hiyerarşisinin nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7100-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="c7100-127">**Boyut hiyerarşisi ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="c7100-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="c7100-128">Boyut hiyerarşisi adı</span><span class="sxs-lookup"><span data-stu-id="c7100-128">Dimension hierarchy name</span></span> | <span data-ttu-id="c7100-129">Boyut</span><span class="sxs-lookup"><span data-stu-id="c7100-129">Dimension</span></span>    | <span data-ttu-id="c7100-130">Boyut hiyerarşisi türü adı</span><span class="sxs-lookup"><span data-stu-id="c7100-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="c7100-131">Erişim listesi hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="c7100-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="c7100-132">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="c7100-132">Organization</span></span>             | <span data-ttu-id="c7100-133">Maliyet merkezleri</span><span class="sxs-lookup"><span data-stu-id="c7100-133">Cost centers</span></span> | <span data-ttu-id="c7100-134">Boyut sınıflandırması hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="c7100-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="c7100-135">**Evet**</span><span class="sxs-lookup"><span data-stu-id="c7100-135">**Yes**</span></span>               |

<span data-ttu-id="c7100-136">Her bir düğüme bir veya birden fazla kullanıcı kimliği eklemek için hiyerarşi tasarımcısındaki **Kullanıcılar** hızlı sekmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7100-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="c7100-137">Düğümler</span><span class="sxs-lookup"><span data-stu-id="c7100-137">Nodes</span></span>                 | <span data-ttu-id="c7100-138">Kullanıcılar</span><span class="sxs-lookup"><span data-stu-id="c7100-138">Users</span></span>            | <span data-ttu-id="c7100-139">Kaynak boyut üyesi</span><span class="sxs-lookup"><span data-stu-id="c7100-139">From dimension member</span></span>     |   <span data-ttu-id="c7100-140">Hedef boyut üyesi</span><span class="sxs-lookup"><span data-stu-id="c7100-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="c7100-141">Organizasyon</span><span class="sxs-lookup"><span data-stu-id="c7100-141">Organization</span></span>                      | <span data-ttu-id="c7100-142">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="c7100-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="c7100-143">&nbsp;&nbsp;Yönetici</span><span class="sxs-lookup"><span data-stu-id="c7100-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="c7100-144">Nisan</span><span class="sxs-lookup"><span data-stu-id="c7100-144">April</span></span>            |                           |                         |
| <span data-ttu-id="c7100-145">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="c7100-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="c7100-146">Alicia</span><span class="sxs-lookup"><span data-stu-id="c7100-146">Alicia</span></span>           | <span data-ttu-id="c7100-147">CC002</span><span class="sxs-lookup"><span data-stu-id="c7100-147">CC002</span></span>                     | <span data-ttu-id="c7100-148">CC003</span><span class="sxs-lookup"><span data-stu-id="c7100-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="c7100-149">CC007</span><span class="sxs-lookup"><span data-stu-id="c7100-149">CC007</span></span>                     | <span data-ttu-id="c7100-150">CC007</span><span class="sxs-lookup"><span data-stu-id="c7100-150">CC007</span></span>                   |
| <span data-ttu-id="c7100-151">&nbsp;&nbsp;&nbsp;&nbsp;İK</span><span class="sxs-lookup"><span data-stu-id="c7100-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="c7100-152">Arnie</span><span class="sxs-lookup"><span data-stu-id="c7100-152">Arnie</span></span>            | <span data-ttu-id="c7100-153">CC001</span><span class="sxs-lookup"><span data-stu-id="c7100-153">CC001</span></span>                     | <span data-ttu-id="c7100-154">CC001</span><span class="sxs-lookup"><span data-stu-id="c7100-154">CC001</span></span>                   |
| <span data-ttu-id="c7100-155">&nbsp;&nbsp;Üretim</span><span class="sxs-lookup"><span data-stu-id="c7100-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="c7100-156">David</span><span class="sxs-lookup"><span data-stu-id="c7100-156">David</span></span>            |                           |                         |
| <span data-ttu-id="c7100-157">&nbsp;&nbsp;&nbsp;&nbsp;Paketleme</span><span class="sxs-lookup"><span data-stu-id="c7100-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="c7100-158">Ellen</span><span class="sxs-lookup"><span data-stu-id="c7100-158">Ellen</span></span>            | <span data-ttu-id="c7100-159">CC005</span><span class="sxs-lookup"><span data-stu-id="c7100-159">CC005</span></span>                     | <span data-ttu-id="c7100-160">CC005</span><span class="sxs-lookup"><span data-stu-id="c7100-160">CC005</span></span>                   |
| <span data-ttu-id="c7100-161">&nbsp;&nbsp;&nbsp;&nbsp;Montaj</span><span class="sxs-lookup"><span data-stu-id="c7100-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="c7100-162">Chris</span><span class="sxs-lookup"><span data-stu-id="c7100-162">Chris</span></span>            | <span data-ttu-id="c7100-163">CC006</span><span class="sxs-lookup"><span data-stu-id="c7100-163">CC006</span></span>                     | <span data-ttu-id="c7100-164">CC006</span><span class="sxs-lookup"><span data-stu-id="c7100-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="c7100-165">Maliyet muhasebesindeki tüm girişleri görebilmeleri için maliyet muhasebecileri, hiyerarşinin en üst düzeyine atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7100-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="c7100-166">Erişim listesi hiyerarşisi ve güvenlik ayarları uygulanabilmeden önce, **Maliyet nesnesi boyut üyelerini görüntüleme erişimini etkinleştir** seçeneği, **Maliyet muhasebesi parametreleri** sayfasında **Genel** sekmesi üzerinde **Evet** olarak ayarlanmalıdır (**Maliyet muhasebesi** > **Kurulum** > **Parametreler**).</span><span class="sxs-lookup"><span data-stu-id="c7100-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="c7100-167">Erişim listesi hiyerarşisi için ayarlar, aşağıdaki alanlarda gösterilen veriyi denetlemek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="c7100-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="c7100-168">**Maliyet kontrolü** çalışma alanı (istemci içinde):</span><span class="sxs-lookup"><span data-stu-id="c7100-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="c7100-169">Sayfalardaki veri ayrıntıya inme için kullanılır</span><span class="sxs-lookup"><span data-stu-id="c7100-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="c7100-170">**Maliyet kontrolü** çalışma alanı (mobil uygulama içinde):</span><span class="sxs-lookup"><span data-stu-id="c7100-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="c7100-171">Kartlardaki bakiyeler</span><span class="sxs-lookup"><span data-stu-id="c7100-171">Balances in cards</span></span>

- <span data-ttu-id="c7100-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="c7100-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="c7100-173">Veri, Power BI görselleştirmeleri içinde gösterilir</span><span class="sxs-lookup"><span data-stu-id="c7100-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="c7100-174">Dynamics 365 Finance istemcisine içine katıştırılmış veri Power BI görselleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="c7100-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="c7100-175">Erişim listesi hiyerarşisi Power BI içerisindeki veriyi etkileyebilmeden önce, Power BI içindeki Erişim listesi hiyerarşisi ve satır düzeyi güvenliği eşleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c7100-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="c7100-176">Daha fazla bilgi için bkz [Maliyet muhasebesi İçerik Paketi için güvenlik kurma](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="c7100-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="c7100-177">Bu konu, **Maliyet kontrolü** çalışma alanını kullanmadan önce ayarlanması gereken önkoşulları gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7100-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="c7100-178">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c7100-178">Additional resources</span></span>

- [<span data-ttu-id="c7100-179">Maliyet kontrolü çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="c7100-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="c7100-180">Boyut hiyerarşisi</span><span class="sxs-lookup"><span data-stu-id="c7100-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="c7100-181">Maliyet muhasebesi içerik paketi için güvenliği kurmak</span><span class="sxs-lookup"><span data-stu-id="c7100-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
