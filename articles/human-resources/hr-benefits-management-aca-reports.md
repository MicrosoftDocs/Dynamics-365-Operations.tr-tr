---
title: Sosyal Hak yönetiminde Ekonomik Bakım Yasası raporları oluşturma
description: Bu konu, Sosyal Haklar yönetiminin Ekonomik Bakım Yasası (ACA) işveren görevi için Form 1095-B ve Form 1095-C'de bildirilen bilgileri izlemenize nasıl yardımcı olduğunu açıklar.
author: andreabichsel
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1417232baeaf03721bd0b25cc3f9fd5f750c65d5
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052277"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="1289b-103">Sosyal Haklar yönetiminde ACA raporları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1289b-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1289b-104">Sosyal Haklar yönetimi Ekonomik Bakım Yasası (ACA) işveren görevi için Form 1095-B ve Form 1095-C'de bildirilen bilgileri izlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1289b-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="1289b-105">Eski **Sosyal Haklar** çalışma alanında ACA raporlama özelliği gibi, bu işlevsellik yalnızca ABD'deki tüzel kişilikler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="1289b-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="1289b-106">Bu işlevi kullanmak için, önce **Gelişmiş Sosyal Haklar Yönetimi**'ni açmalısınız.</span><span class="sxs-lookup"><span data-stu-id="1289b-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="1289b-107">Sosyal Haklar yönetimi hakkında önemli uyarılar da dahil olmak üzere daha fazla bilgi için, bkz. [Sosyal Haklar yönetimini etkinleştirme veya devre dışı bırakma](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="1289b-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1289b-108">ACA raporlamasını yalnızca **Sosyal Haklar yönetimi** çalışma alanından veya eski **Sosyal Haklar** çalışma alanından (her ikisinden değil) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="1289b-109">Örneğin, Sosyal Haklar yönetimine geçtiyseniz, ACA raporlaması eski **Sosyal Haklar** çalışma alanından değil, yalnızca **Sosyal Haklar yönetimi** çalışma alanından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1289b-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="1289b-110">Bir kayıt yılının ortasında Sosyal Haklar yönetimine geçerseniz, Sosyal Haklar yönetiminde tüm yıl için çalışan verilerini doğru şekilde yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1289b-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="1289b-111">Bu şekilde, tüm yıl boyunca doğru raporlama bilgileri aldığınızdan emin olursunuz.</span><span class="sxs-lookup"><span data-stu-id="1289b-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="1289b-112">Başlarken</span><span class="sxs-lookup"><span data-stu-id="1289b-112">Getting started</span></span>

<span data-ttu-id="1289b-113">1095 formlarının bilgilerini izlemek için önce bir veya daha fazla Ekonomik Bakım kapsamı grubu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1289b-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="1289b-114">Bu gruplar aşağıdaki bilgileri gösterir:</span><span class="sxs-lookup"><span data-stu-id="1289b-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="1289b-115">Bir çalışana sağlanan kapsam teklifi</span><span class="sxs-lookup"><span data-stu-id="1289b-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="1289b-116">Maliyet federal yoksulluk sınırının üzerindeyse, çalışanın en düşük maliyetli aylık prim payı</span><span class="sxs-lookup"><span data-stu-id="1289b-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="1289b-117">Varsa işveren tarafından kullanılan Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="1289b-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="1289b-118">Ekonomik Bakım kapsamı grupları, aynı koşullara sahip birden çok çalışan kaydı için bu bilgileri yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1289b-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="1289b-119">Bir veya daha fazla çalışana kolayca grup atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="1289b-120">Ekonomik Bakım kapsama grubu oluşturma veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="1289b-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="1289b-121">**Sosyal Haklar yönetimi** çalışma alanında, **Ekonomik Bakım kapsamı grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Ekonomik Bakım kapsamı grubunu seçme](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="1289b-123">Yeni bir Ekonomik Bakım kapsamı grubu oluşturmak için **Yeni**'yi veya var olan bir grubu değiştirmek için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Yeni veya Düzenle'yi seçme](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="1289b-125">Aşağıdaki alanları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1289b-125">Set the following fields.</span></span>

    | <span data-ttu-id="1289b-126">Alan</span><span class="sxs-lookup"><span data-stu-id="1289b-126">Field</span></span> | <span data-ttu-id="1289b-127">Tanım</span><span class="sxs-lookup"><span data-stu-id="1289b-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="1289b-128">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="1289b-128">Name</span></span> | <span data-ttu-id="1289b-129">Grup için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1289b-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="1289b-130">Tanım</span><span class="sxs-lookup"><span data-stu-id="1289b-130">Description</span></span> | <span data-ttu-id="1289b-131">Grubun açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="1289b-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="1289b-132">Kapsam teklifi</span><span class="sxs-lookup"><span data-stu-id="1289b-132">Offer of coverage</span></span> | <span data-ttu-id="1289b-133">Çalışanlara, eşlerine ve bakmakla yükümlü oldukları kişilere sunulan kapsam.</span><span class="sxs-lookup"><span data-stu-id="1289b-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="1289b-134">Personel maliyet payı</span><span class="sxs-lookup"><span data-stu-id="1289b-134">Employee share of cost</span></span> | <span data-ttu-id="1289b-135">Çalışanın sorumlu olduğu tutar.</span><span class="sxs-lookup"><span data-stu-id="1289b-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="1289b-136">Geçerli bölüm 4980H güvenli liman</span><span class="sxs-lookup"><span data-stu-id="1289b-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="1289b-137">4980H Safe Harbor veya geçiş desteği kodu.</span><span class="sxs-lookup"><span data-stu-id="1289b-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="1289b-138">Plan başlangıç ayı</span><span class="sxs-lookup"><span data-stu-id="1289b-138">Plan start month</span></span> | <span data-ttu-id="1289b-139">Sosyal hak planı yılınızın başladığı zamanın takvim ayını seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="1289b-140">Grup geçerlilik başlangıcı</span><span class="sxs-lookup"><span data-stu-id="1289b-140">Group valid from</span></span> | <span data-ttu-id="1289b-141">Bu kaydın geçerli olduğu ilk tarih.</span><span class="sxs-lookup"><span data-stu-id="1289b-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="1289b-142">Grup geçerliliği sonu</span><span class="sxs-lookup"><span data-stu-id="1289b-142">Group valid through</span></span> | <span data-ttu-id="1289b-143">Bu kaydın geçerli olduğu son tarih.</span><span class="sxs-lookup"><span data-stu-id="1289b-143">The last date when this record is valid.</span></span> <span data-ttu-id="1289b-144">Sona erme tarihi yoksa **Hiçbir Zaman** girin.</span><span class="sxs-lookup"><span data-stu-id="1289b-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Kapsam grubu oluşturma](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="1289b-146">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="1289b-147">Ekonomik Bakım kapsamı grubuna birden fazla çalışan atama</span><span class="sxs-lookup"><span data-stu-id="1289b-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="1289b-148">**Sosyal Haklar yönetimi** çalışma alanında, **Ekonomik Bakım kapsamı grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="1289b-149">Çalışanların atanacağı grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="1289b-150">**Toplu atama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-150">Select **Mass assignment**.</span></span>

    ![Toplu atama'yı seçme](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="1289b-152">Listeden çalışanları seçin ve sonra **Ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Seçilen çalışanları bir gruba atama](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="1289b-154">Kapsama seçeneklerinin birden fazla sürümünü tutma</span><span class="sxs-lookup"><span data-stu-id="1289b-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="1289b-155">Bir kapsama grubunun birden fazla sürümünü tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="1289b-156">Kuruluşunuzda veya sunulan sosyal haklarda bir değişiklik olduğunda, yeni bir grup oluşturmak ve çalışanları yeniden atamak zorunda kalmadan grubun bilgilerini güncel tutabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="1289b-157">Ekonomik Bakım kapsamı grupları oluşturduktan sonra, çalışanları bu gruplara toplu olarak atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="1289b-158">Ayrıca, çalışanları gruplara tek tek atayabilir ve ACA bilgilerinin izlenip izlenmeyeceğini ve raporlanıp raporlanmayacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="1289b-159">Bir çalışanın ACA bilgilerini izlemeniz ve raporlamanız gerekmiyorsa **Rapor kapsamı** seçeneğini **Hayır** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="1289b-160">Örneğin, ACA raporlaması gerektirmeyen yarı zamanlı çalışanlarınız olabilir.</span><span class="sxs-lookup"><span data-stu-id="1289b-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="1289b-161">Çalışan için varsayılan değerleri geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="1289b-161">Override default values for an employee</span></span>

<span data-ttu-id="1289b-162">Ekonomik Bakım kapsamı grubuna atanan çalışanlar için farklı değerler gerektiren herhangi bir ayda aşağıdaki seçenekleri değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1289b-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="1289b-163">Kapsam teklifi</span><span class="sxs-lookup"><span data-stu-id="1289b-163">Offer of coverage</span></span>
- <span data-ttu-id="1289b-164">Personel maliyet payı</span><span class="sxs-lookup"><span data-stu-id="1289b-164">Employee share of cost</span></span>
- <span data-ttu-id="1289b-165">Geçerli bölüm 4980H güvenli liman</span><span class="sxs-lookup"><span data-stu-id="1289b-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="1289b-166">2020 ACA raporları için Form 1095-C'de hem iş hem de ev adresi posta kodlarını bildirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1289b-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="1289b-167">Değerler, geçerli etkin konumlara göre otomatik olarak doldurulur.</span><span class="sxs-lookup"><span data-stu-id="1289b-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="1289b-168">Bir konum, yılın herhangi bir bölümünde farklıysa değeri geçersiz kılmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1289b-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="1289b-169">1095-C raporunun **Posta Kodu** alanı (satır 17) yalnızca **Kapsam teklifi** kodu aşağıdaki gibi **1L** ile **1Q** arasında değer içeriyorsa doldurulur:</span><span class="sxs-lookup"><span data-stu-id="1289b-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="1289b-170">**1L, 1M veya 1N:** Birincil ikamet posta kodu</span><span class="sxs-lookup"><span data-stu-id="1289b-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="1289b-171">**1O, 1P, 1Q:** Birincil iş adresi posta kodu</span><span class="sxs-lookup"><span data-stu-id="1289b-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="1289b-172">Ekonomik Bakım kapsamı grubunun herhangi bir değeri için özel durumlar girmek istiyorsanız bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1289b-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="1289b-173">**Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin ve sonra **Çalışanlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="1289b-174">Listeden çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="1289b-175">**İstihdam** sekmesinde, **Daha fazla bilgi** bölümünde E **konomik Bakım kapsamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Bir çalışan için seçenekleri değiştirme](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="1289b-177">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-177">Select **Edit**.</span></span>
5. <span data-ttu-id="1289b-178">Değişiklik gerektiren her ay için **Varsayılanı geçersiz kıl** onay kutusunu seçin ve diğer değerleri gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="1289b-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Varsayılan değerleri geçersiz kılma](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="1289b-180">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="1289b-181">Sağlık bakımı kapsamasını raporlama</span><span class="sxs-lookup"><span data-stu-id="1289b-181">Report health care coverage</span></span>

<span data-ttu-id="1289b-182">Tam zamanlı ve yarı zamanlı çalışanlar için işveren destekli, kendi kaynaklarından teminat ayırma sigortalı sağlık hizmeti kapsamını izlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1289b-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="1289b-183">Her çalışanı, bakmakla yükümlü oldukları kişilerle birlikte, kapsandıkları aylar için 1095-C raporuna dahil edin.</span><span class="sxs-lookup"><span data-stu-id="1289b-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="1289b-184">Bir sosyal hak planının raporlanıp raporlanmayacağını belirtmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1289b-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="1289b-185">**Sosyal hak yönetimi** çalışma alanında, **Sosyal hak planları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="1289b-186">Raporlanacak sosyal hak planını seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="1289b-187">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-187">Select **Edit**.</span></span>
4. <span data-ttu-id="1289b-188">**Ekonomik Bakım Yasası kapsamında bildiriliyor** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1289b-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Sağlık bakımı kapsamasını raporlama](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="1289b-190">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-190">Select **Save**.</span></span>

<span data-ttu-id="1289b-191">Bir çalışan, bakmakla yükümlü olduğu bir kişi için sağlık hizmeti kapsamını seçerse bakmakla yükümlü olduğu kişinin kapsama süresi, bu kişinin kaydedildiği veya kaldırıldığı tarihe göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="1289b-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="1289b-192">Bakmakla yükümlü olunan kişiler için kapsam tarihleri, bu kişinin kayıt yılı boyunca bir planda uygun ve etkin olduğu döneme göre otomatik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1289b-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="1289b-193">1095-B ve 1095-C formları oluşturma</span><span class="sxs-lookup"><span data-stu-id="1289b-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="1289b-194">ACA 1095-B ve 1095-C formları oluşturabilir ve bunları çalışanlarınızın her birine dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="1289b-195">Internal Revenue Service'e (IRS) göndermek için Form 1095-C ve ilgili 1094-C iletim dosyalarını elektronik olarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="1289b-196">**Sosyal haklar yönetimi** çalışma alanında, **ACA 1095-B formu** veya **ACA 1095-C formu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="1289b-197">Gerekirse parametreleri değiştirin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1289b-198">500'den fazla çalışan için 1095-C formları yazdırıyorsanız birden fazla PDF dosyası alırsınız.</span><span class="sxs-lookup"><span data-stu-id="1289b-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="1289b-199">**Belge yönetimi parametreleri** sayfasındaki **Megabayt cinsinden maksimum dosya boyutu** alanının değerini **150**'ye çıkarmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="1289b-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="1289b-200">(Bu sayfayı hızlı bir şekilde açmak için gezinti çubuğundaki arama alanını kullanabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="1289b-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Maksimum dosya boyutunu değiştirme](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="1289b-202">Raporlarınızın durumunu denetlemek ve görüntülemek için gezinti çubuğundaki arama alanını kullanarak **Elektronik raporlama işleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="1289b-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Elektronik raporlama işleri sayfasını arama](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="1289b-204">Görüntülenecek raporu seçin ve sonra **Dosyaları göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-204">Select the report to view, and then select **Show files**.</span></span>

    ![Dosyaları gösterme](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="1289b-206">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-206">Select **Open**.</span></span>

    ![Dosya açma](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="1289b-208">Tarayıcı penceresinin altında görünen Bildirim çubuğundan zip dosyasını açın ve raporu seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="1289b-209">PDF dosyasını görüntüleyebilir veya yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-209">You can view or print the PDF file.</span></span>

    ![Örnek 1095-C formu](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="1289b-211">ACA kapsamı bilgilerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1289b-211">View ACA coverage information</span></span>

<span data-ttu-id="1289b-212">**Çalışan Ekonomik Bakım kapsamı** sayfasında aşağıdaki bilgiler gösterilir:</span><span class="sxs-lookup"><span data-stu-id="1289b-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="1289b-213">Her kapsam grubuna atanan çalışanlar</span><span class="sxs-lookup"><span data-stu-id="1289b-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="1289b-214">Rapora dahil edilmesi gerekmeyen çalışanlar</span><span class="sxs-lookup"><span data-stu-id="1289b-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="1289b-215">Atanmamış çalışanlar</span><span class="sxs-lookup"><span data-stu-id="1289b-215">Unassigned employees</span></span>

<span data-ttu-id="1289b-216">Bu bilgileri görüntülemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1289b-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="1289b-217">**Sosyal Haklar yönetimi** çalışma alanında, **Çalışan Ekonomik Bakım kapsamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="1289b-218">**Grup adı** alanından bir grup seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-218">In the **Group name** field, select a group.</span></span>

    ![ACA kapsamını görüntüleme](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="1289b-220">Ekonomik Bakım kapsama grubundaki varsayılan değerlerden herhangi biri geçersiz kılınmışsa değiştirilen değerin yanında bir yıldız işareti görünür.</span><span class="sxs-lookup"><span data-stu-id="1289b-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="1289b-221">12 ayın tamamı için değerler aynı ise ve geçersiz kılınmamışsa, değer **Tüm 12 ay** sütununda görünür.</span><span class="sxs-lookup"><span data-stu-id="1289b-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="1289b-222">ACA tarafından raporlanamayan ve Form 1095-C gerektirmeyen çalışanları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="1289b-223">**Filtreleme ölçütü** alanında, **ACA raporlanabilir değil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="1289b-224">Bir gruba atanmamış veya süresi dolmuş bir gruba atanmış çalışanları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="1289b-225">**Filtreleme ölçütü** alanında **Atanmamış veya süresi dolmuş grup** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="1289b-226">Excel'e aktar</span><span class="sxs-lookup"><span data-stu-id="1289b-226">Export to Excel</span></span>

<span data-ttu-id="1289b-227">Listelerden herhangi birini Microsoft Excel'e dışarı aktarmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1289b-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="1289b-228">**Microsoft Office'te Aç** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="1289b-229">Dahili kullanım için **HCM Human Resources geçici tablosu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="1289b-230">**İndir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="1289b-231">ACA tarafından raporlanabilir bakmakla yükümlü olunan kişileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="1289b-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="1289b-232">Kendi kaynaklarından teminat ayırmayla sigorta kapsamı sağladığınız için kapsanan kişileri bildirmeniz gerekiyorsa **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planları kapsamındaki bakmakla yükümlü olunan kişileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1289b-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="1289b-233">Eylem bölmesinde, **Bakmakla yükümlü olunan kişi kapsamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1289b-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Bakmakla yükümlü olunan kişi kapsamını görüntüleme](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="1289b-235">Çalışanın bakmakla yükümlü olduğu kişilerin kapsam bilgileri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1289b-235">Coverage information for the employee's dependents is shown.</span></span>

![Bakmakla yükümlü olunan kişi kapsamı](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="1289b-237">Sayfa yalnızca **ACA raporlanabilir** olarak işaretlenmiş sosyal hak planlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1289b-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]