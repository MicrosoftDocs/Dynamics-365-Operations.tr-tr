---
title: Dynamics 365 for Talent - Onboard kullanarak ekleme şablonu oluşturma
description: Bu konu, yeni işe alım kılavuzu için şablon oluşturmak üzere Dynamics 365 for Talent - Onboard uygulamasının nasıl kullanılacağını açıklamaktadır. Bu görev, insan sermaye yönetimi (HCM) için işe alma stratejisindeki temel bir ilk adımdır.
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
ms.openlocfilehash: c53c24b2913e3ca30cfc6491556b49d5d9230128
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731680"
---
# <a name="create-an-onboarding-template-by-using-dynamics-365-for-talent-onboard"></a><span data-ttu-id="9cca1-104">Dynamics 365 for Talent: Onboard kullanarak ekleme şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="9cca1-104">Create an onboarding template by using Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9cca1-105">Microsoft Dynamics 365 for Talent: Onboard mümkün olduğunca çabuk ekleme kılavuzu oluşturmanıza yardımcı olabilecek çeşitli şablonlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="9cca1-105">Microsoft Dynamics 365 for Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="9cca1-106">Bu şablonlardan birini veya birkaçını kullanabilir ya da kendi şablonlarınızı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cca1-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="9cca1-107">Onboard, kendi şablonlarınızı oluştururken kullanabileceğiniz örnek metin sağlar.</span><span class="sxs-lookup"><span data-stu-id="9cca1-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="9cca1-108">Bu nedenle, sıfırdan başlasanız bile işlem kolayca yapılır.</span><span class="sxs-lookup"><span data-stu-id="9cca1-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="9cca1-109">Varolan şablondan ekleme şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="9cca1-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="9cca1-110">Sol menüde **Şablonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="9cca1-111">**Galeriden popüler şablonlar** veya **Şablonlarım** altında bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="9cca1-112">Daha fazla şablon görüntülemek için **Şablon galerisinde diğer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="9cca1-113">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="9cca1-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="9cca1-114">Şablon galeriden ise, **Şablonumolarak kaydet**'i seçin, şablon için yeni bir ad girin ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="9cca1-115">Şablon **Şablonlarım**'dansa, **Şablonum olarak kaydet**'i seçin, şablon için yeni bir ad girin ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="9cca1-116">[![Varolan şablondan şablon oluşturma](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="9cca1-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="9cca1-117">Yeni işe alım şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="9cca1-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="9cca1-118">Sol menüde **Şablonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="9cca1-119">**Şablonlarım** altında **Ekle** (artı \[**+**\] işareti) döşemesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="9cca1-120">[![Yeni şablon oluşturma](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="9cca1-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="9cca1-121">**Kılavuz şablon oluştur** iletişim kutusunda, şablon için bir ad girin ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9cca1-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9cca1-122">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="9cca1-122">Next steps</span></span>

- [<span data-ttu-id="9cca1-123">İşe alım kılavuzları ve şablonları düzenleme</span><span class="sxs-lookup"><span data-stu-id="9cca1-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="9cca1-124">İçeriği diğer katkıda bulunanlarla paylaşın</span><span class="sxs-lookup"><span data-stu-id="9cca1-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="9cca1-125">Görevlerin ve işe alınan çalışanların durumunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9cca1-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="9cca1-126">Onboard'da işe alma ekipleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="9cca1-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="9cca1-127">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9cca1-127">See also</span></span>

- [<span data-ttu-id="9cca1-128">Onboard uygulamasını deneyin veya satın alın</span><span class="sxs-lookup"><span data-stu-id="9cca1-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="9cca1-129">Yenilikler</span><span class="sxs-lookup"><span data-stu-id="9cca1-129">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="9cca1-130">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="9cca1-130">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="9cca1-131">Destek alma</span><span class="sxs-lookup"><span data-stu-id="9cca1-131">Get support</span></span>](./talent-support.md)
