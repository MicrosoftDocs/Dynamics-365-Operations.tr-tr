---
title: Logo ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914639"
---
# <a name="add-a-logo"></a><span data-ttu-id="6656e-103">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="6656e-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6656e-104">Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6656e-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6656e-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6656e-105">Overview</span></span>

<span data-ttu-id="6656e-106">Sitenizi yapılandırdığınızda, büyük olasılıkla yaptığınız ilk şeyden biri şirketinizi veya marka amblemini sitenin başlığına eklemektir.</span><span class="sxs-lookup"><span data-stu-id="6656e-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="6656e-107">Dynamics 365 Commerce çevrimiçi başlangıç kiti, bu görevi kolaylaştıran bir modül sağlar.</span><span class="sxs-lookup"><span data-stu-id="6656e-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="6656e-108">Bir logoyu doğrudan bir şablon, düzen veya sayfaya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6656e-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="6656e-109">Bu şekilde, belirli sayfalarda veya sayfa gruplarında görünen logoyu kolayca değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6656e-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="6656e-110">Ancak bu konu, logonuzu sitenizdeki tüm sayfalarda yeniden kullanılabilen bir başlık parçasına eklediğiniz en sık kullanılan senaryoyu kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6656e-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6656e-111">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="6656e-111">Prerequisites</span></span>

<span data-ttu-id="6656e-112">Sitenizin tüm sayfalarına logo ekleyebilmeniz için önce bu görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6656e-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="6656e-113">Ambleminizi, **varlıklar** sayfasından erişebileceğiniz dijital varlıklar yöneticisine yükleyin.</span><span class="sxs-lookup"><span data-stu-id="6656e-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="6656e-114">Başlık parçası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6656e-114">Create a header fragment.</span></span> <span data-ttu-id="6656e-115">Parçaların nasıl oluşturulacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Parçalarla çalışma](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="6656e-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="6656e-116">Başlık parçasının, mizanpaj ve modül seçenekleri için sitenizin sayfalarının kullandığı şablona dahil edin.</span><span class="sxs-lookup"><span data-stu-id="6656e-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="6656e-117">Şablonlar hakkında daha fazla bilgi için, bkz. [Şablonlarla çalışma](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="6656e-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="6656e-118">Üstbilgi parçasına Logo ekle</span><span class="sxs-lookup"><span data-stu-id="6656e-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="6656e-119">Sitenizin üstbilgi parçasına logo eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6656e-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="6656e-120">Soldaki gezinti bölmesinde, **Parçalar**'ı seçin ve sonra oluşturduğunuz başlık parçasını seçin.</span><span class="sxs-lookup"><span data-stu-id="6656e-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="6656e-121">**Ödeme yap** seçin.</span><span class="sxs-lookup"><span data-stu-id="6656e-121">Select **Check out**.</span></span>
3. <span data-ttu-id="6656e-122">**Üstbilgi** yuvasını ve **amblem** yuvasını genişletin.</span><span class="sxs-lookup"><span data-stu-id="6656e-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="6656e-123">**Logo** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6656e-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="6656e-124">Logo modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6656e-124">Select the logo module.</span></span>
6. <span data-ttu-id="6656e-125">Daha sonra sağdaki Özellikler bölmesinde, logo modülünü logonuzu gösterecek şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="6656e-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="6656e-126">Üstbilgi parçasını kaydedin, giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="6656e-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="6656e-127">Güncelleştirilmiş başlık parçasını yayımladıktan sonra, başlık parçasını içeren şablonu kullanan tüm site sayfaları logonuzu gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="6656e-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6656e-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6656e-128">Additional resources</span></span>

[<span data-ttu-id="6656e-129">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="6656e-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="6656e-130">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="6656e-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6656e-131">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="6656e-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6656e-132">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="6656e-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="6656e-133">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="6656e-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="6656e-134">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="6656e-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6656e-135">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="6656e-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

