---
title: Logo ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416374"
---
# <a name="add-a-logo"></a><span data-ttu-id="00716-103">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="00716-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="00716-104">Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="00716-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="00716-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="00716-105">Overview</span></span>

<span data-ttu-id="00716-106">Sitenizi yapılandırdığınızda, büyük olasılıkla yaptığınız ilk şeyden biri şirketinizi veya marka amblemini sitenin başlığına eklemektir.</span><span class="sxs-lookup"><span data-stu-id="00716-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="00716-107">Dynamics 365 Commerce çevrimiçi modül kitaplığı, bu görevi kolaylaştıran bir modül sağlar.</span><span class="sxs-lookup"><span data-stu-id="00716-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="00716-108">Bir logoyu doğrudan bir şablon, düzen veya sayfaya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00716-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="00716-109">Bu şekilde, belirli sayfalarda veya sayfa gruplarında görünen logoyu kolayca değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00716-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="00716-110">Ancak bu konu, logonuzu sitenizdeki tüm sayfalarda yeniden kullanılabilen bir başlık parçasına eklediğiniz en sık kullanılan senaryoyu kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="00716-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="00716-111">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="00716-111">Prerequisites</span></span>

<span data-ttu-id="00716-112">Sitenizin tüm sayfalarına logo ekleyebilmeniz için önce bu görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="00716-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="00716-113">Logonuzu ortam kitaplığı 'na yükleyin.</span><span class="sxs-lookup"><span data-stu-id="00716-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="00716-114">Başlık parçası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00716-114">Create a header fragment.</span></span> <span data-ttu-id="00716-115">Parçaların nasıl oluşturulacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Parçalarla çalışma](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="00716-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="00716-116">Başlık parçasının, mizanpaj ve modül seçenekleri için sitenizin sayfalarının kullandığı şablona dahil edin.</span><span class="sxs-lookup"><span data-stu-id="00716-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="00716-117">Şablonlar hakkında daha fazla bilgi için, bkz. [Şablonlarla çalışma](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="00716-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="00716-118">Üstbilgi parçasına Logo ekle</span><span class="sxs-lookup"><span data-stu-id="00716-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="00716-119">Sitenizin üstbilgi parçasına logo eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00716-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="00716-120">Soldaki gezinti bölmesinde **Parçalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="00716-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="00716-121">Oluşturduğunuz başlığı seçin ve sonra **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="00716-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="00716-122">Üstbilgi modülünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="00716-122">Expand the header module.</span></span>
1. <span data-ttu-id="00716-123">Üstbilgi modülünün Özellik bölmesinde logo için bir resim ve bağlantı sağlayın.</span><span class="sxs-lookup"><span data-stu-id="00716-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="00716-124">Başlık parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="00716-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="00716-125">Güncelleştirilmiş başlık parçasını yayımladıktan sonra, başlık parçasını içeren şablonu kullanan tüm site sayfaları logonuzu gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="00716-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00716-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="00716-126">Additional resources</span></span>

[<span data-ttu-id="00716-127">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="00716-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="00716-128">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="00716-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="00716-129">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="00716-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="00716-130">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="00716-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="00716-131">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="00716-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="00716-132">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="00716-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="00716-133">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="00716-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

