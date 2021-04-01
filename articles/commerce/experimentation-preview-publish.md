---
title: Deneme önizleme ve yayımlama
description: Bu konu, Dynamics 365 Commerce'tan denemeyi önizlemeyi ve yayımlamayı açıklamaktadır.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b35af35f5d0347192ed94bed51dfd2484cfa481
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238594"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="251ce-103">Deneme önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="251ce-103">Preview and publish an experiment</span></span>

<span data-ttu-id="251ce-104">Bu konuda, [denemenizi bağlandıktan ve varyasyonlarınızı düzenledikten](experimentation-connect-edit.md) sonra denemenize Dynamics 365 Commerce'ta nasıl önizleme yapacağınız ve denemenizi nasıl yayımlayacağınız açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="251ce-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="251ce-105">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="251ce-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="251ce-106">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="251ce-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="251ce-107">[ ![Deneme kullanıcı yolculuğu - Önizleme ve Yayımlama](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="251ce-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="251ce-108">Deneme varyasyonlarınızı önizleme</span><span class="sxs-lookup"><span data-stu-id="251ce-108">Preview your experiment variations</span></span>
<span data-ttu-id="251ce-109">Varyasyonlarınızın önizlemesini yapabilir ve istediğiniz gibi görününceye kadar bunları düzenlemeye devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="251ce-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="251ce-110">Commerce site oluşturucuda deneme varyasyonlarınızı önizlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="251ce-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="251ce-111">Önizlemek istediğiniz içeriği seçmek için komut çubuğunun altındaki varyasyonlar açılır menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="251ce-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="251ce-112">Komut çubuğunda, **Önizleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="251ce-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="251ce-113">Yayımlandığında içeriğin nasıl görüneceğine ilişkin önizleme görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="251ce-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="251ce-114">Farklı bir varyasyonun önizlemesini görmek için varyasyon açılır menüsünde bunu seçin ve tekrar **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="251ce-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="251ce-115">Denemenizi yayımlama</span><span class="sxs-lookup"><span data-stu-id="251ce-115">Publish your experiment</span></span>
<span data-ttu-id="251ce-116">Denemenizin ne zaman canlı olarak yayımlanacağını planlamak için yayımlama grubu kullanmıyorsanız ve hemen yayımlamak istiyorsanız, komut çubuğunda **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="251ce-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="251ce-117">Denemeye ait tüm varyasyonlar yayımlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="251ce-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="251ce-118">Sayfada yayımdan kaldırılmış bir URL varsa, ilk olarak URL'yi yayımlamanız gerekir aksi durumda web sitesi kullanıcılarınıza gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="251ce-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="251ce-119">Ayrıntılar için bkz. [Sayfa kaydetme, önizleme ve yayımlama](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="251ce-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="251ce-120">Denemenizin ne zaman canlı yayımlanacağını planlamak için yayımlama grupları kullanma</span><span class="sxs-lookup"><span data-stu-id="251ce-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="251ce-121">Site oluşturucuda oluşturulan varyasyonlar, bir yayımlama grubu kullanılarak yayımlanmak üzere zamanlanabilir.</span><span class="sxs-lookup"><span data-stu-id="251ce-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="251ce-122">Bir yayınlama grubunda, soldaki gezinti bölmesinde **Denemeler**'i seçerek bir sayfa veya parçayı denemenize bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="251ce-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="251ce-123">Bunu, **sayfalar** veya **parçaları** seçerek ve [bir denemeyi bağlama ve varyasyonları düzenleme](experimentation-connect-edit.md) bölümündeki yönergeleri izleyerek de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="251ce-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="251ce-124">Yayımlama grupları hakkında daha fazla bilgi için bkz. [Yayımlama gruplarıyla çalışma](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="251ce-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="251ce-125">Yayımlama gruplarını denemeler ile kullanırken, bilinmesi gereken bazı önemli noktalar vardır.</span><span class="sxs-lookup"><span data-stu-id="251ce-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="251ce-126">Bir yayımlama grubuna, üzerinde çalışan deneme bulunan bir sayfa veya parça eklediğinizde, deneme yayınlama grubundaki sayfadan veya parçadan kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="251ce-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="251ce-127">Canlı sitedeki sayfalara bağlanan denemeler yayınlama grupları içindeki sayfalar tarafından kullanılamaz ve bunun tersi de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="251ce-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="251ce-128">Benzer şekilde, canlı bir sitede üzerlerinde denemeler çalıştıran sayfalar, yayımlama gruplarındaki diğer denemelerde kullanılamaz ve tam tersi de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="251ce-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="251ce-129">Bir yayımlama grubunu yayımladığınızda veya zamanladığınızda, yayınlama grubundaki tüm içerik yayımlama grubuyla ilişkilendirilmiş bir deneme olup olmadığına bakılmaksızın yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="251ce-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="251ce-130">Yayımlama grubu canlı bir siteye yayımlandıktan sonra devam ettiğinden, yayımlama grubundaki denemeler de devam eder.</span><span class="sxs-lookup"><span data-stu-id="251ce-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="251ce-131">Bu nedenle, diğer denemeleri aynı sayfa veya parça ile ilişkilendiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="251ce-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="251ce-132">Bu sınırlamayı önlemek için, kalıcı denemeler içeren tüm yayımlama gruplarını silin.</span><span class="sxs-lookup"><span data-stu-id="251ce-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="251ce-133">Benzer şekilde, aynı zamanda bir yayımlama grubunda da bulunan canlı bir sitedeki denemeyi silmek isterseniz, denemeyi önce yaymnlama grubundan silin.</span><span class="sxs-lookup"><span data-stu-id="251ce-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="251ce-134">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="251ce-134">Previous step</span></span>
[<span data-ttu-id="251ce-135">Deneme bağlama ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="251ce-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="251ce-136">Sonraki adım</span><span class="sxs-lookup"><span data-stu-id="251ce-136">Next step</span></span>
[<span data-ttu-id="251ce-137">Deneme çalıştırma ve izleme</span><span class="sxs-lookup"><span data-stu-id="251ce-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]