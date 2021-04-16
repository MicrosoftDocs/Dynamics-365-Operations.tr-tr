---
title: İzin ve devamsızlık türlerini yapılandırma
description: Dynamics 365 Human Resources'ta çalışanların götürebileceği izin tiplerini ayarlayın.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bf868ad44e52b0ed7d0ca6e1f133efa030f3c4a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794577"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="ecc5a-103">İzin ve devamsızlık türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ecc5a-103">Configure leave and absence types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ecc5a-104">Dynamics 365 Human Resources'ta izin türleri, bir personelin bildirebileceği çeşitli türde devamsızlıkları tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="ecc5a-105">İzin tiplerini kuruluşunuzun gereksinimlerine göre uyarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="ecc5a-106">İzin türleri örnekleri:</span><span class="sxs-lookup"><span data-stu-id="ecc5a-106">Examples of leave types include:</span></span>

- <span data-ttu-id="ecc5a-107">Ücretli süre kesintisi (PTO)</span><span class="sxs-lookup"><span data-stu-id="ecc5a-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="ecc5a-108">Ücretsiz izin</span><span class="sxs-lookup"><span data-stu-id="ecc5a-108">Unpaid leave</span></span>
- <span data-ttu-id="ecc5a-109">Ücretli izin</span><span class="sxs-lookup"><span data-stu-id="ecc5a-109">Paid vacation</span></span>
- <span data-ttu-id="ecc5a-110">Hastalık izni</span><span class="sxs-lookup"><span data-stu-id="ecc5a-110">Sick leave</span></span>
- <span data-ttu-id="ecc5a-111">Tıbbi izin</span><span class="sxs-lookup"><span data-stu-id="ecc5a-111">Medical leave</span></span>
- <span data-ttu-id="ecc5a-112">Aile izni</span><span class="sxs-lookup"><span data-stu-id="ecc5a-112">Family leave</span></span>
- <span data-ttu-id="ecc5a-113">Kısa süreli engellilik</span><span class="sxs-lookup"><span data-stu-id="ecc5a-113">Short-term disability</span></span>
- <span data-ttu-id="ecc5a-114">Matem izni</span><span class="sxs-lookup"><span data-stu-id="ecc5a-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="ecc5a-115">İzin türü Ekle</span><span class="sxs-lookup"><span data-stu-id="ecc5a-115">Add a leave type</span></span>

1. <span data-ttu-id="ecc5a-116">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="ecc5a-117">**Kurulum** altında, **izin ve devamsızlık tipleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="ecc5a-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-118">Select **New**.</span></span>

4. <span data-ttu-id="ecc5a-119">**Tür** altındaki izin türü için ad girin, **iş akışı kimliğinden** bir iş akışı seçin ve **açıklama** altında bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="ecc5a-120">**Genel** olarak, **kategori** açılan menüsünde **yok**, **zamanlanmış** veya **zamanlanmamış** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="ecc5a-121">**Kazanç kodu** açılan menüsünden bir kazanç kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="ecc5a-122">**Neden kodu gerekli** olduğunda, neden kodu olmasını istiyorsanız bunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="ecc5a-123">Neden kodları olmasını istiyorsanız, bunları eklemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="ecc5a-124">**Neden kodları** altında, **Ekle**'yi seçin, bir neden kodu seçin ve sonra da yanındaki **etkin** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="ecc5a-125">**Seçili rollere erişimi kısıtlamak** altında, erişimi kısıtlamak istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="ecc5a-126">Sonra, **bu izin türü için güvenlik rolleri** altında güvenlik rollerini seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="ecc5a-127">Güvenlik rolleri, bu yordamda daha önce **iş akışı kodu** altında seçtiğiniz iş akışında tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="ecc5a-128">**Takvim rengi** altında, izin ve devamsızlık takvimlerinde bu izin türü için görüntülenecek rengi seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="ecc5a-129">**Askıya alma ilişkileri** altında , bu tür iznin başka bir izin türünü askıya al veya başka bir izin türü tarafından askıya alınması seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="ecc5a-130">Askıya alma türü için devamsızlık yetkisi isteği gönderildiğinde, askıya alma türü için bir yeniden gönderme askıya alma işlemi otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="ecc5a-131">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="ecc5a-132">İzin türü kurallarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ecc5a-132">Configure leave type rules</span></span>

1. <span data-ttu-id="ecc5a-133">İzin türü için yuvarlama seçeneklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="ecc5a-134">**Yok**, **yukarı**, **aşağı** ve **en yakın** seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="ecc5a-135">Ayrıca, izin tipiyle ilgili Yuvarlama Duyarlığı da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="ecc5a-136">İzin türü için **tatil düzeltmesi** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="ecc5a-137">Bu seçeneği belirlediğinizde, izin türü için sürenin nasıl tahakkuk ettirildiğini belirlemek için İnsan Kaynakları iş gününe denk düşen tatilleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="ecc5a-138">Örneğin, Noel günü Pazartesi gününe denk gelirse İnsan Kaynakları tahakkukları işlerken izin türünden bir günü çıkarır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="ecc5a-139">Tatilleri çlışma zmaanı takviminde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="ecc5a-140">Daha fazla bilgi için bkz. [Çalışma zamanı takvimi oluşturma](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="ecc5a-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="ecc5a-141">İzin türü için **ileriye doğru izin türü** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="ecc5a-142">Bu seçeneği belirlediğinizde, tüm ileri düzey bakiyeleri belirtilen izin türüne aktarılır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="ecc5a-143">İleriye yönelik izin türü de, bırak ve devamsızlık planına dahil edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="ecc5a-144">İzin türü için **süre sonu kurallarını** tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="ecc5a-145">Bu seçeneği konfigüre ettiğinizde, gün veya ay birimini seçebilir ve bitiş tarihi için süreyi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="ecc5a-146">Ayrıca, sona erme kuralının geçerlilik tarihini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="ecc5a-147">Geçerlilik tarihi, izin süresinin dolmasını işleyen toplu işlemin ne zaman çalıştırılmaya başlayacağını veya kuralın ne zaman geçerli olacağını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-147">The effective date is used to determine when to start running the batch job that processes the leave expiration, or the date when the rule takes effect.</span></span> <span data-ttu-id="ecc5a-148">Toplu işlem işlenecek şekilde ayarlandıktan sonra sona erme süresi her zaman izin planı başlangıç tarihinde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-148">The expiration itself will always happen on the leave plan start date once the batch job is set to process.</span></span> <span data-ttu-id="ecc5a-149">Örneğin, plan başlangıç tarihi 1/1/2020 olabilir ancak kural 6/1/2020'ye kadar oluşturulmamıştır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-149">For example, the plan start date may be 1/1/2020, but the rule wasn't created until 6/1/2020.</span></span> <span data-ttu-id="ecc5a-150">Geçerlilik tarihi 6/1/2020 olarak ayarlandığında kural bir sonraki yıl sınırı olan 1/1/2021 tarihinde işlenir.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-150">By setting the effective date to 6/1/2020, the rule will be processed on the next year boundary, so 1/1/2021.</span></span> <span data-ttu-id="ecc5a-151">Bitiş tarihinde varolan tüm izin bakiyeleri izin dışında bırakılacak ve bırakma bakiyesine yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-151">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
## <a name="see-also"></a><span data-ttu-id="ecc5a-152">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ecc5a-152">See also</span></span>

- [<span data-ttu-id="ecc5a-153">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="ecc5a-153">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="ecc5a-154">İzin ve devamsızlık planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ecc5a-154">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="ecc5a-155">Çalışma zamanı takvimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ecc5a-155">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="ecc5a-156">İzni askıya alma</span><span class="sxs-lookup"><span data-stu-id="ecc5a-156">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
