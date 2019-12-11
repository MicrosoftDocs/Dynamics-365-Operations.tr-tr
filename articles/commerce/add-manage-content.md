---
title: İçerik ekleme yolları
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizde içerik ekleme ve yönetme hakkında bilgi sağlar.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3d91235837aee9ad06466ffe47727b435e39094f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770540"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="cd898-103">İçerik ekleme yolları</span><span class="sxs-lookup"><span data-stu-id="cd898-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cd898-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizde içerik ekleme ve yönetme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd898-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="cd898-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="cd898-105">Overview</span></span>

<span data-ttu-id="cd898-106">Sitenizin görünümünü, hissini ve içeriğini değiştirmek için birçok yol vardır.</span><span class="sxs-lookup"><span data-stu-id="cd898-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="cd898-107">Gerekli özelleştirme düzeyine bağlı olarak, bu değişikliklerin çoğu uygulama geliştiricileri tarafından uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="cd898-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="cd898-108">Örneğin, şablon oluşturmak için hiçbir kod yazılması gerekmez, temaları seçin ve modülleri seçin ve konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="cd898-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="cd898-109">Bunun aksine, e-ticaret yazılım geliştirme seti (SDK) ve Microsoft Dynamics Lifecycle Services (LCS) dağıtım iş akışı kullanılması gerektiğinden, yeni bir tema veya modül oluşturmak için geliştirme becerileri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cd898-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="cd898-110">Aşağıdaki konular sitenizde içerik ekleme ve yönetme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd898-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="cd898-111">Bunlar sitenizin geliştirici gerektirmeyen alanlarına odaklanırlar.</span><span class="sxs-lookup"><span data-stu-id="cd898-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="cd898-112">Gerektiğinde, SDK çalışması gerektiren görevleri kullanıma alır.</span><span class="sxs-lookup"><span data-stu-id="cd898-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="cd898-113">Varolan bir site sayfasındaki metni, resimleri veya videoyu değiştirmek için, bkz [Modüllerle çalış](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="cd898-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="cd898-114">Web içeriği yazarları için marka halinde yazma deneyimi sağlamaya yardımcı olmak için, bkz [Şablonlarla çalışma](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="cd898-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="cd898-115">Site sayfasındaki bölümleri yeniden düzenlemek için, bkz [Düzenlerle çalışma](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="cd898-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="cd898-116">Site sayfalarının yazı tiplerini, renklerini ve genel görünümünü değiştirmek için, bkz [Site teması seçin](select-site-theme.md).</span><span class="sxs-lookup"><span data-stu-id="cd898-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd898-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cd898-117">Additional resources</span></span>

[<span data-ttu-id="cd898-118">Sayfa modeli sözlüğü</span><span class="sxs-lookup"><span data-stu-id="cd898-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="cd898-119">Belge durumları ve yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="cd898-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="cd898-120">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="cd898-120">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="cd898-121">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="cd898-121">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="cd898-122">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="cd898-122">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="cd898-123">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd898-123">Customize site navigation</span></span>](customize-site-navigation.md)
