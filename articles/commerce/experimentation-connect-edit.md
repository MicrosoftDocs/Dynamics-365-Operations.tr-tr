---
title: Deneme bağlama ve varyasyonları düzenleme
description: Bu konuda, üçüncü taraf bir hizmetteki bir denemebib Dynamics 365 Commerce'a nasıl bağlanacağı ve denemeler için varyasyonların nasıl düzenleneceği açıklanmaktadır.
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
ms.openlocfilehash: c295f6f8170b6314ddf2d0c3582343b312c815b6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238666"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="0ada6-103">Deneme bağlama ve varyasyonları düzenleme</span><span class="sxs-lookup"><span data-stu-id="0ada6-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="0ada6-104">Bu konu, Commerce'taki denemenizi nasıl bağlayacağınızı ve varyasyonlarınızda varsayımınızla uygun olmaları için nasıl düzenleme yapacağınız açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0ada6-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="0ada6-105">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0ada6-106">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="0ada6-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="0ada6-107">[ ![Deneme kullanıcı yolculuğu - Bağla ve Düzenle](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0ada6-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="0ada6-108">Üçüncü taraf bir hizmette [denemenizi ayarladıktan sonra](experimentation-setup.md), denemeyi Dynamics 365 Commerce'ta bağlayıp deneme varyasyonlarını düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada6-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="0ada6-109">Planlama değerlendirmeleri</span><span class="sxs-lookup"><span data-stu-id="0ada6-109">Planning considerations</span></span>

<span data-ttu-id="0ada6-110">Denemenizi Commerce'ta bağlamadan önce Commerce'ın içeriğinizi yönetme biçimini etkileyen bazı kararlar almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="0ada6-111">Denemenin kapsamını belirleyin</span><span class="sxs-lookup"><span data-stu-id="0ada6-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="0ada6-112">Bir denemeyi bağladığınızda, denemenizin kapsamını tanımlamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="0ada6-113">Denemeler **kısmi** kapsam veya **tam** kapsam olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="0ada6-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="0ada6-114">Sayfanın belirli bir bölümünde denemeler yapmak istiyorsanız **kısmi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="0ada6-115">Bu seçeneği seçerseniz, deneme içine hangi modüllerin dahil edileceğini tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="0ada6-116">Varsayılan sayfa veya parçanın, deneme ile ilgili olmayan kısımlarında yapılan değişiklikler otomatik olarak varyasyonlar arasında eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="0ada6-117">Tüm sayfa veya parça üzerinde denemeler yapmak istiyorsanız, **tüm** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="0ada6-118">Varsayılan sayfa veya parçanın ayrı kopyaları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0ada6-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="0ada6-119">Tüm düzenleme yüzeyinin değiştirilebilir olması nedeniyle, denemeye dahil edilecek modülleri seçmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="0ada6-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="0ada6-120">Gerektiğinde modülleri ekleyebilir, silebilir veya yeniden sıralayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada6-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="0ada6-121">Ancak, denemenin ilişkili olduğu varsayılan sayfa veya parça üzerinde herhangi bir değişiklik yapılırsa, bu değişikliklerin tüm varyasyonlarda el ile eşitlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="0ada6-122">Denemenizi düzen kullanan bir sayfayla ilişkilendirirseniz, yalnızca **tüm** deneme kapsamını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada6-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="0ada6-123">Denemenizin ne zaman yayımlanacağını planlamak isteyip istemediğinize karar verin</span><span class="sxs-lookup"><span data-stu-id="0ada6-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="0ada6-124">Denemenizin canlı sitenizde ne zaman yayımlanacağını planlamak istiyorsanız, deneme ile ilişkilendirmek istediğiniz içeriğin denemeyi bağlamadan *önce* bir yayımlama grubunda kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0ada6-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="0ada6-125">Yayımlama grupları hakkında daha fazla bilgi için [Yayımlama gruplarıyla çalışma](publish-groups.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="0ada6-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="0ada6-126">Denemenizi bağlama</span><span class="sxs-lookup"><span data-stu-id="0ada6-126">Connect your experiment</span></span>
<span data-ttu-id="0ada6-127">Denemenizi bağlamak için **Deneme bağlama** sihirbazını başlatın.</span><span class="sxs-lookup"><span data-stu-id="0ada6-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="0ada6-128">Sihirbaz, denemenizi bağlamak için gerekli olan adımlarda size yol gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="0ada6-129">Sihirbazı tamamladığınızda, denemeniz bağlanır ve varyasyonlar oluşturulup düzenlenmeye hazır hale gelir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="0ada6-130">Commerce site oluşturucuda denemenizi bağlamaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0ada6-131">**Denemeyi bağlama** sihirbazını başlatmak için, sol gezinti bölmesinde **Denemeler**'i seçin ve sonra **Bağlan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="0ada6-132">Alternatif olarak, sihirbaza bir sayfa veya parça düzenleyicisinden de erişebilirsiniz. Bunun için sihirbazı düzenleyin ve komut çubuğunda **Denemeyi bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ada6-133">Bir sayfa, bir seferde yalnızca bir denemeye bağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="0ada6-134">Bir sayfayı farklı bir denemeye bağlamak için, önce sayfanın bağlı olduğu denemeyi silin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="0ada6-135">Denemenizi çalıştırmak istediğiniz sayfayı veya parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="0ada6-136">Yukarıdaki [Denemenizin kapsamını belirleme](#determine-the-scope-of-your-experiment) bölümünde yaptığınız seçimi temel alarak deneme kapsamını **kısmi** veya **tüm** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0ada6-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="0ada6-137">Tam sayfa veya parça üzerinde denemeler yapmak istiyorsanız, **Sayfalar veya parçalar üzerinde deneme** özelliği bayrağının etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0ada6-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="0ada6-138">Daha fazla bilgi için [Dynamics 365 Commerce'ta deneme](experimentation-overview.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="0ada6-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="0ada6-139">Sihirbazın son adımında, **Varyasyonlar oluştur ve sihirbazdan çık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="0ada6-140">Denemeler için varyasyonlar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0ada6-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="0ada6-141">Varyasyonlarınızı düzenleme</span><span class="sxs-lookup"><span data-stu-id="0ada6-141">Edit your variations</span></span>
<span data-ttu-id="0ada6-142">Sihirbazdan çıktığınızda, varyasyonlar sizin için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0ada6-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="0ada6-143">Daha sonra, varyasyonları deneme varsayımında doğrulamanız gereken seçimleri yansıtacak şekilde düzenlersiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada6-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="0ada6-144">Yukarıdaki [Denemenizin kapsamını belirleme](#determine-the-scope-of-your-experiment) bölümünde denemeniz için seçtiğiniz kapsama karşılık gelen aşağıdaki yordamlardan birini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="0ada6-145">Kısmi kapsamlı denemeler için varyasyonları düzenleme</span><span class="sxs-lookup"><span data-stu-id="0ada6-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="0ada6-146">**Denemeyi bağla** sihirbazında denemenizin kapsamını **kısmi** olarak tanımladıysanızşu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="0ada6-147">Düzenleyici görünümünde, her varyasyonu özgün varsayıma göre düzenlemek için komut çubuğunun altındaki varyasyonlar açılan menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="0ada6-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="0ada6-148">Varyasyonlardan birini değiştirilmemiş şekilde bırakarak bir denetim veya temel varyasyon da oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada6-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="0ada6-149">Denemede kullanılacak modülü seçin, üç noktayı (...) seçin ve sonra **Denemeye ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ada6-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="0ada6-150">Tam kapsamlı denemeler için varyasyonları düzenleme</span><span class="sxs-lookup"><span data-stu-id="0ada6-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="0ada6-151">Deneme kapsamını **Denemeyi bağla** sihirbazında **tam** olarak tanımladıysanız, düzenleyici görünümündeyken, özgün varsayımınıza göre her bir varyasyonu düzenlemek için, komut çubuğunun altındaki varyasyonlar açılan menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="0ada6-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="0ada6-152">Her iki durumda da, varyasyonlardan birini değiştirilmemiş şekilde bırakarak bir denetim veya temel varyasyon da oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ada6-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="0ada6-153">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="0ada6-153">Previous step</span></span>
[<span data-ttu-id="0ada6-154">Deneme ayarlama</span><span class="sxs-lookup"><span data-stu-id="0ada6-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="0ada6-155">Sonraki adım</span><span class="sxs-lookup"><span data-stu-id="0ada6-155">Next step</span></span>
[<span data-ttu-id="0ada6-156">Deneme önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="0ada6-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]