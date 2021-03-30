---
title: Yayımlama gruplarıyla çalışma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta grup yayımlama özelliği açıklanmaktadır.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b623573f598f6b21291cafe95fa04e6777cffe11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244851"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="9c61e-103">Yayımlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="9c61e-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9c61e-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta grup yayımlama özelliği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9c61e-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="9c61e-105">Overview</span></span>

<span data-ttu-id="9c61e-106">E-ticaret Web siteleri yıl boyunca yeni içerikle sürekli güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="9c61e-107">Güncelleştirmeler sıklıkla tatiller, mevsimsel pazarlama kampanyaları veya promosyon tarafından başlatılır gibi e-ticaret olaylarının çevresinde toplu olarak yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="9c61e-108">Bu güncelleştirmeler genellikle, Web sitesi içeriği gruplarının (örnekler, sayfalar, resimler, parçalar ve şablonlar) tek bir eylemde aynı anda hazırlanabilsin, doğrulanmalıdır ve yayımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="9c61e-109">Öğeleri, her kümenin kendi yaşam döngüsü olduğu, öğeleri birlikte yayımlayan mantıksal kümeler halinde gruplandırma yeteneği, site yazarlarına birçok avantaj sağlar.</span><span class="sxs-lookup"><span data-stu-id="9c61e-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="9c61e-110">Commerce'da bu mantıksal kümeler, yayınlama grupları olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="9c61e-111">Bunlar, site yazarlarının, kendi yapılandırılabilir, test edilebilir ve yayımlanabilir varlıkları olarak güncelleştirme kümelerini izlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="9c61e-112">Yazarlar, canlı siteyi veya diğer kendi kendini içeren yayınlama gruplarını etkilemeden, aşamalı bir yayınlama grubundaki güncelleştirmelerin önizlemesini yapabilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="9c61e-113">Böylece yazarlar, yayınlama grubundaki tüm öğeleri canlı siteye eşzamanlı olarak yayımlamak için yayınlama eylemini zamanlayabilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="9c61e-114">Olay tabanlı site güncelleştirme kilometre taşları etrafında önemli miktarda yıllık gelir oluşturan kurumsal düzey şirketler için güncelleştirmeleri gruplandırma, önizleme ve zamanlama yeteneği çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="9c61e-115">Şirketler yavaş veya geçersiz kılınan içerik dağıtımları için maliyetler alabilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="9c61e-116">Yayınlama grupları, başlatan, zaman içinde düzenlenen, doğrulanan ve yayımlanan garantiye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9c61e-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="9c61e-117">Bunların büyük veya küçük olup olmadığı, yayınlama grupları yazarların devam eden site güncelleştirme görevlerini düzenlemesine ve basitleştirmesine yardımcı olan değerli bir araç takımı sağlar.</span><span class="sxs-lookup"><span data-stu-id="9c61e-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="9c61e-118">Yayınlama grupları ne zaman kullanılır</span><span class="sxs-lookup"><span data-stu-id="9c61e-118">When to use publish groups</span></span>

<span data-ttu-id="9c61e-119">Birden çok belgeyi birlikte hazırlamak ve yayınlamak gerektiğinde, yayınlama gruplarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="9c61e-120">Örneğin, Web sitenizde her mevsimi bir içerik güncelleştirilebileceği takdirde, bu mevsimlik pazarlama hareketleri için yayınlama grupları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="9c61e-121">"Sonbahar mevsimlik güncelleştirmesi" yayın grubu, yeni mevsimlik görüntüler, mevsimlik pazarlama iletileri bulunan parçalar, mevsimsel ürün koleksiyonları içeren sayfalar veya diğer Web sitesi güncelleştirmeleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="9c61e-122">Yayınlama gruplarının avantajı, çoklu güncelleştirmeleri paralel olarak aşamalayabilmeniz olabilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="9c61e-123">Örneğin, "sonbahar mevsimsel güncelleştirme" yayınlama grubuna ait güncelleştirmeden hemen sonra, belirli bir tatil hafta sonu için içerik güncelleştirmesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="9c61e-124">Bu durumda, sonraki "sonbahar tatil güncelleştirmesi" yayım grubu için içeriği aşamalı olarak, "sonbahar mevsimsel güncelleştirmesi" yayın grubu içeriğini sahne alanı 'nda oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="9c61e-125">Her yayın grubu kendi benzersiz sayfa, resim, parçacık, şablon ve benzer kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="9c61e-126">Bu iki yayınlama grubunu bağımsız olarak, ancak eşzamanlı bir zaman çizelgesinde sahne edebilir, önizleyebilir ve doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="9c61e-127">Böylece, her bir yayınlama grubu sitenizde belirli tarih ve saatlerde canlı duruma geçmek için zamanlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="9c61e-128">Grup yayımlama özelliğini açın</span><span class="sxs-lookup"><span data-stu-id="9c61e-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="9c61e-129">Yayınlama grupları özelliği isteğe bağlıdır ve siteniz için kapatılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="9c61e-130">Commerce geliştirme araçlarında sitenizin grup yayımlama özelliğini etkinleştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="9c61e-131">Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="9c61e-132">**Site ayarları** altında **Özellikler** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="9c61e-133">**Yayın grupları** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9c61e-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="9c61e-134">Yayın grubu oluşturun</span><span class="sxs-lookup"><span data-stu-id="9c61e-134">Create a publish group</span></span>

<span data-ttu-id="9c61e-135">Commerce geliştirme araçlarında sitenizin yayın grup özelliğini oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="9c61e-136">Soldaki gezinti bölmesinde **Yayın Grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="9c61e-137">Komut çubuğunda **yeni** seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="9c61e-138">**Yayınlama grubu oluştur** iletişim kutusunda, **Yayın Grup adı** altında açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="9c61e-139">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="9c61e-140">Yayınlama grubu yazma bağlamını ayarla</span><span class="sxs-lookup"><span data-stu-id="9c61e-140">Set the publish group authoring context</span></span>

<span data-ttu-id="9c61e-141">Commerce'te, varsayılan yazma içeriği canlı site bağlamındadır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="9c61e-142">Canlı site yazma bağlamı, yayınlama grubu kullanmadan web sitenize doğrudan görüntüleyebileceğiniz ve bunlar üzerinde değişiklik yapabileceğiniz varsayılan görünümdür.</span><span class="sxs-lookup"><span data-stu-id="9c61e-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="9c61e-143">Bu, sitenizin yayınlanmış sürümünde en son doğrudan güncelleştirmeleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9c61e-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="9c61e-144">Sol gezinti bölmesinde, **yayınlama grupları** 'nın altındaki içerik denetimi **canlı site** adını gösteriyorsa, canlı site yazma bağlamında çalışıyorsunuz demektir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="9c61e-145">**Canlı site**, bağlam denetiminin varsayılan adıdır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="9c61e-146">Aksi durumda, bağlam denetimi bir yayınlama grubunun adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="9c61e-147">Bir yayınlama grubunda çalışmak için, bunun için yayınlama grubu yazma bağlamına geçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="9c61e-148">Yayınlama grubu bağlamını ayarlamak için aşağıdaki adımlardan birini izleyin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="9c61e-149">Sol gezinti bölmesinde, doğrudan **yayınlama grupları** altında bağlam denetimini seçin ve sonra görünen seçenekler listesinden yayınlama grubunun adını seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="9c61e-150">Bağlam denetimi yeniden adlandırılır ve bir yayınlama grubunun adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="9c61e-151">Sol gezinti bölmesinde, **Yayın grupları**'nı seçin ve sonra **Yayın gruplar**'ı altında, yayınlama grubunun adını seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="9c61e-152">Bağlam denetimi yeniden adlandırılır ve bir yayınlama grubunun adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="9c61e-153">Yayınlama grubu yazma içeriğinizi ayarladıktan sonra, site içeriğini önizlerken ve düzenlerken o yayımlama grubu bağlamında çalışıyorsunuz demektir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="9c61e-154">Varsayılan canlı site yazma bağlamına dönmek için içerik denetimini seçin ve sonra **Canlı site**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="9c61e-155">Yayın grubuna sayfalar veya başka öğeler ekleme</span><span class="sxs-lookup"><span data-stu-id="9c61e-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="9c61e-156">Bir yayın grubu yazma bağlamını seçtikten sonra sol gezinti bölmesindeki içerik denetimi adını gösterir, içeriği varsayılan canlı site bağlamında olduğu gibi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="9c61e-157">Ayrıca, varolan sayfaları veya diğer öğeleri başka yayınlama gruplarından veya canlı site bağlamından ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="9c61e-158">Varolan sayfaları bir yayınlama grubuna kopyalamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="9c61e-159">Kopyalamanın kaynağı olan yazma bağlamını seçin ve sonra sol gezinti bölmesinde **sayfalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="9c61e-160">Bir yayınlama grubuna eklenecek sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="9c61e-161">Komut çubuğunda **yayınlama grubuna Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="9c61e-162">**Bir yayınlama grubu Seç** iletişim kutusunda sayfayı eklemek için yayınlama grubunu seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="9c61e-163">Özelleştirilmiş ürün sayfaları, URL'ler, şablonlar, düzenler, parçalar ve ortam kitaplığı varlıkları oluşturmak ya da bu türlerin varolan öğelerini bir yayınlama grubuna eklemek için aynı temel adımları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="9c61e-164">Yayın grubu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="9c61e-164">Validate a publish group</span></span>

<span data-ttu-id="9c61e-165">Yayın grubu içeriğindeki tüm bağımlılıkların karşılanması ve tüm doğrulamaların geçirildiğinden emin olmak için, bir yayınlama eylemini zamanlamadan önce ele geçirilmesi gereken herhangi bir sorunu tanımlamak üzere doğrulamayı çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c61e-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="9c61e-166">Zamanlamadan önce yayın grubunu doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="9c61e-167">Soldaki gezinti bölmesinde **Yayın Grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="9c61e-168">Doğrulanacak yayın grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="9c61e-169">Komut çubuğunda **Doğrula** seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="9c61e-170">Doğrulama, yayınlama grubundaki tüm içerikte çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="9c61e-171">Başarılı bir yayımlama eyleminin önlenmesi ile ilgili tüm sorunlar, sağ üst tarafta görünen bir bildirim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="9c61e-172">Doğrulama, her zaman bir yayınlama grubu zamanlandığı zaman otomatik olarak çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="9c61e-173">Ancak, bir yayınlama grubunu canlı çalışmaya başlamadan önce düzeltmeniz gereken sorunları tanımlamada yardımcı olduğundan, Komut çubuğundaki **Doğrula** düğmesi kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="9c61e-174">Yayımlama grubunun yayınlanmasını zamanlama</span><span class="sxs-lookup"><span data-stu-id="9c61e-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="9c61e-175">Bir yayınlama grubunun sitenizde etkin olacak şekilde zamanlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="9c61e-176">Soldaki gezinti bölmesinde **Yayın Grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="9c61e-177">**Yayın Grubu** altında, zamanlanacak yayınlama grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="9c61e-178">Komut çubuğunda **Zamanlayı düzenle** seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="9c61e-179">**Zamanlama düzenle** iletişim kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="9c61e-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="9c61e-180">Yayınlama grubunuzun etkin olması gereken tarih ve saati seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="9c61e-181">Bir yayınlama grubunu zamanlamayı iptal etmek için, aynı adımları uygulayın, ancak **zamanlamayı düzenle** iletişim kutusunda **yayınlama grubunu zamanla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9c61e-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="9c61e-182">Çok büyük yayın gruplarının, planlanan zamanı geldiğinde bir dakika veya iki kez yayımlanması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="9c61e-183">Bir yayınlama eyleminin anlık olmadığından ve daha küçük yayınlama gruplarının daha hızlı yayımlanabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9c61e-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="9c61e-184">Yayınlama grubu SSS</span><span class="sxs-lookup"><span data-stu-id="9c61e-184">Publish groups FAQ</span></span>

<span data-ttu-id="9c61e-185">**Bir yayımlama grubunda kaç öğe olabilir?**</span><span class="sxs-lookup"><span data-stu-id="9c61e-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="9c61e-186">Şimdilik, her bir yayınlama grubu için 2.000 madde sınırı vardır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="9c61e-187">Çok büyük yayın gruplarının, planlanan zamanı geldiğinde yayımlanmasının birkaç dakika sürebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9c61e-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="9c61e-188">**Yazılım geliştirme terminolojisinde kod "branşlar" gibi yayınlama grupları mı?**</span><span class="sxs-lookup"><span data-stu-id="9c61e-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="9c61e-189">Evet ve hayır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-189">Yes and no.</span></span> <span data-ttu-id="9c61e-190">Yayınlama grupları, sitenizin çatallanmış sürümleri olarak düşünülebilir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="9c61e-191">Bu şekilde, dallar gibi davranırlar.</span><span class="sxs-lookup"><span data-stu-id="9c61e-191">In that way, they do act like branches.</span></span> <span data-ttu-id="9c61e-192">Ancak, bağımsız öğeler düzeyinde birleştirme kavramı yoktur.</span><span class="sxs-lookup"><span data-stu-id="9c61e-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="9c61e-193">Son yayımlanan madde yalnızca daha önceden var olan öğeleri geçersiz kılar ve en son yayımlama eylemi önceki yayımlama eylemlerinin her zaman yerini alır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="9c61e-194">**Aynı anda canlı çalışmak için iki yayınlama grubunu zamanlayabilir miyim?**</span><span class="sxs-lookup"><span data-stu-id="9c61e-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="9c61e-195">Hayır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-195">No.</span></span> <span data-ttu-id="9c61e-196">Performans ve çakışma nedenleriyle, sistem, zamanlanan yayımlama gruplarını en az beş dakika ayrı olacak şekilde şaşırtmanızı zorlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="9c61e-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="9c61e-197">**İndirimler ve ürün güncelleştirmeleri gibi çok yönlü arka ofis öğelerini planlamak için yayınlama grupları kullanabilir miyim?**</span><span class="sxs-lookup"><span data-stu-id="9c61e-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="9c61e-198">Şu anda, yayınlama grupları özelliği yalnızca Web sitesi içeriğini destekler.</span><span class="sxs-lookup"><span data-stu-id="9c61e-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="9c61e-199">Ancak Microsoft, arka ofis alım satım senaryoları ile tümleştirmenin, çok yönlü kanal kampanyası düzenleme ve otomasyonu için yararlı olabileceğini bilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9c61e-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c61e-200">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9c61e-200">Additional resources</span></span>

[<span data-ttu-id="9c61e-201">İçerik ekleme yolları</span><span class="sxs-lookup"><span data-stu-id="9c61e-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="9c61e-202">Sayfa modeli sözlüğü</span><span class="sxs-lookup"><span data-stu-id="9c61e-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="9c61e-203">Belge durumları ve yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="9c61e-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="9c61e-204">Kanallar arası paylaşımı etkinleştirme ve kullanma</span><span class="sxs-lookup"><span data-stu-id="9c61e-204">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="9c61e-205">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="9c61e-205">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="9c61e-206">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="9c61e-206">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="9c61e-207">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="9c61e-207">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9c61e-208">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="9c61e-208">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]