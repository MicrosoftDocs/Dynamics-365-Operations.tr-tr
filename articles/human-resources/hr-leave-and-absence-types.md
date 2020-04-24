---
title: İzin ve devamsızlık türlerini yapılandırma
description: Dynamics 365 Human Resources'ta çalışanların götürebileceği izin tiplerini ayarlayın.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198062"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="6774c-103">İzin ve devamsızlık türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6774c-103">Configure leave and absence types</span></span>

<span data-ttu-id="6774c-104">Dynamics 365 Human Resources'ta izin türleri, bir personelin bildirebileceği çeşitli türde devamsızlıkları tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="6774c-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="6774c-105">İzin tiplerini kuruluşunuzun gereksinimlerine göre uyarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6774c-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="6774c-106">İzin türleri örnekleri:</span><span class="sxs-lookup"><span data-stu-id="6774c-106">Examples of leave types include:</span></span>

- <span data-ttu-id="6774c-107">Ücretli süre kesintisi (PTO)</span><span class="sxs-lookup"><span data-stu-id="6774c-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="6774c-108">Ücretsiz izin</span><span class="sxs-lookup"><span data-stu-id="6774c-108">Unpaid leave</span></span>
- <span data-ttu-id="6774c-109">Ücretli izin</span><span class="sxs-lookup"><span data-stu-id="6774c-109">Paid vacation</span></span>
- <span data-ttu-id="6774c-110">Hastalık izni</span><span class="sxs-lookup"><span data-stu-id="6774c-110">Sick leave</span></span>
- <span data-ttu-id="6774c-111">Tıbbi izin</span><span class="sxs-lookup"><span data-stu-id="6774c-111">Medical leave</span></span>
- <span data-ttu-id="6774c-112">Aile izni</span><span class="sxs-lookup"><span data-stu-id="6774c-112">Family leave</span></span>
- <span data-ttu-id="6774c-113">Kısa süreli engellilik</span><span class="sxs-lookup"><span data-stu-id="6774c-113">Short-term disability</span></span>
- <span data-ttu-id="6774c-114">Matem izni</span><span class="sxs-lookup"><span data-stu-id="6774c-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="6774c-115">İzin türü Ekle</span><span class="sxs-lookup"><span data-stu-id="6774c-115">Add a leave type</span></span>

1. <span data-ttu-id="6774c-116">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6774c-117">**Kurulum** altında, **izin ve devamsızlık tipleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="6774c-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-118">Select **New**.</span></span>

4. <span data-ttu-id="6774c-119">**Tür** altındaki izin türü için ad girin, **iş akışı kimliğinden** bir iş akışı seçin ve **açıklama** altında bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="6774c-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="6774c-120">**Genel** olarak, **kategori** açılan menüsünde **yok**, **zamanlanmış** veya **zamanlanmamış** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6774c-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="6774c-121">**Kazanç kodu** açılan menüsünden bir kazanç kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="6774c-122">**Neden kodu gerekli** olduğunda, neden kodu olmasını istiyorsanız bunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="6774c-123">Neden kodları olmasını istiyorsanız, bunları eklemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="6774c-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="6774c-124">**Neden kodları** altında, **Ekle**'yi seçin, bir neden kodu seçin ve sonra da yanındaki **etkin** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="6774c-125">**Seçili rollere erişimi kısıtlamak** altında, erişimi kısıtlamak istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="6774c-126">Sonra, **bu izin türü için güvenlik rolleri** altında güvenlik rollerini seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="6774c-127">Güvenlik rolleri, bu yordamda daha önce **iş akışı kodu** altında seçtiğiniz iş akışında tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6774c-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="6774c-128">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-128">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="6774c-129">İzin türü kurallarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6774c-129">Configure leave type rules</span></span>

1. <span data-ttu-id="6774c-130">İzin türü için yuvarlama seçeneklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6774c-130">Set rounding options for the leave type.</span></span> <span data-ttu-id="6774c-131">**Yok**, **yukarı**, **aşağı** ve **en yakın** seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="6774c-131">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="6774c-132">Ayrıca, izin tipiyle ilgili Yuvarlama Duyarlığı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6774c-132">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="6774c-133">İzin türü için **tatil düzeltmesi** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6774c-133">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="6774c-134">Bu seçeneği belirlediğinizde, izin türü için sürenin nasıl tahakkuk ettirildiğini belirlemek için İnsan Kaynakları iş gününe denk düşen tatilleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="6774c-134">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="6774c-135">Örneğin, Noel günü Pazartesi gününe denk gelirse İnsan Kaynakları tahakkukları işlerken izin türünden bir günü çıkarır.</span><span class="sxs-lookup"><span data-stu-id="6774c-135">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="6774c-136">Tatilleri çlışma zmaanı takviminde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6774c-136">You set holidays in the working time calendar.</span></span> <span data-ttu-id="6774c-137">Daha fazla bilgi için bkz. [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="6774c-137">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
## <a name="configure-preview-features"></a><span data-ttu-id="6774c-138">Önizleme özelliklerine yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6774c-138">Configure preview features</span></span>

<span data-ttu-id="6774c-139">İzin ve devamsızlık için Önizleme özelliklerini etkinleştirdiyseniz, bu ayarları sizin için de konfigüre etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6774c-139">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="6774c-140">Transfer edilecek devir bakiyeleri için izin türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6774c-140">Choose the leave type for carry forward balances to be transferred to.</span></span> <span data-ttu-id="6774c-141">Ayrıca, devir için yeni bir izin türü oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6774c-141">You can also create a new leave type for carry forward.</span></span> 

## <a name="see-also"></a><span data-ttu-id="6774c-142">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="6774c-142">See also</span></span>

- [<span data-ttu-id="6774c-143">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="6774c-143">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="6774c-144">İzin ve devamsızlık planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6774c-144">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="6774c-145">Çalışma süresi takvimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="6774c-145">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
