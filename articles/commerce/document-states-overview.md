---
title: Belge durumları ve yaşam döngüsü
description: Bu konu, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.
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
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974042"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="b7b6f-103">Belge durumları ve yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="b7b6f-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7b6f-104">Bu konu, Microsoft Dynamics 365 Commerce içindeki sayfa öğelerinin çeşitli belge durumlarını kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="b7b6f-105">Belge durumu açıklamaları</span><span class="sxs-lookup"><span data-stu-id="b7b6f-105">Document state descriptions</span></span>

<span data-ttu-id="b7b6f-106">[Sayfa öğeleri](page-elements-overview.md) konusu, içerik yönetim sistemindeki (CMS) çeşitli belge türlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="b7b6f-107">Bu belge türlerinin, geliştirme aracında birçok durumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="b7b6f-108">Belge durumları veri çakışmalarını önlemeye ve sürüm kontrolünü uygulamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="b7b6f-109">Bunlar, belgeleri kimlerin değiştirebileceğini, belgelerin ne zaman değiştirilebileceğini ve değişikliklerin diğer kişiler tarafından ne zaman görüntülenebileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="b7b6f-110">Aşağıdaki tablo, ticari sayfa öğelerinin olası belge durumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="b7b6f-111">Belge durumu</span><span class="sxs-lookup"><span data-stu-id="b7b6f-111">Document state</span></span>      | <span data-ttu-id="b7b6f-112">Site oluşturucu eylemi</span><span class="sxs-lookup"><span data-stu-id="b7b6f-112">Site builder action</span></span>        | <span data-ttu-id="b7b6f-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7b6f-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="b7b6f-114">Kullanıma alındı</span><span class="sxs-lookup"><span data-stu-id="b7b6f-114">Checked out</span></span>         | <span data-ttu-id="b7b6f-115">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-115">Select **Edit**.</span></span>           | <span data-ttu-id="b7b6f-116">Uygun belge kullanımınıza alınır.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="b7b6f-117">Belge bu durumundayken, diğer kimliği doğrulanmış sistem kullanıcıları tarafından değiştirilemez ve belgede yaptığınız tüm değişiklikler yalnızca size gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="b7b6f-118">Kaydedildi</span><span class="sxs-lookup"><span data-stu-id="b7b6f-118">Saved</span></span>               | <span data-ttu-id="b7b6f-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-119">Select **Save**.</span></span>           | <span data-ttu-id="b7b6f-120">Kullanıma alınmış belgede yapılan değişiklikler veritabanına kaydedilir ancak belge henüz iade edilmez veya yayımlanmaz.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="b7b6f-121">Kaydedilen değişiklikler, yazar **Düzenlemeyi bitir** seçeneğini seçene kadar diğer kimliği doğrulanmış sistem kullanıcıları tarafından görülemez.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="b7b6f-122">Bunlar, öğe yayımlanana kadar harici kullanıcılar tarafından görülemez.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="b7b6f-123">Kullanıma alma atıldı</span><span class="sxs-lookup"><span data-stu-id="b7b6f-123">Discarded check out</span></span> | <span data-ttu-id="b7b6f-124">**Düzenlemeleri at**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="b7b6f-125">Kullanıma aldığınız belgede yapılan tüm değişiklikler atılır ve öğe iade edilen son sürüme geri döner.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="b7b6f-126">Teslim edildi</span><span class="sxs-lookup"><span data-stu-id="b7b6f-126">Checked in</span></span>          | <span data-ttu-id="b7b6f-127">**Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-127">Select **Finish editing**.</span></span> | <span data-ttu-id="b7b6f-128">Düzenlenen belge iade edilir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-128">The edited document is checked in.</span></span> <span data-ttu-id="b7b6f-129">Tüm değişiklikler, kimliği doğrulanmış diğer sistem kullanıcıları tarafından görülebilir ve bu kullanıcılar belgeyi düzenleyebilir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="b7b6f-130">Her iade etme öğenin geçmişinde bir belge sürümü kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="b7b6f-131">Yayınlanmış</span><span class="sxs-lookup"><span data-stu-id="b7b6f-131">Published</span></span>           | <span data-ttu-id="b7b6f-132">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-132">Select **Publish**.</span></span>        | <span data-ttu-id="b7b6f-133">Belge yayımlanır ve değişiklikler yayımlanmış sitenize itilir ve harici kullanıcılar tarafından keşfedilebilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="b7b6f-134">Öğeler yalnızca **Düzenlemeyi bitir** seçilerek iade edilmiş olmaları durumunda yayımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="b7b6f-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b7b6f-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b7b6f-135">Additional resources</span></span>

[<span data-ttu-id="b7b6f-136">İçerik ekleme yolları</span><span class="sxs-lookup"><span data-stu-id="b7b6f-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="b7b6f-137">Sayfa modeli sözlüğü</span><span class="sxs-lookup"><span data-stu-id="b7b6f-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="b7b6f-138">Yayımlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="b7b6f-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="b7b6f-139">Kanallar arası paylaşımı etkinleştirme ve kullanma</span><span class="sxs-lookup"><span data-stu-id="b7b6f-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="b7b6f-140">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="b7b6f-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="b7b6f-141">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="b7b6f-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="b7b6f-142">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="b7b6f-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b7b6f-143">Site gezintisini özelleştirme</span><span class="sxs-lookup"><span data-stu-id="b7b6f-143">Customize site navigation</span></span>](customize-site-navigation.md)
