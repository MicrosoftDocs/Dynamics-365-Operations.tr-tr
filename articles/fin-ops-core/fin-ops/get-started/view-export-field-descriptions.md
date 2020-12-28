---
title: Alan açıklamalarını görüntüleme ve dışarı aktarma
description: Bu makalede, alan açıklamalarının nasıl görüntüleneceği ve açıklamaları dışa aktarmak için Alan açıklamalarının nasıl kullanılacağı açıklanmaktadır.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7a9e12eae7065bb37fc0ddbb579a0437120c165
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693533"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="e5ef2-103">Alan açıklamalarını görüntüleme ve dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="e5ef2-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5ef2-104">Bu makalede, alan açıklamalarının nasıl görüntüleneceği ve açıklamaları dışa aktarmak için Alan açıklamalarının nasıl kullanılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="e5ef2-105">Daha karmaşık alanlardan bazılarında alan açıklamaları vardır.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="e5ef2-106">Bu açıklamalar, alanın üzerine geldiğinizde görünür.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="e5ef2-107">Ayrıca, **Alan açıklamaları** sayfasından alan açıklamalarını görüntüleyebilir ve dışa aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="e5ef2-108">Tüm sayfaların alan açıklamaları yoktur.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="e5ef2-109">Kullanımı belirgin olan alanların değil, yalnızca daha karmaşık alanların açıklamalarını sağlamak istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="e5ef2-110">Bu nedenle, bazı sayfalarda alan açıklamaları bulunmaz, bazı sayfalarda birkaç açıklama vardır ve parametre sayfaların çoğunda olduğu gibi daha karmaşık sayfalarda birçok açıklama vardır.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="e5ef2-111">Geliştirme ortamına erişiminiz varsa yeni alan açıklamalarınızı ekleyebilirsiniz ve mevcut açıklamaları özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="e5ef2-112">Örneğin, bir alan açıklamasına şirkete özgü bilgiler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="e5ef2-113">Daha fazla bilgi için bkz. [Alan açıklamalarını özelleştirme](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="e5ef2-113">For more information, see [Customize field descriptions](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="e5ef2-114">Kullanıcı arabirimindeki alan açıklamalarına bakın</span><span class="sxs-lookup"><span data-stu-id="e5ef2-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="e5ef2-115">Alanın üzerine getirerek alan açıklamaları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="e5ef2-116">Açıklama yoksa, üzerine getirdiğinizde alan adını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="e5ef2-117">Dynamics AX 7.0'da (Şubat 2016) alan açıklamaları, yalnızca **Alan açıklamaları** sayfasında görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="e5ef2-118">Aşağıdaki çizim **Sayım sırasında madde kilitlemesi** alanı üzerine getirdiğinizde görüntülenen alan açıklamalarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="e5ef2-119">[![Alan açıklaması örneği](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="e5ef2-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="e5ef2-120">Alan açıklamaları sayfasını kullanarak alan yardımını görüntüleme ve dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="e5ef2-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="e5ef2-121">**Alan açıklamaları** sayfası, alan açıklamalarını görüntülemenizi ve dışarı aktarmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="e5ef2-122">Tek seferde bir sayfa için mevcut olan açıklamaları görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="e5ef2-123">Bir sayfanın açıklamalarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e5ef2-123">View the descriptions for a page</span></span>

<span data-ttu-id="e5ef2-124">Bir sayfanın açıklamalarını görüntülemek için, aşağıdaki adımı izleyin.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="e5ef2-125">**Sayfa seç** alanında, sayfanın adını yazın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="e5ef2-126">Alternatif olarak, tüm sayfaların bir listesini açmak için oka tıklayın ve ardından listeye göz atın veya filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="e5ef2-127">Kullanıcı arabiriminde (UI) gösterilen sayfa adını (örneğin, **Müşteriler**) veya bir sayfaya sağ tıkladığınızda görebileceğiniz (örneğin, **CustTable**) kod adını (AOT adı) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="e5ef2-128">Sayfalar listesini filtrelemenin çeşitli yolları hakkında daha fazla bilgi için bu makalenin ilerisindeki "Sayfa arama" bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="e5ef2-129">**Açıklama olmayan alanları ekle** seçeneğini **Evet** olarak ayarlarsanız, sayfadaki tüm alanlar, alan açıklaması olmasa bile gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="e5ef2-130">Bir sayfanın açıklamalarını dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="e5ef2-130">Export the descriptions for a page</span></span>

<span data-ttu-id="e5ef2-131">Bir sayfanın açıklamalarını dışa aktarmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="e5ef2-132">**Sayfa seçin** alanından bir sayfa seçin.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="e5ef2-133">Sağ üst köşedeki **Microsoft Office'te aç** düğmesine tıklayın ve ardından **FieldDescriptionTmp** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="e5ef2-134">Sayfa arama</span><span class="sxs-lookup"><span data-stu-id="e5ef2-134">Searching for a page</span></span>

<span data-ttu-id="e5ef2-135">**Sayfa seçin** alanında sayfa aramanın çeşitli yolları vardır.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="e5ef2-136">Çoğu durumda, açılır listeyi açmak için **Sayfa seçin** alanındaki oka tıklamanız ve ardından filtrelenmiş sayfa listesinden seçim yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="e5ef2-137">Adın bir bölümünü yazın ve ardından filtrelenmiş sayfa listesinden seçim yapmak için açılır listeyi açın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="e5ef2-138">Açılır listeyi açın ve ardından listenin en üstündeki **Sayfa adı** başlığına veya **Sayfa AOT adı** başlığına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="e5ef2-139">**Sayfa adı şununla başlar** gibi gelişmiş filtreleme seçeneklerini kullanabileceğiniz bir iletişim görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="e5ef2-140">Sayfanın tam adını yazın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-140">Type the full name of the page.</span></span> <span data-ttu-id="e5ef2-141">Bu seçeneği kullandığınızda, alan açıklamaları gösterilse bile açılır listeyi açıp listedeki diğer sayfalara da bakmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="e5ef2-142">Ad için tek bir eşleşme varsa bu sayfanın alan açıklamaları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="e5ef2-143">Birden fazla tam eşleşme varsa hiçbir açıklama gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="e5ef2-144">Açılır listeyi açıp istediğiniz sayfayı seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="e5ef2-145">Yazdığınız ad, başka bir sayfanın adının parçası ise sayfanızın açıklamalarını görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="e5ef2-146">Ancak, açılır listeyi açarsanız bu adı içeren ek sayfaları da görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="e5ef2-147">Örneğin **Sayfa seçin** alanında **Sayım** yazarken hiçbir açıklama gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="e5ef2-148">Açılır listeyi açın ve adı **Sayım** olan iki sayfa ve adı, "Sayım" kelimesini içeren birkaç sayfa olduğunu görün.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="e5ef2-149">AOT adı **InventJournalCount** olan sayfayı seçerseniz, bu sayfanın alan açıklamaları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="e5ef2-150">Ancak açılır listeyi yeniden açarsanız listenin artık AOT adında "InventJournalCount" geçen tüm sayfaları içerdiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e5ef2-151">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="e5ef2-151">Troubleshooting</span></span>

<span data-ttu-id="e5ef2-152">Bu bölüm, alan açıklamalarını kullanırken karşılaşabileceğiniz sorunları gidermenize yardımcı olacak bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="e5ef2-153">Bir alanın açıklamasını bulamıyorum</span><span class="sxs-lookup"><span data-stu-id="e5ef2-153">I can't find a field description</span></span>

<span data-ttu-id="e5ef2-154">Daha karmaşık alanların açıklamalarını eklemeye devam ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="e5ef2-155">Belirli bir alanla ilgili yardım gereksiniminiz varsa bu konuya yorum ekleyerek bize bildirin.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="e5ef2-156">Alan açıklaması yardımcı olmuyor</span><span class="sxs-lookup"><span data-stu-id="e5ef2-156">The field description isn't helpful</span></span>

<span data-ttu-id="e5ef2-157">Bu konuya yorum ekleyerek bize bildirin.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="e5ef2-158">Yapabiliyorsanız ihtiyacınız olan ek bilgileri açıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="e5ef2-159">Alan açıklamaları sayfasında bir alanı bulamıyorum</span><span class="sxs-lookup"><span data-stu-id="e5ef2-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="e5ef2-160">Bir sayfadaki tüm alanları görüntülemek için **Açıklama olmayan alanları dahil et** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="e5ef2-161">Doğru sayfayı seçtiğinizi doğrulamak için **Sayfa seçin** alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="e5ef2-162">Yazdığınız ad, başka bir alan adının parçası ise, daha uzun ada sahip olan sayfayı seçmiş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="e5ef2-163">Alan açıklamaları sayfasında bir sayfayı bulamıyorum.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="e5ef2-164">Sayfaları aramanın çeşitli yolları hakkında daha fazla bilgi için, bu makalede daha önceki "Sayfa arama" bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="e5ef2-165">Sayfanın tam adını yazdıysanız ve aynı adlı birden fazla sayfa varsa alan açıklamaları gösterilemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="e5ef2-166">**Sayfa seçin** alanındaki oka tıklayarak kullanılabilir sayfaların filtrelenmiş bir listesini açın.</span><span class="sxs-lookup"><span data-stu-id="e5ef2-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5ef2-167">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e5ef2-167">Additional resources</span></span>

[<span data-ttu-id="e5ef2-168">Alan açıklamalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="e5ef2-168">Customize field descriptions</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
