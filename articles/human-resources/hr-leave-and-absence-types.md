---
title: İzin ve devamsızlık türlerini yapılandırma
description: Dynamics 365 Human Resources'ta çalışanların götürebileceği izin tiplerini ayarlayın.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b21d4d631bcdf603b38212f5f76bb78937d3d3c
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115088"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="8383b-103">İzin ve devamsızlık türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8383b-103">Configure leave and absence types</span></span>

<span data-ttu-id="8383b-104">Dynamics 365 Human Resources'ta izin türleri, bir personelin bildirebileceği çeşitli türde devamsızlıkları tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="8383b-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="8383b-105">İzin tiplerini kuruluşunuzun gereksinimlerine göre uyarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8383b-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="8383b-106">İzin türleri örnekleri:</span><span class="sxs-lookup"><span data-stu-id="8383b-106">Examples of leave types include:</span></span>

- <span data-ttu-id="8383b-107">Ücretli süre kesintisi (PTO)</span><span class="sxs-lookup"><span data-stu-id="8383b-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="8383b-108">Ücretsiz izin</span><span class="sxs-lookup"><span data-stu-id="8383b-108">Unpaid leave</span></span>
- <span data-ttu-id="8383b-109">Ücretli izin</span><span class="sxs-lookup"><span data-stu-id="8383b-109">Paid vacation</span></span>
- <span data-ttu-id="8383b-110">Hastalık izni</span><span class="sxs-lookup"><span data-stu-id="8383b-110">Sick leave</span></span>
- <span data-ttu-id="8383b-111">Tıbbi izin</span><span class="sxs-lookup"><span data-stu-id="8383b-111">Medical leave</span></span>
- <span data-ttu-id="8383b-112">Aile izni</span><span class="sxs-lookup"><span data-stu-id="8383b-112">Family leave</span></span>
- <span data-ttu-id="8383b-113">Kısa süreli engellilik</span><span class="sxs-lookup"><span data-stu-id="8383b-113">Short-term disability</span></span>
- <span data-ttu-id="8383b-114">Matem izni</span><span class="sxs-lookup"><span data-stu-id="8383b-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="8383b-115">İzin türü Ekle</span><span class="sxs-lookup"><span data-stu-id="8383b-115">Add a leave type</span></span>

1. <span data-ttu-id="8383b-116">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="8383b-117">**Kurulum** altında, **izin ve devamsızlık tipleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="8383b-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-118">Select **New**.</span></span>

4. <span data-ttu-id="8383b-119">**Tür** altındaki izin türü için ad girin, **iş akışı kimliğinden** bir iş akışı seçin ve **açıklama** altında bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8383b-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="8383b-120">**Genel** olarak, **kategori** açılan menüsünde **yok**, **zamanlanmış** veya **zamanlanmamış** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8383b-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="8383b-121">**Kazanç kodu** açılan menüsünden bir kazanç kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="8383b-122">**Neden kodu gerekli** olduğunda, neden kodu olmasını istiyorsanız bunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="8383b-123">Neden kodları olmasını istiyorsanız, bunları eklemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="8383b-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="8383b-124">**Neden kodları** altında, **Ekle**'yi seçin, bir neden kodu seçin ve sonra da yanındaki **etkin** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="8383b-125">**Seçili rollere erişimi kısıtlamak** altında, erişimi kısıtlamak istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="8383b-126">Sonra, **bu izin türü için güvenlik rolleri** altında güvenlik rollerini seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="8383b-127">Güvenlik rolleri, bu yordamda daha önce **iş akışı kodu** altında seçtiğiniz iş akışında tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="8383b-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="8383b-128">**Takvim rengi** altında, izin ve devamsızlık takvimlerinde bu izin türü için görüntülenecek rengi seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="8383b-129">**Askıya alma ilişkileri** altında , bu tür iznin başka bir izin türünü askıya al veya başka bir izin türü tarafından askıya alınması seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8383b-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="8383b-130">Askıya alma türü için devamsızlık yetkisi isteği gönderildiğinde, askıya alma türü için bir yeniden gönderme askıya alma işlemi otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8383b-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="8383b-131">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8383b-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="8383b-132">İzin türü kurallarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8383b-132">Configure leave type rules</span></span>

1. <span data-ttu-id="8383b-133">İzin türü için yuvarlama seçeneklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8383b-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="8383b-134">**Yok**, **yukarı**, **aşağı** ve **en yakın** seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="8383b-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="8383b-135">Ayrıca, izin tipiyle ilgili Yuvarlama Duyarlığı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8383b-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="8383b-136">İzin türü için **tatil düzeltmesi** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8383b-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="8383b-137">Bu seçeneği belirlediğinizde, izin türü için sürenin nasıl tahakkuk ettirildiğini belirlemek için İnsan Kaynakları iş gününe denk düşen tatilleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="8383b-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="8383b-138">Örneğin, Noel günü Pazartesi gününe denk gelirse İnsan Kaynakları tahakkukları işlerken izin türünden bir günü çıkarır.</span><span class="sxs-lookup"><span data-stu-id="8383b-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="8383b-139">Tatilleri çlışma zmaanı takviminde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8383b-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="8383b-140">Daha fazla bilgi için bkz. [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="8383b-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="8383b-141">İzin türü için **ileriye doğru izin türü** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8383b-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="8383b-142">Bu seçeneği belirlediğinizde, tüm ileri düzey bakiyeleri belirtilen izin türüne aktarılır.</span><span class="sxs-lookup"><span data-stu-id="8383b-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="8383b-143">İleriye yönelik izin türü de, bırak ve devamsızlık planına dahil edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8383b-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="8383b-144">İzin türü için **süre sonu kurallarını** tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="8383b-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="8383b-145">Bu seçeneği konfigüre ettiğinizde, gün veya ay birimini seçebilir ve bitiş tarihi için süreyi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8383b-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="8383b-146">Ayrıca, sona erme kuralının geçerlilik tarihini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8383b-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="8383b-147">Bitiş tarihinde varolan tüm izin bakiyeleri izin dışında bırakılacak ve bırakma bakiyesine yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="8383b-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="8383b-148">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="8383b-148">See also</span></span>

- [<span data-ttu-id="8383b-149">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="8383b-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="8383b-150">İzin ve devamsızlık planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8383b-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="8383b-151">Çalışma zamanı takvimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8383b-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="8383b-152">İzni askıya alma</span><span class="sxs-lookup"><span data-stu-id="8383b-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

