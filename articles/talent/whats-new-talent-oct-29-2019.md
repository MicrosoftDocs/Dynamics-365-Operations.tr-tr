---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (29 Ekim 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897454"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="c8029-103">Dynamics 365 Talent'taki yenilikler veya değişiklikler (29 Ekim 2019)</span><span class="sxs-lookup"><span data-stu-id="c8029-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

<span data-ttu-id="c8029-104">Bu konuda, Dynamics 365 Talent'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c8029-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c8029-105">Attract'te değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c8029-105">Changes in Attract</span></span>

<span data-ttu-id="c8029-106">Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.</span><span class="sxs-lookup"><span data-stu-id="c8029-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="c8029-107">Onboard'taki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c8029-107">Changes in Onboard</span></span>

<span data-ttu-id="c8029-108">Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.</span><span class="sxs-lookup"><span data-stu-id="c8029-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="c8029-109">Core HR içindeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="c8029-109">Changes in Core HR</span></span>

<span data-ttu-id="c8029-110">Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2586 için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c8029-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="c8029-111">Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="c8029-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="c8029-112">Rolü olmayan tarafları sil varsayılan olarak açık olmalı (371233)</span><span class="sxs-lookup"><span data-stu-id="c8029-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="c8029-113">Talent'te yeni bir ortam hazırladığınızda **Rol yoksa tarafları sil** varsayılan olarak açıktır.</span><span class="sxs-lookup"><span data-stu-id="c8029-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="c8029-114">Bir çalışanı sildiğinizde çalışanla ilişkili taraf bu ayar açık olmadıkça kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="c8029-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="c8029-115">Bu değişiklik, çalışanları içe aktarmanız, değiştirmeniz veya yeniden içe aktarmanız gerektiğinde genel adres defterindeki tekrarlanan kayıtları sınırlar.</span><span class="sxs-lookup"><span data-stu-id="c8029-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="c8029-116">Taslak ve iptal edilmiş izin isteklerinin Common Data Service'te silinmesine izin verilmelidir (376999)</span><span class="sxs-lookup"><span data-stu-id="c8029-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="c8029-117">Bu değişiklikle artık **Taslak** veya **İptal edildi** durumundaki izin istekleri Common Data Service'te silinebilir.</span><span class="sxs-lookup"><span data-stu-id="c8029-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="c8029-118">Özel alanlar formunda Uygula'ya tıkladıktan sonra özel alanlardaki ek liste değerleri Common Data Service'te yansıtılmıyor (379599)</span><span class="sxs-lookup"><span data-stu-id="c8029-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="c8029-119">Common Data Service ile önceden eşitlenen mevcut özel alana yeni liste değerleri eklediğinizde değişikliklerinizi **Özel alanlar** formunda uyguladıktan sonra bunlar artık Common Data Service'te kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c8029-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="c8029-120">Birden fazla çalışan varken tüzel kişilikler arasında işe alım yapılacaklar listeleri uygulama (371270)</span><span class="sxs-lookup"><span data-stu-id="c8029-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="c8029-121">Bu haftanın sürümünde, **Çalışan formu > Yapılacaklar listeleri**'nde birden fazla çalışana yapılacaklar listeleri uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8029-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="c8029-122">Kazançlar açık kayıt önizlemesi özelliği kaldırıldı</span><span class="sxs-lookup"><span data-stu-id="c8029-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="c8029-123">Microsoft, [Core HR operasyonel mükemmellik sağlama konusunda stratejik yatırımlar](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog gönderisindeki duyurumuzla birlikte genel önizlemedeki kazançlar açık kayıt özelliğini kaldırdı.</span><span class="sxs-lookup"><span data-stu-id="c8029-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="c8029-124">Gelecekte yeni işlevler yayımlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="c8029-124">New functionality will be released in the future.</span></span> <span data-ttu-id="c8029-125">Kazançlar açık kayıt özelliğinin üretim kullanımı desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c8029-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c8029-126">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="c8029-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="c8029-127">Performans incelemelerini yazdırma</span><span class="sxs-lookup"><span data-stu-id="c8029-127">Print performance reviews</span></span>

<span data-ttu-id="c8029-128">Dynamics 365: 2019 sürüm dalgası 2 planındaki [Performans incelemelerini yazdır](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c8029-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="c8029-129">Özellik yönetimi çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="c8029-129">Feature management workspace</span></span>

<span data-ttu-id="c8029-130">Özellikler, her sürümüne eklenir ve güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c8029-130">Features are added and updated in every release.</span></span> <span data-ttu-id="c8029-131">Özellik yönetimi deneyimi, her sürümde teslim edilen özelliklerin listesini görüntüleyebileceğiniz bir çalışma alanı sağlar.</span><span class="sxs-lookup"><span data-stu-id="c8029-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="c8029-132">Varsayılan olarak, bu özellikler kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="c8029-132">By default, new features are turned off.</span></span> <span data-ttu-id="c8029-133">Çalışma alanını, bu özellikleri açıp ilgili belgelere bakmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8029-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="c8029-134">Özellik yönetimiyle gelen değişiklikler hakkında daha fazla bilgi edinmek için bkz. [Özellik yönetimine genel bakış](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="c8029-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
