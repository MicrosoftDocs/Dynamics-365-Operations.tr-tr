---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (08 Temmuz 2020)
description: Bu konuda, Microsoft Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 7/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fe7bc33407bd5781d565f854c0f096766da5fc9
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555400"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="a3cdd-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (8 Temmuz 2020)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="a3cdd-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a3cdd-105">Değişiklikler derleme numarası 8.1.3382 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="a3cdd-106">Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="a3cdd-107">Veritabanı günlüklerine kaydetme</span><span class="sxs-lookup"><span data-stu-id="a3cdd-107">Database logging</span></span>

<span data-ttu-id="a3cdd-108">Veritabanı günlükleri hangi tablo ve alanların izleneceğini belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="a3cdd-109">Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="a3cdd-110">Zaman içinde yapılan bu değişiklikleri görmek için veritabanı günlüğü kaydetme yeteneklerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="a3cdd-111">Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma ve yönetme](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="a3cdd-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="a3cdd-112">Personel self servisi adını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a3cdd-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="a3cdd-113">**İnsan Kaynakları parametrelerinde** artık **Personel self servisi** çalışma alanının adını **Self servis** olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="a3cdd-114">Daha fazla bilgi için bkz. [Personel self servise çalışma alanı adını değiştirme](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="a3cdd-115">Kazanç yönetimi açık kayıt erişimi dönem dışında</span><span class="sxs-lookup"><span data-stu-id="a3cdd-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="a3cdd-116">Bu sürüm, personelin kayıt dönemi dışındaki veya yaşam olayı olmaksızın açık kazanç kaydına erişebilmesini sağlayan bir hatayı düzeltir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="a3cdd-117">Sonuç olarak, Personel self servisinde açık kaydı göstermeniz gerekiyorsa, erişilebilir olması için açık kayıt tarihlerini bugüne (veya daha öncesine) ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="a3cdd-118">Bu ayarı, **Kazanç yönetimi > Kurallar ve seçenekler dönemleri** altından değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="a3cdd-119">Personel kaydı e-posta onayı</span><span class="sxs-lookup"><span data-stu-id="a3cdd-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="a3cdd-120">Şimdi, kazanç seçimlerini tamamladıktan sonra personele e-posta gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="a3cdd-121">Varsayılan bir ileti gönderebilir veya bir kuruluş e-posta şablonu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="a3cdd-122">Bu ayarlar, **İnsan kaynakları parametreleri > Kazanç yönetimi** altında bulunur.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="a3cdd-123">İptal edilen izin, Kişiler çalışma alanında yaklaşan izinde görünmeye devam ediyor (441358)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="a3cdd-124">İptal edilen izin artık **Kişiler** çalışma alaındaki izin kartlarında yaklaşan izin olarak görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="a3cdd-125">PositionV2 varlığındaki departman varlığı özelliği kullanılamıyor (456486)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="a3cdd-126">Artık, yinelenen ilişki oluşturmadan bir departman ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="a3cdd-127">PayrollWorkerEnrolledBenefitDetailEntity emeklilik planları için yalnızca hesaplanan alanları kullanmalıdır (459779)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="a3cdd-128">**PayrollWorkerEnrolledBenefitDetailEntity** varlığı dışa aktarıldığında, dışa aktarma işlemi bir oran tablosuna göre bir hesaplanan alan mı veya destekleyici tablodaki **ContributionAmountCur** alanın mı kullanılması gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="a3cdd-129">Veri varlığının kullandığı mantık, uygulamanın normalde kullanmadığı durumlarda oran tablosunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="a3cdd-130">Bu mantık varlık dışarı aktarma işlemlerinin bu sütun için bir sıfır değeri döndürmesine neden olur çünkü bir hesaplama oran tablosu yoktur ve ürün müşterinin bir tablo belirtmesine izin vermez.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="a3cdd-131">Personel yönetimi ve Personel self servisinde Çekçe dilinde kafa karıştırıcı çeviri (400276)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="a3cdd-132">Bu sürüm **Şirket dizini**, **Sonraki kayıtlı kurs**, **İş** ve **Pozisyon** için çevirileri düzeltir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="a3cdd-133">WorkCalendarEmployment tablosunda oluşturulan veya değiştirilen sistem alanları sağlanmıyor (460171)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="a3cdd-134">Oluşturulan ve değiştirilen sistem alanları artık Human Resources'taki **WorkCalendarEmployment** tablosunda sunulmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="a3cdd-135">Gelecekte personel işe alma ve ayrıntı ekleme için boş referans özel durumu (455475)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="a3cdd-136">Bu sürüm, bir personel işe alındığında **İşe alma ve ayrıntı ekleme** seçeneği kullanıldığında personel girişinde oluşan bir hatayı (boş referans) düzeltir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="a3cdd-137">Common Data Service Çalışan varlığında yapılan değişiklikler Human Resources'ta yansıtılmıyor (455652)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="a3cdd-138">Common Data Service'teki **Çalışan** varlığında aşağıdaki alanlarda yapılan değişiklikler artık Human Resources'ta görünecek:</span><span class="sxs-lookup"><span data-stu-id="a3cdd-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="a3cdd-139">**Evden çalışıyor**</span><span class="sxs-lookup"><span data-stu-id="a3cdd-139">**Works from home**</span></span>
- <span data-ttu-id="a3cdd-140">**Kıdem tarihi**</span><span class="sxs-lookup"><span data-stu-id="a3cdd-140">**Seniority date**</span></span>
- <span data-ttu-id="a3cdd-141">**Yıldönümü tarihi**</span><span class="sxs-lookup"><span data-stu-id="a3cdd-141">**Anniversary date**</span></span>
- <span data-ttu-id="a3cdd-142">**Orijinal işe alma tarihi**</span><span class="sxs-lookup"><span data-stu-id="a3cdd-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="a3cdd-143">Doğru ücret düzeyi pozisyona atanan işe göre varsayılana ayarlanmıyor (394136)</span><span class="sxs-lookup"><span data-stu-id="a3cdd-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="a3cdd-144">Bu değişiklikle, doğru ücret düzeyi **Pozisyon ayrıntıları** için **Geçerlilik tarihi** kayıtları ve **Ücret planı ataması**'nın **Başlangıç tarihi** temel alınarak varsayılana ayarlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="a3cdd-145">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="a3cdd-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="a3cdd-146">Zorunlu alanlar</span><span class="sxs-lookup"><span data-stu-id="a3cdd-146">Mandatory fields</span></span> 

<span data-ttu-id="a3cdd-147">Artık İnsan Kaynakları kişiselleştirme yetenekleri kullanarak alan zorunlu hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="a3cdd-148">Bu özellik için **Kaydedilmiş görünümler** gereklidir .</span><span class="sxs-lookup"><span data-stu-id="a3cdd-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="a3cdd-149">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="a3cdd-149">Human Resources application in Teams</span></span>

<span data-ttu-id="a3cdd-150">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="a3cdd-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="a3cdd-151">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="a3cdd-152">Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="a3cdd-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="a3cdd-153">Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları</span><span class="sxs-lookup"><span data-stu-id="a3cdd-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="a3cdd-154">Kazançlar yönetimi varlıkları serbest bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="a3cdd-155">DMF varlıkları, kazanç yönetimini kolayca yapılandırmak için verilerin içe ve dışa aktarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="a3cdd-156">Verileri taşımak için bir Kazanç yönetimi şablonu kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="a3cdd-157">Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="a3cdd-158">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="a3cdd-158">Buy and sell leave</span></span> 

<span data-ttu-id="a3cdd-159">Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="a3cdd-160">Bu işlem genellikle el ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-160">This process is often managed manually.</span></span> <span data-ttu-id="a3cdd-161">Bu özellik, İK departmanı ile ilgili ilkelerin ve isteklerin yönetilmesini otomatikleştirir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="a3cdd-162">İzin yönetimi işlemini kolaylaştırır ve hataları gidermek için yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="a3cdd-163">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="a3cdd-163">For more information, see:</span></span>

- [<span data-ttu-id="a3cdd-164">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="a3cdd-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="a3cdd-165">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="a3cdd-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="a3cdd-166">Tek bir şirket veya tek bir plan için izin tahakkuku</span><span class="sxs-lookup"><span data-stu-id="a3cdd-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="a3cdd-167">Müşteriler tek bir şirket veya tek bir izin ve devamsızlık planı için tahakkukları işleyebilir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="a3cdd-168">Bu özellik, farklı izin yılı veya izin tahakkuk ilkeleri olan müşteriler için tahakkuk işlemine açıklık sağlar.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="a3cdd-169">Daha fazla bilgi için bkz. [Şirket veya izin planı başına izin tahakkuku](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="a3cdd-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="a3cdd-170">İzin isteklerine ekler ekleme</span><span class="sxs-lookup"><span data-stu-id="a3cdd-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="a3cdd-171">Onaylanmış izin isteklerine ek ekleme yeteneği, geçerli COVID-19 ortamında kritik öneme sahip.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="a3cdd-172">Çalışanlar şimdi bu ekleri ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-172">Employees can now add these attachments.</span></span> <span data-ttu-id="a3cdd-173">Ayrıca, izin isteklerinde güncelleştirmelerin nasıl yapıldığıyla ilgili daha fazla öngörüye shaip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="a3cdd-174">Daha fazla bilgi için, bkz. [Mevcut bir isteğe ek ekleme](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="a3cdd-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="a3cdd-175">Tahakkuk askıya almalara neden kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="a3cdd-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="a3cdd-176">Neden kodları tahakkuk askıya almaya eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="a3cdd-177">Devretme kuralları</span><span class="sxs-lookup"><span data-stu-id="a3cdd-177">Carry forward rules</span></span> 

<span data-ttu-id="a3cdd-178">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="a3cdd-179">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="a3cdd-180">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="a3cdd-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="a3cdd-181">Belirtilen izin türleri için izin tahakkunu askıya alma</span><span class="sxs-lookup"><span data-stu-id="a3cdd-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="a3cdd-182">Ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="a3cdd-183">Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="a3cdd-184">Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="a3cdd-185">Tahakkuk askıya almaları için DMF varlığı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="a3cdd-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="a3cdd-186">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="a3cdd-187">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="a3cdd-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="a3cdd-188">Common Data Service'te bulunan denetim listesi varlıkları</span><span class="sxs-lookup"><span data-stu-id="a3cdd-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="a3cdd-189">Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Common Data Service'te kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3cdd-190">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a3cdd-190">See also</span></span>

[<span data-ttu-id="a3cdd-191">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="a3cdd-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="a3cdd-192">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="a3cdd-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="a3cdd-193">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="a3cdd-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="a3cdd-194">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="a3cdd-194">Manage features</span></span>](hr-admin-manage-features.md)
