---
title: Saat ve işe devamda devamsızlık kaydı
description: Bu konu, Saat ve işe devamda devamsızlık kayıtlarının nasıl ele alınacağını açıklar.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16b338010662f8c2115fcc38f6830b58c49259e2
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826226"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="8129d-103">Saat ve işe devamda devamsızlık kaydı</span><span class="sxs-lookup"><span data-stu-id="8129d-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8129d-104">Bu konu devamsızlık kavramlarını tanımlar ve devamsızlığın Saat ve işe devamda nasıl ele alınacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8129d-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="8129d-105">Normal çalışma saatlerine dayalı devamsızlık</span><span class="sxs-lookup"><span data-stu-id="8129d-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="8129d-106">Çalışanlar, normal çalışma saatleri içinde çalışmadıkları saatlerde yok sayılır.</span><span class="sxs-lookup"><span data-stu-id="8129d-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="8129d-107">Normal çalışma saatleri bir çalışanın standart zaman profilinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="8129d-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="8129d-108">Örneğin, bir çalışan girişin saat 07:00'de çıkışın saat 15:00'te olduğu bir gün profilinde çalışmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8129d-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="8129d-109">Çalışan 09:00'da giriş yaparsa, kendisi o gün saat 07:00 ile 09:00 arasında yok kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="8129d-110">Bu durumda, çalışanlardan devamsızlık için bir neden girmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="8129d-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="8129d-111">Bir devamsızlık kodu seçerek bir neden belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8129d-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="8129d-112">Devamsızlık kodları</span><span class="sxs-lookup"><span data-stu-id="8129d-112">Absence codes</span></span>

<span data-ttu-id="8129d-113">Devamsızlık kodları çeşitli devamsızlık türlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8129d-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="8129d-114">Devamsızlık kodları şirket tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="8129d-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="8129d-115">Devamsızlık kodlarına çeşitli kurallar uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="8129d-116">Örneğin, bir devamsızlık kodu kesinti veya ödeme yapmak üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="8129d-117">Örneğin, bir şirket çalışanlar geç geliyorsa ve iyi bir nedenleri yoksa bir **Geç** devamsızlık kodu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8129d-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="8129d-118">Şirket ayrıca çalışanların dahili kurslara katılmak üzere harcadıkları zaman için kullanılan bir **Dahili kurs** devamsızlık kodu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8129d-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="8129d-119">Bu devamsızlık kodları **Geç** bir çalışanın ödemesinden kesinti yapılacak ancak **Dahili kurs** bir çalışanın ödemesinden kesinti yapılmayacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="8129d-120">Otomatik devamsızlık kodları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8129d-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="8129d-121">Bu devamsızlık kodları devamsızlık kaydı olmadığında bir çalışanın süresini hesaplamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="8129d-122">Çalışanın zaman profili, devamsızlık kodunun standart zaman veya esnek zaman için kullanılıp kullanılmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="8129d-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="8129d-123">Standart zaman ve esnek zaman ayarla</span><span class="sxs-lookup"><span data-stu-id="8129d-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="8129d-124">**Zaman ve katılımcı parametreleri** sayfasındaki **Otomatik devamsızlık ekleme** ve **Otomatik Esnek ekleme-** seçeneklerini kullanarak standart zaman ve esnek zaman için parametreleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8129d-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="8129d-125">Devamsızlık grupları</span><span class="sxs-lookup"><span data-stu-id="8129d-125">Absence groups</span></span>

<span data-ttu-id="8129d-126">Devamsızlık kodları, devamsızlık grupları olarak gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="8129d-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="8129d-127">Devamsızlık gruplarını ortak özelliklere sahip devamsızlık kodlarını gruplandırmak için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="8129d-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="8129d-128">Örnekler arasında yasal devamsızlık veya doktor randevusu, jüri görevi veya çocuk hastalığı nedeniyle devamsızlık için devamsızlık kodları yer alır.</span><span class="sxs-lookup"><span data-stu-id="8129d-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="8129d-129">Planlanan devamsızlık</span><span class="sxs-lookup"><span data-stu-id="8129d-129">Planned absence</span></span>

<span data-ttu-id="8129d-130">Bir çalışanın yaklaşmakta olan bir tatil nedeniyle belirli bir süre işe gelmeyeceğini biliyorsanız, planlanan devamsızlığı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8129d-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="8129d-131">Devamsızlık kodunu planlanan devamsızlığı dikkate alacak şekilde yapılandırarak planlanan devamsızlığı ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="8129d-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="8129d-132">Bir planlanan devamsızlık ayarladığınızda, kullanıcı zaman kayıtları hesaplandığında devamsızlık süresince bir devamsızlık kodu istenmez.</span><span class="sxs-lookup"><span data-stu-id="8129d-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="8129d-133">Planlanan devamsızlık tek bir çalışan için tanımlanabilir veya çalışanlar için planlanan devamsızlığı toplu güncelleştirmek için bir toplu iş tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8129d-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="8129d-134">Planlanan devamsızlık ayarla</span><span class="sxs-lookup"><span data-stu-id="8129d-134">Set up planned absence</span></span>

1. <span data-ttu-id="8129d-135">**İnsan kaynakları** &gt; **Çalışanlar** &gt; **Personel** seçin ve bir personel seçin.</span><span class="sxs-lookup"><span data-stu-id="8129d-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="8129d-136">**Zaman** &gt; **Zaman atamaları** &gt; **Zaman Devamsızlık kaydı** seçin ve planlanan devamsızlığı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8129d-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="8129d-137">Durdurulmuş planlanan devamsızlık</span><span class="sxs-lookup"><span data-stu-id="8129d-137">Interrupted planned absence</span></span>

<span data-ttu-id="8129d-138">Bir planlanan devamsızlık ayarladığınızda **Durdur** seçeneğini uygularsanız, çalışan planlanan devamsızlık süresince işe gelirse planlanan devamsızlık durdurulur.</span><span class="sxs-lookup"><span data-stu-id="8129d-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="8129d-139">Planlanan devamsızlık **Durduruldu** olarak işaretlenir ve gelecekteki hesaplamalar üzerinde hiçbir etkisi olmaz.</span><span class="sxs-lookup"><span data-stu-id="8129d-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="8129d-140">Durdurmak için bir planlanan devamsızlık ayarla</span><span class="sxs-lookup"><span data-stu-id="8129d-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="8129d-141">Planlanan devamsızlık ayarlama prosedüründe açıklandığı gibi **Zaman devamsızlık kaydı** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="8129d-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="8129d-142">**Durdur** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8129d-142">Select **Interrupt**.</span></span>

<span data-ttu-id="8129d-143">**Durdur** seçeneği zaman mağaza katı terminali veya mağaza katı cihazı aracılığıyla kaydedildiğinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8129d-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="8129d-144">Kayıtlar hesaplama ve onay sayfalarına veya **Elektronik zaman kartı** sayfasına girilmişse, bu seçenek kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="8129d-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="8129d-145">Esnek profilde, devamsızlık kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="8129d-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="8129d-146">Aşağıdaki üç örnekte esnek dönemleri olan bir profilde devamsızlığın nasıl hesaplandığı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8129d-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="8129d-147">Örneklerde aşağıdaki profil kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8129d-147">The examples use the following profile.</span></span>

| <span data-ttu-id="8129d-148">Giriş saati</span><span class="sxs-lookup"><span data-stu-id="8129d-148">Clock-in</span></span> | <span data-ttu-id="8129d-149">Standart zaman</span><span class="sxs-lookup"><span data-stu-id="8129d-149">Standard time</span></span>    | <span data-ttu-id="8129d-150">Mola</span><span class="sxs-lookup"><span data-stu-id="8129d-150">Break</span></span>             | <span data-ttu-id="8129d-151">Standart zaman</span><span class="sxs-lookup"><span data-stu-id="8129d-151">Standard time</span></span> | <span data-ttu-id="8129d-152">Esnek-</span><span class="sxs-lookup"><span data-stu-id="8129d-152">Flex-</span></span>        | <span data-ttu-id="8129d-153">Çıkış saati</span><span class="sxs-lookup"><span data-stu-id="8129d-153">Clock-out</span></span> | <span data-ttu-id="8129d-154">Esnek+</span><span class="sxs-lookup"><span data-stu-id="8129d-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="8129d-155">08:00</span><span class="sxs-lookup"><span data-stu-id="8129d-155">8 AM</span></span>     | <span data-ttu-id="8129d-156">09:00 - 11:30</span><span class="sxs-lookup"><span data-stu-id="8129d-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="8129d-157">11:30 - 00:00</span><span class="sxs-lookup"><span data-stu-id="8129d-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="8129d-158">00:00 - 15:00</span><span class="sxs-lookup"><span data-stu-id="8129d-158">12 PM to 3 PM</span></span> | <span data-ttu-id="8129d-159">15:00 - 16:00</span><span class="sxs-lookup"><span data-stu-id="8129d-159">3 PM to 4 PM</span></span> | <span data-ttu-id="8129d-160">16:00</span><span class="sxs-lookup"><span data-stu-id="8129d-160">4 PM</span></span>      | <span data-ttu-id="8129d-161">16:00 - 18:00</span><span class="sxs-lookup"><span data-stu-id="8129d-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="8129d-162">Örnek 1: Bir Esnek dönemde çıkış yapma</span><span class="sxs-lookup"><span data-stu-id="8129d-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="8129d-163">Çalışan saat 08:00'de giriş ve saat 15:30'da çıkış yapıyor.</span><span class="sxs-lookup"><span data-stu-id="8129d-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="8129d-164">Bu durumda, çalışan Esnek bir dönemde çıkış yaptığından, devamsızlık hesaplanmaz ve çalışanın esnek bakiyesinden yarım saat kesilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="8129d-165">Örnek 2: Standart zaman döneminde çıkış yapma</span><span class="sxs-lookup"><span data-stu-id="8129d-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="8129d-166">Çalışan saat 08:00'de giriş ve saat 14:30'da çıkış yapıyor.</span><span class="sxs-lookup"><span data-stu-id="8129d-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="8129d-167">Bu durumda, çalışan Standart zaman döneminde çıkış yaptığından, devamsızlık 14:30 ile 16:00 saatleri arasında hesaplanır ve 1,5 saatlik bir devamsızlık dönemi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="8129d-168">Bu döneme ait devamsızlık kodu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8129d-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="8129d-169">Örnek 3: Bir Esnek+ dönemde çıkış yapma</span><span class="sxs-lookup"><span data-stu-id="8129d-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="8129d-170">Çalışan saat 08:00'de giriş ve saat 16:30'da çıkış yapıyor.</span><span class="sxs-lookup"><span data-stu-id="8129d-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="8129d-171">Bu durumda, çalışan Esnek+ bir dönemde çıkış yaptığından, devamsızlık hesaplanmaz ve çalışanın esnek bakiyesine yarım saat eklenir.</span><span class="sxs-lookup"><span data-stu-id="8129d-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="8129d-172">Hesaplama ve onay işleminde devamsızlık</span><span class="sxs-lookup"><span data-stu-id="8129d-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="8129d-173">Bordro sistemine ödeme maddeleri olarak aktarmadan önce çalışan zaman kayıtlarının hesaplanması ve onaylanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8129d-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="8129d-174">Bir onaylayan çalışanın zaman kayıtlarını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="8129d-175">Onaylayan çalışanın kaydolduğu bir devamsızlığı da değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="8129d-176">Onaylayan el ile bir devamsızlık koduna sahip bir süre girerse, bu döneme ait devamsızlık kodu Zaman ve katılımcı parametrelerinden varsayılan devamsızlık kodu tarafından geçersiz kılınmaz.</span><span class="sxs-lookup"><span data-stu-id="8129d-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="8129d-177">Örneğin, bir çalışan 10:00'da giriş yapıyor ve geç geldiğini belirten bir devamsızlık kodunu seçiyor.</span><span class="sxs-lookup"><span data-stu-id="8129d-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="8129d-178">Daha sonra çalışan yöneticisine saat 08:00 ile 10:00 arasında bir doktor randevusu olduğunu bildiriyor.</span><span class="sxs-lookup"><span data-stu-id="8129d-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="8129d-179">Doktor randevusu çalışanın ödemesinden kesinti yapılmasına neden olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="8129d-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="8129d-180">Bu nedenle, bu durumda, yönetici iki saat süreyle hastalığı belirten bir devamsızlık kodunu el ile girerek saat 08:00 ile 10:00 arasında iki saatlik devamsızlık ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="8129d-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="8129d-181">Devamsızlığı hesapla ve onayla</span><span class="sxs-lookup"><span data-stu-id="8129d-181">Calculate and approve absence</span></span>

- <span data-ttu-id="8129d-182">**İşe devam zamanı** &gt; **Gözden geçirme ve onaylama** &gt; **Onaylama veya Hesaplama** öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="8129d-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>
