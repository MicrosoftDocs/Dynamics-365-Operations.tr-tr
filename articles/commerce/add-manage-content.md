---
title: İçerik ekleme yolları
description: Bu konu, Microsoft Dynamics 365 Commerce Site Builder Web yazma aracı kümesi kullanılarak içeriğin nasıl ve nasıl başlanacağı ile ilgili genel bakış ve bağlantı sağlar.
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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 802a41b8c55e65eee58d26137c2f160b69847010
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973992"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="27364-103">İçerik ekleme yolları</span><span class="sxs-lookup"><span data-stu-id="27364-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27364-104">Bu konu Microsoft Dynamics 365 Commerce site yapıcısı web yazma araç takımı kullanarak içeriği yönetme hakkında genel bakış ve bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="27364-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

## <a name="overview"></a><span data-ttu-id="27364-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="27364-105">Overview</span></span>

<span data-ttu-id="27364-106">Sitenizin görünümünü, hissini ve içeriğini değiştirmek için birçok yol vardır.</span><span class="sxs-lookup"><span data-stu-id="27364-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="27364-107">Bu değişikliklerin çoğu, gerekli özelleştirme düzeyine bağlı olarak, Site Builder içinde bulunan Web yazma araç takımı içindeki geliştiriciler tarafından gerçekleştirilebilir Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27364-107">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="27364-108">Site Builder, şablon oluşturmanızı, temaları seçmenizi ve herhangi bir kod yazmadan modülleri seçmenizi ve yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="27364-108">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="27364-109">Bunun aksine, e-ticaret yazılım geliştirme seti (SDK) ve Microsoft Dynamics Lifecycle Services (LCS) dağıtım iş akışı kullanılması gerektiğinden, yeni bir tema veya modül oluşturmak için geliştirme becerileri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="27364-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="27364-110">Aşağıdaki konular, Site içeriğinin nasıl ekleneceğini ve yönetileceğini anlamaya başlamak için puanlar atmasına uygundur.</span><span class="sxs-lookup"><span data-stu-id="27364-110">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="27364-111">Listelenen pek çok konu, sitenizin geliştirici gerektirmeyen alanlarına odaklanırlar.</span><span class="sxs-lookup"><span data-stu-id="27364-111">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="27364-112">Bazı adres temel içerik düzenleme, diğerleri Site Yöneticisi görevlerine odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="27364-112">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="27364-113">Bu konuların her biri, belirli görevlerin SDK çalışması gerektirebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="27364-113">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="27364-114">Her konu, bir siteyi önceden sağlamış olduğunuzu ve siteniz için Site Builder Araç Takımı'na erişim verildiğini varsayar.</span><span class="sxs-lookup"><span data-stu-id="27364-114">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="27364-115">Başlamak için aşağıdaki konulardan birini seçin.</span><span class="sxs-lookup"><span data-stu-id="27364-115">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="27364-116">Site Builder ve bu dokümentasyonda kullanılan içerik yönetim terminolojisini öğrenmek bk. [Sayfa model sözlüğü](page-elements-overview.md).</span><span class="sxs-lookup"><span data-stu-id="27364-116">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="27364-117">Modüllerin içerik yönetimi iş akışları içinde nasıl çalıştığını anlamak için bk. [Modüllerle çalışmka](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="27364-117">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="27364-118">Varolan bir site sayfasındaki metni, resimleri veya videoyu değiştirmek için, bkz [Modüllerle çalış](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="27364-118">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="27364-119">Parçaların içerik yönetimini daha etkili ve esnek hale getirme şeklini görmek için bk. [Parçalarla çalışmak](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="27364-119">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="27364-120">Web içerik yazarlarının marka yazarlığı deneyimini başarıyla sağlamalarına yardımcı olmak için bkz. [Şablonlar ve düzenler genel bakışı](templates-layouts-overview.md) ve [Şablonlar ile çalışmak](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="27364-120">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="27364-121">Site sayfasındaki bölümleri yeniden düzenlemek için, bkz [Düzenlerle çalışma](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="27364-121">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="27364-122">Site sayfalarının yazı tiplerini, renklerini ve genel görünümünü değiştirmek için, bkz [Site teması seçin](select-site-theme.md) veya [CSS geçersiz kılma dosyalarıyla çalışmak](css-override-files.md).</span><span class="sxs-lookup"><span data-stu-id="27364-122">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="27364-123">Yeniden düzenlemek veya yeni gezinti seçenekleri eklemek için bk. [Site gezintisini özelleştirmek](customize-site-navigation.md).</span><span class="sxs-lookup"><span data-stu-id="27364-123">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="27364-124">Ardışık web içeriği değişikliklerini aşamalandırma, önizleme ve yayınlama için bk. [Yayınlama gruplarıyla çalışmak](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="27364-124">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27364-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="27364-125">Additional resources</span></span>

[<span data-ttu-id="27364-126">Yazma sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="27364-126">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="27364-127">Sayfa modeli sözlüğü</span><span class="sxs-lookup"><span data-stu-id="27364-127">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="27364-128">Belge durumları ve yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="27364-128">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="27364-129">Kanallar arası paylaşımı etkinleştirme ve kullanma</span><span class="sxs-lookup"><span data-stu-id="27364-129">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)
