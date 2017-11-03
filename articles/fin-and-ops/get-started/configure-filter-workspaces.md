---
title: "Çalışma alanlarını yapılandırma ve filtreleme"
description: "Bu makalede, çalışma alanlarının nasıl yapılandırılacağı ve filtreleneceğine ilişkin bir genel bakış verilmektedir."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c90384c798023ac4fcab06502d77f832a8e4c4c2
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="configure-and-filter-workspaces"></a><span data-ttu-id="5549c-103">Çalışma alanlarını yapılandırma ve filtreleme</span><span class="sxs-lookup"><span data-stu-id="5549c-103">Configure and filter workspaces</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5549c-104">Bu makalede, çalışma alanlarının nasıl yapılandırılacağı ve filtreleneceğine ilişkin bir genel bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5549c-104">This article provides an overview about how to configure and filter workspaces.</span></span>

<a name="configuring-a-workspace"></a><span data-ttu-id="5549c-105">Bir çalışma alanını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5549c-105">Configuring a workspace</span></span>
-----------------------

<span data-ttu-id="5549c-106">Tüm çalışma alanı için uygulanan ayarları güncelleştirerek, bazı çalışma alanlarının görünümünü ve davranışını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5549c-106">You can change the appearance and behavior of some workspaces by updating settings that apply to the whole workspace.</span></span> <span data-ttu-id="5549c-107">Çalışma alanı yapılandırılabiliyorsa, Eylem Bölmesinde, yapılandırma değişikliklerini yapmak üzere tıklamanız gerektiği belirtilen bir düğme görünür.</span><span class="sxs-lookup"><span data-stu-id="5549c-107">When a workspace can be configured, the Action Pane includes a button that instructs you to click it to make configuration changes.</span></span> <span data-ttu-id="5549c-108">Örneğin aşağıdaki çizimde düğme adı **Çalışma alanımı yapılandır**'dır.</span><span class="sxs-lookup"><span data-stu-id="5549c-108">For example, in the following illustration, the button is named **Configure my workspace**.</span></span> 

<span data-ttu-id="5549c-109">[![çalışma-alanlarını-yapılandır-ve-filtrele](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="5549c-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span></span>   

<span data-ttu-id="5549c-110">Düğmeye tıkladığınızda çalışma alanı için önceden tanımlanmış olan ayarlarda değişiklik yapabileceğiniz bir iletişim görünür.</span><span class="sxs-lookup"><span data-stu-id="5549c-110">When you click the button, a dialog appears, where you can modify the predefined settings for the workspace.</span></span> <span data-ttu-id="5549c-111">Bu iletişim kutusunda gördüğünüz belirli ayarlar çalışma alanına göre değişir ve çalışma alanında kullanılabilir olan belirli denetimlere ve iş verilerine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="5549c-111">The specific settings that you see in this dialog vary by workspace, and depend on the specific controls and business data that are available in the workspace.</span></span> 

<span data-ttu-id="5549c-112">[![çalışma-alanımı-yapılandır](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="5549c-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span></span>

## <a name="filtering-a-workspace"></a><span data-ttu-id="5549c-113">Bir çalışma alanını filtreleme</span><span class="sxs-lookup"><span data-stu-id="5549c-113">Filtering a workspace</span></span>
<span data-ttu-id="5549c-114">Birçok çalışma alanı, içinde görüntülenen içeriği filtrelemenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="5549c-114">Many workspaces let you filter the content that appears in them.</span></span> <span data-ttu-id="5549c-115">Kullanılabilen denetimler, çalışma alanındaki tüm içeriği veya belirli bir bölümdeki içeriği filtrelemenize izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="5549c-115">The controls that are available might let you filter all the content in the workspace or only the content in a specific section of the workspace.</span></span> <span data-ttu-id="5549c-116">Çalışma alanlarındaki filtreler aramalar, açılan kutular, serbest biçimli metin alanları veya diğer türde denetimler olabilir.</span><span class="sxs-lookup"><span data-stu-id="5549c-116">The filters on workspaces can be lookups, combo boxes, free-form text fields, or other types of controls.</span></span> <span data-ttu-id="5549c-117">Ancak, her filtre türü, aşağıdaki bölümlerde açıklandığı gibi, aynı etkilere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5549c-117">However, every type of filter has the same effects, as described in the following sections.</span></span>

### <a name="workspace-wide-filters"></a><span data-ttu-id="5549c-118">Çalışma alanı genelindeki filtreler</span><span class="sxs-lookup"><span data-stu-id="5549c-118">Workspace-wide filters</span></span>

<span data-ttu-id="5549c-119">Çalışma alanı genelinde filtre kullanarak tüm çalışma alanını filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5549c-119">You can filter the whole workspace by using a workspace-wide filter.</span></span> <span data-ttu-id="5549c-120">Çalışma alanının sol üst köşesinde, çalışma alanı genelinde bir filtre görünür.</span><span class="sxs-lookup"><span data-stu-id="5549c-120">A workspace-wide filter appears in the upper-left corner of the workspace.</span></span> <span data-ttu-id="5549c-121">Açılır listeden belirli bir değer seçtiğiniz zaman, çalışma alanının içeriği o seçime bağlı olarak filtrelenir.</span><span class="sxs-lookup"><span data-stu-id="5549c-121">When you select a specific value in the drop-down list, the contents of the workspace are filtered based on that selection.</span></span> 

<span data-ttu-id="5549c-122">[![çalışma-alanı-filtresi](./media/workspace-filter.png)](./media/workspace-filter.png)</span><span class="sxs-lookup"><span data-stu-id="5549c-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span></span> 

<span data-ttu-id="5549c-123">Filtreyi açmak için tıkladığınızda karşınıza çeşitli seçenekler çıkar.</span><span class="sxs-lookup"><span data-stu-id="5549c-123">When you click to open the filter, you're presented with several options.</span></span> 

<span data-ttu-id="5549c-124">[![çalışma-alanı-filtresi-genişletildi](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span><span class="sxs-lookup"><span data-stu-id="5549c-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span></span> 

<span data-ttu-id="5549c-125">O seçeneğe bağlı olarak çalışma alanını filtrelemek için bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5549c-125">Select an option to filter the workspace based on that option.</span></span>

### <a name="workspace-section-filters"></a><span data-ttu-id="5549c-126">Çalışma alanı bölümü filtreleri</span><span class="sxs-lookup"><span data-stu-id="5549c-126">Workspace section filters</span></span>

<span data-ttu-id="5549c-127">Çalışma alanının ayrı ayrı bölümlerinde filtreler varsa, her bölüme ayrı ayrı filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5549c-127">If individual sections of the workspace have filters, you can filter each section separately.</span></span> <span data-ttu-id="5549c-128">Aşağıdaki çizimde, filtre (içinde "Filtre" yazan alan) serbest biçimli bir metin alanı filtresi örneğidir.</span><span class="sxs-lookup"><span data-stu-id="5549c-128">In the following illustration, the filter (the field that contains the text "Filter") is an example of a free-form text field filter.</span></span> 

<span data-ttu-id="5549c-129">[![çalışma-alanı-bölüm-filtreleri](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span><span class="sxs-lookup"><span data-stu-id="5549c-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span></span> 

<span data-ttu-id="5549c-130">Çalışma alanı genelinde filtrede olduğu gibi, bölümün içeriğini filtrelemek için, alanda bir değer seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="5549c-130">As with a workspace-wide filter, select or enter a value in the field to filter the contents of the section.</span></span>




