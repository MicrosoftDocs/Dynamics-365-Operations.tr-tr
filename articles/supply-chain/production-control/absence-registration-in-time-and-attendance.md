---
title: Saat ve işe devamda devamsızlık kaydı
description: Bu konu, Saat ve işe devamda devamsızlık kayıtlarının nasıl ele alınacağını açıklar.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b765ae63cfb17e26439758f2a0ed64770ef70881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809290"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="51cf5-103">Saat ve işe devamda devamsızlık kaydı</span><span class="sxs-lookup"><span data-stu-id="51cf5-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51cf5-104">Bu konu devamsızlık kavramlarını tanımlar ve devamsızlığın Saat ve işe devamda nasıl ele alınacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="51cf5-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="51cf5-105">Normal çalışma saatlerine dayalı devamsızlık</span><span class="sxs-lookup"><span data-stu-id="51cf5-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="51cf5-106">Çalışanlar, normal çalışma saatleri içinde çalışmadıkları saatlerde yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="51cf5-107">Normal çalışma saatleri bir çalışanın standart zaman profilinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="51cf5-108">Örneğin, bir çalışan girişin saat 07:00'de çıkışın saat 15:00'te olduğu bir gün profilinde çalışmaktadır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="51cf5-109">Çalışan 09:00'da giriş yaparsa, kendisi o gün saat 07:00 ile 09:00 arasında yok kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="51cf5-110">Bu durumda, çalışanlardan devamsızlık için bir neden girmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="51cf5-111">Bir devamsızlık kodu seçerek bir neden belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="51cf5-112">Devamsızlık kodları</span><span class="sxs-lookup"><span data-stu-id="51cf5-112">Absence codes</span></span>

<span data-ttu-id="51cf5-113">Devamsızlık kodları çeşitli devamsızlık türlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="51cf5-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="51cf5-114">Devamsızlık kodları şirket tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="51cf5-115">Devamsızlık kodlarına çeşitli kurallar uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="51cf5-116">Örneğin, bir devamsızlık kodu kesinti veya ödeme yapmak üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="51cf5-117">Örneğin, bir şirket çalışanlar geç geliyorsa ve iyi bir nedenleri yoksa bir **Geç** devamsızlık kodu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="51cf5-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="51cf5-118">Şirket ayrıca çalışanların dahili kurslara katılmak üzere harcadıkları zaman için kullanılan bir **Dahili kurs** devamsızlık kodu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="51cf5-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="51cf5-119">Bu devamsızlık kodları **Geç** bir çalışanın ödemesinden kesinti yapılacak ancak **Dahili kurs** bir çalışanın ödemesinden kesinti yapılmayacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="51cf5-120">Otomatik devamsızlık kodları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="51cf5-121">Bu devamsızlık kodları devamsızlık kaydı olmadığında bir çalışanın süresini hesaplamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="51cf5-122">Çalışanın zaman profili, devamsızlık kodunun standart zaman veya esnek zaman için kullanılıp kullanılmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="51cf5-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="51cf5-123">Standart zaman ve esnek zaman ayarla</span><span class="sxs-lookup"><span data-stu-id="51cf5-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="51cf5-124">**Zaman ve katılımcı parametreleri** sayfasındaki **Otomatik devamsızlık ekleme** ve **Otomatik Esnek ekleme-** seçeneklerini kullanarak standart zaman ve esnek zaman için parametreleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="51cf5-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="51cf5-125">Devamsızlık grupları</span><span class="sxs-lookup"><span data-stu-id="51cf5-125">Absence groups</span></span>

<span data-ttu-id="51cf5-126">Devamsızlık kodları, devamsızlık grupları olarak gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="51cf5-127">Devamsızlık gruplarını ortak özelliklere sahip devamsızlık kodlarını gruplandırmak için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="51cf5-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="51cf5-128">Örnekler arasında yasal devamsızlık veya doktor randevusu, jüri görevi veya çocuk hastalığı nedeniyle devamsızlık için devamsızlık kodları yer alır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="51cf5-129">Planlanan devamsızlık</span><span class="sxs-lookup"><span data-stu-id="51cf5-129">Planned absence</span></span>

<span data-ttu-id="51cf5-130">Bir çalışanın yaklaşmakta olan bir tatil nedeniyle belirli bir süre işe gelmeyeceğini biliyorsanız, planlanan devamsızlığı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="51cf5-131">Devamsızlık kodunu planlanan devamsızlığı dikkate alacak şekilde yapılandırarak planlanan devamsızlığı ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="51cf5-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="51cf5-132">Bir planlanan devamsızlık ayarladığınızda, kullanıcı zaman kayıtları hesaplandığında devamsızlık süresince bir devamsızlık kodu istenmez.</span><span class="sxs-lookup"><span data-stu-id="51cf5-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="51cf5-133">Planlanan devamsızlık tek bir çalışan için tanımlanabilir veya çalışanlar için planlanan devamsızlığı toplu güncelleştirmek için bir toplu iş tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="51cf5-134">Planlanan devamsızlık ayarla</span><span class="sxs-lookup"><span data-stu-id="51cf5-134">Set up planned absence</span></span>

1. <span data-ttu-id="51cf5-135">**İnsan kaynakları** &gt; **Çalışanlar** &gt; **Personel** seçin ve bir personel seçin.</span><span class="sxs-lookup"><span data-stu-id="51cf5-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="51cf5-136">**Zaman** &gt; **Zaman atamaları** &gt; **Zaman Devamsızlık kaydı** seçin ve planlanan devamsızlığı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="51cf5-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="51cf5-137">Durdurulmuş planlanan devamsızlık</span><span class="sxs-lookup"><span data-stu-id="51cf5-137">Interrupted planned absence</span></span>

<span data-ttu-id="51cf5-138">Bir planlanan devamsızlık ayarladığınızda **Durdur** seçeneğini uygularsanız, çalışan planlanan devamsızlık süresince işe gelirse planlanan devamsızlık durdurulur.</span><span class="sxs-lookup"><span data-stu-id="51cf5-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="51cf5-139">Planlanan devamsızlık **Durduruldu** olarak işaretlenir ve gelecekteki hesaplamalar üzerinde hiçbir etkisi olmaz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="51cf5-140">Durdurmak için bir planlanan devamsızlık ayarla</span><span class="sxs-lookup"><span data-stu-id="51cf5-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="51cf5-141">Planlanan devamsızlık ayarlama prosedüründe açıklandığı gibi **Zaman devamsızlık kaydı** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="51cf5-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="51cf5-142">**Durdur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="51cf5-142">Select **Interrupt**.</span></span>

<span data-ttu-id="51cf5-143">**Durdur** seçeneği zaman mağaza katı terminali veya mağaza katı cihazı aracılığıyla kaydedildiğinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="51cf5-144">Kayıtlar hesaplama ve onay sayfalarına veya **Elektronik zaman kartı** sayfasına girilmişse, bu seçenek kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="51cf5-145">Esnek profilde, devamsızlık kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="51cf5-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="51cf5-146">Aşağıdaki üç örnekte esnek dönemleri olan bir profilde devamsızlığın nasıl hesaplandığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="51cf5-147">Örneklerde aşağıdaki profil kullanılır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-147">The examples use the following profile.</span></span>

| <span data-ttu-id="51cf5-148">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="51cf5-148">Clock-in</span></span> | <span data-ttu-id="51cf5-149">Standart zaman</span><span class="sxs-lookup"><span data-stu-id="51cf5-149">Standard time</span></span>    | <span data-ttu-id="51cf5-150">Mola</span><span class="sxs-lookup"><span data-stu-id="51cf5-150">Break</span></span>             | <span data-ttu-id="51cf5-151">Standart zaman</span><span class="sxs-lookup"><span data-stu-id="51cf5-151">Standard time</span></span> | <span data-ttu-id="51cf5-152">Esnek-</span><span class="sxs-lookup"><span data-stu-id="51cf5-152">Flex-</span></span>        | <span data-ttu-id="51cf5-153">Çıkış saati</span><span class="sxs-lookup"><span data-stu-id="51cf5-153">Clock-out</span></span> | <span data-ttu-id="51cf5-154">Esnek+</span><span class="sxs-lookup"><span data-stu-id="51cf5-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="51cf5-155">08:00</span><span class="sxs-lookup"><span data-stu-id="51cf5-155">8 AM</span></span>     | <span data-ttu-id="51cf5-156">09:00 - 11:30</span><span class="sxs-lookup"><span data-stu-id="51cf5-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="51cf5-157">11:30 - 00:00</span><span class="sxs-lookup"><span data-stu-id="51cf5-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="51cf5-158">00:00 - 15:00</span><span class="sxs-lookup"><span data-stu-id="51cf5-158">12 PM to 3 PM</span></span> | <span data-ttu-id="51cf5-159">15:00 - 16:00</span><span class="sxs-lookup"><span data-stu-id="51cf5-159">3 PM to 4 PM</span></span> | <span data-ttu-id="51cf5-160">16:00</span><span class="sxs-lookup"><span data-stu-id="51cf5-160">4 PM</span></span>      | <span data-ttu-id="51cf5-161">16:00 - 18:00</span><span class="sxs-lookup"><span data-stu-id="51cf5-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="51cf5-162">Örnek 1: Bir Esnek dönemde çıkış yapma</span><span class="sxs-lookup"><span data-stu-id="51cf5-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="51cf5-163">Çalışan saat 08:00'de giriş ve saat 15:30'da çıkış yapıyor.</span><span class="sxs-lookup"><span data-stu-id="51cf5-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="51cf5-164">Bu durumda, çalışan Esnek bir dönemde çıkış yaptığından, devamsızlık hesaplanmaz ve çalışanın esnek bakiyesinden yarım saat kesilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="51cf5-165">Örnek 2: Standart zaman döneminde çıkış yapma</span><span class="sxs-lookup"><span data-stu-id="51cf5-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="51cf5-166">Çalışan saat 08:00'de giriş ve saat 14:30'da çıkış yapıyor.</span><span class="sxs-lookup"><span data-stu-id="51cf5-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="51cf5-167">Bu durumda, çalışan Standart zaman döneminde çıkış yaptığından, devamsızlık 14:30 ile 16:00 saatleri arasında hesaplanır ve 1,5 saatlik bir devamsızlık dönemi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="51cf5-168">Bu döneme ait devamsızlık kodu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="51cf5-169">Örnek 3: Bir Esnek+ dönemde çıkış yapma</span><span class="sxs-lookup"><span data-stu-id="51cf5-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="51cf5-170">Çalışan saat 08:00'de giriş ve saat 16:30'da çıkış yapıyor.</span><span class="sxs-lookup"><span data-stu-id="51cf5-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="51cf5-171">Bu durumda, çalışan Esnek+ bir dönemde çıkış yaptığından, devamsızlık hesaplanmaz ve çalışanın esnek bakiyesine yarım saat eklenir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="51cf5-172">Hesaplama ve onay işleminde devamsızlık</span><span class="sxs-lookup"><span data-stu-id="51cf5-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="51cf5-173">Bordro sistemine ödeme maddeleri olarak aktarmadan önce çalışan zaman kayıtlarının hesaplanması ve onaylanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="51cf5-174">Bir onaylayan çalışanın zaman kayıtlarını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="51cf5-175">Onaylayan çalışanın kaydolduğu bir devamsızlığı da değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="51cf5-176">Onaylayan el ile bir devamsızlık koduna sahip bir süre girerse, bu döneme ait devamsızlık kodu Zaman ve katılımcı parametrelerinden varsayılan devamsızlık kodu tarafından geçersiz kılınmaz.</span><span class="sxs-lookup"><span data-stu-id="51cf5-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="51cf5-177">Örneğin, bir çalışan 10:00'da giriş yapıyor ve geç geldiğini belirten bir devamsızlık kodunu seçiyor.</span><span class="sxs-lookup"><span data-stu-id="51cf5-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="51cf5-178">Daha sonra çalışan yöneticisine saat 08:00 ile 10:00 arasında bir doktor randevusu olduğunu bildiriyor.</span><span class="sxs-lookup"><span data-stu-id="51cf5-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="51cf5-179">Doktor randevusu çalışanın ödemesinden kesinti yapılmasına neden olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="51cf5-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="51cf5-180">Bu nedenle, bu durumda, yönetici iki saat süreyle hastalığı belirten bir devamsızlık kodunu el ile girerek saat 08:00 ile 10:00 arasında iki saatlik devamsızlık ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="51cf5-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="51cf5-181">Devamsızlığı hesapla ve onayla</span><span class="sxs-lookup"><span data-stu-id="51cf5-181">Calculate and approve absence</span></span>

- <span data-ttu-id="51cf5-182">**İşe devam zamanı** &gt; **Gözden geçirme ve onaylama** &gt; **Onaylama veya Hesaplama** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="51cf5-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]