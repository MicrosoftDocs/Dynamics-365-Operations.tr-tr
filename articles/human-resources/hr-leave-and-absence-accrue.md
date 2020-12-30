---
title: İzin ve devamsızlık planlarını tahakkuk et
description: İzin ve Devamsızlığı birden fazla çalışan veya bir birey için Dynamics 365 Human Resources'ta tahakkuk edebilirsiniz.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 43c16c5d0de91bf1f433f4fde36e7d13775f44a0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420996"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="4d552-103">İzin ve devamsızlık planlarını tahakkuk et</span><span class="sxs-lookup"><span data-stu-id="4d552-103">Accrue leave and absence plans</span></span>

<span data-ttu-id="4d552-104">İzin ve Devamsızlığı birden fazla çalışan veya bir birey için Dynamics 365 Human Resources'ta tahakkuk edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d552-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="4d552-105">Birden fazla personel için izin ve devamsızlık tahakkuk etme</span><span class="sxs-lookup"><span data-stu-id="4d552-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="4d552-106">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4d552-107">**İzinleri Yönet** altında, **izin ve devamsızlık planları tahakku et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="4d552-108">**İzin ve devamsızlık planları tahakkuk ettirme** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d552-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="4d552-109">**Tahakkuk tarihi** alanında **Bugünün tarihi**'ni seçin veya **Özel tarih**'i seçin ve özel bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="4d552-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="4d552-110">Tüm şirketler için tahakkukları çalıştırmak istiyorsanız **Tüm şirketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="4d552-111">Tek bir izin planıyla ilgili tahakkukları işlemek istiyorsanız **Tüm planlar** için **Hayır**'ı seçip **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="4d552-112">Tüm şirketleri seçerseniz tek bir izin planını seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d552-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="4d552-113">Tahakkuk İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="4d552-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="4d552-114">Tahakkuk İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="4d552-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="4d552-115">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="4d552-116">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="4d552-117">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-117">Select **OK**.</span></span> <span data-ttu-id="4d552-118">Tahakkuk İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="4d552-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="4d552-119">Personel için izin ve devamsızlık tahakkuk etme</span><span class="sxs-lookup"><span data-stu-id="4d552-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="4d552-120">Çalışanın kaydında, **izin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4d552-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="4d552-121">**İzin ve devamsızlık planları tahakkuk etme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="4d552-122">**İzin ve devamsızlık planları tahakkuk ettirme** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d552-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="4d552-123">**Tahakkuk tarihi** alanında **Bugünün tarihi**'ni seçin veya **Özel tarih**'i seçin ve özel bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="4d552-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="4d552-124">Tüm şirketler için tahakkukları çalıştırmak istiyorsanız **Tüm şirketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="4d552-125">Tek bir izin planıyla ilgili tahakkukları işlemek istiyorsanız **Tüm planlar** için **Hayır**'ı seçip **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="4d552-126">Tüm şirketleri seçerseniz tek bir izin planını seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d552-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="4d552-127">Tahakkuk İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="4d552-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="4d552-128">Tahakkuk İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="4d552-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="4d552-129">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="4d552-130">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="4d552-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-131">Select **OK**.</span></span> <span data-ttu-id="4d552-132">Tahakkuk İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="4d552-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="4d552-133">Birden fazla personel için izin ve devamsızlık tahakkuklarını silme</span><span class="sxs-lookup"><span data-stu-id="4d552-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="4d552-134">Belirli bir plan ve tarih aralığı için tahakkuk kayıtlarını silin.</span><span class="sxs-lookup"><span data-stu-id="4d552-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="4d552-135">Tahakkuk tarihleri bugün veya gelecekte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d552-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="4d552-136">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4d552-137">**İzni yönet** altında, **İzin ve devamsızlık planı tahakkuklarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="4d552-138">**İzin ve devamsızlık planı tahakkuklarını sil** iletişim kutusunda **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="4d552-139">Uygunsa, **Bakiye ayarlamalarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="4d552-140">**İzin tahakkuk tarihi** girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="4d552-141">Bu tarih, bugünün tarihi ya da gelecekteki bir tarih olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d552-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="4d552-142">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-142">Select **OK**.</span></span> <span data-ttu-id="4d552-143">Tahakkuk İşlem, ayarladığınız parametrelerle tahakkukları silecektir.</span><span class="sxs-lookup"><span data-stu-id="4d552-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="4d552-144">Tek bir personel için izin ve devamsızlık tahakkuklarını silme</span><span class="sxs-lookup"><span data-stu-id="4d552-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="4d552-145">Çalışanın kaydında, **izin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4d552-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="4d552-146">**İzin ve devamsızlık planı tahakkuklarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="4d552-147">**İzin ve devamsızlık planı tahakkuklarını sil** iletişim kutusunda **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="4d552-148">Uygunsa, **Bakiye ayarlamalarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="4d552-149">**İzin tahakkuk tarihi** girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="4d552-150">Bu tarih, bugünün tarihi ya da gelecekteki bir tarih olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d552-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="4d552-151">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-151">Select **OK**.</span></span> <span data-ttu-id="4d552-152">Tahakkuk İşlem, ayarladığınız parametrelerle tahakkukları silecektir.</span><span class="sxs-lookup"><span data-stu-id="4d552-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="4d552-153">İzin tahakkukunu gözden geçirme ve silme işlemi</span><span class="sxs-lookup"><span data-stu-id="4d552-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="4d552-154">**İzin tahakkuk planı** bir kişi veya tüm personel için bir tahakkuku her çalıştırma veya silme olayını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4d552-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="4d552-155">Tarih ve eylemi gerçekleştiren kişi de görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d552-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="4d552-156">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4d552-157">**İzni yönet** altında, **İzin tahakkuk denetimini sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4d552-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d552-158">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="4d552-158">See also</span></span>

[<span data-ttu-id="4d552-159">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="4d552-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="4d552-160">İzin ve devamsızlık planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4d552-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
