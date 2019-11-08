---
title: Dynamics 365 Talent - Onboard'u kullanarak işe alım ve alıştırma şablonu oluşturma
description: Bu konuda yeni işe alımlarda işe alım ve alıştırma şablonu oluşturmak için Dynamics 365 Talent - Onboard uygulamasının nasıl kullanılacağı açıklanmaktadır. Bu görev, insan sermaye yönetimi (HCM) için işe alma stratejisindeki temel bir ilk adımdır.
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a1fac239524d4873a782e6a3d177a573a382d0f6
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552060"
---
# <a name="create-an-onboarding-template-by-using-dynamics-365-talent---onboard"></a><span data-ttu-id="10c7e-104">Dynamics 365 Talent - Onboard'u kullanarak işe alım ve alıştırma şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="10c7e-104">Create an onboarding template by using Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10c7e-105">Microsoft Dynamics 365 Talent: Onboard - Onboard, mümkün olduğunca çabuk işe alım ve alıştırma kılavuzu oluşturmanıza yardımcı olabilecek çeşitli şablonlar sunar.</span><span class="sxs-lookup"><span data-stu-id="10c7e-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="10c7e-106">Bu şablonlardan birini veya birkaçını kullanabilir ya da kendi şablonlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10c7e-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="10c7e-107">Onboard, kendi şablonlarınızı oluştururken kullanabileceğiniz örnek metin sağlar.</span><span class="sxs-lookup"><span data-stu-id="10c7e-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="10c7e-108">Bu nedenle, sıfırdan başlasanız bile işlem kolayca yapılır.</span><span class="sxs-lookup"><span data-stu-id="10c7e-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="10c7e-109">Varolan şablondan ekleme şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="10c7e-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="10c7e-110">Sol menüde **Şablonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="10c7e-111">**Galeriden popüler şablonlar** veya **Şablonlarım** altında bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="10c7e-112">Daha fazla şablon görüntülemek için **Şablon galerisinde diğer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="10c7e-113">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="10c7e-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="10c7e-114">Şablon galeriden ise, **Şablonumolarak kaydet**'i seçin, şablon için yeni bir ad girin ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="10c7e-115">Şablon **Şablonlarım**'dansa, **Şablonum olarak kaydet**'i seçin, şablon için yeni bir ad girin ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="10c7e-116">[![Varolan şablondan şablon oluşturma](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="10c7e-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="10c7e-117">Yeni işe alım şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="10c7e-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="10c7e-118">Sol menüde **Şablonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="10c7e-119">**Şablonlarım** altında **Ekle** (artı \[**+**\] işareti) döşemesini seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="10c7e-120">[![Yeni şablon oluşturma](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="10c7e-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="10c7e-121">**Kılavuz şablon oluştur** iletişim kutusunda, şablon için bir ad girin ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10c7e-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="10c7e-122">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="10c7e-122">Next steps</span></span>

- [<span data-ttu-id="10c7e-123">İşe alım kılavuzları ve şablonları düzenleme</span><span class="sxs-lookup"><span data-stu-id="10c7e-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="10c7e-124">İçeriği diğer katkıda bulunanlarla paylaşın</span><span class="sxs-lookup"><span data-stu-id="10c7e-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="10c7e-125">Görevlerin ve işe alınan çalışanların durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="10c7e-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="10c7e-126">Onboard'da işe alma ekipleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="10c7e-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="10c7e-127">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="10c7e-127">See also</span></span>

- [<span data-ttu-id="10c7e-128">Onboard uygulamasını deneyin veya satın alın</span><span class="sxs-lookup"><span data-stu-id="10c7e-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="10c7e-129">Yenilikler</span><span class="sxs-lookup"><span data-stu-id="10c7e-129">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="10c7e-130">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="10c7e-130">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="10c7e-131">Destek alma</span><span class="sxs-lookup"><span data-stu-id="10c7e-131">Get support</span></span>](./talent-support.md)
