---
title: İçerik ekleme yolları
description: Bu konu, Microsoft Dynamics 365 Commerce Site Builder Web yazma aracı kümesi kullanılarak içeriğin nasıl ve nasıl başlanacağı ile ilgili genel bakış ve bağlantı sağlar.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e6794e528d9fa6066d7246e99a3307bb1bdc9c78
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797587"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="04848-103">İçerik ekleme yolları</span><span class="sxs-lookup"><span data-stu-id="04848-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04848-104">Bu konu Microsoft Dynamics 365 Commerce site yapıcısı web yazma araç takımı kullanarak içeriği yönetme hakkında genel bakış ve bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="04848-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

<span data-ttu-id="04848-105">Sitenizin görünümünü, hissini ve içeriğini değiştirmek için birçok yol vardır.</span><span class="sxs-lookup"><span data-stu-id="04848-105">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="04848-106">Bu değişikliklerin çoğu, gerekli özelleştirme düzeyine bağlı olarak, Site Builder içinde bulunan Web yazma araç takımı içindeki geliştiriciler tarafından gerçekleştirilebilir Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="04848-106">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="04848-107">Site Builder, şablon oluşturmanızı, temaları seçmenizi ve herhangi bir kod yazmadan modülleri seçmenizi ve yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="04848-107">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="04848-108">Bunun aksine, e-ticaret yazılım geliştirme seti (SDK) ve Microsoft Dynamics Lifecycle Services (LCS) dağıtım iş akışı kullanılması gerektiğinden, yeni bir tema veya modül oluşturmak için geliştirme becerileri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="04848-108">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="04848-109">Aşağıdaki konular, Site içeriğinin nasıl ekleneceğini ve yönetileceğini anlamaya başlamak için puanlar atmasına uygundur.</span><span class="sxs-lookup"><span data-stu-id="04848-109">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="04848-110">Listelenen pek çok konu, sitenizin geliştirici gerektirmeyen alanlarına odaklanırlar.</span><span class="sxs-lookup"><span data-stu-id="04848-110">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="04848-111">Bazı adres temel içerik düzenleme, diğerleri Site Yöneticisi görevlerine odaklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="04848-111">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="04848-112">Bu konuların her biri, belirli görevlerin SDK çalışması gerektirebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="04848-112">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="04848-113">Her konu, bir siteyi önceden sağlamış olduğunuzu ve siteniz için Site Builder Araç Takımı'na erişim verildiğini varsayar.</span><span class="sxs-lookup"><span data-stu-id="04848-113">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="04848-114">Başlamak için aşağıdaki konulardan birini seçin.</span><span class="sxs-lookup"><span data-stu-id="04848-114">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="04848-115">Site Builder ve bu dokümentasyonda kullanılan içerik yönetim terminolojisini öğrenmek bk. [Sayfa model sözlüğü](page-elements-overview.md).</span><span class="sxs-lookup"><span data-stu-id="04848-115">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="04848-116">Modüllerin içerik yönetimi iş akışları içinde nasıl çalıştığını anlamak için bk. [Modüllerle çalışmka](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="04848-116">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="04848-117">Varolan bir site sayfasındaki metni, resimleri veya videoyu değiştirmek için, bkz [Modüllerle çalış](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="04848-117">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="04848-118">Parçaların içerik yönetimini daha etkili ve esnek hale getirme şeklini görmek için bk. [Parçalarla çalışmak](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="04848-118">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="04848-119">Web içerik yazarlarının marka yazarlığı deneyimini başarıyla sağlamalarına yardımcı olmak için bkz. [Şablonlar ve düzenler genel bakışı](templates-layouts-overview.md) ve [Şablonlar ile çalışmak](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="04848-119">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="04848-120">Site sayfasındaki bölümleri yeniden düzenlemek için, bkz [Düzenlerle çalışma](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="04848-120">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="04848-121">Site sayfalarının yazı tiplerini, renklerini ve genel görünümünü değiştirmek için, bkz [Site teması seçin](select-site-theme.md) veya [CSS geçersiz kılma dosyalarıyla çalışmak](css-override-files.md).</span><span class="sxs-lookup"><span data-stu-id="04848-121">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="04848-122">Yeniden düzenlemek veya yeni gezinti seçenekleri eklemek için bk. [Site gezintisini özelleştirmek](customize-site-navigation.md).</span><span class="sxs-lookup"><span data-stu-id="04848-122">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="04848-123">Ardışık web içeriği değişikliklerini aşamalandırma, önizleme ve yayınlama için bk. [Yayınlama gruplarıyla çalışmak](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="04848-123">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04848-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="04848-124">Additional resources</span></span>

[<span data-ttu-id="04848-125">Yazma sayfasına genel bakış</span><span class="sxs-lookup"><span data-stu-id="04848-125">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="04848-126">Sayfa modeli sözlüğü</span><span class="sxs-lookup"><span data-stu-id="04848-126">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="04848-127">Belge durumları ve yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="04848-127">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="04848-128">Kanallar arası paylaşımı etkinleştirme ve kullanma</span><span class="sxs-lookup"><span data-stu-id="04848-128">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
