---
title: Belge durumları ve yaşam döngüsü
description: Bu konu, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914899"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="a1baa-103">Belge durumları ve yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="a1baa-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a1baa-104">Bu konu, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="a1baa-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="a1baa-105">Belge durumu açıklamaları</span><span class="sxs-lookup"><span data-stu-id="a1baa-105">Document state descriptions</span></span>

<span data-ttu-id="a1baa-106">[Sayfa öğeleri](page-elements-overview.md) konusu, içerik yönetim sistemindeki (CMS) çeşitli belge türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="a1baa-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="a1baa-107">Bu belge türlerinin, geliştirme aracında birçok durumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="a1baa-108">Belge durumları veri çakışmalarını önlemeye ve sürüm kontrolünü uygulamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a1baa-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="a1baa-109">Bunlar, belgeleri kimlerin değiştirebileceğini, belgelerin ne zaman değiştirilebileceğini ve değişikliklerin diğer kişiler tarafından ne zaman görüntülenebileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a1baa-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="a1baa-110">Aşağıdaki tablo, ticari sayfa öğelerinin olası belge durumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="a1baa-111">Belge durumu</span><span class="sxs-lookup"><span data-stu-id="a1baa-111">Document state</span></span> | <span data-ttu-id="a1baa-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1baa-112">Description</span></span> |
|---|---|
| <span data-ttu-id="a1baa-113">Kullanıma alındı</span><span class="sxs-lookup"><span data-stu-id="a1baa-113">Checked out</span></span> | <span data-ttu-id="a1baa-114">Bir CMS öğesi size teslim edildiğinde, diğer kimliği doğrulanmış sistem kullanıcıları tarafından düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="a1baa-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="a1baa-115">Öğede yaptığınız tüm değişiklikler yalnızca size görünebilir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="a1baa-116">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="a1baa-116">Checked in</span></span> | <span data-ttu-id="a1baa-117">Bir CMS öğesi iade edildiğinde, tüm değişiklikler kimliği doğrulanmış diğer sistem kullanıcıları tarafından görülebilir ve bu kullanıcılar öğeyi kullanıma alabilir ve düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="a1baa-118">Her iade etme öğenin geçmişinde bir belge sürümü kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1baa-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="a1baa-119">Yayınlanmış</span><span class="sxs-lookup"><span data-stu-id="a1baa-119">Published</span></span> | <span data-ttu-id="a1baa-120">Bir CMS öğesi yayımlandığında, bunlar canlı siteniz ile gönderilir ve internette kimliği doğrulanmamış dış kullanıcılar tarafından bulunabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="a1baa-121">Maddeler yalnızca iade edilmiş olmaları halinde yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="a1baa-122">Kaydedildi</span><span class="sxs-lookup"><span data-stu-id="a1baa-122">Saved</span></span> | <span data-ttu-id="a1baa-123">Kullanıma alınmış CMS öğesine yapılan değişiklikler, öğe iade edilene veya yayımlanmadan önce CMS'e kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="a1baa-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="a1baa-124">Bu kaydedilen değişiklikler, madde iade edilene kadar, diğer kimliği doğrulanmış sistem kullanıcıları tarafından görülemez.</span><span class="sxs-lookup"><span data-stu-id="a1baa-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="a1baa-125">Bunlar, öğe yayımlanana kadar harici kullanıcılar tarafından görülemez.</span><span class="sxs-lookup"><span data-stu-id="a1baa-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="a1baa-126">Kullanıma alma atıldı</span><span class="sxs-lookup"><span data-stu-id="a1baa-126">Discarded check out</span></span> | <span data-ttu-id="a1baa-127">Kullanıma aldığınız bir CMS öğesi iptal edildiğinde, kaydedilen tüm değişiklikler silinir ve öğe en son iade edilen sürüme döner.</span><span class="sxs-lookup"><span data-stu-id="a1baa-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a1baa-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a1baa-128">Additional resources</span></span>

[<span data-ttu-id="a1baa-129">İçerik ekleme yolları</span><span class="sxs-lookup"><span data-stu-id="a1baa-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="a1baa-130">Sayfa modeli sözlüğü</span><span class="sxs-lookup"><span data-stu-id="a1baa-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="a1baa-131">Yayınlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="a1baa-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="a1baa-132">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="a1baa-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="a1baa-133">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="a1baa-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="a1baa-134">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="a1baa-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a1baa-135">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="a1baa-135">Customize site navigation</span></span>](customize-site-navigation.md)
