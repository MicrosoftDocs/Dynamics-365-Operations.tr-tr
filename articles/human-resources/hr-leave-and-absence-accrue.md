---
title: İzin ve devamsızlık planlarını tahakkuk et
description: İzin ve Devamsızlığı birden fazla çalışan veya bir birey için Dynamics 365 Human Resources'ta tahakkuk edebilirsiniz.
author: andreabichsel
ms.date: 05/04/2020
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
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303476"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="2a01a-103">İzin ve devamsızlık planlarını tahakkuk et</span><span class="sxs-lookup"><span data-stu-id="2a01a-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2a01a-104">İzin ve Devamsızlığı birden fazla çalışan veya bir birey için Dynamics 365 Human Resources'ta tahakkuk edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a01a-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="2a01a-105">Birden fazla personel için izin ve devamsızlık tahakkuk etme</span><span class="sxs-lookup"><span data-stu-id="2a01a-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="2a01a-106">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2a01a-107">**İzinleri Yönet** altında, **izin ve devamsızlık planları tahakku et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="2a01a-108">**İzin ve devamsızlık planları tahakkuk ettirme** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2a01a-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="2a01a-109">**Tahakkuk tarihi** alanında **Bugünün tarihi**'ni seçin veya **Özel tarih**'i seçin ve özel bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="2a01a-110">Tüm şirketler için tahakkukları çalıştırmak istiyorsanız **Tüm şirketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="2a01a-111">Tek bir izin planıyla ilgili tahakkukları işlemek istiyorsanız **Tüm planlar** için **Hayır**'ı seçip **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="2a01a-112">Tüm şirketleri seçerseniz tek bir izin planını seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a01a-112">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="2a01a-113">Tahakkuk İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="2a01a-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

    1. <span data-ttu-id="2a01a-114">Tahakkuk İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-114">Enter information for the accrual process.</span></span>
    2. <span data-ttu-id="2a01a-115">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and then select **OK**.</span></span>
    3. <span data-ttu-id="2a01a-116">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>
    4. <span data-ttu-id="2a01a-117">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-117">Select **OK**.</span></span> <span data-ttu-id="2a01a-118">Tahakkuk İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="2a01a-118">The accrual process will run with the parameters you set.</span></span> 

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="2a01a-119">Personel için izin ve devamsızlık tahakkuk etme</span><span class="sxs-lookup"><span data-stu-id="2a01a-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="2a01a-120">Çalışanın kaydında, **izin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="2a01a-121">**İzin ve devamsızlık planları tahakkuk etme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="2a01a-122">**İzin ve devamsızlık planları tahakkuk ettirme** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2a01a-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="2a01a-123">**Tahakkuk tarihi** alanında **Bugünün tarihi**'ni seçin veya **Özel tarih**'i seçin ve özel bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="2a01a-124">Tüm şirketler için tahakkukları çalıştırmak istiyorsanız **Tüm şirketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="2a01a-125">Tek bir izin planıyla ilgili tahakkukları işlemek istiyorsanız **Tüm planlar** için **Hayır**'ı seçip **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="2a01a-126">Tüm şirketleri seçerseniz tek bir izin planını seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a01a-126">If you select all companies, you can't select an individual leave plan.</span></span>

5. <span data-ttu-id="2a01a-127">Tahakkuk İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="2a01a-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2a01a-128">Tahakkuk İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="2a01a-129">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2a01a-130">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2a01a-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-131">Select **OK**.</span></span> <span data-ttu-id="2a01a-132">Tahakkuk İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="2a01a-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="2a01a-133">Birden fazla personel için izin ve devamsızlık tahakkuklarını silme</span><span class="sxs-lookup"><span data-stu-id="2a01a-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="2a01a-134">Belirli bir plan ve tarih aralığı için tahakkuk kayıtlarını silin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="2a01a-135">Tahakkuk tarihleri bugün veya gelecekte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a01a-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="2a01a-136">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2a01a-137">**İzni yönet** altında, **İzin ve devamsızlık planı tahakkuklarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="2a01a-138">**İzin ve devamsızlık planı tahakkuklarını sil** iletişim kutusunda **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span>

4. <span data-ttu-id="2a01a-139">Uygunsa, **Bakiye ayarlamalarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="2a01a-140">**İzin tahakkuk tarihi** girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="2a01a-141">Bu tarih, bugünün tarihi ya da gelecekteki bir tarih olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a01a-141">This date has to be either today or in the future.</span></span>

6. <span data-ttu-id="2a01a-142">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-142">Select **OK**.</span></span> <span data-ttu-id="2a01a-143">Tahakkuk İşlem, ayarladığınız parametrelerle tahakkukları silecektir.</span><span class="sxs-lookup"><span data-stu-id="2a01a-143">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="2a01a-144">Tek bir personel için izin ve devamsızlık tahakkuklarını silme</span><span class="sxs-lookup"><span data-stu-id="2a01a-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="2a01a-145">Çalışanın kaydında, **izin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="2a01a-146">**İzin ve devamsızlık planı tahakkuklarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="2a01a-147">**İzin ve devamsızlık planı tahakkuklarını sil** iletişim kutusunda **İzin planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span>

4. <span data-ttu-id="2a01a-148">Uygunsa, **Bakiye ayarlamalarını sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="2a01a-149">**İzin tahakkuk tarihi** girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="2a01a-150">Bu tarih, bugünün tarihi ya da gelecekteki bir tarih olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a01a-150">This date must be either today or in the future.</span></span>

6. <span data-ttu-id="2a01a-151">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-151">Select **OK**.</span></span> <span data-ttu-id="2a01a-152">Tahakkuk İşlem, ayarladığınız parametrelerle tahakkukları silecektir.</span><span class="sxs-lookup"><span data-stu-id="2a01a-152">The accrual process will delete accruals with the parameters you set.</span></span>

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="2a01a-153">İzin tahakkukunu gözden geçirme ve silme işlemi</span><span class="sxs-lookup"><span data-stu-id="2a01a-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="2a01a-154">**İzin tahakkuk planı** bir kişi veya tüm personel için bir tahakkuku her çalıştırma veya silme olayını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="2a01a-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="2a01a-155">Tarih ve eylemi gerçekleştiren kişi de görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="2a01a-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="2a01a-156">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="2a01a-157">**İzni yönet** altında, **İzin tahakkuk denetimini sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="leave-accrual-transaction-auditing"></a><span data-ttu-id="2a01a-158">İzin tahakkuku hareketi denetleme</span><span class="sxs-lookup"><span data-stu-id="2a01a-158">Leave accrual transaction auditing</span></span>

<span data-ttu-id="2a01a-159">Bu özellik, çıkış ve devamsızlık yöneticilerinin belirli bir izin türü için bir çalışanın dengelemesinin zamanıyla ilgili bırakma ve devamsızlık tahakkuk hareketlerini anlamasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2a01a-159">This feature helps leave and absence managers understand the leave and absence accrual transactions related to an employee’s time off balances for a specific leave type.</span></span>

<span data-ttu-id="2a01a-160">İşlem Ayrıntılarını görüntülemek için:</span><span class="sxs-lookup"><span data-stu-id="2a01a-160">To view transaction details:</span></span>

1. <span data-ttu-id="2a01a-161">Çalışanın kaydında, **izin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-161">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="2a01a-162">**İzin zamanını görüntüle**'yi seçin ve sonra **bakiyeler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-162">Select **View time off**, and then select the **Balances** tab.</span></span>

<span data-ttu-id="2a01a-163">Belirli bir izin türüyle ilgili tahakkuk hareketlerini görüntülemek için, **Geçerli Bakiye** sütunundaki sayısal değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="2a01a-163">To view the accrual transactions related to a specific leave type, select the numerical value in the **Current balance** column.</span></span>

<span data-ttu-id="2a01a-164">Belirli bir tahakkuk tutarına ait hareket ayrıntılarını görüntülemek için, bir tahakkuk satırı seçin, sağ tarafta **ilgili bilgi** panelini açın ve **işlem ayrıntıları** bölümünü açın.</span><span class="sxs-lookup"><span data-stu-id="2a01a-164">To view the transaction details for a specific accrual amount, select an accrual row, open the **Related information** panel on the right, and then open the **Transaction details** section.</span></span> <span data-ttu-id="2a01a-165">Hareket ayrıntıları bölümünde şunu görüntüler:</span><span class="sxs-lookup"><span data-stu-id="2a01a-165">The Transaction details section displays:</span></span>

- <span data-ttu-id="2a01a-166">Çalışanın izin türü bakiyesindeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2a01a-166">Changes to the employee’s leave type balance</span></span>
- <span data-ttu-id="2a01a-167">Belirtilen tahakkuk dönemine ait işe alma ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="2a01a-167">Employment details for that specified accrual period</span></span>
- <span data-ttu-id="2a01a-168">Tahakkuk dönemi ve oranları hakkında ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="2a01a-168">Details about the accrual period and rates</span></span>
- <span data-ttu-id="2a01a-169">Plan konfigürasyonlarına izin vermek için yapılan tüm değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2a01a-169">Any changes made to leave plan configurations</span></span>

![İzin tahakkuku hareketi denetlemeyi göster](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a><span data-ttu-id="2a01a-171">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="2a01a-171">See also</span></span>

[<span data-ttu-id="2a01a-172">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="2a01a-172">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="2a01a-173">İzin ve devamsızlık planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a01a-173">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
